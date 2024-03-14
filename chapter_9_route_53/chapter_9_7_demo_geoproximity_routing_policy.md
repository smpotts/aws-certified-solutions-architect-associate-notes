# Demo: Using a Geoproximity Routing Policy

Route 53 Traffic Flow
- can be used to create a routing flow based on : geo location, latency, and availability to route traffic
- build traffic routing policies from scratch or from a library

Geoproximity Routing Policy
- only available when using traffic flow
- route traffic based on location and resources or can give a "bias" to have majority of traffic go to a certain location
- this can get very complication
- probably will not see this in the exam
- bias expands or shrinks the size of the geographic region from which traffic is routed to in a resource

Demo
- Route 53 -> traffic flow
- Create a traffic policy

Exam Tips
- likely won't see in exam
- know what geoproximity routing policies are: routes traffic based on location of users and resources
- can route more traffic to a given resource by specifying a bias
- to use geoproximity routing you have to have traffic flow set up