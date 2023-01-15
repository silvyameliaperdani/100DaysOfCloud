
# EC2 Instance Storage - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## EBS Overview 
In this lesson we will look at the different storage options for EC2 instances.

## What's an EBS Volume ?
- EBS Volume stands for Elastic Block Store. this is a network drive that can be attached to your instance when it starts up.
- So these EBS volumes allow us to retain data, even after the instances have been terminated, and that's our goal, to be able to recreate an instance and mount to the same EBS volume from before and be able to get our data back.
- so these EBS Volumes, at the CCP level can only be mounted to one machine at a time,
- and when creating an EBS Volume, it will be bound to a specific availability zone.
- Analogy : Think of them as a "Network USB stick"
- this feature gives us 30 GB of free EBS storage, General Purpose (SSD) or Magnetic type per month. and here we use this with GP2 to GP3 Volumes

## EBS Volume 
- so this EBS Volume is a network drive, not a physical drive.
- so to communicate between the instance and the EBS Volume, it will use the network.
- EBS volumes, because they are network drives, they can be detached from an EC2 instance and attached to another instance very quickly.
- EBS volumes are locked to a specific Availability Zone (AZ)
 • An EBS Volume in us-east-1a cannot be attached to us-east-1b 
 • To move a volume across, you first need to snapshot it
• Have a provisioned capacity (size in GBs, and IOPS)  
• You get billed for all the provisioned capacity  
• You can increase the capacity of the drive over team
## EBS - Delete on Termination Attribute

- so it controls EBS Behavior when EC2 instances are terminated
- can control with AWS Console / AWS CLI
- Use case : Preserve root volume when instance is terminated

## EBS Snapshots 
- Can capture EBS volumes and create Snapshots, which are also called backups, whenever you want.
- There's no need to unmount the volume before backing up, but it's recommended just to make sure everything is clean on your EBS volume.
- Can restore them but we can also copy snapshots across availability zones or regions.
## EBS Snapshots Features 
1. EBS snapshot archive
2. Recycle Bin for EBS Snapshots

## AMI Overview 
- AMI = Amazon Machine Image 
- AMI represent EC2 instance customization
  - Add your own software, configurations, etc.,
  - Faster boot/configuration times as all your software comes pre-packaged
  - AMI are built for a Spesific Region
  - And you can use to launch EC2 Instance are :
  - A Public AMI : AWS Provided
  - Your own AMI : you make and maintain them yourself 
  - An AWS Marketplace AMI : an AMI someone else made 
