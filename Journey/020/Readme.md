
# Global Infrastructure Part 2 - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## AWS Global Acceleration 
Improve global application availability and performance using the AWS global network and leverage the AWS internal to network to optimize the route to your application [ 60% inprovement ]
## AWS Global Accelerator VS CloudFront 
- They both use the AWS global network and its edge locations around the world
- Both services integrate with AWS Shield for DDoS protection.
- CloudFront – Content Delivery Network
	- Improves performance for your cacheable content (such as images and videos)
	- Content is served at the edge
- Global Accelerator
	- No caching, proxying packets at the edge to applications running in one or more AWS Regions.
	- Improves performance for a wide range of applications over TCP or UDP
	- Good for HTTP use cases that require static IP addresses
	- Good for HTTP use cases that required deterministic, fast regional failover
## AWS Outposts 
AWS Outposts is a "server rack" that offers the same AWS infrastructure, services, APIs & tools to build your own applications on-premises as in the cloud and you are responsible for the physical security of Outposts Rack
Benefits :
- Low-latency access to on-premises systems
- Local data processing
- Data residency
- Easier migration from on-premises to the cloud
- Fully managed service
- Some service that work on Outposts :EC2, EBS, S3, EKS, ECS, RDS, EMR
## AWS WaveLength 
- WaveLength Zones are infrastructure deployments embedded within the telecommunications providers' datacenters at the edge of the 5G networks
- Ultra-low latency applications through 5G networks
- Traffic doesn't leave the Communication Service Provider's (CSP) network
- High-bandwidth and secure connection to the parent AWS Regionand no additional charges or service agreements
- Use cases: Smart Cities, ML-assisted diagnostics, Connected Vehicles, Interactive Live Video Streams,AR/VR, Real-time Gaming
## AWS Local Zones 
- Places AWS compute, storage, database,and other selected AWS services closer to end users to run latency-sensitive applications
Example :
- AWS Region: N. Virginia (us-east-1)
- AWS Local Zones: Boston, Chicago, Dallas,Houston, Miami, …
## Global Applications Architecture 
- Single region,single AZ -> high availibility [X],global latency [X]
- Single region,multi AZ -> high availibility [√],global latency [X]
- Multi region,active-passive -> Global Reads’ Latency [√], Global Writes’ Latency [X]
- Multi Region, Active-Active -> Global Reads’ Latency [√], Global Writes’ Latency [√]

## Social Proof

[Twitter](https://twitter.com/silvyameliaa_/status/1631500196881510401)
