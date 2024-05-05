# Chapter 17.2 CloudFormation

CloudFormation Overview
- requires us to write code
- CloudFormation is a declarative programming language
- JSON or YAML
- deploy your template
- builds the infrastructure you defined

Console Demo
- automatically puts template in an S3 bucket
- add parameters
- CloudFormation might create roles
- mappings are basically like parameters that fill themselves in
	- AMI values or resource id : if in some region use one value
- if template not working in a new region, could be an issue in the mapping section

Exam Tips
- perfect for creating immutable architecture
- can easily pick that template up and run it anywhere
- can easily audit what goes into the template
- consistency
- want everything to be disposable
- parameters : questions the end users are asked
- mapping : VPC size, region
- resource section : what goes into it
- hardcoded resource IDs can cause template creation to fail (especially AMI IDs)
- rolls back to the last known good state
- just making an API call faster and simpler
- immutable : throw it away and recreate it
