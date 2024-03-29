# Files: tar / gzip

## tar file vs zip file

A tar file is simply an uncompressed archive consisting of multiple files.
A zip file on the other hand has not just archived the files but compressed them too.

## Create a new none compressed tar archive

```bash
tar -c -v -f $archive.tar $files_or_directories

tar -c -v -f test-tar.tar out/test1 out/test2
```

`-c` Create a new archive.

`-v` Verbose mode.

`-f` The name of the archive file.

`files_or_directories`: List the files and directories you want to include in the archive.

## Extract files from a tar archive

```bash
tar -x -v -f $archive.tar

tar -x -v -f test-tar.tar
```

`-x` Extract files from an archive.

`-v`: Verbose mode.

`-f`: The name of the archive file.

## Create a new compressed tar archive

```bash
tar -c -v -z -f $archive.tar.gz $files_or_directories

tar -c -v -z -f test-tar.tar.gz out/test1 out/test2
```

`-z`: Compress the archive using gzip.

## Extract files from a compressed tar archive

```bash
tar -x -v -z -f $archive.tar.gz

tar -x -v -z -f test-tar.tar.gz
```

## View the contents of an archive without extracting it

```bash
tar -t -v -f $archive.tar

tar -t -v -f test-tar.tar.gz
```

## Compress a file

```bash
# by default, the original file will be replaced with the compressed version
gzip $file_path

# use the -c flag to keep the original file and send the compressed data to standard output
gzip -c $file_path > $file_path.gz

# recursively `-r` compress (or decompress) directories and their contents
# and keep `-k` the original files when compressing
gzip -r -k $dir_path
```

## Decompress a file

```bash
# by default, the compressed version will be replaced with the original file
gzip -d $compressed_file.gz
```

## View the contents of a compressed file without decompress it

```bash
zless $compressed_file.gz
zless $compressed_file.gz | grep $search_pattern
```
