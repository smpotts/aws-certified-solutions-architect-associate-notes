# Chapter 17.4 Systems Manager

What is Systems Manager?
- suite of tools designed to let you view, control and automate your architecture and on-prem resources
- free set of tools

Feature Overview
- automation documents: allow you to configure your instances or AWS resources (now called runbooks)
- run command : execute commands as root
- patch applications: manage your application versions
- parameter store: passwords, usernames
- requires an agent to be installed on EC2 instances or on prem architecture
- remotely connect and interact with your architecture

Console Demo
- need to have an EC2 instance with the Systems Manager host installed on it
- click on Fleet Manager
- instance needs role to communicate with the Systems Manager service
- can broswer the file system on the console
- instance actions -> start session -> you're on the command line of the server
- don't have to manage ssh anymore
- Parameter Store : place to store secret values
	- basically just KV storage
- SecureStrings are encrypted and used for passwords
- can dynamically look up the value

Exam Tips
- Session Manager
- Automation documents and parameter store
- supports on prem architecture
- Systems Manager agent needs to be installed on intances
- usually used for patching updating and configuring 
- unpaid sys admin
- free if inside AWS