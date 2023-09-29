# Script

```bash
# execute a script and assign the result to a variable
result=$(ls -a) && echo $result
result1=$(whoami) && result2=$(date) && echo "name: $result1, date: $result2"

# execute a script file
./$script_file.sh

# the PATH environment variable controls where the shell looks for executable files
echo $PATH

# to append both standard output (stdout) and standard error (stderr) to a specified log file when executing a Bash script in Linux by using the `2>&1` redirection
./your_script.sh >> /path/to/output.log 2>&1
```
