# Chapter 15.4 Container Overview

What is a Container?
- a unit of software that packages up code and all it's dependencies
- allows the app to run quickly and reliably from one computing environment to another
- contents don't change between environments
- reason for containers is the guest operating system so you don't have to duplicate it over and over

Container Terminology
- Dockerfile : set of instructions for what the container includes
- Image : built by the Dockerfile, immutable, contains the code libraries, dependencies and configuration files needed to run the app
- Registry : kinda like GitHub but for your image
- Container : a running copy of the image that has been created

Console Demo
- open Terminal window
- look at the Dockerfile
- curl command to hit the website

Exam Tips
- containers are more flexible
- full control of what's inside with Dockerfile
- easy to standardize
- situation talking about flexible, immutable environment : containers
- portability, easy of use, etc.
