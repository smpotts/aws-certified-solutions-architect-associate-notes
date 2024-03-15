# Using Application Load Balancers

Layer 7 Load Balancing
- review what the OSI model is
- application layer is layer 7 in the model
- after the load balancer gets a request, it evaluates the listener rules in prio order to determine which rule to apply and then selects a target from the target group for the rule action

Listeners, Rules and Target Groups

Listener
- check for connection requests from clients using the protocol and port you configure
- you can define rules that determine how the load balancer routes requests to its registered targets
- rules have one or more actions or conditions

Rules
- when conditions for a rule are met then the actions are performed
- must define a default rule for a listener 

Target Groups
- route requests to one or more registered targets like EC2 instances

Application Load Balancer Diagram
- listener sends traffic to targets inside the target group and there is a health check attached to it
- target group is a group of targets
- rules are on listeners

Path-Based Routing
*common scenario in exam
-   load balancer can look at pathway and make routing decisions based on your path
- ELB are layer 7 aware and can do intelligent pathing

Limitations of Application Load Balancers
- only supports HTTP and HTTPS

HTTPS Load Balancing
- in order to use a HTTPS listener, you must deploy at least one SSL/ TLS server cert on your load balancer
- load balancers use a server cert to terminate the frontend connection and then decrypt requests fro mthe client before sending them to the targets
- AWS will do this for you if you use AWS's DNS to register your domain name

Demo
- launch 3 web servers -> creating 3 EC2 instances
- paste bootstrap script into the user data field that does installs
- go to ELB and select the application load balancer
- Internet facing
- IPv4 is fine
- add web dmz security group
- in listeners and routing we need to create a target group
- grouped by isntances
- port 80, http
- health checks
- register targets
- create target group

- create target group first and then application load balancer
- copy DNS address 
- make sure targets are in the registered target group
- refresh and notice it is load balancing across all 3 EC2 instances so you could get any of those 3 when you try to read that DNS endpoint

Exam Tips
- listeners: checks for connection reqs from client using the protocol and port you configure
- rules: determine how the load balancer routes requests to targets
- target groups: routes requests to one or more targets
- application load balancers limited to http and https
- https needs an ssl certificate so it can terminate front end connection and decrypt requests from clients before sending them to targets
