# Keep system upto date
## Debian, Ubuntu
  * `sudo apt-get update` updates the list of available packages and their versions, but it does not install or upgrade any packages.
  * `sudo apt-get upgrade` only upgrades the packages which have a new release available as stated in the sources.list file in the “/etc/apt” folder.
  * `sudo apt-get dist-upgrade` its upgrade plus will also upgrade to a new kernel, is proactive and it installs new packages or removes existing ones on its own in order to complete the upgrade.  
  * `sudo apt-get autoremove` will remove those dependencies that were installed with applications and are no longer used by anything else on the system.

# Common
  * find
  * `ls -la`
  * dir
  * grep
  * `rm -fr path/to/folder`
  * `sudo su` switch to root.
  * 
# Permission settings
## chmod [discussion thread](https://www.linux.org/threads/file-permissions-chmod.4124/), [Stackoverflow](https://stackoverflow.com/a/8328529/209609)
  * `sudo chmod -R 777 ./` give recursive permission to all the files in the current directory have all permissions.
  * `sudo chmod -R 754 /folder` give recursive permission to the folder and it's all contents
  * chmod wont work for filesystem NFTS / exFAT / FAT32
  * numeric equivalent (octal): read (r) = 4 , write (w) = 2 , execute (x) = 1 
    * First Number - Owner - 7 (4+2+1) - Read, write, and execute for the user.
    * Second Number - Group - 5 (4+1) - Read and execute for the group.
    * Third Number - World - 4 - Read for others.
```
    N   Description                      ls   binary    
    0   No permissions at all            ---  000
    1   Only execute                     --x  001
    2   Only write                       -w-  010
    3   Write and execute                -wx  011
    4   Only read                        r--  100
    5   Read and execute                 r-x  101
    6   Read and write                   rw-  110
    7   Read, write, and execute         rwx  111
```
  * `chmod u=rwx,g=rx,o=rx /path/to/file` alternative syntax (no spaces used in permission)
## chown
  * `chown -R user:root /home/user` change owner and group recursively
 
# vi
  * `:wq` save and quit
  * `:q!` force quit without saving



# restart system
  * `sudo reboot`
  * `sudo shutdown -r +5` will restart in 5 mins. replace `+5` with `now` for immediate.

