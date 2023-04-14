# EC2 Section - Web Server with Wordpress

## Introduction
On this journey, we will practice launching a web server with WordPress on EC2, so we will configure:
- Launch instances
- Remote instances
- Install php
- Install mariadb and create database
- Install wordpress
- Virtualhost
- Access web server & install and create a wordpress account

# Cloud Research
## Launch Instance
- First we will load the instance first click on EC2

![image](https://user-images.githubusercontent.com/121029600/231914051-93a79b0e-0684-4f13-b4f9-ef185897acff.png)

- In the instance section, click launch instance

![image](https://user-images.githubusercontent.com/121029600/231914186-0750f6d2-d10f-4359-a6df-cefe331c666f.png)

- Give it a name and here I choose Debian OS

![image](https://user-images.githubusercontent.com/121029600/231914299-0c8e2ad3-32d5-4ab2-9c31-6f7f9a839b95.png)

- Then in the keypair section, I click create new keypair

![image](https://user-images.githubusercontent.com/121029600/231914418-40a2ffda-c074-4d8c-9fb2-45d6955a4856.png)

- Give it a name and choose the type then click create keypair

![image](https://user-images.githubusercontent.com/121029600/231914505-152de4ed-5f06-4178-90cd-f26f9dbb0f48.png)

- In network settings, click edit

![image](https://user-images.githubusercontent.com/121029600/231914566-65cfaafb-17e5-4489-a7ea-bf09c3d34eb1.png)

- Here I created a new security group where I allow ssh and http

![image](https://user-images.githubusercontent.com/121029600/231914667-97d9b374-7227-4ccb-a08e-b642bad35b01.png)

- Then I gave userdata the command to install the web server, namely Apache2, and cick create instance

![image](https://user-images.githubusercontent.com/121029600/231914803-1d8650c5-6454-43e5-b35d-8edce60098c9.png)

- OK, if you've tried copying the public IPv4 and accessing it in the browser

![image](https://user-images.githubusercontent.com/121029600/231914957-8115635f-3538-4591-ae53-bde0863e6950.png)

- And yeah. Success

![image](https://user-images.githubusercontent.com/121029600/231915018-5d6eb7e7-40f8-4b01-b676-8b457dc73a8c.png)

- Then here I want to try ssh, so select the instance that was created then click connect

![image](https://user-images.githubusercontent.com/121029600/231915133-c212b1de-a5d9-41c0-bddc-449700abed82.png)

- Copy the commands

![image](https://user-images.githubusercontent.com/121029600/231915214-85af4b0f-8d6b-43e2-8ea3-9407bd69f60d.png)

- Open cmd and enter the directory where the keypair is stored, then paste the command that was copied earlier

![image](https://user-images.githubusercontent.com/121029600/231915342-fa0ba277-9460-4b60-ac2e-00812b4de3d5.png)

- Install PHP 

![image](https://user-images.githubusercontent.com/121029600/231915775-e25bdfa5-bc22-42d1-9348-e234aba424e3.png)

- Integrate php and apache2

![image](https://user-images.githubusercontent.com/121029600/231916075-49462fd0-9d02-4e43-a0aa-3d7399726237.png)

- Install mariadb-server

![image](https://user-images.githubusercontent.com/121029600/231916174-ca466512-224b-4475-ba87-c2760e1a8fae.png)

- Create a database, then create a user and give access to the database

![image](https://user-images.githubusercontent.com/121029600/231916400-2d62840a-242a-4f0d-9b00-7714d533b06b.png)

- Move to /var/www/,then install wordpress

![image](https://user-images.githubusercontent.com/121029600/231916479-5916e77a-1a47-4724-bf8f-80dc1ea71ede.png)

- Unzip package
- Change the ownership of the wordpress folder to user and group www-data

![image](https://user-images.githubusercontent.com/121029600/231916822-96d4815f-f637-4874-b24a-14ea6da638f1.png)

- Move to /etc/apache/sites-enabled/,then edit file 000-default.conf

![image](https://user-images.githubusercontent.com/121029600/231917007-e1139b15-50b9-40bc-a43d-78ccb4b79fb3.png)

- Change DocumentRoot according to the location of the wordpress folder

![image](https://user-images.githubusercontent.com/121029600/231917138-c6bca01f-62e9-466b-b34f-e97a6c82e213.png)

- 

