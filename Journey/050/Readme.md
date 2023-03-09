# Amazon Pinpoint, Well Architected Framework (General Guiding Principles) & AWS Cloud Best Practices – Design Principles - Course AWS Certified Cloud Practitioner on Udemy by Stephane Maarek

## Cloud Research
## Amazon Pinpoint
- Scalable 2-way (outbound/inbound) marketing communications service
- Supports email, SMS, push, voice, and in-app messaging
- Ability to segment and personalize messages with the right content to customers
- Possibility to receive replies
- Scales to billions of messages per day
- Use cases: run campaigns by sending marketing, bulk, transactional SMS messages
- Versus Amazon SNS or Amazon SES :
	- In SNS & SES you managed each message's audience, content, and delivery schedule
	- In Amazon Pinpoint, you create message templates, delivery schedules, highly-targeted segments, and full campaigns

## Well Architected Framework (General Guiding Principles)
- Stop guessing your capacity needs
- Test systems at production scale
- Automate to make architectural experimentation easier
- Allow for evolutionary architectures (design based on changing requirements)
- Drive architectures using data
- Improve through game days, simulate applications for flash sale days

## AWS Cloud Best Practices – Design Principles
- Scalability: vertical & horizontal
- Disposable Resources: servers should be disposable & easily configured
- Automation: Serverless, Infrastructure as a Service, Auto Scaling
- Loose Coupling:
	- Monolith are applications that do more and more over time, become bigger
	- Break it down into smaller, loosely coupled components
	- A change or a failure in one component should not cascade to other components
- Services, not Servers:
	- Don’t use just EC2
	- Use managed services, databases, serverless, etc !
