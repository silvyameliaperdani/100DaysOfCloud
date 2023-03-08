# Cloud Monitoring Part 2 - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## Amazon EventBridge
- Schedule; Cron jobs (scheduled scripts)
- Event Pattern; Event rules to react to a service doing something
- Trigger Lambda functions, send SQS/SNS messages
- Schema Registry: model event schema
- You can archive events (all/filter) sent to an event bus (indefinitely or set period)
- Ability to replay archived events


## CloudTrail
- Provides governance, compliance and audit for your AWS Account
- CloudTrail is enabled by default!
- Get an history of events / API calls made within your AWS Account by: Console, SDK, CLI, AWS Services
- Can put logs from CloudTrail into CloudWatch Logs or S3
- A trail can be applied to All Regions (default) or a single Region
- For example : If a resource is deleted in AWS, investigate loudTrail first
  
## AWS X-Ray
We do debugging in production but there is no general view of the whole architecture for that X-ray is a visual analysis of our application
Advantages ;
- Troubleshooting performance (bottlenecks)
- Understand dependencies in a microservice architecture
- Pinpoint service issues
- Review request behavior
- Find errors and exceptions
- Are we meeting time SLA?
- Where I am throttled?
- Identify users that are impacted

## Amazon CodeGuru
- An ML-powered service for automated code reviews and application performance recommendations
- Provides two functionalities
	- CodeGuru Reviewer: automated code reviews for static code analysis (development)
	- CodeGuru Profiler: visibility/recommendations about application performance during runtime (production)
# Amazon CodeGuru Reviewer
- Identify critical issues, security vulnerabilities, and hard-to-find bugs
- For Example : common coding best practices,resource leaks, security detection, input validation
- Uses Machine Learning and automated reasoning
- Supports Java and Python
- Integrates with GitHub, Bitbucket, and AWS CodeCommit

# Amazon CodeGuru Profiler
- Helps understand the runtime behavior of your application
- Features:
	- Identify and remove code inefficiencies
	- Improve application performance (e.g., reduce CPU utilization)
	- Decrease compute costs
	- Provides heap summary (identify which objects using up memory)
	- Anomaly Detection
Example: identify if your application is consuming excessive CPU capacity on a logging routine
- Support applications running on AWS or on- premise
- Minimal overhead on application

## AWS Health Dashboard
- Shows all regions, all services health
- Shows historical information for each day
- Has an RSS feed you can subscribe to
- Previously Called AWS Service Health Dashboard

## Summary 
- CloudWatch:
	- Metrics: monitor the performance of AWS services and billing metrics
	- Alarms: automate notification, perform EC2 action, notify to SNS based on metric
	- Logs: collect log files from EC2 instances, servers, Lambda functions
	- Events (or EventBridge): react to events in AWS, or trigger a rule on a schedule
- CloudTrail: audit API calls made within your AWS account
- CloudTrail Insights: automated analysis of your CloudTrail Events
- X-Ray: trace requests made through your distributed applications
- Service Health Dashboard: status of all AWS services across all regions
- Personal Health Dashboard: AWS events that impact your infrastructure
- Amazon CodeGuru: automated code reviews and application performance recommendations

## Social Proof

[Twitter](https://twitter.com/silvyameliaa_/status/1633315148273430528)
