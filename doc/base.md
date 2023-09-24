# Base

```bash
# print to console
echo "some_text"
echo "$variable"
echo "$($expression)"

echo "hi there!"
echo $(whoami)

# exit from terminal
exit

# print current date and time
date "+%Y-%m-%dT%H:%M:%S"

# clear terminal
clear

# execute a script and assign the result to a variable
result=$(ls -a) && echo $result
result1=$(whoami) && result2=$(date) && echo "name: $result1, date: $result2"
```
