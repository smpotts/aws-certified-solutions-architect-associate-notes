# Optimizing with EC2 Placement Groups

3 Types of placement groups
- clustered
- spread
- partitioned 

Clustered
- grouping of instances within a single availability zone
- low network latency
- high network throughput
- speeding up the rate they communicate

Spread
- instances on distinct underlying hardware
- recommended when you have critical instances that should be separate
- used for individual instances

Partition
- every partition placement group has it's own set of racks
- isolate impact of hardware failure
- partition: a rack, grouping of ec2 instances into dedicated network and power sources

Exam Tips
- cluster plavement: low latency, high thruput
- spread: critical instances on own hardware
- partition: on their own dedicated racks
- clustered placement group in one AZ
- only certain types of instances can be in placement group
- recommends same type of instance within clustered placement group
- can't merge placement groups
- can move existing instance into a placement group if you stop it first from the command line
