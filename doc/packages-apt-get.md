# Packages: apt-get

```bash
# update the local package database from the configured repositories
sudo apt-get update

# upgrade all installed packages to their latest versions
sudo apt-get upgrade

# install one or more packages
sudo apt-get install package1 package2

# uninstall packages while keeping their configuration files
sudo apt-get remove package1 package2

# remove the packages along with their configuration files
sudo apt-get purge package1 package2

# search for packages by name or keyword
apt-cache search keyword

# displays detailed information about a package
apt-cache show package-name
```
