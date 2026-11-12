** File System Structure **

/	Root, the top of everything

/boot   kernel image 

/home	Personal folders for each user (yours is /home/shruti)

/etc	System configuration files

/var	Changing data: logs (/var/log), web files, caches

/usr	Installed programs and libraries
/sbin   more binaries
/bin    more binaries 
/lib    more libraries

/bin, /sbin	Essential commands (normal and admin)

/lib    libraries

/tmp	Temporary files, cleared on reboot

/root	Home folder of the root (admin) user

/dev	Device files (disks, terminals)

/proc, /sys	Live info about the system and kernel

/opt	Optional third-party software

/mnt, /media	Mount points for other drives (in WSL, /mnt/c is your Windows C: drive)


See the structure 
ls /                  # list the root directory

ls -l /               # detailed list

ls -la ~              # include hidden files in your home

tree -L 1 /           # show as a tree, 1 level deep

tree -L 2 ~           # 2 levels (install first: sudo apt install tree)


