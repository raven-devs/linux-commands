# Command / script

```bash
# execute a script and assign the result to a variable
result=$(ls -a) && echo $result
result1=$(whoami) && result2=$(date) && echo "name: $result1, date: $result2"

# manual (help) for a command
man $command

# help for a command
$command --help

# view the location of a command
whereis $command
whereis ls
```
