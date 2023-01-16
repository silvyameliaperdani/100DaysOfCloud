

# ELB [Elastic Load Balancing] & ASG [Auto Scalling Groups] - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## Scalability & High Availability 
- So if your app is scalable, it means it can handle bigger loads by adapting
- There are two types of scalability in the Cloud :
 - vertical scalability
 - horizontal scalability
- Scalability will be connected, but differ high availability

## Vertical Scalability 
Vertical Scalability means increasing the size of the instance, example from t2.micro to t2.large. Very common for non-distributed systems, such as databases
## Horizontal Scalability 
Horizontal Scalability means increasing the number of instances / systems for your application. This is very common for web applications / modern applications.And, it's easy to horizontally scale thanks the cloud offerings such as Amazon EC2
## High Availability 
High Availability usually goes hand in hand with horizontal scaling, running your application / system in at least 2 Availability Zones, The goal of high availability is to survive a data center loss (disaster)

## For Example 
- Vertical Scaling: Increase instance size (= scale up / down) 
• From: t2.nano -0.5G of RAM, 1 vCPU 
• To: u-12tb1.metal –12.3 TB of RAM, 448 vCPUs
- Horizontal Scaling: Increase number of instances (= scale out / in) 
• Auto Scaling Group 
• Load Balancer 
- High Availability: Run instances for the same application across multi AZ 
• Auto Scaling Group multi AZ 
• Load Balancer multi AZ

## What's that Elastic Load Balancer [ELB] ?
 ELB (Elastic Load Balancer) is a managed load balancer 
 - AWS guarantees that it will be working 
 - AWS takes care of upgrades, maintenance, high availability 
 - AWS provides only a few configuration knobs 
- It costs less to setup your own load balancer but it will be a lot more effort on your end (maintenance, integrations) •
- 4 kinds of load balancers offered by AWS: 
 - Application Load Balancer (HTTP / HTTPS only) –Layer 7 
 - Network Load Balancer (ultra-high performance, allows for TCP) –Layer 4 
 - Gateway Load Balancer –Layer 3 
 - Classic Load Balancer (retired in 2023) –Layer 4 & 7

## What's that Auto Scaling Groups [ASG] ?
- In real-life, the load on your websites and application can change 
- In the cloud, you can create and get rid of servers very quickly 
- The goal of an Auto Scaling Group (ASG) is to: 
 - Scale out (add EC2 instances) to match an increased load 
 - Scale in (remove EC2 instances) to match a decreased load 
 - Ensure we have a minimum and a maximum number of machines running 
 - Automatically register new instances to a load balancer 
 - Replace unhealthy instances 
 - Cost Savings: only run at an optimal capacity (principle of the cloud)
