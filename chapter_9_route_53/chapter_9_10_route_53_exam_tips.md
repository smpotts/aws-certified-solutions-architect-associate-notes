# Route 53 Exam Tips

Route 53 Exam Tips
- understand alias record vs c name
- always choose an alias record over a c name in a scenario based question
- alias record unique to aws : translates naked domain name to a resource
- c name only allows you to translate subdomain name from one to another

Common DNS records
- SOA records
- C NAME
- NS record
- A record : turn web address into IP address

Routing Policies
- simple routing
- weighted
- failover
- geolocation
- latency based routing
- geoproximity
- multivalue 

Registering domain names
- can do it on AWS
- can take 3 days

Health Checks
- can set on individual record sets
- if it fails, removed until it passes health checks

Routing Policies
- simple routing policy: one record with multiple IP addresses, returns all values in a random order
- weighted routing policies: send a certain percentage of traffic to resources
- latency: sends traffic to resources where they will have the lowest latency
- failover: active and passive setup in case there is a failure
- geolocation: send users to resource based on their location
- geoproximity: sends users to a resource based based on resources, can give a bias to expand or shrink the size of the region, must use Route 53 traffic flow for this
- multivalue answer routing: health checks on each record basically
