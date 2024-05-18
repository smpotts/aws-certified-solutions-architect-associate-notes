# Chapter 18.2 Global Caching with CloudFront

What is CloudFront?
- content delivery network
- take static content and distribute content out to edge locations all over the globe

Using Edge Locations
- take single locations and make it globally distributed

Important Settings
- security : defaults to HTTPS connection with ability to attach SSL certificate
- can route your entire domain through CloudFront
- can't pick specific edge locations 
- can pick general areas but more continent based
- can create deny list but don't want to use it with CloudFront use WAF
- can be used to front AWS endpoints along with non AWS apps
- can enforce TTL on content in the cache

Console Demo
- create distribution
- you can restrict access to content using pre-signed url and pre-signed cookies
- continent based
- can upload custom SSL certificate
- grab the distribution domain name

Exam Tips
- CloudFront fixes all connection issues
- good for slow connections around the globe
- if content delivery is slow
- cache the things that take a long time
- AWS and on-site architecture
- can block certain countries but you should use WAF
- can't use specific edge locations
