# Reset a Forgotten Root Password

What if you forgot your root password and wished to reset it? The passwd command won’t be of any use to you then.Fret not though, for you can reset your forgotten root password through the [GRUB bootloader](https://www.makeuseof.com/what-is-grub/) recovery mode. Here’s how:

1. Restart your Linux desktop and in the GRUB bootloader menu, press the **E** key. That should open up the GRUB configuration file.
2. Navigate through the wall of text with arrow keys till you find a line starting with the word **linux**.
3. In that line, replace **ro** with **rw**, **quiet** with **init=/bin/bash**, and erase **splash**. Essentially telling the GRUB bootloader to mount the root partition with read and write permissions and initialize a Bash shell.
4. Once you have the Bash shell, use the passwd command to change the password. Only this time around the system won’t prompt you for the current root password:

```
sudo passwd root
```

1. Type in your new password and finalize it by hitting **Enter**. Once done, restart your system with the reboot command:

```
reboot -f
```

That’s all you need to do. Once you boot up, you should find your root password changed to the one you just typed in. Run any command with superuser privileges to check it yourself.
