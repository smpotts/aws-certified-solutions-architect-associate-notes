# Chapter 18.4 Fixing IP Caching with Global Accelerator

What is Global Accelerator?
- networking service
- sends your user traffic through edge locations to increase performance
- helps deal with IP caching
- users computer caches load balancer IP address and if that changes, things will ...suck?
- Global Accelerator gives us 2 static IP addresses

3 Top Features
- masks complex architecture
- becomes the IP addresses you can rely on
- speeds things up
- weighted pools

Console Demo
- listener : lives in a particular region
- can adjust weight
- can have different endpoints inside the listener

Exam Tips
- Global Accelerator solves IP caching problems
- solves the issue of users not being able to access things when underlying IP changes
- speeds things up
- can setup weights between different endpoints
	- can set them per country and region
- you get 2 static IP addresses that do not change

