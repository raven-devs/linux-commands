# Files search: find

Search for files and directories within a specified directory hierarchy based on various criteria.

```bash
find $directory $options $expression
```

- `$directory` Specifies the directory where the search will begin.

- `$options` These are optional flags that modify how the find command behaves.

- `$expression` Specifies the search criteria or conditions that files and directories must meet to be included in the search results.

## Usage

```bash
# find all
find $dir_name
find src

# find by name
find $dir_name -name "$file_name"
find src -name "global.d.ts"
find src -name "types"
find . -name "*.jpg"  # Find all files with a ".jpg" extension in the current directory and its subdirectories

# find by a file ext
find $dir_name -name "*.$file_ext"
find src -name "*.ts"

# find directories only
find $dir_name -type d
find src -type d
find ~/ -type d -name "docs"  # Find all directories named "docs" in the home directory

# find regular files only
find $dir_name -type f
find src -type f

# find by modification time
find src -mtime -$days
find /data -type f -mtime -3  # find all files modified within the last 3 days in the "/data" directory

# find by size
find src -size $size  # c (bytes), k (kilobytes), M (megabytes), or G (gigabytes)
find src -size 30c

# -and, -or, -not: Logical operators to combine multiple search conditions.
# For example, finds files with either ".txt" or ".log" extensions:
find /data -name "*.txt" -or -name "*.log"

# -exec <command> {} \;: Executes a command on each file or directory found. You can use {} as a placeholder for the found item.
# For example, find and delete all files with a ".tmp" extension in the "/temp" directory:
find /temp -type f -name "*.tmp" -exec rm {} \;
```
