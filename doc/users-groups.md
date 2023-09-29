# Users and groups

## List users and groups

```bash
# print a current user name
whoami

# print current user id and a current user group id
echo $UID
echo $GID

# print user identity
id

# list all user groups
cat /etc/group

# list the groups to which a specific user belongs
groups $username

# list all users
cat /etc/passwd
```

## Create a new user

```bash
# create a new user with the default settings
sudo useradd john

#  create a user with a specific home directory and login shell
sudo useradd -m -d /home/myuser -s /bin/bash myuser

`-m` Create the users home directory if it doesn not exist.

`-d` Specify the users home directory.

`-s` Set the users login shell.

# assign a user to one or more supplementary groups using the -G option
sudo useradd -G group1,group2 myuser

# by default, "useradd" does not set a password for the new user.
# Set the user's password
sudo passwd myuser
```

## Change a user

```bash
# use the "-l" option to change the username of an existing user
sudo usermod -l newusername oldusername

# the "-u" option allows you to change the user's UID,
# be cautious when changing the UID, as it can affect file ownership and permissions
sudo usermod -u newuid username

# use the "-d" option to change the user's home directory
sudo usermod -d /new/home/directory username

# the "-s" option allows you to change the user's login shell
sudo usermod -s /bin/bash username

# to add a user to one or more groups, you can use the "-aG" option. To remove a user from a group, use "-G"
sudo usermod -aG groupname username   # add user to group
sudo usermod -G groupname username    # replace user's groups with groupname

# Use the "-L" (lock) and "-U" (unlock) options to lock or unlock a user account, preventing or allowing login
sudo usermod -L username   # lock the account
sudo usermod -U username   # unlock the account
```

## Create a new group

```bash
sudo groupadd mygroup
```

## Execute commands with the privileges of the superuser or another user

```bash
# run a command as the superuser (root), the "sudo" command will prompt the user for their password to confirm their identity and then execute the specified command as root
sudo $command

# to execute a command as a user other than root by specifying the "-u" option
sudo -u $username $command

# displays a list of available commands that the user can execute with "sudo"
sudo -l

# to execute a command in a new shell environment with superuser privileges, use the "-i" option
# this starts a new shell as the superuser, allowing you to execute multiple commands with elevated permissions
sudo -i

# the "sudoers" configuration file (usually located at "/etc/sudoers") controls who can use "sudo" and what commands they can execute; to edit this file, you should use the "visudo" command, which provides syntax checking to prevent configuration errors
sudo visudo
```
