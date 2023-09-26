# Command / script

```bash
# execute a script and assign the result to a variable
result=$(ls -a) && echo $result
result1=$(whoami) && result2=$(date) && echo "name: $result1, date: $result2"

# execute a script file
./$script_file.sh

# run a command in a background
$command &
ls -l | lpr &

# manual (help) for a command
man $command

# help for a command
$command --help

# used to quickly retrieve brief descriptions of Unix commands and system functions from the system's manual (man) pages
whatis $command

# view the location of a command
whereis $command
whereis ls
```
