# Savings Plan and AWS Compute Optimizer - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## Savings Plan 
- Commit a certain $ amount per hour for 1 or 3 years
- Easiest way to setup long-term commitments on AWS
- EC2 Savings Plan
	- Up to 72% discount compared to On-Demand
	- Commit to usage of individual instance families in a region (e.g. C5 or M5)
	- Regardless of AZ, size (m5.xl to m5.4xl), OS (Linux/Windows) or tenancy
	- All upfront, partial upfront, no upfront
- Compute Savings Plan
	- Up to 66% discount compared to On-Demand
	- Regardless of Family, Region, size, OS, tenancy, compute options
	- Compute Options: EC2, Fargate, Lambda
- Machine Learning Savings Plan: SageMaker
- Setup from the AWS Cost Explorer console

## AWS Compute Optimizer
- Reduce costs and improve performance by recommending optimal AWS resources for your workloads
- Helps you choose optimal configurations and right - size your workloads (over/under provisioned)
- Uses Machine Learning to analyze your resources configurations and their utilization CloudWatch metrics
- Supported resources
	- EC2 instances
	- EC2 Auto Scaling Groups
	- EBS volumes
	- Lambda functions
- Lower your costs by up to 25%
- Recommendations can be exported to S3
