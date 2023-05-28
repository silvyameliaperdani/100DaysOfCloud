# Load Balancer at EasyStack [ Mentor : Dea Tristianti ]

## Introduction
On this journey, we will learn how to make load balancing on easy stack, the things we will do this time are:

- Create instances
- Create a security group
- Add a security group to the instance
- Create a simple web in an example
- Create Load Balancers
- Create an HTTP Listener
- Create a Resource Pool
- Add resources
- Associate floating IP

# Cloud Research 

## Create Instance 
In load balancing we need 2 instances, and we have created 2 instances as shown below, for how to create an instance can be seen in the previous journey

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/c48495de-fe05-4c29-9acf-ec82b5eb4523)

## Create Security Group 
To make the instance web accessible, we need to grant HTTP permission to it, for that we need to create a security group
- Give it a name then click create

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/4276035d-920e-42a3-b2fa-645e3d3d3bd6)

- Click add rule

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/488eb75a-577d-4159-b3c4-47c59b1dce1f)

- Choose HTTP,for others leave it default and click add rule

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/5b08b924-e5a9-41c4-a319-c416e6d0c4dd)

## Add Security Group to Instance 
- Select instance,click more and choose edit security group

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/818ea88a-d9b0-4e1b-a630-c8ec3ac7cc5b)

- Then,click security group that you want to add,click save

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/ef4193dd-ed52-4f5c-b3ae-9fb59319e108)

## Create Simple Web in Instance 
First you must remote the instance,you can remote by keypair or password

## First instance 
- Install httpd 

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/a9f7459b-c6a4-4e13-991b-7997efca3b86)

-Edit file index.html 

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/a257a84e-9d58-4baf-818e-de4d94e541dd)

- Enter teks that you need to display when accessed by a web server

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/cdd16e2f-5d69-4d50-846d-b0c235f2c138)

- Start and enabled httpd service

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/6657427d-1439-4b51-8fd3-47130fb7953c)

## Second Instance 
- Install httpd 
- Edit file index.html 
![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/08b19e8d-e1b2-4ba5-9911-9de838d96ba4)

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/10dc8859-8be9-4ddd-bfbd-b8ac5f823e8b)

- Start and enabled httpd service

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/6d64daa5-b391-4a63-b5e3-dc22c8b961e6)


