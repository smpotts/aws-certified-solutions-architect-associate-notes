# Controlling Subnet Traffic with Network ACLs

What are Network ACLs?
- first line of defense
- optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of subnets
- might set them up to add another layer of security
- like a 

Traffic goes:
Internet gateway -> Router -> Route table -> Network ACL
- first line of defense

Network ACL Overview
- comes with default network ACL that allows all inbound and outbound traffic by default
- custom network ACLs deny everything by default
- each subnet needs to be associated with network ACL
	- otherwise associated with the default
- can block IP addresses with network ACLs, not security groups

Network ACL Tips
- can associate with multiple subnets but one subnet can only be associated with one network ACL
- numbered list of rules
- have separate inbound or outbound rules that can allow or deny traffic
- stateless: have to go in and allow rules for both inbound and outbound traffic

Demo
- create Network ACL
- create in our VPC
- denied everything by default
- update subnet association
- ACL rules should be named in increments of 100
- have to add inbound and outbound rules
- ephemeral ports? **READ MORE ABOUT THIS
	- for things to connect to the VPC
- conflicting rules: rules evaluated based on their number with smallest ones overuling 
- blocking specific IP addresses: the rule number has to be smaller than to apply before the allow permissions

Exam Tips
- default network ACLs: by default allows all outbound and inbound traffic
- custom ones deny everything by default
- subnet associations, must have a network ACL, if not then uses the default
- block IP addresses with network ACLs
- multiple subnet using a network ACL, each subnet can only have one network ACL
- network ACLs contain a numbered list of rules, evaluated starting with the lowest number
- have separate inbound and outbound rules
- stateless: inbound rules subject to outbound rules vice versa
