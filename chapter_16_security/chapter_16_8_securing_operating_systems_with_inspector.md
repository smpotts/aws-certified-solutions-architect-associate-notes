# Chapter 16.8 Securing Operating Systems with Inspector

What is Amazon Inspector
- automated security assessment service
- improves security and compliance of apps in AWS
- assesses apps for vulnerabilities and deviations of best practices

Assessment Findings
- Inspector produces a list of findings, prioritized by level of severity
- can be reviewed on the console or API

Assessment Types 
1. network : looks at network configuration analysis, checks ports reachable outside VPC, agent not required
2. host assessments : vulnerable sortware, host hardening and security best practices, agent required
	- install inspector agent host

How Does it Work?
- create assessment target
- install agents on EC2 instances
- create an assessment template
- perform assessment run
- review findings against the rules

Exam Tips
- Inspector is used to perform vulnerability scans on EC2 instances and VPCs
- host assessments and network assessments
- can run assessment once or weekly