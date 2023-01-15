
# 


## Cloud Research
## EC2 Image Builder
- This is used to automate virtual machine creation, maintain, validate and test AMIs.
- EC2 Image Builder can run on schedule

## EC2 Instance Store
 - EBS Volume has limited performance 
 - If you nee high-perfomance hardware disk use EC2 Instance Store
 - Better I/O Performance
 
## EFS - Elastic File System 
 it's the third type of storage that can be attached to an EC2 instance.
EFS is a managed network file system. and can be attached to 100s of EC2 instances. EFS only works with Linuz EC2 instances, and works across multiple availability zones. EFS is highly available, scalable, and quite expensive (3x gp2), pay per use, and no capacity planning

## EFS Infrequent Access [EFS-IA]
- Storage classes save money on files that are not accessed often.
- given up to 92% lower data storage costs compared to another class of spikes, called the EFS standard
- EFS automatically transfers your files to EFS-IA

## Shared Responsbility Model for EC2 Storage 
AWS 
 - Infrastucture 
 - Replication fo data for EBS Volume & EFS Drives
 - Replacing faulty hardware 
 - Ensuring their employees cannot access your data
COSTUMER 
 - Setting up backup / snpshot procedures
 - Setting up data encyption
 - Responsibility of any data on the drives 
 - Understanding the risk of using EC2 Instance Store 

## Amazon FSx - Overiew 
- Lunch 3rd party high-performance file systems on AWS 
- Fully managed service

 
