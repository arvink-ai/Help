# Vmware
## tips
1. How do I mount shared folders in Ubuntu using VMware tools?
Ans: 
(https://askubuntu.com/questions/29284/how-do-i-mount-shared-folders-in-ubuntu-using-vmware-tools): Virtual Machine settings Folder sharing = Always Enabled Make sure you have at least one Folder shared between the host and guest On the Ubuntu Guest check /mnt/hgfs that you can access your shared folder.

If you don't see your shared folders (automounted) inside /mnt/hgfs , run VMware configuration tools:

sudo vmware-config-tools.pl

update your /etc/fstab using the details below:

.host:/{shared-folder} /{path-to-mount-on} vmhgfs defaults,ttl=5,uid=1000,gid=1000 0 0

Restart your vm (You may need to restart few times or get error message saying unable to mount just skip the error and restart)