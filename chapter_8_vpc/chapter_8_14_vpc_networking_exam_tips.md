# VPC Networking Exam Tips

VPCs
- think of it as a logical data center in AWS
- internet gateways, route tables, network ACLs, subnets, security groups
- 1 subnet per AZ

NAT Gateways
- redundant inside AZ
- no need to patch
- not associated with any security groups
- automatically assigned public IP

EXAM TIP
- if you have resources in multiple AZs and they share NAT Gateway, if the AZ of the NAT Gateway goes down, they are going to lose internet access
	- create an AZ independent architecture, you need to create NAT Gateways in each AZ and configure routing to ensure resources use each NAT gateway in the same AZ
- AWS handles autoscaling for you

Security Groups
- stateful, if you send a request from your instance the response traffic is allowed to flow in regardless of inbound security group rules

Network ACLs
- get a default network ACL: allows all inbound and outbound traffic
- can create a custom network ACL: everything denied by default until you add rules
- subnet associations: each subnet must be associated with a network ACL otherwise associated with the default
- can block IP addresses with network ACLs
- can associate with multiple subnets but subnet only gets one network ACL
- contain a numbered list of rules evaluated in order starting with lowest number first
- have separate inbound and outbound rules
- stateless

Direct Connect
- connect your data center to AWS
- high throughput
- stable and reliable connection i.e. VPN dropping out
- does not provide an encrypted connection to your AWS account by default

VPC Endpoints
- connect AWS without leaving the AWS internet network
- interface and gateway endpoints
	- gateway endpoints only support S3 and DynamoDB

Peering
- allows you to connect VPCs using private IP addresses
- instances behave as if they were on the same private network
- always done in a star configuration
- cannot have transitive peering
- can peer between regions
- can peer across accounts
- peering would fail if IP addresses overlapped

PrivateLink
- peering VPCs to 10s 100s 1000s of VPCs
- does not require VPC peering, just a network load balancer and ENI

Transit Gateway
- use route tables to limit how VPCs talk to each other
- works with Direct Connect and VPN
- supports IP multicast
- simplifying network topology
- makes it so you don't have to have a ton of peering connections

Securing Network with VPN Hub
- a way of allowing customers to combine VPNs
- combining VPN at different offices in different regions
- simplifying network topology

AWS Wavelength
- mobile edge computing or 5G
