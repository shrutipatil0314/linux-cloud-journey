1. Who am I?

whoami = your username

id   = your user ID, group ID, and groups

id shruti =  same info for a specific user

who  = who is logged in

w    = who is logged in and what they're doing

last = login history

2. Where user info is stored

File	

/etc/passwd =	List of users (name, ID, home folder, shell)

/etc/shadow =	Encrypted passwords (only root can read)

/etc/group  = 	List of groups and their members

/etc/sudoers =	Who can use sudo

3. Create users

sudo useradd testuser                      # basic (no home folder on some systems)

sudo useradd -m testuser                   # -m creates a home folder

sudo useradd -m -s /bin/bash testuser      # set the shell too

sudo useradd -m -c "Test User" -s /bin/bash testuser

sudo adduser testuser                      # friendlier, interactive

4. Set and manage passwords

sudo passwd testuser          # set or change a user's password

passwd                        # change your own password

sudo passwd -l testuser       # lock the account

sudo passwd -u testuser       # unlock the account

sudo passwd -e testuser       # force a password change at next login

sudo chage -l testuser        # show password expiry info

sudo chage -M 90 testuser     # password expires after 90 days

5. Modify users (usermod)

sudo usermod -aG sudo testuser          # add to the sudo group (-a is important!)

sudo usermod -aG developers testuser    # add to another group

sudo usermod -s /bin/zsh testuser       # change shell

sudo usermod -l newname testuser        # rename the user

sudo usermod -d /home/newhome -m testuser   # move home folder

sudo usermod -L testuser                # lock account

sudo usermod -U testuser                # unlock account

sudo usermod -c "New comment" testuser  # change the description

6. Delete users

sudo userdel testuser          # delete user, keep home folder

sudo userdel -r testuser       # delete user and home folder

sudo deluser testuser          # Ubuntu/Debian friendly version

7. Groups

groups                         # groups you belong to

groups testuser                # groups of another user

sudo groupadd developers       # create a group

sudo groupadd -g 1500 devops   # create with a specific ID

sudo groupmod -n engineers developers   # rename a group

sudo groupdel engineers        # delete a group

sudo gpasswd -a testuser developers     # add user to group

sudo gpasswd -d testuser developers     # remove user from group

getent group developers        # show group and members

newgrp developers              # switch your active group in this session

8. Switch users and use sudo

su - testuser                  # switch to another user (needs their password)

sudo su -                      # become root

sudo -i                        # root shell

sudo -u testuser whoami        # run one command as another user

sudo command                   # run one command as root

sudo -l                        # list what you are allowed to run with sudo

sudo !!                        # rerun the last command with sudo

exit                           # leave the switched user


9. The /etc/sudoers file

Never edit it with nano directly. A typo can break sudo for everyone. Always use visudo, which checks the syntax before saving:


sudo visudo


10. Lock down and check

sudo lastlog                   # last login for every user

sudo faillog                   # failed logins (if available)

sudo grep sudo /var/log/auth.log   # who used sudo

sudo usermod -s /usr/sbin/nologin testuser   # block interactive logi

