
# Other Compute Services - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## Docker
- Docker is a software development platform for deploying applications
- With docker, you will package your application into something called container which can run on any OS
example: EC2 instance which runs docker javascript, docker Mysql, etc.
- Applications once in waddah will run in the same way
- Can scale containers very quickly and unload in seconds

## Docker VS Virtual Machines 
![image](https://user-images.githubusercontent.com/121029600/213897660-669b8924-5b56-4ba0-b435-a84eedcb5e4a.png)

## ECS 
- ECS stands for Elastic Container Service
- Launch Docker containers on AWS
- Must provision & maintain the infrastructure (the EC2 instances)
- AWS takes care of starting / stopping containers
- And has integrations with the Application Load Balance

## Fargate
- Launch Docker containers on AWS, no infrastructure required so it's simpler
- Serverless offering and runs AWS based on CPU/RAM required.

## ECR 
- ECR stands for Elastic Container Registry
- ECR is a private Docker Registry on AWS
- Here you can store docker images and run them on ECS or Fargate

## Serveless
Serverless is a new paradigm in which developers no longer manage servers, initially serverless is FaaS (Function as a Service) pioneered by AWS Lambda.
example : S3,DynamoDB,Lambda,Fargate

## Social Proof

[Twitter](https://twitter.com/silvyameliaa_/status/1616984442207375365)
