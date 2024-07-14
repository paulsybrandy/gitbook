---
description: How to use the SetUserFTA Utility
---

# SetUserFTA Utility

To set http, https, .htm, and .html defaults to a specific program, (i.e. ff-unbranded):

* First make sure the program is located in the `HKEY_CLASSES_ROOT\Applications\` section of the registry
* Then use the below command(s) to set chosen app or program as default
  * Use your EXE file for what you want to use
  * Change the file type to what you want the default set to be

`cd c:\setuserfta`

`setuserfta .html applications\ff-unbranded.exe`

`setuserfta .htm applications\ff-unbranded.exe`

`setuserfta http applications\ff-unbranded.exe`

`setuserfta https applications\ff-unbranded.exe`

📝**NOTE:** Using the above commands will change all webpages and HTML files to open in Unbranded Firefox by default.
