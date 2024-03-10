# Using Roles

What is an IAM role?
- Identity you can create that has permissions
- instead of being assoc. with one person it is assumable by anyone who needs it
- roles are temporary
- can be assumed by people, AWS architecture
- can allow cross account access

Exam Tips
- they are the preferred option
- avoid hardcoding credentials
- roles are made of policy docs
- you can update a policy attached to a role
- attaching and detaching roles without having to stop or terminate instances
- choose roles over hardcoding credentials
