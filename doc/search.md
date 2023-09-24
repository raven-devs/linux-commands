# Search

## grep

Global Regular Expression Print.

```bash
grep $options $pattern $file
```

- `$options`:

  `-i`: Perform a case-insensitive search.

  `-r, -R`: Recursively search directories.

  `-l`: List only the names of files containing the pattern.

  `-n`: Display line numbers along with matching lines.

  `-v`: Invert the match, showing lines that do not contain the pattern.

- `$pattern` A regular expression or text string to search for.

- `$file` An optional argument that specifies the files to search within. If not to provide any filenames, "grep" will read from standard input.

## Usage

```bash
# Search case-insensitive and recursively for "export" pattern in the "src" dir and display found file names with line numbers along with matching lines
grep -irn "export" src

> src//types/global.d.ts:3:export {};
```

```bash
# Search case-insensitive for "ravendevs" pattern in the "LICENSE" file and display found line numbers along with matching lines
grep -in "ravendevs" LICENSE

> 3:Copyright (c) 2023 RavenDevs
```

```bash
# Search for lines in a file that do not contain the word "error"

grep -v "error" logfile
```
