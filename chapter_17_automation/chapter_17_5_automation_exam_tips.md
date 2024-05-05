# Chapter 17.5 Automation Exam Tips

CloudFormation
- parameters, mappings and resource section
- immutable, stateless architecture (it's the best)
- mapping and parameter store - never hardcode, use parameter store or put ids in the mapping section, do not hardcode in the resource section

Elastic Beanstalk
- one stop shop for simple solutions to build things in AWS
- simple and to bundle with deployments then prefer this over CloudFormation

Systems Manager
- Automation Documents : configuring inside EC2 instances
- Automation Documents, Parameter Store and Session Manager