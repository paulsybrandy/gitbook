# How to Merge Multiple Text Files in Command Prompt, Notepad, & More

If you want to merge multiple text \*(.txt) files into a single new file in Windows 10 or 11, you can easily do so in Command Prompt using the "copy" command. You can also merge text files using PowerShell commands, or by copying and pasting in Notepad. Before you get started, place all the files that need to be joined into a single folder.

### Quick Steps

1. Open the folder containing the files you want to combine.
2. Hold down Shift and right-click in the folder.
3. Click Open command window here or Open Terminal here.
4. If using Terminal, click the down-arrow and select Command Prompt.
5. Type copy \*.txt newfile.txt and press Enter to merge.

## Method1

### Using Command Prompt

[![Step 1 Right-click the Start icon button and select File Explorer.](https://www.wikihow.com/images/thumb/9/98/Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-1-Version-5.jpg/v4-728px-Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-1-Version-5.jpg.webp)](https://www.wikihow.com/Merge-Text-\(.Txt\)-Files-in-Command-Prompt#/Image:Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-1-Version-5.jpg)

*   Right-click the Start [![Windows Start](https://www.wikihow.com/images/0/07/Windowsstart.png)](https://www.wikihow.com/Merge-Text-\(.Txt\)-Files-in-Command-Prompt#/Image:Windowsstart.png) button and select File Explorer. The [Start menu](https://www.wikihow.com/Use-the-Windows-10-Start-Menu) is usually at the bottom-left corner of the screen.

    * You'll want the files to be in the same folder to make things easier from the command prompt. If the files are scattered in multiple locations, copy them to a single folder first.

    Make sure all of your text files end with a blank line (or the dividing text of your choice) to make it clear where each section begins.

Open the folder in which the [text files](https://www.wikihow.com/Save-a-Text-or-.txt-File) are saved. Start by opening the This PC or Computer directory in the right panel, and then browse to the folder where you've saved your files. Once you open the folder, you should see your text files in the right panel.

Press ⇧ Shift as you right-click a blank area of the right panel. A context menu will expand.

Click Open command window here. This opens a command prompt window that's already set to the current directory.

* If you're using Windows 11 and don't see the option to open the command window, select Open in Terminal instead. Then, once the [Terminal](https://www.wikihow.com/Open-Terminal-in-Windows) is open, click the down-arrow at the top of the window and select Command Prompt.
* If the option isn't available in Windows 10, right-click the taskbar at the bottom of the screen and select Taskbar settings. Toggle off the option that says "Replace Command Prompt with Windows PowerShell in the menu when I right-click the start button or press Windows key + x", then try again.

Type copy \*.txt _newfile.txt_ at the prompt and press ↵ Enter. This command combines all files ending in .txt into a single file called _newfile.txt_. You can replace _newfile.txt_ with the name of the file you want to create (e.g., mergedfiles.txt).

* If you just want to combine two or more text files into a single file but not _all_ text files in the directory, use the command copy _file1.txt_+_file2.txt_+_file3.txt_ newfile.txt. Replace _file1_, etc., with the names of the files you want to combine.[\[1\]](https://www.wikihow.com/Merge-Text-\(.Txt\)-Files-in-Command-Prompt#_note-1)
* Once you've verified that your output file looks how you'd like, you can delete the files you no longer need.

## Method2

### Using PowerShell

[![Step 1 Right-click the Start icon button and select File Explorer.](https://www.wikihow.com/images/thumb/e/ec/Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-6-Version-2.jpg/v4-728px-Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-6-Version-2.jpg.webp)](https://www.wikihow.com/Merge-Text-\(.Txt\)-Files-in-Command-Prompt#/Image:Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-6-Version-2.jpg)

Right-click the Start  button and select File Explorer. If you prefer using PowerShell to Command Prompt, merging text files into one is similar, but the commands are slightly different.

* You'll want the files to be in the same folder to make things easier from the command prompt. If the files are scattered in multiple locations, copy them to a single folder first.

[![Step 2 Open the folder in which the text files are saved.](https://www.wikihow.com/images/thumb/f/f6/Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-7.jpg/v4-728px-Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-7.jpg.webp)](https://www.wikihow.com/Merge-Text-\(.Txt\)-Files-in-Command-Prompt#/Image:Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-7.jpg)

Open the folder in which the text files are saved. Start by opening the This PC or Computer directory in the right panel, and then browse to the folder where you've saved your files. Once you open the folder, you should see your text files in the right panel.

[![Step 3 Press ⇧ Shift as you right-click a blank area of the right panel.](https://www.wikihow.com/images/thumb/1/1d/Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-8.jpg/v4-728px-Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-8.jpg.webp)](https://www.wikihow.com/Merge-Text-\(.Txt\)-Files-in-Command-Prompt#/Image:Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-8.jpg)

Press ⇧ Shift as you right-click a blank area of the right panel. A context menu will expand.

[![Step 4 Click Open PowerShell window here….](https://www.wikihow.com/images/thumb/3/37/Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-9.jpg/v4-728px-Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-9.jpg.webp)](https://www.wikihow.com/Merge-Text-\(.Txt\)-Files-in-Command-Prompt#/Image:Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-9.jpg)

Click Open PowerShell window here…. This opens a new PowerShell window to the directory that contains your text files.

[![Step 5 Run the command Get-Content file1.txt, file2.txt | Set-Content newfile.txt.](https://www.wikihow.com/images/thumb/5/52/Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-10.jpg/v4-728px-Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-10.jpg.webp)](https://www.wikihow.com/Merge-Text-\(.Txt\)-Files-in-Command-Prompt#/Image:Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-10.jpg)

Run the command Get-Content _file1.txt_, _file2.txt_ | Set-Content _newfile.txt_. Replace _file1.txt,_ etc., with the file names you want to merge. You can also replace _newfile.txt_ with the name you want to give to the final merged file.

* If you want to merge all text files in the current directory into a single text file, use the command Get-Content \*.txt .

## Method3

### Using Notepad

[![Step 1 Open the text files in Notepad.](https://www.wikihow.com/images/thumb/e/e5/Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-11.jpg/v4-728px-Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-11.jpg.webp)](https://www.wikihow.com/Merge-Text-\(.Txt\)-Files-in-Command-Prompt#/Image:Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-11.jpg)

Open the text files in Notepad. If you just want to combine 2 or 3 text files into a single text file, you can do it easily with Notepad.

* Open Notepad by typing notepad into the Windows search bar and clicking Notepad.
* Click File > Open, select the first text file, then click Open.
* Repeat for other text files you want to combine.

[![Step 2 Create a new blank text file in Notepad.](https://www.wikihow.com/images/thumb/3/3a/Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-12.jpg/v4-728px-Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-12.jpg.webp)](https://www.wikihow.com/Merge-Text-\(.Txt\)-Files-in-Command-Prompt#/Image:Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-12.jpg)

Create a new blank text file in Notepad. If you're using Windows 11, go to File > New tab to create the file in a new tab. On Windows 10, just open another new instance of Notepad.

[![Step 3 Copy the text from the first file you want to combine.](https://www.wikihow.com/images/thumb/a/a1/Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-13-Version-2.jpg/v4-728px-Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-13-Version-2.jpg.webp)](https://www.wikihow.com/Merge-Text-\(.Txt\)-Files-in-Command-Prompt#/Image:Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-13-Version-2.jpg)

Copy the text from the first file you want to combine. An easy way to do this is to click anywhere in the text, press Ctrl + A on the keyboard to select all, then press Ctrl + C to copy.

[![Step 4 Paste the copied text into the blank text file.](https://www.wikihow.com/images/thumb/a/a2/Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-14-Version-3.jpg/v4-728px-Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-14-Version-3.jpg.webp)](https://www.wikihow.com/Merge-Text-\(.Txt\)-Files-in-Command-Prompt#/Image:Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-14-Version-3.jpg)

Paste the copied text into the blank text file. In your new blank Notepad file, click anywhere in the file, then press Ctrl + V to paste the copied text.

[![Step 5 Repeat for the other files you want to combine.](https://www.wikihow.com/images/thumb/8/85/Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-15-Version-3.jpg/v4-728px-Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-15-Version-3.jpg.webp)](https://www.wikihow.com/Merge-Text-\(.Txt\)-Files-in-Command-Prompt#/Image:Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-15-Version-3.jpg)

Repeat for the other files you want to combine. Go to your next text file, press Ctrl + A to select all, then press Ctrl + C to copy. In your new blank file, click where you want to paste the copied text, then press Ctrl + V to paste.

[![Step 6 Save your file.](https://www.wikihow.com/images/thumb/c/c6/Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-16.jpg/v4-728px-Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-16.jpg.webp)](https://www.wikihow.com/Merge-Text-\(.Txt\)-Files-in-Command-Prompt#/Image:Merge-Text-\(.Txt\)-Files-in-Command-Prompt-Step-16.jpg)

Save your file. In the new file that contains your merged text, go to File > Save as, give the file a name, and click Save.\
