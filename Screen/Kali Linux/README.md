# Install Kali on your HackberryPi5

You can download the image from [pi-imager](https://www.raspberrypi.com/software/)  
After you download and flash the image into the tf card, Copy and paste the following lines into the `/boot/config.txt`  

```sh
dtoverlay=vc4-kms-v3d
dtoverlay=vc4-kms-dpi-hyperpixel4sq
```

Insert the tf card and you can see HackberryPi running Kali linux
![image](https://github.com/user-attachments/assets/9a049e49-eef4-46af-961e-31cb7b6daf2d)


## Username and Password

Try 
```sh
kali
kali
```
Or
```sh
pi
pi
```

# Calibrate the Touchdisplay

Because desktop on Kali is running on x11, while other newer os lie RpiOS are updated to wayland, the touch can be handled differently on kali like the touch is inverted.
Follow the steps to do the calibration
Open a terminal and type
```sh
sudo nano /etc/X11/xorg.conf.d/40-libinput.conf
```
This should be an empty new file

Then type 
```sh
Section "InputClass"
Identifier "libinput touchscreen catchall"
MatchIsTouchscreen "on"
Option "CalibrationMatrix" "0 1 0 1 0 0 0 0 1"
MatchDevicePath "/dev/input/event**
Driver "libinput"
EndSection
```

Save and exit this file.  
Then reboot, then the touch is no more inverted.  
I suggest you do that under ssh, here is the way of [activating ssh on Kali](https://www.geeksforgeeks.org/how-to-enable-and-start-ssh-on-kali-linux/)
