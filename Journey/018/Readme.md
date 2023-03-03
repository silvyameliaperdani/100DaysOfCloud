# Deploying and Managing Infrastructure Part 2 - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## AWS CodeDeploy 
Hybrid service to deploy applications automatically and upgrade it from version 1 to version 2, working with EC2 instances and on-promises servers. must provide a server that has CodeDeploy installed first.
## AWS CodeCommit 
Developers pushing code for applications in repositories with Git technology for example GitHub , but on AWS there is also the same product is CodeCommit. CodeCommit Makes it easy to collaborate with others on code and code changes are automatically versioned.
Benefits :
- Fully managed
- Scalable & highly available
- Private, Secured, Integrated with AWS
## AWS CodeBuild 
- Code building service in the cloud
- compiles source code, run tests, and produces packages that are ready to be deployed 
Benefits :
- Fully managed, serverless
- Continuously scalable & highly available
- Secure
- Pay-as-you-go pricing – only pay for the build time
## AWS CodePipeline 
- Service for orchestrate the different steps to have the code automatically pushed to production
	- Code -> Build -> Test -> Provision -> Deploy 
	- Basis for CICD (Continuuuous Integration & Continuous Delivery)
Benefits :
- Fully managed, compatible with CodeCommit, CodeBuild, CodeDeploy, Elastic Beanstalk, CloudFormation, GitHub, 3rd-party services (GitHub…) & custom plugins…
- Fast delivery & rapid updates
## AWS CodeArtifact 
- Software packages depend on each other to be built (also called dependency code), and new ones are created
- Traditionally you need to set up your own artifact management system, now you can use CodeArtifact for secure, scalable and cost-effective artifact management for software development.
## AWS CodeStar
Manage software development activities easily in one place, here you can start setting up CodeCommit, CodePipeline, CodeBuild, CodeDeploy, Elastic Beanstalk, EC2, etc…
## AWS Cloud9
- AWS Cloud9 is a cloud IDE (Integrated Development Environment) for writing, running, and debugging code
- such as Intellij, Visual Studio Code etc. is a classic IDE, downloaded on the computer and installed before use
- but if it's Cloud IDE you can use it in browser. You can work on projects from the office, from home or from anywhere with internet access without the need for any setup
- AWS Cloud9 also enables code collaboration in real-time (pair programming)

## AWS SSM
- SSM can be called AWS System Manager
- Another Hybrid AWS service  
- Service for Help you manage your EC2 and On-Premises systems at scale
- Get operational insights about the state of your infrastructure
How Systems Manager Works?
- We need to install the SSM agent onto the systems we control
- Installed by default on Amazon Linux AMI & some Ubuntu AMI
- If an instance can’t be controlled with SSM, it’s probably an issue with the SSM agent!
- Thanks to the SSM agent, we can run commands, patch & configure our servers
## AWS OpsWorks 
- Chef & Puppet help you perform server configuration automatically, or repetitive actions
- They work great with EC2 & On-Premises VM
- AWS OpsWorks = Managed Chef & Puppet
- It’s an alternative to AWS SSM
- Only provision standard AWS resources like EC2 Instances, Databases, Load Balancers, EBS volumes…

## Summary 
- CloudFormation : Infrastructure as Code, work with almost all of AWS resoures
- Beanstalk : Pratform as a Service (PaaS), limited to certain progamming languages or Docker 
- Code Deploy : Deploy & upgrade any application servers 
- CodeCommit: Store code in private git repository (version controlled)
- CodeBuild: Build & test code in AWS
- CodeDeploy: Deploy code onto servers
- CodePipeline: Orchestration of pipeline (from code to build to deploy)
- CodeArtifact: Store software packages / dependencies on AWS
- CodeStar: Unified view for allowing developers to do CICD and code
- Cloud9: Cloud IDE (Integrated Development Environment) with collab
- AWS CDK: Define your cloud infrastructure using a programming language 

## Social Proof

[Twitter](https://twitter.com/silvyameliaa_/status/1631497751556141058)
