# Devops-Project-4-Rearchitecting-Webapp

# Backend Setup

## Setup RDS

```
sudo -i
apt update
apt install mysql-client -y
cd /tmp/
git clone https://github.com/devopshydclub/vprofile-project.git
cd vprofile-project
git checkout aws-Refactor
cd src/main/resources/

# initialize rds
mysql -h rds-mysql.c7rvwaqxmcfm.us-east-1.rds.amazonaws.com -u admin -pX98aNgQ8zvvhl79i34tt accounts < db_backup.sql

# login and validate
mysql -h rds-mysql.c7rvwaqxmcfm.us-east-1.rds.amazonaws.com -u admin -pX98aNgQ8zvvhl79i34tt accounts
show tables;
```
![image](https://user-images.githubusercontent.com/96833570/211896524-7b3c95d6-cefb-4553-9e48-c0b130cb4c0f.png)


After initializing the RDS i deleted the ec2 instance.

## Memcached Setup 

![image](https://user-images.githubusercontent.com/96833570/211895811-506bcfe8-ffcc-4b1a-9b61-85f223044b5b.png)

## Amazon MQ Setup

![image](https://user-images.githubusercontent.com/96833570/211899042-2351bd59-01d2-4f3a-8ac6-bcb120b2d295.png)

## Beanstalk


![image](https://user-images.githubusercontent.com/96833570/211910719-17d56fa3-c079-4d01-bfbb-f3804535bbab.png)

![image](https://user-images.githubusercontent.com/96833570/211910759-5c7db851-59ff-4cd6-9040-e3a417b0c110.png)
