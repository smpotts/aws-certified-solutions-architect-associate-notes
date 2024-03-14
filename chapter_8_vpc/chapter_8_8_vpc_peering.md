# Building Solutions across VPCs with Peering

Multiple VPCs
- sometimes might have multiple VPCs and need to connect them

VPC Peering
- connect one VPC with another via a direct network route using private IP addresses
- instances behave as if they were on the same private network
- can peer VPCs across accounts as well as with other VPCs in the same account
- peering is always done in a star configuration
- can peer between regions

Transitive Peering
- basically can't let two "leaf nodes" talk through the center, they have to have a direct connection

Demo
- go to Peering Connections
- cannot have overlapping CIDR address ranges
- Actions -> Accept Request

Exam Tips
- allows you to connect 1 VPC with another via a direct network route using private IP addresses
- transitive peering not supported
- can do between regions
- not overlapping CIDR address ranges