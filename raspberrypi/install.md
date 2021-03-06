  * Using the installer created ubuntu server 20 64 bit mirco sd card
  * logged in using default ubuntu = ubuntu and changed password
  * ran sudo apt-get update && apt-get upgrade-dist
  * Installed webmin [using instructions](https://sourceforge.net/p/webadmin/bugs/4742/)
  * ran `/etc/webmin/start` to start webmin then opened https://<192.168.ipaddress>:10000
  * Installed firewallD and added all the exposed ports and applied config
  * Installed Docker
  * Installed Portainer
  * Installed Thiea IDE (vscode in browser)
  * Intalled Heimdall Application Dashboard
  * ~~Installed Bind9 and configured using https://www.linuxbabe.com/ubuntu/set-up-local-dns-resolver-ubuntu-20-04-bind9 , https://catalin.works/blog/bind9-dns-setup-local-domain-names/ and https://github.com/Trellmor/bind-adblock~~
  * Installed PiHole docker and uninstalled Bind9, because it has dns name and ad-block built in and so easy to do
    * stopped and disabled systemd-resolved, and `rm /etc/resolv.conf`
  * Installed Nginx Proxy Manager via docker for reverse proxy local dns names 
  * [Mount Synology to respberry pi](https://kb.synology.com/en-uk/DSM/tutorial/How_to_access_files_on_Synology_NAS_within_the_local_network_NFS)
  * https://www.home-assistant.io/installation/raspberrypi#docker-compose
  * https://github.com/oznu/docker-homebridge
  * https://docs.linuxserver.io/images/docker-habridge
  
  ## Troublshoot steps
  * make sure port is applied to firewallD and apply config through webmin
  * restart server
  * `curl -i https://<192.168.ipaddress>:<port>/`
  * https://www.cyberciti.biz/faq/unix-linux-check-if-port-is-in-use-command/
