# How to Create Symbolic Links with mklink

You can create symbolic links using the mklink command in a Command Prompt window as Administrator or as a regular user. To do this without an Administrator Command Prompt window, you must first enable Developer Mode from Settings > Update & Security > For Developers.

⚠️ To open Command Prompt as admin, click the Start button, search “cmd” or “Command Prompt,” then select “Run as Administrator”. ⚠️ Windows 11 doesn’t require administrative privileges to create symbolic links.

![](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/08/launch-command-prompt.png)

https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2023/08/launch-command-prompt.png

Without any extra options, `mklink` creates a symbolic link to a file. The below command creates a symbolic, or “soft”, link at `Link` pointing to the file `Target` :

```
mklink Link Target
```

Use /D when you want to create a soft link pointing to a directory. like so:

```
mklink /D Link Target
```

Use /H when you want to create a hard link pointing to a file:

```
mklink /H Link Target
```

Use /J to create a hard link pointing to a directory, also known as a directory junction:

```
mklink /J Link Target
```

![](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2016/12/img_585a0d3194149.png)

https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2016/12/img\_585a0d3194149.png

So, for example, if you wanted to create a directory junction (a hard link to a folder) at “C:\LinkToFolder” that pointed to “C:\Users\Name\OriginalFolder,” you’d run the following command:

```
mklink /J C:\LinkToFolder C:\Users\Name\OriginalFolder
```

You’ll need to put quotation marks around paths with spaces. For example, if the folders are instead named “C:\Link To Folder” and “C:\Users\Name\Original Folder,” you’d use the following command instead:

```
mklink /J "C:\Link To Folder" "C:\Users\Name\Original Folder"
```

![](https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2016/12/img_585a0d4f1fbf2.png)

https://static1.howtogeekimages.com/wordpress/wp-content/uploads/2016/12/img\_585a0d4f1fbf2.png

If you see the message “You do not have sufficient privilege to perform this operation.”, you need to launch the Command Prompt as Administrator before running the command.
