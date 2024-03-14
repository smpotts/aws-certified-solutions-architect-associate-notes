# Demo: Geolocation Routing Policy

Geolocation Routing Policy
- lets you choose where traffic will be sent based on geographic location of your users
- localization reasons - display in euros and certain language
- have EU users route to eu-west-1 and US users to us-east-1

Demo
- Route 53 -> hosted zones
- Create a record
- A record
- Choose Geolocation and choose location
	- by continent or individual countries


Exam Tips
- scenario based question where you have users in different parts of the world and you want to send them to different locations
- location of users and sent to particular country, not latency, use geolocation routing