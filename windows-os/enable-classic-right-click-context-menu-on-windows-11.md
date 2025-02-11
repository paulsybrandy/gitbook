# Enable classic right-click context menu on Windows 11

To bring back the classic context menu on Windows 11, use these steps:

1. Open **Start** on Windows 11.
2. Search for **regedit** and click the top result to open the **Registry**.
3. Navigate to the following path:

```
HKEY_CURRENT_USER\\SOFTWARE\\CLASSES\\CLSID
​
```

1. Right-click the **CLSID** key, select the **New** menu, and select the **Key** option.

86ca1aa0-34aa-4e8b-a509-50c905bae2a2

2. Name the key **{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}** and press **Enter**.
3. Right-click the newly created key, select the **New** menu and select the **Key** option.

InprocServer32

4. Name the key **InprocServer32** and press **Enter**.
5. Double-click the newly created key and set its value to **blank** to enable the classic context menu on Windows 11.

Registry enable full context menu

6. Click the **OK** button.
7. Restart the computer.
