# Chapter 12.2 What are Launch Templates/ Configurations?

What are Launch Templates?
- specifies all the needed settings that go into building out EC2 instances
- collection of settings that you can configure, so you don't have to do it over and over

Templates vs Configurations
- templates: better, faster, stronger, best practice
	- more than just autoscaling, supports versioning, more granular
- configurations: immutable, only for autoscaling, don't use them, limited configs

Demo
- EC2 -> Launch Templates -> create launch template
- autoscaling guidance, check if you intend to include in auto scaling group
- have to give it AMI
- some things can be overwritten or provided later
- must specify Key pair at the time of template creation
- VPC blank: if we specify then it can't be used in autoscaling group
- if you want to provision/ bootstrap, provide user data 

Exam Tips
- need to know what makes a template: AMI, EC2 instance size, security groups and potential network information
- if we include networking, can't use template in autoscaling group
- launch templates are the best way to templatize the EC2 instance
- launch configurations are older
- user data is included in the template or configuration
- when we need to make changes, launch templates can be changed
- launch configurations are immutable
