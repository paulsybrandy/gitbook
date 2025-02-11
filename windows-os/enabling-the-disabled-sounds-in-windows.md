# Enabling the disabled sounds in Windows

### Logoff Sound:

#### Enable Using Registry Editor:

**Step 1:** Press the **Windows key + R** together on your keyboard to open the Run box. Now, type **regedit** in the search field and hit **Enter** to open the **Registry Editor**.

**Step 2:** In the **Registry Editor** window, navigate to the below path:

```
HKEY_CURRENT_USER\\AppEvents\\EventLabels
​
```

Now, under the **EventLabels** key, scroll down and click on **WindowsLogoff**. On the right side you will see the **DWORD (32-bit) Value** – **ExcludeFromCPL.** Double-click to edit this field.

**Step 3:** In the **Edit DWORD (32-bit) Value** dialogue box, change the **Value Data** field from **1** to **0**. Click **OK** to save the changes and exit.

**Step 4:** Now, click on **WindowsLogon** and on the right side you will see the same **DWORd (32-bit) Value**, **ExcludeFrom CPL** (as you saw in the case of **WindowsLogoff**).

Now, follow the **Step 2** and **Step 3** as above to change the **Value Data** field from **1** to **0**. Press **OK** to save the changes and exit.

Now, the Windows Log Off and Log On sounds are enabled in the Control Panel. From here, you need to go to the Control Panel to enable the sounds.

#### Add play a sound at Logoff in Task Scheduler:

You can create an automated task that will allow your computer to play the logoff sound.

1. Press the **Windows key+S** keys together.
2. Type “**Task Scheduler**” in the search box and click on “**Task Scheduler**“.
3. You have to click on the “**Task Scheduler Library**” and then click on the “**Create Task..**.”.
4. Go to the “**General**” tab.
5. Set the name of the program as “**Play logoff sound**“.
6. Then, click on the radio button beside the “**Run whether the user is logged on or not**“.
7. Then, **check** the option “**Run with highest privileges**” box.
8. Finally, click on the ‘Configure for:’ and set it to “**Windows 10**“.
9. Next, go to the “**Triggers**” tab.
10. Then, click on “**New…**” to create a new trigger.
11. In the New Trigger window, set the ‘Begin the Task:’ to “**On an event**“.
12. Then, set the ‘Log:’ to “**Security**“.
13. After that, set the ‘Event ID:’ to “**4647**“.
14. Then, click on “**OK**” to create a new trigger.
15. At the next step, go to the “**Actions**” window.
16. Thereafter, click on “**New**“.
17. Then, set the ‘Action:’ to “**Start a program**” from the drop-down.
18. After that, type “**PowerShell**” in the Program/script.
19. Now, copy-paste this code in the ‘Add arguments (optional):’.

```
-c (New-Object Media.SoundPlayer 'C:\\Windows\\Media\\Windows Logoff Sound.wav').PlaySync();
​
```

✎ **NOTE:** This is standard Windows Log off the sound. If you want to customize the ‘Log off’ sound, simply paste the address of the preferred sound in the place of ’C:\Windows\Media\Windows Logoff Sound.wav‘ in the code.

1. Then, click on “**OK**” to save the action.
2. In the ‘Create Task’ window, go to the “**Conditions**” tab.
3. Then, **uncheck** the “**Start the task only if the computer is on AC power**“.
4. Next, click on “**OK**” to save it.
5. Now, Task Scheduler will ask for your account password.
6. Just type in your account password and tap on “**OK**” to finally create the task.

You can see the ‘Play Logoff Sound’ task in the Task Scheduler window. From now on, this computer will make a sound once any of the users logs off from the system.

#### How to delete the automated task

If you ever feel you don’t need the logoff sound while logging out, you can easily get rid of it.

1. Open the Task Scheduler.
2. Then, on the left-hand pane, click on the “**Task Scheduler Library**“.
3. On the right-hand side, look for the “**Play logoff sound**“.
4. Right-click on the task and click on “**Delete**“.

Deleting the task will stop the logoff sound while logging out from the system.

### Logon Sound:

#### Create a VBScript File to play a logon sound:

✮ Open Notepad and paste the following lines into it:

