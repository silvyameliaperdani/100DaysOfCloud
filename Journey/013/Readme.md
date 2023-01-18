
# Database Part 1 - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## Introduction Database 
when we store data on disk (EBS drives, EBS Volumes, EC2 instance store, Amazon S3) you have limitations. If you want to store data in a structured way you may want to store it in a database. You can build indexes and efficiently query/search data. You can define relationships between data sets. So today's databases are all optimized for a purpose and will come with different features, forms and constraints.

## Database Type
- Relational Database 
-  is a group of items in the data with a predetermined relationship.
   Generally these items are organized into a table consisting of columns and rows.
   Tables are used to store information about objects represented in the database.
- NoSQL Database 
NoSQL = non-SQL = non relational databases 
NoSQL databases are purpose built for spesific data models and have flexible schemas for building modern applications. 
So the benefit of using a NoSQL database is that you have a lot of flexibility, Scalability, high-performance.
NoSQL data example : JSON [ JavaScript Object Notation ]
 
## Database & Shared Responsibility on AWS 
Benefit of using a managed database :
- Quick Provisioning, High Availability, Vertical and Horizontal Scaling
- Automated Backup & Restore, Operations, Upgrades
- Operating System Patching is handled by AWS
- Monitoring, alerting

## RDS [Relational Database Service]
It's a managed DB service for DB use SQL as a Query Language. It allows you to create databases in the cloud that are managed by AWS 
These databases can be of various types such as:
- Postgres
- MySQL
- MariaDB
- Oracle
- Microsoft SQL Server
- Aurora (AWS Proprietary database)

## Advantage over using RDS vs Deploying DB on EC2 
- RDS is a managed service :
 ~ Automated provisioning, OS patching
 ~ Continuous backups and restore to specific timestamp (Point in Time Restore)
 ~ Monitoring dashboards
 ~ Read replicas for improved read performance
 ~ Multi AZ setup for DR (Disaster Recovery)
 ~ Maintenance windows for upgrades
 ~ Scaling capability (vertical and horizontal)
 ~ Storage backed by EBS (gp2 or io1)
- BUT can't SSH into your instances 

## Amazon Aurora 
- Aurora not open sourced
- And aurora supports two types of database technologies it supports PostgreSQL and MySQL.
- Aurora is AWS Cloud Optimized 
- Aurora storage automatically grows in increments of 10GB, up to 64TB
- Aurora costs more than RDS (20% more) - but is more efficient 
- Not in the free tier

## RDS Deployments : Read Replicas, Multi-AZ 
- Read Replicas, Scale the read workload of your DB, can create up to 5 Read Replicas, and data is only written to the main DB 
- Multi-AZ, failover will be availale in case of a outage in the AZ, data is only read/written to the main database, and can only have 1 other AZ as failover.
- Multi Region, create read replicas in multi-region, this is used for disaster recovery in case of region problem event

## Amazon ElastiCache 
- The same way you use RDS to get a managed relational database
- ElastiCache is to get managed Redis or Memcached
- Caches are in-memory databases with high performance, low latency
- Helps reduce load off databases for read intensive workloads


## Social Proof


[Twitter](https://twitter.com/silvyameliaa_/status/1615699784903561217)
