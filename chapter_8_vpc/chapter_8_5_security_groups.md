# Protecting Your Resources with Security Groups

Review of Security Groups
- "basic human senses"
- computers communicate on with different protocols: ssh, rdp, http, https

Security Groups with Networking
- last line of defense
- start troubleshooting with route table, Network ACL and then security groups

Security Groups
- virtual firewalls
- by default everything is blocked
- to let everything in 0.0.0.0/0

Exam Tips
** security groups are stateful, if you send a request from instance, response traffic is allowed to flow in regardless of inbound
- responses are allowed to flow out regardless of outbound rules