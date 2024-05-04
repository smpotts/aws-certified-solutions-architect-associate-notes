# Chapter 16.21 Security Exam Tips

DDoS
- distributed denial of service attack
- attempts to make website unavailable
- layer 4 attacks like SYN or NTP amplification
- layer 7 floors or get/post reqs

CloudTrail
- after the fact incident investigation
- intrusion detection
- regulatory compliance
- CCTV for your account
- logs all API calls made to your AWS account

Shield
- protects aginast layer 3 and 4 attacks ONLY
- used to protect against DDoS attacks
- free
- Advanced is $3,000 per month but you get 24/7 response team

WAF
- allow all reqs/block all/... except specified ones
- operates at layer 7 application layer
- block access to IP addresses or countries

AWS Firewall Manager
- multiple resources/ accounts that need to be secured centrally

GuardDuty
- uses AI to learn what normal behavior is to alert you on abnormal behavior
- monitors logs
- findings appear in a GuardDuty dashboard

Macie
- uses AI to analyze data in S3 and find PII
- HIPAA and GDPR
- can setup alerts with Macie
- can automate remediation actions using other services

Inspector
- vulnerability scans on VPCs and EC2 instances

KMS and CloudHSM
- KMS : create and control encryption keys
	- start by requesting a customer master key (CMK)
	- key policy, IAM with key policy, or grants with key policy
- KMS : using shared tenancy of underlying hardware, automatic key rotation
- CloudHSM : dedicated physical hardware device, full control of hardware and users groups / keys, no key rotation

Secrets Manager
- store database creds, API keys, SSH keys, passwords
- rotating is easy
- make sure all your apps are configured to use it (especially before enabling rotation)

Parameter Store vs Secrets Manager
- minimize costs = parameter store
- more than 10k params, key rotation or password gen = Secrets Manager

Presigned URLs
- where you need to share private files in your S3 bucket

Advanced IAM Policies
- implicitly denied
- explicit deny > everything else
- only attached policies have an effect
- can have multiple policies attached
- customer and AWS managed policies

Certificate Manager
- SSL certificate manager
- supported services are API Gateway, ELB CloudFront
- free
- autorenew certs

Audit Manager
- continuous auditing HIPAA or GDPR
- automating auditing reports

Artifact
- audits and compliance reports
- usually a distractor

Cognito
- user pool : user directories that provide sign in and sign up options
- identity pool : allows your uses to access AWS services
- process: devices connects to user pool gets tokens, exchanges tokens with identity pool and gets access to AWS credentials

Detective
- operates across multiple services and analyzes root cause of an events
- usually a distractor

Network Firewall
- filtering network traffic before it reaches internet gateway
- hardware firewall reqs
- AWS manage hardware

Security Hub
- single place to view security alerts across accounts and services
