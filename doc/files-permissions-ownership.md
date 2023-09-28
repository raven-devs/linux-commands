# Files: permissions and ownership

## File permissions

Each file is associated with an owner and a group and assigned with permission access rights for three different classes of users:

- The file owner.
- The group members.
- Others (everybody else).

View file permissions

```bash
ls -l $file_path

-rw-r--r-- 12 linuxize users 12.0K Apr  8 20:51 filename.txt
|[-][-][-]-   [------] [---]
| |  |  | |      |       |
| |  |  | |      |       +-----------> 7. Group
| |  |  | |      +-------------------> 6. Owner
| |  |  | +--------------------------> 5. Alternate Access Method
| |  |  +----------------------------> 4. Others Permissions
| |  +-------------------------------> 3. Group Permissions
| +----------------------------------> 2. Owner Permissions
+------------------------------------> 1. File Type
```

The first character shows the file type. It can be a regular file (-), directory (d), a symbolic link (l), or any other special type of file.

The next nine characters represent the file permissions, three triplets of three characters each. The first triplet shows the owner permissions, the second one group permissions, and the last triplet shows everybody else permissions.

## Change the permissions of files and directories

```bash
# basic syntax
chmod $options $who=$permissions $file_path
```

- `$options`:

  `-R` Recursively change permissions for all files and directories under a directory.

- `$who` Specifies who you want to change the permissions for and can be one or more of the following:

  `u` for file owner, if the `u` flag is omitted, the default one is `a` and the permissions that are set by umask are not affected.

  `g` for the users who are members of the group

  `o` for all other users

  `a` for all users (equivalent to specifying `ugo`)

- `$permissions` Specifies the permissions you want to set, using symbolic or octal notation.

  `+` Adds the specified permission(s).

  `-` Removes the specified permission(s).

  `=` Sets the specified permission(s) and removes all others.

  `r` Allows reading or viewing the contents of a file or directory.

  `w` Allows modifying or deleting a file, as well as creating or deleting files in a directory.

  `x` Allows running a file as a program or script or accessing the contents of a directory.

`$file_path`: The file or directory.

```bash
# grant read-write-execute permissions to the owner to a file or a dir recursively
chmod -R u+rwx file.txt

# adds read permission for the owner of the file
chmod u+r file.txt

# removes write permission for the owner of the directory
chmod u-w src

# give the members of the group permission to read the file, but not to write and execute it
chmod g=r file.txt

# remove the execute permission for all users
chmod a-x file.txt

# recursively remove the write permission for other users
chmod -R o-w src

# Remove the read, write, and execute permission for all users except the file’s owner
chmod og-rwx file.txt
chmod og= file.txt

# Give read, write and execute permission to the file’s owner, read permissions to the file’s group and no permissions to all other users:
chmod u=rwx,g=r,o= file.txt
```

## Change the ownership of files and directories

```bash
# basic syntax
chown $options $user_name:$group_name $file_path
```

- `$options`:

  `-R` Recursively change the ownership for all files and directories under a directory.

- `$user_name` User name.

- `$group_name` Group name.

- `$file_path` The file or directory..

```bash
# change the owner of a file to the user "alice" and the group "users"
chown alice:users myfile.txt

# change the owner of a directory and its contents recursively
chown -R bob:developers mydirectory/

# change only the group ownership of a file
chown :admins file.txt
```

## Changing file permissions in bulk

```bash
find /var/www/my_website -type d -exec chmod u=rwx,go=rx {} \;
find /var/www/my_website -type f -exec chmod u=rw,go=r {} \;
```
