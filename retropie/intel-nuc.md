# Run RetroPie & Kodi as Kiosk in Intel NUC Hades Canyon
* Download Ubuntu minimal and make Bootable USB using Roofus
* Install and choose all defaults, Select SAMBA Server and SSH Server
* sudo apt install git dialog unzip xmlstarlet
* mkdir git && cd git && git clone --depth=1 https://github.com/RetroPie/Retropie-Setup.git
* cd Retropie-Setup && sudo ./retropie_setup.sh
* Do Basic Install
* [Setup Samba](https://github.com/surenrao/til/blob/master/retropie/samba.md)
* sudo apt install ubuntu-drivers-common 
* `sudo ubuntu-drivers autoinstall` if graphics card will install drivers
* `sudo apt install lightdm openbox` for autologin and minimal X servers window manager.
* `sudo apt install alsa-base alsa-utils pavucontrol pulseaudio` [for hdmi](https://askubuntu.com/a/1316585)
* [Setup lightdm](https://github.com/surenrao/til/blob/master/retropie/lightdm.md)
* sudo ./retropie_setup.sh
* Configuration / tools > autostart > Enabled. Exit
* `EDITOR=nano sudo visudo` 
```
surenrao     ALL=(ALL) NOPASSWD: ALL   
```
* sudo gpasswd -d surenrao sudo
* sudo usermod -a -G audio surenrao
* groups surenrao
* restart

## References
[Building a Custom Retrogaming PC with RetroPie and Ubuntu Minimal](https://www.youtube.com/watch?v=2yjsugy8hyc)

[Ubuntu audio trobleshooting](https://askubuntu.com/questions/112512/ubuntu-refuses-to-output-audio-via-hdmi)

[Some apps install hints](https://www.ubuntuopenbox.com/lessons/course/)

[To enable KODI](https://retropie.org.uk/docs/KODI/)
