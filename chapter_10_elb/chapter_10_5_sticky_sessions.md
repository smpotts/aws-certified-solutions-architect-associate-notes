# Getting "Stuck" with Sticky Sessions

What are Sticky Sessions?
- classic load balancer route each request independent to a registered EC2 instance with the smallest load
- sticky sessions allow you to bind a user's session to a specific EC2 instance
- this ensures all requests from the user during the session are sent to the same instance

Scaling Issues
- tries to route traffic to EC2 instance even if it's unavailable and then the user will get an error
- need to disable sticky sessions
- can use sticky sessions with application load balancers
- traffic will be sent at the target group level

Exam Tips
- stick sessions enable users to stick to the same EC2 instance
- can be useful if you are storing information on that instance
- may see a scenario based question about removing an EC2 instance from a pool but the load balancer continues to direct traffic to that instance
- disable sticky sessions