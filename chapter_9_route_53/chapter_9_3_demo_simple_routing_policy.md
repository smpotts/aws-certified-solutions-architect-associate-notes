# Demo: Using a Simple Routing Policy

Simple Routing Policy
- can only have one record with multiple IP addresses
- if you specify multiple values in a record, Route 53 returns all values to a user in a random order

Demo
- Route 53
- Hosted zones
- create record -> quick create
- choose an A record and naked domain name
- choose simple routing policy
- 1m TTL so when you make DNS changes it only take 60 seconds
- open EC2 -> grab IP addresses for N. VA and Tokyo
- copy public IP addresses and paste as Value for Route 53 record
- no alias
- create record to create an A record, sending traffic to two different IP addresses
- test by going to domain name in Incognito mode

Exam Tips
- remember what simple routing policy is and how it works
- can only have one record with multiple IP addresses
- returns all values to a user in a random order

