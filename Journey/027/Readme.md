# Security And Compliance Part 1 - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## AWS Shared Responsibility Model 
- AWS responsibility - Security of the Cloud
- Customer responsibility - Security in the Cloud
- Shared controls :
	- Patch Management
	- Configuration Management
	- Awareness & Training

## Shared Responsibility for RDS 
- AWS responsibility:
	- Manage the underlying EC2 instance, disable SSH access
	- Automated DB patching
	- Automated OS patching
	- Audit the underlying instance and disks & guarantee it functions
- Your responsibility:
	- Check the ports / IP / security group inbound rules in DB’s SG
	- In-database user creation and permissions
	- Creating a database with or without public access
	- Ensure parameter groups or DB is configured to only allow SSL connections
	- Database encryption setting

## Shared Responsibility for S3
- AWS responsibility:
	- Guarantee you get unlimited storage
	- Guarantee you get encryption
	- Ensure separation of the data between different customers
	- Ensure AWS employees can’t access your data
- Your responsibility:
	- Bucket configuration
	- Bucket policy / public setting
	- IAM user and roles
	- Enabling encryption

## DDOS 
DDOS stands for Distributed Denial-of-Service
The picture of how it works is like this, let's say there is an attack carried out by hackers by sending lots of requests to the server so that when an ordinary user wants to access the server they can't because the server is overwhelmed and can't be responsive, so this DDos attack is quite scary.

But AWS can protect you by:
- AWS Shield Standard: protects against DDOS attack for your website and applications, for all customers at no additional costs 
- AWS Shield Advanced: 24/7 premium DDoS protection 
- AWS WAF: Filter specific requests based on rules 
- CloudFront and Route 53: 
	- Availability protection using global edge network 
	- Combined with AWS Shield, provides attack mitigation at the edge

## AWS Shield
- AWS Shield Standard:
	- Free service that is activated for every AWS customer
	- Provides protection from attacks such as SYN/UDP Floods, Reflection attacks and other layer 3/layer 4 attacks
- AWS Shield Advanced:
	- Optional DDoS mitigation service ($3,000 per month per organization)
	- Protect against more sophisticated attack on Amazon EC2, Elastic Load Balancing (ELB), Amazon CloudFront, AWS Global Accelerator, and Route 53
	- 24/7 access to AWS DDoS response team (DRP)
	- Protect against higher fees during usage spikes due to DDoS

## AWS WAF - Web Application Firewall 
Protects your web application from common web exploits at layer 7 such as HTTP, so it can be used in application load balancers, API gateways and others

Define Web ACL ( Web Access Control List ) :
- Rules can include IP addresses, HTTP headers, HTTP body, or URI strings
- Protects from common attack - SQL injection and Cross-Site Scripting (XSS)
- Size constraints, geo-match (block countries)
- Rate-based rules (to count occurrences of events) – for DDoS protection

- At rest : data is stored or archived on the device (RDS,S3 Glacier Deep Archive, etc.
- In transit (moving): data being moved from one location to another
