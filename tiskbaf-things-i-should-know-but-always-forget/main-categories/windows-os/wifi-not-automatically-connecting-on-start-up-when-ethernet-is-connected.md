# Wifi not automatically connecting on start-up when Ethernet is connected

Edit or Create Group Policy via Registry Editor

1. Press Windows Key + R.
2. Type “regedit” and click OK.
3. Navigate to the registry path `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\POLICIES\MICROSOFT\WINDOWS\WCMSVC\`
4. If the “GroupPolicy” subkey does not exist, highlight “WcmSvc” and right click it.
5. Choose “New -> Key”
6. Name it “GroupPolicy”
7. Click the newly created “GroupPolicy”
8. Right-click anywhere in the right window and choose “New -> DWORD (32-bit)”
9. Name that new value `fMinimizeConnections` and click OK.
10. Reboot and test.
