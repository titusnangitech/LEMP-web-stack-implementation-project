
# Deployed a LEMP (Linux, Nginx, MySQL, PHP) stack website on AWS

# STEP 01 - Created and connected to an EC2 instance in the us-east-1 region

![ec2 pic](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/f43b1685-2d20-4b4d-b811-598b7960532c)

- **Selected the us-east-1 region and launched a new EC2 instance of t2.nano family with Ubuntu Server 20.04 LTS (HVM) launch EC2**

![creating an ec2 instance with t2 nano](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/67ef9089-e6f1-47c8-aa34-a8b757c75876)

- **Created a key pair**

![creating a key pair](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/2a786407-a7dc-4453-9aad-1b71c6e82796)

- **Created a security group**

![created a security group](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/f75c3051-822c-45b6-9c1e-c27bc34dcddc)

- **Used the existing security group**

![used the existing sg that we have created](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/09b6ee80-17ce-4606-8996-ff6b6a5efbfd)

- **Ec2 instance launched successfully**

![ec2 launched succesfully](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/50e3eced-4a1e-4de3-aa48-5b3b091e3be2)

# STEP 02 – Installed the Nginx webserver

- **populated Mobaxterm with ec2 public IP address, username and key pair details to connect to the EC2 instance**

![populating the mobaxterm with details](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/547bbb00-0465-40ce-a286-9792cd318fc8)



- **connected successfully into the EC2 instance using Mobaxterm**

![connected to the ec2 instance](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/f09d2a1a-68d9-47f5-9b24-efc6f5ef52b5)

- **Switch from ubuntu user to root user**

 ```
sudo -i

```
  
  
![switching to root user](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/cb88f52e-dc1e-4b4d-90f4-49387d12c203)

- **start off by updating my server’s package index. Following that, I can use apt install to get Nginx installed:**

```
apt update
apt install nginx
```
![apt update](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/cd192bec-dd02-46f5-a709-5a5e7947239f)

![install nginx](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/642531de-b1e9-4089-8bf1-a3806e81ee4e)


- **Verify that Nginx is running**

![verify that nginx is running](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/effc6966-8ea9-41bd-a3b5-7062f148d2aa)

  
- **checking if we can connecting to our server from localhost**

![checking if we can connecting to our server from localhost](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/059f5fb4-552f-4408-a3e7-bccff7379dac)

![localhost connection successful](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/39a163ac-e048-4fd6-bdec-8df22487daff)

- **Now it is time for us to test how our Nginx server can respond to requests from the Internet. Open a web browser of your choice and try to access following url. If you see following page, then your web server is now correctly installed and accessible through your firewall.**

  
![connecting from the intenet](https://github.com/titusnangitech/LEMP-web-stack-implementation-project/assets/128609800/1997cf0a-89a1-49a8-8ded-ad0ba2f3f874)

# STEP 03 — Installing MySQL

**Now that i have a web server up and running, I installed a Database Management System (DBMS) to be able to store and manage data for my site in a relational database. MySQL is a popular relational database management system used within PHP environments, I used it in our project.**

```
apt install mysql-server
```

**When the installation is finished, log in to the MySQL console by typing:**
```
mysql
```
**To finish**

# STEP 04 - Installing PHP

**I have Nginx installed to serve your content and MySQL installed to store and manage your data. Now you can install PHP to process code and generate dynamic content for the web server. While Apache embeds the PHP interpreter in each request, Nginx requires an external program to handle PHP processing and act as a bridge between the PHP interpreter itself and the web server. This allows for a better overall performance in most PHP-based websites, but it requires additional configuration. You’ll need to install php-fpm, which stands for “PHP fastCGI process manager”, and tell Nginx to pass PHP requests to this software for processing. Additionally, you’ll need php-mysql, a PHP module that allows PHP to communicate with MySQL-based databases. Core PHP packages will automatically be installed as dependencies**



To install these 2 packages at once, run:

```
apt install php-fpm php-mysql
```


I now have your PHP components installed. Next, you will configure Nginx to use them.

