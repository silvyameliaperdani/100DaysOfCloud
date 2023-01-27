
# Other Compute Services - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## AWS Lambda 
AWS Lambda is Virtual Function but no servers to manage, Limited by time, Run on-demand and Scaling is automated. Lambda is a very popular service from AWS

## Benefits of AWS Lambda 
- Easy Pricing [you will pay for requests and per compute time]
- Integrated with the entire suite of AWS services
- the function will be called by AWS when needed
- Fully integrated with many programming languages
- Get easy monitoring via CloudWatch
- Easy to get more resources per function
- If it increases RAM, it also increases CPU and network quality
AWS Lambda Language Support : Node.js (JavaScript), Python, Java, C#, Golang, Ruby

# Amazon API Gateway 
Fully managed service for developers to easily build, publish, maintain, monitor APIs and be serverless and scalable

## Batch 
- Fully managed batch processing at any scale
- Efficiently run 100,000s of computing batch jobs on AWS
- A “batch” job is a job with a start and an end (opposed to continuous)
- Batch will dynamically launch EC2 instances or Spot Instances
- AWS Batch provisions the right amount of compute / memory
- You submit or schedule batch jobs and AWS Batch does the rest!
- Batch jobs are defined as Docker images and run on ECS
- Helpful for cost optimizations and focusing less on the infrastructure

Batch vs Lambda 
Lambda :
- Time limit
- Limited runtimes
- Limited temporary disk space
- Serverless

Batch :
- No time limit
- Any runtime as long as it’s packaged as a Docker image
- Rely on EBS / instance store for disk space
- Relies on EC2 (can be managed by AWS)


## Amazon Lightsail 
Amazon Lightsail is a standalone service
 - used for virtual servers, storage, databases, and networking
 - low & predictable price
 - simpler than previously learned services like EC2, RDS, etc.
 - for people who have little cloud experience and don't want to learn the complexities of how services work
 -  Can manage notifications and monitor your Lightsail resources
Use case:
 - Simple web app (has templates for LAMP, Nginx, MEAN, Node.js…)
 - Website (template for WordPress, Magento, Plesk, Joomla)
 - Developer/Test Environment
 Has high availability but without auto-scaling, limited AWS integration

# Summary 
- Docker: container technology for running applications
- ECS: run a Docker container on an EC2 instance
- Fargates: Run Docker containers without infrastructure provisioning and serverless offerings (no EC2 instances)
- ECR: Private Docker Image Repository
- Batch: run batch jobs on AWS across managed EC2 instances
- Lightsail: predictable & low priced for simple apps & DB stacks
- Lambda Serverless, Works as a Service, seamless scaling, reactive
- Lambda Language Support: many programming languages except Docker (arbitrary).
- Lambda Prayer Time: up to 15 minutes
- Lambda Use Cases:
- Create Thumbnails for images uploaded to S3
- Run a Serverless cron job
- API Gateway: exposes Lambda functions as HTTP APIs

## Social Proof

[Twitter](https://twitter.com/silvyameliaa_/status/1618775806456762368)
