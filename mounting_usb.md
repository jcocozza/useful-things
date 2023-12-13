# Mounting a USB in ubuntu

1) Insert USB -- keep track of any output.
2) `lsusb` to check its there
3) create a directory for it: `sudo mkdir /media/usb`
4) `sudo mount /dev/sdX1 /media/usb` where `X` is a variable that you'll know when you see the output when the USB is inserted; ex: sdb1
5) check to ensure it worked: `ls /media/usb`

# Unmounting
`sudo umount /media/usb`
And you can eject with:
`sudo eject /dev/sdX`

