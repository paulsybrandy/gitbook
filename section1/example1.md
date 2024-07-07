# Useful Linux commands

### Start Bluetooth if not already started

```
sudo service bluetooth start
sudo systemctl enable bluetooth
sudo systemctl status bluetooth

sudo /etc/init.d/bluetooth start
```

### Restart Bluetooth

```
sudo systemctl daemon-reload
sudo systemctl restart bluetooth
```

***

### Start snap if it isnt already started

```
service snapd start
sudo systemctl start snapd.service
```

### “snap-confine has elevated permissions and is not confined but should be. Refusing to continue to avoid permission escalation attacks” Error

```
sudo apparmor_parser -r /etc/apparmor.d/*snap-confine*
sudo apparmor_parser -r /var/lib/snapd/apparmor/profiles/snap-confine*
```

***

### “cannot change profile for the next exec call: No such file or directory

### snap-update-ns failed with code 1” Error

`⁠sudo apparmor_parser -r /var/lib/snapd/apparmor/profiles/*⁠⁠`

### To temp. start Anbox run the following from terminal

`EGL_PLATFORM=x11 anbox.appmgr`

***

### To enable syncthing type the following command replacing username with your actual username:

`sudo systemctl enable syncthing@neocube.service`

***

### To get Drive information

#### Used, free, & total size

`df -H /mnt/SP-LIBRARY`

***

### To load the kernel module v4l2loopback.ko

`sudo modprobe -v v4l2loopback`

***

### Using ‘rename’ command to change the file extensions of many files at once

#### For example to change all of the files with the JFIF extension to the JPG extension you would use the following:

`rename 's/\\.jfif$/.jpg/' *.jfif`

***

### Reload Font Cache

`sudo fc-cache -fv`
