# Network Privacy with AWS PrivateLink

Opening Your Services in a VPC to another VPC
- opening VPC up to the internet or doing VPC peering to share services in VPC to another

Sharing Applications across VPCs
- opening VPC to internet
	- a lot more to manage
	- security considerations, everything in the public subnet is public
- using VPC peering
	- have to create and manage peering relationships
	- whole network is accessible

Using PrivateLink
- best way to expose a service VPC to other VPCs
- doesn't require VPC peering
- requires a Network Load Balancer on a service BPC and an ENI on the customer VPC
	- doing VPC peering at scale and not actually using a peering relationship

Exam Tips
- PrivateLink: peering VPCs to 10s, 100s, 1000s of VPCs
- doesn't require VPC peering, no route tables, NAT gateways, internet gateways
- requires a Network Load Balancer on the service VPC and an ENI on the customer VPC