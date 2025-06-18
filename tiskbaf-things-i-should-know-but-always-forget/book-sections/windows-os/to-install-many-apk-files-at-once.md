# To install many APK files at once

#### To install many APK files at once using ADB

* Open a command prompt window
* Go to the directory containing the APK files
* Use the following command to start the process:`for %e in (*.apk) do adb install %e`

✎ **NOTE:** _If there are any spaces within any of the filenames, they must be renamed or the above command will not work. This can be achieved by using the script below and creating a .bat file with it._
