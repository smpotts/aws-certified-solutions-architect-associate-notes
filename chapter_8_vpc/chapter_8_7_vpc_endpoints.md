# Private Communication Using VPC Endpoints

What are VPC Endpoints?
- enable you to privately connect to your VPC to supported AWS service
- don't need Internet Gateway, NAT device
- like a NAT gateway but not leaving AWS environment
- instance in VPC do not require public IP addresses to communicate with resources in the service
- traffic between VPC and other services does not leave the AWS network
- virtual devices that allow communication between instances and services without imposing availabilty risks or bandwidth constraints on your network traffic

Endpoints
- virtual devices
- no bandwidth constraints

VPC Endpoint Types
- interface endpoints : elastic network interface with a private IP address
- gateway endpoint : similar to NAT gateways, virtual device that you provision to connect to S3 or DynamoDB
	- don't have to traverse NAT Gateway and go out to the internet

What's happening
- add a VPC endpoint in the private subnet to have a direct connection to S3 outside the VPC

Demo
- attach IAM S3 admin role to DB instance
- go into VPC and create endpoint
- search S3 in services and choose the Gateway one
- put it in the route table
- does not traverse  the private internet

Exam Tips
- remember use cases: want to connect services without leaving the internal network
- 2 types of endpoints: interface and gateway endpoints
- gateway endpoints support s3 and DynamoDB