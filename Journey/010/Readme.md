

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
