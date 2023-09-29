# Unique

```bash
uniq out/test1
echo -e "apple\napple\nbanana\norange\norange" | uniq

# the "-c" (or "--count") option is used to count and display the number of times each line appears in the input
echo -e "apple\napple\nbanana\norange\norange" | uniq -c

# the "-d" (or "--repeated") option is used to display only the lines that are duplicated in the input
echo -e "apple\napple\nbanana\norange\norange" | uniq -d

# to display only the lines that occur once in the input, you can use the "-u" (or "--unique") option
echo -e "apple\napple\nbanana\norange\norange" | uniq -u

# count and display the number of unique lines using both the "-c" and "-u" options
echo -e "apple\napple\nbanana\norange\norange" | uniq -c -u

# the "-i" (or "--ignore-case") option makes "uniq" case-insensitive when comparing lines for uniqueness
echo -e "apple\nApple\nbanana\nBanana" | uniq -i
```
