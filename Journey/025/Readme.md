
# VPC And Networking Part 1 - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## VPC 
- VPC is Virtual Private Cloud,private network to deploy your resources (regional resource)
- Subnets allow you to partition your network inside your VPC (Availability Zone resource). there are 2 subnets that you should know :
	- Public subnet is a subnet that can be accessed from the internet
	- Private subnets are subnets that are not accessible from the internet
- To define access to the internet and between subnets, we use Route Tables

## Internet Gateway & NAT Gateways
- Internet Gateways helps our VPC instances connect with the internet
- Public Subnets have a route to the internet gateway.
- NAT Gateways (AWS-managed) & NAT Instances (self-managed) allow your instances in your Private Subnet to access the internet while remaining private

## Network ACL & Security Groups
- NACL (Network ACL)
	- A firewall which controls traffic from and to subnets
	- Can have ALLOW and DENY rules
	- Are attached at the Subnet level
	- Rules only include IP addresses
- Security Groups
	- A firewall that controls traffic to and from an ENI / an EC2 Instance
	- Can have only ALLOW rules
	- Rules include IP addresses and other security groups

## Social Proof

[Twitter](https://twitter.com/silvyameliaa_/status/1633315771169509376)
