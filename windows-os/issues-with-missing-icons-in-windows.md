# Issues with missing icons in Windows

One of the common “it’s still Windows” chores we have to do now and then is reset the icon and thumbnail cache. If your icons are corrupted in some way—blank, taken over by another app, or not displaying as they normally do—then resetting the icon cache can fix the problem.The same goes for the thumbnail cache, which keeps a preview of images, videos, and documents. There are several ways to do this. The most common involves using the command line. Or you can use a free third-party utility. We’ll look at both options.✎ **NOTE:** Usually the option marked with the ❗ symbol below worked after all the other options did not. **Try that one first.**

### Reset the Icon and Thumbnail Caches

If your icons are corrupted or not displaying properly, you can reset the Windows 10 icon cache to fix them.The easiest way to do it is by using the free Winaero Tweaker utility. After completing setup, launch Winaero Tweaker, scroll down to Tools group, select Reset Icon Cache, then click Reset Icon Cache. That’s it; your icons should return to normal.

### Fix Icons and Thumbnails from Run or Command Prompt

If you don’t want to go through a third-party app, you can try resetting several ways. From the run command, type: **ie4uinit -show** and hit Enter.Still not seeing those icons? Then let’s jump into the command line and get our hands dirty. First, you will need to disable Explorer.exe. Press Windows key + X then click Task Manager (or press Control + Shift + Esc). From the Processes tab, select Windows Explorer, right-click it, then click End task.✰ Click File ➜ Run new task, type: CMD, hold down the Shift key, and click OK. This will open the command prompt with administrator privileges.Type each command (each line), then hit Enter. Alternatively, you can copy all the commands and it will exce

```
cd %homepath%\\AppData\\Local\\Microsoft\\Windows\\Explorer
dir iconcache*
del iconcache*
dir iconcache*
explorer.exe
exit
```

### Reset Your Thumbnail Cache

A similar issue can happen when your thumbnail previews. Instead of seeing a preview of your actual image, video, or document, you may only see a generic icon.Fixing this one should be a lot easier. Press Windows key + R, type: cleanmgr.exe, and hit Enter. Scroll down, check the box next to Thumbnails and click OK.If none of those options work, try the following:

#### **Method 1: Let’s run the fixit provided in the following link and check if that helps to resolve the issue. Refer the following link provided to run the fix it.**

‘Diagnose and repair Windows File and Folder Problems automatically’[http://support.microsoft.com/mats/windows\_file\_and\_folder\_diag/](http://support.microsoft.com/mats/windows\_file\_and\_folder\_diag/)

#### **Method 2: This issue can occur by corrupted icon cache. To fix the issue, rebuild icon cache.**

❗_This option typically worked after all the other methods did not. Therefore, it is advised to try this method first when you experience this issue!_✎ **NOTE: Best to complete this method logged under a different Admin account.**

1. Click the Start button, and click Computer.
2. On the Tool bar, click ‘Organize’ and choose Folder and Search Options.
3. Click the View tab, and check to select the ‘Show hidden files and folders option’ & uncheck ‘Hide extensions for known file types’, and click OK.
4. Then, enter the following directory: “%USERPROFILE%\AppData\Local”
5. Find the “IconCache.db” file, and rename it as “IconCache.db.old”
6. Close the window, and restart the computer.

#### **Method 3: If the issue persists then follow the steps provided in the following article and check if that helps.**

Icons change incorrectly in Windows - view the following support page:
