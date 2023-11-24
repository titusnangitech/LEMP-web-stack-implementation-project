
# Deployed a LEMP (Linux, Nginx, MySQL, PHP) stack website on AWS

# STEP 01 - Created and connected to an EC2 instance in the us-east-1 region

![ec2 pic](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/f43b1685-2d20-4b4d-b811-598b7960532c)

- **Selected the us-east-1 region and launched a new EC2 instance of t2.nano family with Ubuntu Server 20.04 LTS (HVM) launch EC2**

![creating an ec2 instance with t2 nano](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/67ef9089-e6f1-47c8-aa34-a8b757c75876)


![creating a key pair](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/2a786407-a7dc-4453-9aad-1b71c6e82796)

![created a security group](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/f75c3051-822c-45b6-9c1e-c27bc34dcddc)

![used the existing sg that we have created](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/09b6ee80-17ce-4606-8996-ff6b6a5efbfd)

- **Ec2 instance launched successfully**

![ec2 launched succesfully](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/50e3eced-4a1e-4de3-aa48-5b3b091e3be2)

# STEP 02 – Installed the Nginx webserver

- **populated Mobaxterm with ec2 public IP address, username and key pair details to connect to the EC2 instance**




- **connected successfully into the EC2 instance using Mobaxterm**


- **Switch from ubuntu user to root user**


- 

```
Since this is our first time using apt for this session, start off by updating your server’s package index. Following that, you can use apt install to get Nginx installed:
apt update
apt install nginx
```
