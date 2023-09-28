# Network

## List all open internet connections

```bash
# List of
lsof -i
lsof -i | grep -E "(LISTEN|ESTABLISHED)"
```

## Network configuration, route management, and interface administration

For macOS: `brew install iproute2mac`.

```bash
#  list of all network interfaces and their associated IP addresses
ip address show
```

## Trace the route that packets take from a local computer or device to a remote destination host or server

```bash
#  list of all network interfaces and their associated IP addresses
traceroute example.com
```

## Test the reachability and responsiveness of a remote host

```bash
#  ping a host or IP address
ping example.com

# by default, "ping" sends packets indefinitely, to specify the number of packets to send using the "-c" option
ping -c 5 example.com

# set the time interval between packets using the "-i" option
ping -i 2 example.com

# set the size of the packets in bytes using the "-s" option
ping -s 100 example.com
```

## View or set the hostname of the local system

```bash
#  list of all network interfaces and their associated IP addresses
hostname
```

## Perform DNS (Domain Name System) lookups and query DNS servers to retrieve various types of DNS records associated with a given domain or hostname

```bash
host www.example.com
```
