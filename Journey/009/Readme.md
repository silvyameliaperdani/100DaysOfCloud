
# EC2 Image Builder, EC2 Instance Storage, EFS - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek


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

## EC2 Instance Storage - Summary 
- EBS Volume : 
 - Network drives attached to one EC2 Instance at a time 
 - Mapped to an Availability Zones 
 - Can use EBS Snapshots for backups / transferring EBS Volume across AZ 
- AMI: create ready-to-use EC2 instances with our customizations 
- EC2 Image Builder: automatically build, test and distribute AMIs 
- EC2 Instance Store: 
 - High performance hardware disk attached to our EC2 instance 
 - Lost if our instance is stopped / terminated 
- EFS: network file system, can be attached to 100s of instances in a region 
- EFS-IA: cost-optimized storage class for infrequent accessed files 
- FSx for Windows:Network File System for Windows servers 
- FSx for Lustre:High Performance Computing Linux file system 

 ## Social Proof


[Twitter](https://twitter.com/silvyameliaa_/status/1614775246288195584)
