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
```