```
Set oVoice = CreateObject("SAPI.SpVoice")
set oSpFileStream = CreateObject("SAPI.SpFileStream")
oSpFileStream.Open "C:\\Windows\\Media\\Windows Logon.wav"
oVoice.SpeakStream oSpFileStream
oSpFileStream.Close
​
```

✮ Save this file anywhere with a .VBS extension. For example, “LogonSound.vbs”.

✮ Double-click the file you’ve created and ensure that it plays your sound file.

✎ **NOTE:** This is a simple VBScript for Windows to play any sound using the Speech API. I prefer this method because it doesn’t depend on loading some slow program such as Windows Media Player or any third-party app to play the sound.

In this script, I am using the default sound file, C:\Windows\Media\Windows Logon.wav. You can use any file you want. Just modify the appropriate line.

💡 **TIP:** In the Notepad’s Save dialog, include the file name to quotes to ensure that you are saving the file with the VBS file extension and not TXT.

_Now we need to create a special Task Scheduler task to play this sound. Task Scheduler is able to run tasks at logon, so specifying our script as the task’s action will make it play the sound every time you sign-in._

#### Play the Logon Sound that you created automatically upon logon:

✮ Open Administrative Tools.

✮ Click the Task Scheduler icon.

✮ In the Task Scheduler library, click on the _Create Task…_ link on the right.

✮ In Create Task dialog, fill in the Name box some meaningful text like “Play logon sound”.

✮ Set the option Configure for: Windows 10.

✮ Switch to the Triggers tab and click on the **New** button.

✮ Set the event for the trigger to _At log on_.

✮ Switch to the _Actions_ tab and click on the _New…_ button.

✮ In the next dialog, set the action type to _Start a program_.

✮ In the _Program_ box, specify wscript.exe as the program.

✮ Type the full path to your VBScript file into the Add arguments text box.

✮ Switch to the _Conditions_ tab and disable the option _Start the task only if the computer is on AC power._

✮ Click on the OK button to create the task.

✎ **NOTE:** If your operating system is preventing you from saving your task due to a blank password, you can [add a password](https://winaero.com/blog/all-ways-to-change-the-user-password-in-windows-10/) to your user account or disable the restriction in Local Security Policy under Administrative tools.

### Shutdown Sound:

#### Creating a Shutdown Sound event:

We need to create a task in Task Scheduler attached to a special Shut Down event. The event we need has ID 1074 = User Initiated Shutdown, as shown in the following screenshot.

Task Scheduler is able to run tasks attached to any event, so specifying our script as the task’s action will make it play the sound every time you shut down the OS. To play the sound, we have to use PowerShell.

**Method limitations:**

**⚠** This method only works when you know and can use credentials for an administrative user account.

**⚠** It doesn’t work if your user account has no password.

**⚠** It might not work if you have Fast Startup disabled.

_Unfortunately, there is no way to bypass these limitations._

#### Playing the Shutdown Sound upon shutdown of your system:

✮ Open Administrative Tools.

✮ Click the Task Scheduler icon.

✮ In the Task Scheduler library, click on the _Create Task…_ link on the right.

✮ In Create Task dialog, fill in the Name box some meaningful text like “Play shutdown sound

✮ Set the options as follows:

✮ Configure for Windows 10.

✮ Run whether user is logged on or not

✮ Run with highest privileges box

✮ Switch to the Triggers tab and click on the _New…_ button.

✮ Set the event for the trigger to _On an event_.

✮ Select _System_ in the drop down list under _Log_.

✮ Enter the value 1074 in the _Event ID_ text box.

✮ Switch to the _Actions_ tab and click on the _New…_ button.

✮ In the next dialog, set the action type to _Start a program_.

✮ In the _Program_ box, specify _powershell.exe_ as the program.

✮ Type the following text (or use copy and paste) into the Add arguments text box:

```
    -c (New-Object Media.SoundPlayer 'C:\\Windows\\Media\\Windows Shutdown.wav').PlaySync();
​
```

✮ Switch to the _Conditions_ tab and disable the option _Start the task only if the computer is on AC power_

✮ Click on the OK button to create the task.

✮ Type your user account password (or other administrative user account credentials).

… and that’s it! Finished. You did it!
