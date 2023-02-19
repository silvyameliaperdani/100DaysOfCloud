# AWS Organizations, SCP and Control Tower - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## AWS Organization 
You can manage multiple AWS accounts. The primary account will be called the master account and all other accounts will be called child accounts, API is available to automate AWS account creation and Restrict acount privilages using Service Control Policies (SCP)
## Cost Benefits:
- Consolidated Billing across all accounts - single payment method
- Pricing benefits from aggregated usage (volume discount for EC2, S3, etc)
- Pooling of Reserved EC2 instances for optimal savings

## Service Control Policies (SCP)
This allows you to whitelist or blacklist IAM actions that are enforced at the OU or account level but do not apply to the master account. SCP has no effect on the master account. So SCP, we're going to look at an example soon. They can only be applied to user and account roles, including root.

## Consolidated Biling - AWS Organization 
- When enabled gives you combined usage,one bill for all accounts
- The management account can turn off Reserved Instances discount sharing for any account in the AWS Organization, including itself

## AWS Control Tower 
Easy way to set up and govern a secure and compliant multi-account AWS environment based on best practices
- Benefits:
	- Automate the setup of your environment in a few clicks
	- Automate ongoing policy management using guardrails
	- Detect policy violations and remediate them
	- Monitor compliance through an interactive dashboard
AWS Control Tower runs on top of AWS Organizations, It automatically sets up AWS Organizations to organize accounts and implement SCPs (Service Control Policies)


