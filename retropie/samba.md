# Insecure SAMBA Server settings for Home
* `systemctl status smbd` check if Samba is running
* `cd /etc/samba`
* `sudo mv smb.conf smb.conf.orig`
* `sudo nano smb.conf`

```
[global]
server string = Retropie Gaming Console
workgroup = MYWORKGROUP
security = user
map to guest = Bad User
name resolve order = bcast wins
include = /etc/samba/smbshared.conf
```

* `sudo nano smbshared.conf`

```
[RetroRie]
path = /home/surenrao/RetroPie
force user = surenrao
force group = surenrao
create mask = 0664
force create mask = 0664
directory mask = 0777
force directory mask = 0777
public = yes
writable = yes
```

* `sudo systemctl restart smbd`
* `systemctl status smbd`
