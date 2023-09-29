# Files search: locate

Search for files and directories on a system quickly. It relies on a pre-built database, which makes it much faster than searching the entire filesystem when compared to commands like "find." The "locate" command is especially useful when you need to find files quickly by name, but it may not return real-time results because the database is typically updated periodically.

```bash
# the "locate" command relies on a pre-built database to perform its searches.
# This database is typically updated regularly. If you suspect that the database is not up to date, you can update it manually.
sudo launchctl load -w /System/Library/LaunchDaemons/com.apple.locate.plist

# search for files by name
locate myfile.txt

# use wildcards, such as asterisks (*) and question marks (?), to perform more flexible searches
# this command will return all file paths that contain "example" in their names
locate '*example*'

# by default, "locate" performs case-insensitive searches. To perform a case-sensitive search, you can use the "-b" option
locate -b myfile.txt

# limit the number of results displayed using the "-n" option
locate -n 5 myfile.txt

# display only exact matches, use the "-e" option
locate -e myfile.txt
```
