# Extreme Performance with Network Load Balancers

Layer 4 Load Balancing
- network load balancer functions at the 4th layer

Requests Received
- after it receives a connection request it selects a target from the target group for the default rule

Listeners 
- checks for connection requests from clients using protocol and ports
- forward request to the target group

Target Groups
- routes request to one or more registered targets

Ports and Protocols
- TCP, TLS, UDP, TCP_UDP
- ports from 1-65535

Encryption
- can use a TLS listener to offload the work of encryption and decryption to your load balancer so your apps can focus on their business logic
- if the listener protocol is TLS, you must deploy exactly 1 SSL certificate on the listener

Exam Tips
- network load balancers are best suited for load balancing of TCP traffic where extreme performance is required
- layer 4 connection level
- extreme performance
- other use cases is where Application load balancers do not support the protocols
- can decrypt and encrypt, but you will need to install the certificate on the load balancer
