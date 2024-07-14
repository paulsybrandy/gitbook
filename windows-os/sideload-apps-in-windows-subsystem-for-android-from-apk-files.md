# Sideload Apps in Windows Subsystem for Android from APK Files

1. Download the APK file for the Android app you want to run. You should use trusted sources like [APKPure](https://m.apkpure.com/) or [APKMirror](https://www.apkmirror.com/).
2. Now, download [Android Platform Tools](https://dl.google.com/android/repository/platform-tools-latest-windows.zip).
3. Extract the contents of the _platform-tools_ archive to any folder of your choice, say c:\adb.
4. Run the Amazon Store app to warm up the WSA and fire up its network layer.
5. Now, launch the Windows Subsystem for Android settings from the Start menu.
6. Turn on the _Developer mode_ toggle option. Note the connection line for adb it shows. **(127.0.0.1:58526)**
7. Open [Windows Terminal](https://winaero.com/how-to-open-windows-terminal-in-windows-11/) to the Command Prompt profile and type `cd c:\\adb`. Correct the path to your Android Platform Tools if needed and hit Enter.
8. Type the command `adb connect <ip address>.` Specify the IP address you noted. Press Enter and ignore any authentication error message.
9. Now, type the command `adb install apk full\\path\\to\\file.apk` and provide the full path to your game or app APK file you want to sideload.
10. Once Windows 11 finishes installing the app, it will appear in the Start menu.

You are done!Now you can open the Start menu and run the sideloaded app as usual. It should be able to play sounds and make Internet connections, like if it was installed from Amazon Store.✎ **NOTE:** Keep in mind that WSA is still a work in progress and may have compatibility issues. Certain apps may fail to start, crash, or work unpredictable. Some apps just show a blank window.Be careful downloading APK files from untrusted sources.💡[APKPure](https://m.apkpure.com/) and [APKMirror](https://www.apkmirror.com/) are well-known websites to grab APK files (and the like). Russian users may have heard about 4PDA. But on the Internet, there is a bunch of sites that redistribute modified malicious Android APKs. **So pick what you download and install very carefully.**
