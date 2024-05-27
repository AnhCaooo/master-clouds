# Commands to update, install and remove packages 
The reason why I mention [Update packages](#update-packages) part before [Install packages](#install-packages) is it is recommended to update all existing packages in your Linux machine. Later I will try to install package called 'Docker'

## Basic instructions
### Update packages 
Update all existing packages
```bash
sudo apt update
```

### Install packages 
```bash
sudo apt install <package_name>
```

### Remove packages 
#### Detail commands 
1. Remove the given package
```bash 
sudo apt-get remove <package_name>
```
2. Purge any related code
```bash
sudo apt-get purge <package_name>
```

3. Autoremove
```bash
sudo apt-get autoremove
```

4. Check everything is correctly removed
```bash
sudo apt-get clean
```

#### All in one command 
```bash
sudo apt-get purge --auto-remove packagename
```
## Advanced instructions
### Install Docker on Ubuntu 20.04
Learn more by reading [Install Docker Engine on Ubuntu](https://docs.docker.com/engine/install/ubuntu/)

