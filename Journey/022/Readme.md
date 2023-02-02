# Cloud Integration - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Introduction
When we start deploying multiple applications, they inevitably need to communicate with each other

There are two patterns of application communication
-Synchronous communications (application to application)
-Asynchronous / Event based (application to queue to application)
If you are used to encoding 10 videos then suddenly need 1000 then Synchronous between apps can be problematic due to sudden spikes in traffic

In this case, it's best to separate your applications:
-use SQS: queuing model
-using SNS: pub/sub mode
-using Kinesis: real-time data streaming models
## Cloud Research
## SQS 
SQS stands for Simple Queue Service which is a liaison between producers and consumers which does not only consist of 1 producer/consumer but can be more.
Amazon SQS - Standart Queue
- Fully managed service (serverless), use to decouple applications
- No limit to how many messages can be in the queue and messages are deleted after they’re read by consumers
- Low latency
- Consumers share the work to read messages & scale horizontally
