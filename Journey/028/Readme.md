
# Security And Compliance Part 2 - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## AWS KMS 
Encryption service in AWS is KMS (Key Management Service),KMS manages encryption keys for us

## CloudHSM
is a service that provides encryption hardware and you can manage your own encryption keys completely and tamper resistant.

## Types of Customer Master Keys : CMK 
- Customer Managed CMK: Create, manage and use by customers, can enable or disable, possibility of rotation policy, possibility to bring-your-own-key 
- AWS managed CMK: Created, managed and used on the customer’s behalf by AWS and used by AWS services (aws/s3, aws/ebs, aws/redshift)
- AWS owned CMK: Collection of CMKs that an AWS service owns and manages to use in multiple accounts and used to protect the resources in your account.
- CloudHSM key (custom keystore): Keys are generated from your own CloudHSM hardware and cryptographic operations are performed within the CloudHSM cluster

## AWS Certificate Manager (ACM)
- Service used to easily provision, manage, and deploy SSL/TLS Certificates.
- Provides in-flight encryption for websites (HTTPS)
- Support public and private TLS certificates, free for public TLS certificates
- Automatic TLS certificate renewal

## AWS Secrets Manager
New service used to store secrets and can force the secret to be created with a lambda every X days. integrated with amazon RDS and secrets are encrypted with KMS

## AWS Artifact 
Portal that provides customers with on-demand access to AWS compliance documentation and AWS agreements

## Amazon GuardDuty
- Helps perform intelligent threat discovery to protect your AWS account
- Uses Machine Learning algorithms, anomaly detection, 3rd party data
- One click to enable (30 days trial), no need to install software
- Can protect against CryptoCurrency attacks (has a dedicated “finding” for it)
- Can setup CloudWatch Event rules to be notified in case of findings,can target AWS Lambda or SNS

## Social Proof

[Twitter](https://twitter.com/silvyameliaa_/status/1633335217456041984)
