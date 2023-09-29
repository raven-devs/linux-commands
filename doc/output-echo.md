# Output: echo

```bash
echo "some_text"
echo "$variable"
echo "$($expression)"

echo "hi there!"
echo $(whoami)

# the -e option is a special flag that you can use with the echo command to enable the interpretation of escape sequences within the text you want to display

# without -e (default behavior)
echo "Hello\nWorld"
> Hello\nWorld

# with -e option:
echo -e "Hello\nWorld"
> Hello
> World
```
