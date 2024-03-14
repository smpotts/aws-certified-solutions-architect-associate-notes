# Route 53 Overview

Route 53 allows you to provide DNS for both public and private IP addresses

What is DNS?
- something computers use to convert human friendly domain names into IP addresses
- IP addresses come in two forms: IPv4 and IPv6

IPv4 vs IPv6
- IPV4 addresses are running out, 32 bits 
- IPV6 created to solve the depletion issue, 128 bits

Top level Domains
- google.com, acloud.guru
- last word in a domain name is the top level domain name,
- like .com, .gov, .uk, .edu
- controlled by IANA in a root zone database which is a database of all top level domains

Domain Registrars
- an authority that can assign domain names so they are unique
- enforces the uniqueness
- each domain becomes registered

Common DNS Record Types
- the SOA record stores information about: the name of the server that supplied data for the zone, admin of zone, current version of the data file
- start of authority
- contains all the DNS records

NS : name server records - used by top level domain servers to direct traffic to different content DNS serversthat contain authoritative DNS record

What is an A record?
- an address
- most common DNS record
- what the computer uses to look up the name of the domain and translate that to an IP address

What is a TTL?
- the length that a DNS record is cached on either on the resolving server or on the users own PC
- time to live (in seconds)
- the lower the time to live the faster the changes to the records take to propagate 

CNAME : canonical name - resolve one domain name to another
- mapping one domain name to another

Alias Records 
- map resource records from hosted zone to a load balancer
- in the AWS ecosystem

*CNAME cannot be used for a named domain name like http://acloudguru.com it needs to be something like http://m.acloudguru.com

*A record/ alias can be used for a naked domain name because these are mapping to individual services

Routing Policies
- there are 7

Exam Tips
- difference between an alias record and a CNAME: alias record can map to a naked domain name so it will map IP to s3 bucket or elasitc load balancer
	- always choose alias when presented with a question regarding AWS
- common DNS record types:
	- SOA: start of authority record, where your DNS starts
	- CNAME record: map one domain to another
	- NS: name server record : where is the DNS information stored
	- A record: maps domain name to IP address
