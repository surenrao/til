## Internet not working

most probably during install, chosed wrong nic. run `ip link show` note all nic values and open `/etc/network/interfaces` and set bridge-ports with correct nic

## For non subscribers 

comment out item in file /etc/apt/sources.list.d/pve-enterprise.list

    `# deb https://enterprise.proxmox.com/debian/pve bullseye pve-enterprise`

Add below to /etc/apt/sources.list

    `deb http://download.proxmox.com/debian/pve bullseye pve-no-subscription`
    
[Reference](https://pve.proxmox.com/wiki/Package_Repositories)

## Remove “No valid subscription.” popup

open `nano /usr/share/javascript/proxmox-widget-toolkit/proxmoxlib.js` search for `No valid subscription` change if condition to false `if (false) {`

[Reference](https://www.geekdecoder.com/how-to-remove-you-do-not-havea-valid-subscription-for-this-server-on-proxmox/)
