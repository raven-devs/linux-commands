# Data sync: rsync

To efficiently copy and synchronize files and directories between two locations, which can be local or remote, while minimizing data transfer and ensuring data integrity.

## Basic syntax

```bash
rsync $options $source $destination
```

## Usage

```bash
# to copy files or directories from one location to another on the same system
# this command copies the contents of the source directory to the destination directory while preserving file attributes and recursively copying subdirectories
rsync -av outsync1/ outsync2/

# to perform a synchronization where only the differences between the source and destination are transferred (making it efficient for backups), use the "-u" (or "--update") option
rsync -avu outsync1/ outsync2/

# to copy files to remote servers over SSH, which is a secure method for data transfer
rsync -avz -e ssh /local/source/ user@remote-server:/remote/destination/

# use the "--dry-run" option to simulate the synchronization without making any actual changes, this is useful for previewing what "rsync" would do
rsync -av --dry-run /source/directory/ /destination/directory/

# use the "--exclude" option to exclude specific files or directories from the synchronization
rsync -av --exclude="*.log" /source/directory/ /destination/directory/

# the "-v" (or "--verbose") option provides detailed information about the synchronization process, showing each file as it is transferred
rsync -av /source/directory/ /destination/directory/
```
