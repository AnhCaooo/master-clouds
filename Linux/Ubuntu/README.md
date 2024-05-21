# Ubuntu 

## Setup Linux user 

### Step 1: login as root user 

```bash
ssh root@<your_ip_address> 
```

### Step 2: Create new user 
Once you add your user, you will be asked to give password.

```bash
adduser <user_name>
```

### Step 3: Add user privileges

```bash
usermod -aG sudo <user_name>
```

### Step 4: Verify your user 

```bash
# option 1: check which groups your user belongs to
groups <user_name> 

# option 2: test command with sudo privileges
sudo ls 
```

## Login and switch to root user from normal user 

Assume you log in to your Linux server with default user. 

```bash 
# login to Linux server with 'example' user
ssh example@<ip_address> 

# in order to switch to 'root', you could try
sudo -s 
```