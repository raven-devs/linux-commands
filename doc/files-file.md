# Files: file

```bash
# determine the file type of a single file
file $file_path

# display the MIME type
file -i $file_path

# batch processing
# this command uses "find" to locate files, runs the "file" command on each file found, and then uses "grep" to filter the results for text files.
find /path/to/directory -type f -exec file {} \; | grep "text"
```
