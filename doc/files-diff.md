# Files: diff

Used to compare and highlight the differences between two text files or directories.

```bash
head $options $file1 $file2
```

- `$options`:

  `-q` Only report whether the files differ, without providing detailed differences.

  `-r` Recursively compare directories.

  `-i` Ignore case differences in files.

  `-u` Output unified context diffs (default).

  `-c` Output context diffs.

  `-y` Output the differences in a side-by-side format.

  `-w` Ignore whitespace and indentation changes.

  `-B` Ignore changes that only involve blank lines.

- `$file1, $file2` The names of the two files you want to compare. These can be text files or directories.

## Usage

```bash
# compare two text files
diff -q out/test1 out/test2

# compare two text files and display the differences in a unified format
diff out/test1 out/test2

# compare two directories and show differences recursively
diff -r out out2

# compare two text files and display context
diff -c out/test1 out/test2

# show side-by-side differences between two files
diff -y out/test1 out/test2
```
