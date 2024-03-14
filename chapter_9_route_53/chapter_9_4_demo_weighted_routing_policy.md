# Demo: Using a Weighted Routing Policy

Weighted Routing Policy
- allows you to split traffic based on different weights assigned

Health Checks
- can set on individual record sets : load balancers, records, ec2 instances
- if a record set fails a health check it will be removed until it passes
- can alert via SNS notifications

Demo
- Route 53 -> Hosted zones
- Domain name -> remove simple record set
- Create health check for each weighted route we create
- Monitor the endpoint, specify by IP address
- Create alarm? You can
- Create another one for Tokyo (other region)
- Create record sets
- Create an A record
- Weighted routing policy : adds weight and divides it by total
- Specify the health check
- Only put the IP address for the N. VA server

Exam Tips
- remember what a weighted routing policy is
- sending a certain percentage of traffic to specific regions -> weighted policies
- health checks : can be put on individual record sets
- if health check fails it will pause until it passes
- can use SNS notifications for health checks