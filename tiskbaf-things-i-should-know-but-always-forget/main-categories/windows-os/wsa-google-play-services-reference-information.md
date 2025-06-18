---
description: WSA ➪ Windows Subsystem for Android
---

# WSA/Google Play Services Reference Information

**WSA (mirrors):** [https://www.mediafire.com/file/k344j98tkbascfs/WsaPackage\_1.7.32815.0\_x64\_Release-Nightly.zip/file](https://www.mediafire.com/file/k344j98tkbascfs/WsaPackage\_1.7.32815.0\_x64\_Release-Nightly.zip/file)[https://www.dropbox.com/s/meafp0p9vd7j50m/WsaPackage\_1.7.32815.0\_x64\_Release-Nightly.zip?dl=0](https://www.dropbox.com/s/meafp0p9vd7j50m/WsaPackage\_1.7.32815.0\_x64\_Release-Nightly.zip?dl=0)[https://mega.nz/file/G0UnzYZR#mQ0GsIeTxxhIWZXjT\_aWCpa8HoC4gzneHai4FgnIR1M](https://mega.nz/file/G0UnzYZR#mQ0GsIeTxxhIWZXjT\_aWCpa8HoC4gzneHai4FgnIR1M)WSA can also be downloaded by visiting [https://store.rg-adguard.net/](https://store.rg-adguard.net/) and…

1. In the search field put “[https://www.microsoft.com/store/productId/9P3395VX91NR”](https://www.microsoft.com/store/productId/9P3395VX91NR%E2%80%9D)
2. Select the Slow ring
3. Click search
4. Choose the big file that follows the following format: **MicrosoftCorporationII.WindowsSubsystemForAndroid\_**_\_.msixbundle_(where \*\*\* will be a version number)

**Kernel (mirrors):**[https://www.dropbox.com/s/02drq90e1uw1ycm/kernel?dl=0](https://www.dropbox.com/s/02drq90e1uw1ycm/kernel?dl=0)[https://www.mediafire.com/file/gdh8au8bw03jpad/kernel/file](https://www.mediafire.com/file/gdh8au8bw03jpad/kernel/file)

1. Go into the Developer Settings in Windows Settings app and activate Developer Mode.
2. Change out the “kernel” file for the one downloaded above.
3. Open PowerShell as admin.
4. Navigate to the directory that the downloaded (and extracted) WSA from above is.
5. Copy and paste “1st Command” from below and hit enter.

1st Command: (PowerShell)

```
cd\\
cd wsa
Add-AppxPackage -Register .\\AppxManifest.xml
```

2nd Command: (Command Prompt)

```
adb connect 127.0.0.1:58526
adb shell
su
setenforce 0
```
