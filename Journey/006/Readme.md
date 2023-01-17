
# EC2 Part 2 - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek


## Cloud Research
## Security Groups 
- security groups, will be the basis for implementing network security 
  on the AWS Cloud.
- they will control how traffic is allowed in and out of the EC2 instance
- security groups would be very easy, they only contain allow rules.
- security groups can have rules that refer well to IP addresses

## Security Groups Deeper Dive 
- security groups are "firewall" on EC2 instances
- they will arrange : 
 - Access to Ports 
 - Authorised IP Ranges - IPV4 and IPV6 
 - Control of inbound network 
 - Control of outbound network 

## Security Groups Good to Know 
- Can be attached to multiple instances
- Locked down to a region/VPC combination 
- Does live "outside" the EC2 
- It's good to maintain one separate security group for SSH access 
- If your application is not accessible (time out), then it's a seurity group issue 
- If your application gives a "connection refursed" error, then it's an application 
  error or it's not launched 
- By default, all inbound traffic is blocked 
- By default, all outbound traffic is authorised

## Classis Ports 
- 22 = SSH (Secure Shell) - log into a Linux instance 
- 21 = FTP (File Transfer Protocol) - upload file into a file share 
- 22 = SFTP (Secure File Transfer Potocol) - upload file using SSH  
- 80 = HTTP - access unsecured wesites 
- 443 = HTTPS - access secured websites 
- 3389 = RDP (Remote Desktop Protocol) - log into a Windows instances 

## EC2 On Demand 
- Pay for what you use :
 - Linux or Windows - biling per seond, after the first minute 
 - All other operating systems - biling per hour 
- Has the highest cost but no upfront payment 
- No long-term commitment 
- Recommended for short-term and up-interrupted workloads

## Shared Responsibility Model for EC2 
AWS
- Infrastructure (global network security)
- Isolation on physical hosts
- Replacing faulty hardware
- Compliance validation 
User 
- Security Groups rules 
- Operating-system patches and updates
- Software and utilities installed on the EC2 instance
- IAM Roles assigned to EC2 & IAM user access management 
- Data security on your instance

## EC2 Summary 
- EC2 Instace and they consist of AMI (OS) + Instance Size (CPU + RAM) + Storage + security groups + EC2 User Data 
- Security Groups, Firewall attached to the EC2 instance 
- EC2 User Data is the script we launch on the first startup of the instance that we use to set up our EC2 instance to be a web server
- ssh is how we start the terminal from our computer to our EC2 instances [port 22]
- Purhasing Options : On-Demand, Spot, Reserved (Standard + Convertible +Scheduled), Dedicated Host, Dedicated Instance

 ## Social Proof


[Twitter](https://twitter.com/silvyameliaa_/status/1614774110965624834)
