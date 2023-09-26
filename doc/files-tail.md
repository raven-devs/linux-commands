# Files: tail

Display the last few lines of a text file or a stream of text. It is particularly useful for viewing the most recent entries in log files or monitoring the output of continuously updated files.

```bash
tail $options $file
```

- `$options`:

  `-n $lines_number` Display the last `$lines_number` lines of the file.

  `-f` This option is used for monitoring files in real-time. It will keep the "tail" command running and display new lines as they are appended to the file. This is especially useful for watching log files as they are updated.

  `-s $seconds` These options are often used in combination with `-f` to control how frequently "tail" checks for new data in the file when following it.

- `$file` The name of the file you want to display the last lines of. If not provided, "tail" will read from standard input (e.g., output from another command).

## Usage

```bash
# display the last 10 lines of a file and continuously monitor a file for new data every 5 seconds
tail -n 10 -f -s 5 file_log.log

tail -n 100 file_log.log | grep "text_to_search"
```
