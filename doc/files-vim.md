# Files: vim

## Open a directory listin

```bash
vim $dir_path
vim .
vim src
```

## Exit

```bash
:q
```

## Edit a file

```bash
# 1. open a new or existing file with
vim $file_name .
vim out/test1 .

# 2. type "i" to switch into "insert" mode so that you can start editing the file
i

# 3. update the text with your file

# 4. once you're done, press the escape key "esc" to get out of "insert" mode and back to command mode
[esc]

# 5. type ":w" to save, type ":wq" to save and exit
:wq!

# 6. Type :qa! to exit without saving
:qa!
```

## Search in a file

```bash
# type "/" followed by the text you want to search for and press Enter
/$pattern
/find_some_text
```
