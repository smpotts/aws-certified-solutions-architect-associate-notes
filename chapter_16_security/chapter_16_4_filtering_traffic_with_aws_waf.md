# Chapter 16.4 Filtering Traffic with AWS WAF

What is WAF?
- web application firewall
- monitor HTTP and HTTPS requests that are forwarded to AWS
- control access to content
- configure what IP addresses can make requests or what query string parameters needed to be passed for request

Layer 7
- WAF
- application layer

Behaviors
- all requests except the ones you specify
- block requests except the ones you specify
- count the requests that match the properties you specify

Conditions
- you can define conditions by using characteristics of web requests
	- IP addresses
	- country req comes from
	- values in req headers
	- presense of SQL code
	- presence of a script
	- strings that appear in requests

Exam Tips
- WAF operates in layer 7 : application layer
- blocking access to specific countries or IP addresses