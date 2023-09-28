# Connection: ssh

## Create a new ssh session

```bash
# Secure Shell
ssh user_name@host_name $sommand

ssh v-sergey@speechservice-dev.lingsoft.fi
```

## File transfer

```bash
# Secure Copy Protocol
scp $source $destination
```

`$source` The file or directory to copy. It can be a local file or a remote file specified in the form of `user@host:/path/to/file` if copying from a remote server.

`destination`: The location where to copy the source file or directory. It can also be a remote location specified similarly to the source.

```bash
# copy a file from the local machine to a remote server
scp local-file.txt user@remote-server:/path/to/destination/
```

```bash
# copy a file from a remote server to the local machine:
scp user@remote-server:/path/to/remote-file.txt local-destination/
```

```bash
# copy a directory and its contents from the local machine to a remote server
scp -r local-directory/ user@remote-server:/path/to/destination/
```

## Logout

```bash
logout
```
