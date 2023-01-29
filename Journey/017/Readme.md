
# Deploying and Managing Infrastructure Part 1 - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
# CloudFormation
CloudFormation is a declarative way to describe AWS infrastructure, and other resources
for example you would say :
	- I want a security group
	- I want two EC2 instances using this security group
	- I want an S3 bucket
	- I want a load balancer (ELB) in front of these machines
Then CloudFormation builds them for you, in the right order, with the exact configurations you specify

## Benefits of AWS Cloudformation :
	- Infrastructure as code
	- Cost
	- Productivity
	- Take advantage of templates and  documentation
	- Support (almost) all AWS resources
 
## CDK 
CDK stands for AWS Cloud Development Kit
So this is how you define cloud infrastructure using familiar programming languages
	-  For example JavaScript, Python, Java, etc.
The code will be compiled by the CDK into a CloudFormation template that can be used in JSON or YAML format
Can deploy your application's infrastructure and runtime code together as they may share the same language
	- Great for Lambda Functions
	- Great for Docker containers in ECS / EKS 
example : CDK - CDK CLI - CloudFormation Trmplate - CloudFormation 

## Developer Problem on AWS
- Managing Infrastructure 
- Deploying Code 
- Configuring all the database,load balancers,etc
- Scaling Concerns
- Most web apps have the same architecture (ALB + ASG)
- All the developers want is for their code to run 
- Possibly, consistenly across different application an environment 

## Beanstalk 
Elastic Beanstalk is a developer-centric deployment view the application on AWS
beanstalk is a development centric view
has control over the configuration of all components
Beanstalk is PaaS (Platform as a Service)
Beanstalk is free but you pay for the underlying instances

## Elastic Beanstalk 
- Manages services like instance configuration, load balancing and auto scaling, etc.
- Just the application code is the responsibility of the developer 
- Support for many platfroms :
	- Go
	- Java SE
	- Java with Tomcat 
	- Node.js, etc
## Elastic Beanstalk - Health Monitoring 
- Health agent pushes metrics to CloudWatch
- Checks for apps health, Publiishes health events 

## Social Proof

[Twitter](https://twitter.com/silvyameliaa_/status/1619832111002980355)
