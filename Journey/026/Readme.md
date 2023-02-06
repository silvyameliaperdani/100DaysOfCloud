
# VPC And Networking Part 2 - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## VPC Flow Logs 
- Capture information about IP traffic going into your interfaces:
	- VPC Flow Logs
	- Subnet Flow Logs
	- Elastic Network Interface Flow Logs
- Helps to monitor & troubleshoot connectivity issues. Example:
	- Subnets to internet
	- Subnets to subnets
	- Internet to subnets
- Captures network information from AWS managed interfaces too: Elastic Load Balancers, ElastiCache, RDS, Aurora, etc
- VPC Flow logs data can go to S3 / CloudWatch Logs

## VCP Peering 
- VPC Peering is connecting two VPCs privately using a network from AWS and make them behave as if they were in the same network 
- Must not have overlapping CIDR (IP address ranges)
- Peering VPC connections are not transitive (must be established for each VPC that needs to communicate with one another)

## VPC Endpoints 
- Endpoints allow you to connect to AWS Services using a private network instead of the public wwwnetwork
- This gives you enhanced security and lower latency to access AWS services
- VPC Endpoint Gateway: S3 & DynamoDB
- VPC Endpoint Interface: the rest

## AWS PrivateLink (VPC Endpoint Services)
it is the most secure and scalable way to expose services to multiple VPCs even up to 1000's. PrivateLink lets you connect services running inside your VPC to other VPCs directly and privately. So no need for VPC peering, route tables, NAT or anything else. By requiring a load balancer for VPC services and ENI for VPC customers
  
## Site to Site VPN & Direct Connect
- Site to Site VPN
	- Connect an on-premises VPN to AWS
	- The connection is automatic encrypted
	- Goes over the public internet
- Direct Connect (DX)
	- Establish a physical connection between on-premises and AWS
	- The connection is private, secure and fast
	- Goes over a private network
	- Takes at least a month to establish

## AWS Client VPN 
- Connect from your computer using OpenVPN to your private network in AWS and on-premises
- Allow you to connect to your EC2 instances over a private IP (just as if you were in the private VPC network)
- Goes over public Internet

## Transit Gateway
- For having transitive peering between thousands of VPC and on-premises, hub-and-spoke (star) connection
- One single Gateway to provide this functionality
- Works with Direct Connect Gateway, VPN connections
