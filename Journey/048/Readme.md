# AWS DataSync, AWS Application Discovery Service, and AWS MGN - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## AWS DataSync
- Move large amount of data from on-premises to AWS
- Can synchronize to: Amazon S3 (any storage classes – including Glacier), Amazon EFS, Amazon FSx for Windows
- Replication tasks can be scheduled hourly, daily, weekly
- The replication tasks are incremental after the first full load 

## AWS Application Discovery Service
- Plan migration projects by gathering information about on-premises data centers 
- Server utilization data and dependency mapping are important for migrations
- Agentless Discovery (AWS Agentless Discovery Connector) 
	- VM inventory, configuration, and performance history such as CPU, memory, and disk usage 
- Agent-based Discovery (AWS Application Discovery Agent) 
	- System configuration, system performance, running processes, and details of the network connections between systems
- Resulting data can be viewed within AWS Migration Hub

## AWS Application Migration Service ( MGN )
- The “AWS evolution” of CloudEndure Migration, replacing AWS Server Migration Service (SMS)
- Lift-and-shift (rehost) solution which simplify migratingapplications to AWS 
- Converts your physical, virtual, and cloud-based servers to run natively on AWS, Supports wide range of platforms, Operating Systems, and databases
- Minimal downtime, reduced costs
