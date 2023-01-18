
# Amazon S3 Part 2 - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## Amazon S3 - Static Website Hosting 
- S3 can host static websites and have them accessible on the internet
- The website URL will be (depending on the region)
- If you get a 403 Forbidden error, make sure the bucket policy allows public reads

## Amazon S3 - Versioning 
- You can Version your files in Amazon S3 
- It is enabled at the bucket level 
- Best practice to version your buckets
- Suspending versioning does not delete the previous versions 

## Amazon S3 - Replication [ CRR & SRR ]
- Must enable Versioning in source and destination buckets
 - Cross-Region Replication [CRR]
 - Same-Region Replication [SRR]
- Bucket can be in different AWS Account 
- Must give proper IAM permissions to S3 
- Copying is asynchronous 
- Use cases : 
 - CRR – compliance, lower latency access, replication across accounts
 - SRR – log aggregation, live replication between production and test accounts

## S3 Storage Classes
- Amazon S3 Standard - General Purpose
- Amazon S3 Standard-Infrequent Access (IA)
- Amazon S3 One Zone-Infrequent Access
- Amazon S3 Glacier Instant Retrieval
- Amazon S3 Glacier Flexible Retrieval
- Amazon S3 Glacier Deep Archive
- Amazon S3 Intelligent Tiering

## S3 Encryption
- Server-Side Encryption [Default]
- Client-Side Encryption 

## Shared Responsibility Model for S3 
- AWS 
 - Infrastructure (global security,durability,availability,sustain concurrent loss of data in two facilities)
 - Configuration and vulnerability analysis
 - Compliance Validation 
- USER AMAZON S3 
 - S3 Versioning 
 - S3 Buket Policies 
 - S3 Replication Setup 
 - Logging and Monitoring 
 - S3 Storage Classes
 - Data enryption at rest and in transit. 

## AWS Snow Family 
- Highly-secure, portable devices to collect and process data at the edge, and migrate data into and out of AWS
- Data migration : Snowcone,Snowball Edge,Snowmobile
- Edge computing : Snowcone,Snowball Edge

## Hybrid Cloud for Storage 
Hybrid Cloud for Storage
- AWS is pushing for ”hybrid cloud”,part of your infrastructure are on-premises and on the cloud
- This can be due to long cloud migration, security requirements, compliance requirements, IT strategy

## AWS Storage Gateway 
- Bridge between on-premise data and cloud data in S3
- Hybrid storage service to allow on-premises to seamlessly use the AWS Cloud
- Use cases: disaster recovery, backup & restore, tiered storage
- Types of Storage Gateways (File Gateways,Gateway Volumes,Tape Gateways)

## Social Proof


[Twitter](https://twitter.com/silvyameliaa_/status/1615504069522780162)
