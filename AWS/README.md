# AWS documentation 

Documentations to help config AWS to have your own cloud instance running 

## Table of contents

- [VPC](#vpc)
- [EC2](#ec2)

## Step 1: set up VPC 
A VPC is an isolated portion of the AWS Cloud populated by AWS objects, such as Amazon EC2 instances.

See [VPC setup][VPC setup] to learn and familiarize how to set up VPC 

## Step 2: create EC2 
Amazon EC2 allows you to create virtual machines, or instances, that run on the AWS Cloud.

See [EC2 setup][EC2 setup] to learn and familiarize how to set up EC2 

## Step 2: create Elastic IP
**Note**: for free tier, you are allowed to use only one Elastic IP address for free. If you want to have new one, you need to delete existing one and create new one.
Also, you will be charged if Elastic IP is not assigned to any EC2. So please remember to delete it when you shut down your EC2 



[VPC setup]: https://github.com/AnhCaooo/master-clouds/tree/main/AWS/VPC.md
[EC2 setup]: https://github.com/AnhCaooo/master-clouds/tree/main/AWS/EC2.md
