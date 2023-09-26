# Files: head

Display the beginning (or the top) of a text file

```bash
head $options $file
```

- `$options`:

  `-n $lines_number` Display the first `$lines_number` lines of the file.

- `$file` The name of the file you want to display the last lines of. If not provided, "tail" will read from standard input (e.g., output from another command).

## Usage

```bash
# display the first 15 lines of a file
head -n 15 -f out/test1
```
