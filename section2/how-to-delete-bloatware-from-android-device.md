---
description: How to use ADB to delete bloatware from Android device.
---

# How to delete bloatware from Android device

To delete bloatware apps from an Android device using ADB (Android Debug Bridge), you need to enable USB debugging on your phone, connect it to your computer, open a command prompt, and use the command "adb shell pm uninstall -k --user 0 \<package\_name>", where "package\_name" is the unique identifier of the bloatware app you want to remove; be cautious as this can potentially brick your device if done incorrectly; it's best to research the specific package names for your device before attempting to uninstall any system apps. Key steps:

* **Enable USB debugging:** Go to your phone's Settings > About Phone > Developer options and toggle on "USB debugging."&#x20;
* **Install ADB:** Download and install the Android SDK Platform Tools on your computer, which includes ADB.&#x20;
* **Connect your phone:** Plug your phone into your computer using a USB cable.&#x20;
* **Open command prompt:** Navigate to the directory where you installed ADB on your computer and open a command prompt or terminal window.&#x20;
* **Verify connection:** Run the command "adb devices" to check if your device is recognized.&#x20;
* **Find package name:** To identify the exact package name of the bloatware app you want to remove, use the command "adb shell pm list packages".&#x20;
* **Uninstall the app:** Once you have the package name, use the following command to uninstall the bloatware app: "adb shell pm uninstall -k --user 0 \<package\_name>".&#x20;

Important points to remember:

* **Backup your data:**&#x42;efore uninstalling any system apps, always back up your important data as removing the wrong app could cause issues with your device.&#x20;
* **Check for compatibility:**&#x4E;ot all bloatware apps can be completely removed using ADB, and attempting to remove critical system apps could potentially brick your device.&#x20;
* **Research package names:**&#x4C;ook up the exact package names of the bloatware apps you want to remove specific to your phone model to avoid accidentally removing important system components.&#x20;
