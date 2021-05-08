Right-click "Install Mac OS X Lion.app" and choose Show Package

open Contents, then open Shared Support, look for disk-image file called InstallESD.dmg copy to desktop

double click to mount it

Open /Applications/Utilities/Disk Utility, select usb drive and restore, select the Mac OS X Install ESD volume

If getting error then run below

sudo asr restore -source /Volumes/Mac\ OS\ X\ Install\ ESD.dmg -target /Volumes/usb_drive -noprompt -noverify -erase


now restart and press and hold option key, select the usb bootable drive

Install Lion, if getting error - There was a problem installing "Mac OS X" then check date via Terminal and 
clear PRAM (hold "Option + Command + P + R" for 20 secs, should restart 2 times) 
