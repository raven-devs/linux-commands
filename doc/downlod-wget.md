# Download: wget

Download files from the internet.

```bash
wget $options $URL
```

## Usage

```bash
# download a single file
wget https://example.com/file.zip

# download a file and specify the output filename
wget -O output-file.zip https://example.com/file.zip

# mirror a website recursively
wget --mirror -p --convert-links -P ./local-directory https://example.com/
```
