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

## Create Load Balancer 
- Choose load balancer on service catalog

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/0fc050c8-67b8-4041-a1be-4ba45e314f80)

- Click create load balancer

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/36abd241-91cf-4ac2-ad52-07a5c18d7c68)

- Give name for load balancer,and choose subnet from instance that will be used as a load balancer,here we choose auto assign to make it easier and click create

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/31499588-0341-483f-923b-8e2a9386ab10)

## Creating an HTTP Listener
To forward incoming traffic, users need to create a listener that identifies traffic transmitted in compliance with a specified protocol

- In tab listener,click create listener

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/2cd852b2-2aed-4aec-9cef-010ebba86316)

- Give name,choose load balancer,choose protocol,enter port,and enter connection limit.click create

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/82904903-83fc-4922-9663-2d459c1aa3eb)

## Creating a Resource Pool 
After a load balancer and a listener are created, you need to add the instance in the network to a load balancing resource pool

- In tab Pools click create pool

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/e1c4c1e1-5e09-4073-a2e0-24f9e52eaf46)

- Give name,choose load balancer,choose protocol and choose method,here i choose round robin because this mode is very easy to verify, click create

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/2460a76a-b4ff-4cc3-93f8-6dd9f155a4ac)

## Add Resource
After a load balancing resource pool is created, you can open the detail page by clicking the name of the resource pool and add instances to the pool

- Click add resource 

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/9c6b7179-f10a-4cbb-a7c6-6fd416504cdd)

- Choose subnet,choose instance and vNIC,enter port number,and weight. Add 2 instances we created earlier for the load balancer,that is loadbalancer-1 and loadbalancer-2

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/91223091-c356-4c54-a84b-c53017442827)

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/e04deaa0-2cb8-431e-a304-c6bbf87b29d0)

note : When adding an instance, you need to specify Weight. The weight of an instance defines whether a load balancer takes priority in distributing network load to the instance,and at this time we give the same priority which is 1 weight

## Associate Floating IP 
- In tab load balacers choose the loadbalancer and click more then choose associate floating IP

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/0ad87bad-7f44-41ec-a13f-a0461e5c948d)

- Choose your floating IP,floating IP use for access web server from loadbalancer

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/d676bf7b-fb85-4c18-bdcc-77a83b123ec8)

- verify When creating a load balancing resource pool, you can set LB Mode to one of the following types:

## Mode Round Robin
Polling: The load balancer distributes traffic to instances in a resource pool in turn based on their weights. This load balancing mode is usually selected for processing short connection services, such as the HTTP service

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/d52e3a51-fdbc-4c78-90bf-ecbbde166d99)

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/28f63e6a-2d69-4c9e-a166-655eb0269b17)

- Refresh page and then page will change to another web server instance
![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/a7c60a50-6caa-43b3-b57b-13b8fdf732c9)

## Mode Least Connection 
For change the method,you go to pools and click pool load balancer then click more actions and choose edit, Then you can change the method

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/38613ed4-ea4b-4581-97a0-56586d0420c9)

Minimum number of connections: The load balancer preferentially sends service requests to instances with the fewest connections. This load balancing mode is usually selected for processing long connection services, such as the database connection service. If the priority of an instance in the resource pool has been adjusted, the system will distribute traffic based on the priority and current connection quantity of instances

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/e40195fd-0910-4315-8b77-42c8ce581288)

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/a1b95862-566e-4b3f-a8f9-a53b9a527891)

## Mode Source IP 
![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/b90c1018-973e-4835-8993-8af06eff2c89)

Source IP address: The load balancer performs hash calculation using the source IP address of a request, and determines which instance to send the request to by factoring in the calculation result and instance weights. This load balancing mode enables the load balancer to send all requests of one client to the same server and applies to TCP services without the cookie function

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/a4445a02-d787-4ac5-948a-5ffb9fdb2d10)

When you refresh the page many times the web server will remain the same and doesn't change






