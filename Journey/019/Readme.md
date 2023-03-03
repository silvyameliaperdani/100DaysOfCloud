
# Global Infrastructure Part 1 - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## Global Application 
Global application are apps that are deployed across multiple geographies and deployed across multiple Regions or Edge Locations for lower latency. Functions for disaster recovery (DR). More secure because global distributed infrastructure is more difficult to attack
- Latency is the time it takes for a network packet to reach a server

Global AWS Infrastructure :
- Regions, For deploying applications and infrastructure
- Availability Zones, Made of multiple data centers
- Edge Locations (Points of Presence), for content delivery as close as possible to users

Global Application in AWS :
- Global DNS : Amazon 53
- Global Content Delivery Network (CDN): CloudFront
- S3 Transfer Acceleration
- AWS Global Accelerator

## Amazon S3
- Route 53 is a DNS (Domain Name System) managing service
- In AWS, the most common records are :
	- A
	- AAAA
	- CNAME 
	- Alias 
# Route S3 Routing Policies 
- Simple routing policy
- Weighted routing policy
- Latency routing policy
- Failover routing policy

## AWS CloudFront 
- Content Delivery Network (CDN)
- It improves read performance, content is cached at the edge
- Improves user experience and DDoS Protection
# CloudFront vs S3 Cross Region Replication
CloudFront:
- Global Edge network
- Files are cached for a TTL (maybe a day)
- Great for static content that must be available everywhere
S3 Cross Region Replication:
- Must be setup for each region you want replication to happen
- Files are updated in near real time
- Read only
- Great for dynamic content that needs to be available at low-latency in some regions
## S3 Transfer Acceleration 
Increase transfer speed by transferring file to an AWS edge location which will forward the data to the S3 bucket in the target region

## Social Proof

[Twitter](https://twitter.com/silvyameliaa_/status/1631499172099641352)
