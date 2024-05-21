# Documentation to play with EC2 

## Create and setup EC2 

### Set up VPC (Virtual Private Cloud)
You should set up VPC first by following this [VPC instruction][VPC instruction]. Then continue next steps 

### Create your EC2
Check more from this video from 10:53 to end: [How to Create an AWS VPC with Public and Private Subnets](https://www.youtube.com/watch?v=ApGz8tpNLgo) 

### Login to your EC2 via OpenSSH
Check from AWS 

### Create you Linux user (for Ubuntu)
See my [setup Linux user][ubuntu user setup] to set up your user in your EC2 

### Enable Password Authentication in AWS EC2
At default, you have to pass cert key with SSH in order to log in to your EC2. However, there is a way to use password instead. 

#### Step 1: Login to AWS instance 
This case, default user is `ubuntu`

```bash 
ssh -i your-key.pem ubuntu@ip_address
```

#### Step 2: Set password for default user 

```bash
sudo passwd ubuntu
```

#### Step 3: Edit `sshd_config` file.

```bash 
sudo vi /etc/ssh/sshd_config
```

- Find the line containing `PasswordAuthentication` parameter and change its value from `no` to `yes`
```
PasswordAuthentication yes
```

- If you want to set up `root` login, find `PermitRootLogin` and change its value from `prohibit-password` to `yes`

```
PermitRootLogin yes
```

After this changes save file and exit.

#### Step 4: Restart the SSH service.

```bash
service ssh restart
```

#### Step 5: Test your work 

```bash
ssh ubuntu@ip_address
```


[VPC instruction]: https://github.com/AnhCaooo/master-clouds/blob/main/AWS/VPC.md
[ubuntu user setup]: https://github.com/AnhCaooo/master-clouds/blob/main/Linux/Ubuntu/README.md