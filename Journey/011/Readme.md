
# Amazon S3 Part 1 - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## Amazon S3 Section 
Amazon S3 is one of the key building blocks of AWS. this is infinitely scalable storage. Many websites depend on Amazon S3, for example many websites use Amazon S3 as the backbone and many AWS services also use Amazon S3

## Amazon S3 Use Cases 
- Backup and Storage 
- Disaster Recovery 
- Archive 
- Hybrid Cloud Storage 
- Application Hosting 
- Media Hosting 
- Data Lakes & Big Data Analytics
- Software Delivery 
- Static Website
and others

## Amazon S3 - Buckets
- Buckets can be seen as top-level directories, and actually the files in an S3 bucket are called objects
- and these buckets, they are created in your account and they must have a globally unique name
- Buckets are defined at region level
- there is a naming convention for S3 buckets
 ~ No uppercase, No underscore 
 ~ 3-63 characters long 
 ~ Not an IP 
 ~ Must start with lowercase letter or number 
 ~ Must NOT start with the prefix xn--
 ~ Must NOT end with the suffix -s3alias

## Amazon S3 - Objects 
- Object [Files] have a Key
- The key is the Full path 
- The key is composed of prefix + object name 
- There's no concept of directories within buckets 
- Keys with very long names that contain slashes (/)

## Amazon S3 - Objects [cont.]
- Object values are the content of the body max size is 5TB [5000GB], if uploading more than 5GB, must use "multi-part upload"
- Metadata [list of text key - system or user metadata]
- Tags [Unicode key]
- Version ID [if versioning is enabled]

## Amazon S3 - Security 
- User-Based [IAM Policies]
- Resource-Based [Bucked Policies,Object Access Control List,Bucket Access Control List]
- Encryption  


## Social Proof
[https://twitter.com/silvyameliaa_/status/1614814728026738692?s=20&t=FKVmCUmoYShhPfaGRgn7wQ] (link)
