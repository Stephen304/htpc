# HTPC
A collection of things that helped me set up my htpc.

## Kodi
* Getting CEC to work
`sudo usermod -aG dialout <user>`

## Steam
* Installing Jamestown
```
sudo apt-get install libsdl1.2debian:i386 libopenal1:i386
```
```
sudo wget https://github.com/ValveSoftware/source-sdk-2013/raw/master/sp/src/lib/public/linux32/libsteam_api.so
```
into Jamestown install directory

## XBoxDrv
* `rmmod xpad`
* `/etc/modprobe.d/xpad.conf`:
```
blacklist xpad
```

* Copy `org.seul.Xboxdrv.conf` to `/etc/dbus-1/system.d/`
* Copy `xboxdrv.service` to `/etc/systemd/system/`
* `sudo systemctl enable xboxdrv.service`
* `sudo systemctl start xboxdrv.service`
