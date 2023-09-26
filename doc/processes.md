# Processes

- <https://ss64.com/osx/ps.html>
- <https://ss64.com/osx/ps_keywords.html>

## List processes

```bash
top
ps aux
ps aux | grep $pattern
```

## All processes associated with the current terminal session or user session

```bash
ps -a
ps -a -o user,uid,gid,pid,ppid,pgid,state,%cpu,%mem,lstart,command
```

## All processes running on the system (system-wide)

```bash
ps -e
ps -e -o user,uid,gid,pid,ppid,pgid,state,%cpu,%mem,lstart,command
```

## Kill a process

```bash
kill -9 $PID

kill -9 19046
```

## Find a process listening a port

```bash
lsof -i tcp:$PID

lsof -i tcp:3000
```
