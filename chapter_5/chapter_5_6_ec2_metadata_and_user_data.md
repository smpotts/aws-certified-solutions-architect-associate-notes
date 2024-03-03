EC2 Metadata and User Data

What is EC2 Metadata?
- data about your EC2 instance: private ip address, public ip address, hostname

Retrieving Metadata
- using a curl command we can query metadata about our instance
- can use a bootstrap script to save metadata

Demo
- you can put the "bootstrap commands" in the user data section when creating an EC2 instance

curl http://169.254.169.254/latest/meta-data/

Query user data
curl http://169.254.169.254/latest/user-data/
- this can be used to query the user data/bootstrap script that was used when we setup this instance

Exam Tips
- user data: bootstrap scripts
- meta data: data about your ec2 instance 
- you can use your bootstrap scripts to access metadata