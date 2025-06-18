# Permanently Remove OneDrive from Windows

1. Disable it permanently in Group Policy (Only available in Windows Pro versions).

* Local Computer > Computer Configuration > Administrative Templates > Windows Components > OneDrive
* In the right pane, double-click policy named ‘Prevent the usage of OneDrive for file storage’
* Select the ‘Enabled’ radio button
* Click ‘OK’ when done

2. Remove it via PowerShell (Admin)

* First, run `taskkill /f /im OneDrive.exe` to end process
* Secondly, run `%SystemRoot%\SysWOW64\OneDriveSetup.exe /uninstall` to uninstall
