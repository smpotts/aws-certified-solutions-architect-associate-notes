# Chapter 16.1 DDoS Overview

What is a DDoS Attack
- distributed denial of service attack : attempts to make your website or application unavailable

Layer 4 Attacks
- SYN flood : works at the TCP layer
- a 3-way handshake takes place
	- after that the TCP connection is established and apps begin sending data
- SYN flood happens when we overwhelm the server by sending a large number of SYN packets and then ignoring the ACKs returned by the server
	- manipulating the handshake
	- server uses up resources and eats through the allowed number of TCP connections

Amplification Attacks
- NTP, DNS, CharGen, SNMP
- attacker sends a 3rd party server a request with a spoofed IP address
- server responds with a greater payload to the spoofed IP address
- attacker sends a spoofed source IP address

Layer 7 Attacks
- when a web server receives a large number of get or post requests
- users cannot access the website

Exam Tips
- DDoS - distributed denial of service : attempts to make the site unusable
- common layer 4 attacks are SYN flood and NTP amplification attacks
- common layer 7 attacks are floods of GET and POST requests
- need to know the differences between layer 4 and 7

