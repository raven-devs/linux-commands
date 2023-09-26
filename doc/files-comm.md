# Files: comm

Used to compare two sorted text files line by line and display the lines that are unique to each file and the lines that are common between them.

```bash
comm $options $file1 $file2
```

- `$options`:

  `-1` Suppress the display of lines unique to FILE1.

  `-2` Suppress the display of lines unique to FILE2.

  `-3` Suppress the display of lines common to both files.

  `-i` Ignore differences in case (treat uppercase and lowercase characters as equal).

- `$file1, $file2` The names of the two sorted text files you want to compare.

## Usage

```bash
# display lines that are unique to 'out/test1'
comm -23 out/test1 out/test2

# display lines that are common to both files
comm -12 out/test1 out/test2

# display lines that are unique to 'out/test2'
comm -13 out/test1 out/test2

# display lines that are unique to both files
comm -3 out/test1 out/test2
```
