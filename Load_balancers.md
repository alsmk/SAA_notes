# Application Load Balancer(HTTP, HTTPS, Webs socket)
Application Load Balancer is a layer load balancer
load balancing to multiple HTTP applications across machines (target groups)
It can follow routing tables to different target groups:
It can be routing based on Path on URL or hostname or Query String , Headers
ALB is best fit for Microservices and Container based applications (like DOCKER and amazon ECS)
The applicatioons server can't see the clients IP directly, The true IP of the client is inserted in the header X-forwarded-For, we can also get the port (x-forwarded-port) and proto


# Network Load balncer (TCP, UDP, HTTP, HTTPS)
Network load balancer (lsayer 4) allows to :
- Forward TCP & UDP  traiffic to your instances
- Handle millions of requests per seconds
- Less latency (~100ms) (vs 400 ms for ALB)
- Used for very high perfomance
  NLB has one static IP per AZ and supports assigns Elastic IP 
Like the ALB the target groups are EC2 instances , ALB can also be use as target group of NLB ( since ALB has a static IP )

# Gateway Load balancer
Deploy ,scale and manage a fleet of 3rd party network virtual appliances in AWS(Firewalls, Intrusion Detection and prevention Systems, Deep packet inspections System, payload manipulations etc)
It operates at layer 3 (network layer) IP packets
Uses Geneve protocol (port 6081)
