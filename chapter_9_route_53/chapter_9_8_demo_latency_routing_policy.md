# Demo: Using a Latency Routing Policy

Latency Routing Policy
- allow you to route traffic based on lowest network latency for the end user
- gives the user the fastest response time
- create a latency resource record set for the EC2 instance in each region that hosts your website
- Route 53 responds with the value asspciated with the result record set

Demo
- sets up records with the latency routing type

Exam Tips
- latency routing policy : sends traffic to lowest latency resource
- scenario about lowest latency
