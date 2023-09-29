# Files

```bash
# make a dir
mkdir $dir_path

# navigate to a dir
cd $dir_path

# navigate to a root dir
cd /

# navigate to a parent dir
cd ../

# refer to a home dir
~/

# refer to a current dir
.

# open a current dir
open .

# open a file or a dir
open $file_path

# current dir
pwd

# list files
ls -a
ls -a $dir_path
ls -al
ls -al $dir_path

# list a file
ls -a | grep $pattern

# create a file
touch $file_path

# replace a file content
echo "$data" > $file_path

# append a file content
echo "$data" >> $file_path

# delete an empty dir
rmdir $dir_path

# delete a file or a dir
rm -r $file_path
rm -rf $file_path

# rename a file or a dir
mv $file_path1 $file_path2

# copy a file
cp $file_path1 $file_path2y

# start writing to a file
> $file_path
(to exit: command + C)

# empty the content of a file
true > $file_path

# count the number of lines, words, and characters in a file
wc $file_path

# to calculate number of files in a directory
ls -l | grep "^-" | wc -l

# ls -l: This command lists the files and directories in the current directory in long format. The long format includes additional information about each file or directory, such as permissions, owner, group, size, and modification time.

# grep "^-": The grep command is used to filter the list of files and directories. In this case, we use grep to only select lines that start with a hyphen -, which indicates regular files. This filters out directories and other special files.

# wc -l: Finally, the wc command with the -l option counts the number of lines in the filtered output. Since each line represents a regular file, this gives you the total number of files in the directory.
```
