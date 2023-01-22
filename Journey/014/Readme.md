
# Database Part 2 - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## DynamoDB
- DynamoDB is a highly available and fully managed database with replication across three availability zones
- It's not relational database 
- DynamoDB is one of AWS' flagship products
- Scaling very large workloads and distributed serverless databases
- DynamoDB is great because it scales to millions of requests per second, trillions of rows and 100TB of storage
- Has fast and consistent performance
- It integrates with IAM for security, authorization, and administration
- Low latency,low cost and auto scaling capabilities 

## DynamoDB Accelerator - DAX
- So it's a fully managed in-memory cache for DynamoDB
- 10x performance improvement 
- Secure, highly scalable and highly available 

## DynamoDB - Global Tables 
- Make a DynamoDB table accessible with low latencyin multiple-region
- Active replication (read/write to any AWS Region) 

## Redshift - Overview
- Redshift is a database based on PostgreSQL. But not used for OLTP. OLTP stands for Online Transaction Processing
- Redshift is OLAP namely Online Analytical Processing, which is used for analytics and data storage.
- load data every hour, not every second.
- 10x better performance than other data warehouses, and scales to PBs of data
- Data is stored in columns. So this is called columnar data storage
- Has something called Parallel Query Execution [MPP], highly avalable
- pay according to usage, based on the instance you have provided
- Has SQL interface to perform queries
- BI tools such as AWS Quicksight or Tableau intergate with it

## EMR - Overview 
- EMR stands for Elastic MapReduce
- This EMR is for creating so-called Hadoop clusters when you want to do big data on AWS
- Hadoop clusters are used to analyze and process large amounts of data
- Hadoop is an open-source technology, and they allow multiple servers working in a cluster to analyze data together
- Can create clusters made up of hundreds of EC2 instances that will collaborate together to analyze data.
- Also supports Apache Spark,HBase,Presto,Flink..
- EMR takes care of provisioning all these EC2 instances and configuring them so they can work together and analyze data together from a big data perspective
- Has auto-scaling with Spot instances
- Use cases : data processing, machine learning, we indexing, big data

## Amazon Athena 
- Amazon Athena is a serverless query service for performing analytics on S3 objects
- Uses standard SQL language to query the files 
- Uses standard SQL language to query the files 
- Supports CSV, JSON, ORC, Avro, and Parquet (built on Presto) 
- Pricing: $5.00 per TB of data scanned 
- Use compressed or columnar data for cost-savings (less scan)
- Use cases: Business intelligence / analytics / reporting, analyze & query VPC Flow Logs, ELB Logs, CloudTrail trails, etc

## Amazon QuickSight 
- Serverless machine learning-powered business intelligence service to create interactive dashboards 
- Fast, automatically scalable, embeddable, with per-session pricing 
- Use cases: 
- Business analytics 
- Building visualizations 
- Perform ad-hoc analysis 
- Get business insights using data 
- Integrated with RDS, Aurora, Athena, Redshift, S3

## DocumentDB  
- Aurora is an “AWS-implementation” of PostgreSQL / MySQL
- DocumentDB is the same for MongoDB (which is a NoSQL database)
- MongoDB is used to store, query, and index JSON data
- Similar “deployment concepts” as Aurora
- Fully Managed, highly available with replication across 3 AZ
- DocumentDB storage automatically grows in increments of 10GB, up to 64 TB
- Automatically scales to workloads with millions of requests per seconds

## Amazon Neptune 
- Fully managed graph database 
- A popular graph dataset would be a social network 
 1. Users have friends 
 2. Pots have comments 
 3. Comments have like from users 
 4. User shared and like posts 
- Highly available aros 3 AZ, with up to 15 read replicas 
- Build and run applications working with highly connected datasets – optimized for these complex and hard queries
- Can store up to billions of relations and query the graph with milliseconds latency
- Highly available with replications across multiple AZs
- Great for knowledge graphs (Wikipedia), fraud detection,recommendation engines, social networking

## QLDB 
- A ledger is a book recording financial transactions
- Fully Managed, Serverless, High available, Replication across 3 AZ
- Used to review history of all the changes made to your application data over time
- Immutable system,no entry can be removed or modified, cryptographically verifiable
- 2-3x better performance than common ledger blockchain frameworks, manipulate data using SQL
- Difference with Amazon Managed Blockchain: no decentralization component, in accordance with financial regulation rules

## Amazon Managed Blockchain
- Blockchain makes it possible to build applications where multiple parties can execute transactions without the need for a trusted, central authority.
- Amazon Managed Blockchain is a managed service to:
- Join public blockchain networks
- Or create your own scalable private network
- Compatible with the frameworks Hyperledger Fabric & Ethereum

## AWS Glue 
- Managed extract, transform, and load (ETL) service
- Useful to prepare and transform data for analytics
- Fully serverless service
- Glue Data Catalog: catalog of datasets
- Can be used by Athena, Redshift, EMR

## DMS [ Database Migration Service ]
- Quickly and securely migrate databases to AWS, resilient, self healing
- The source database remains available during the migration
Supports:
- Homogeneous migrations: ex Oracle to Oracle
- Heterogeneous migrations: ex Microsoft SQL Server to Aurora

## Social Proof

[Twitter](https://twitter.com/silvyameliaa_/status/1616965331234492417)
