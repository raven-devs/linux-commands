# Info: Disk

```bash
# file system information
df

# disk usage, by default, displays sizes in bytes
du $dir_path

# use the "-h" (or "--human-readable") option to make the sizes more human-readable
du -h $dir_path

# multiple Directories
du -h $dir_path1 $dir_path2 $dir_pathN
du -h node_modules src

# limit the depth of the directory hierarchy displayed in the output use the "-d" option
du -h -d=1 node_modules
```
