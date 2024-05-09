#  Route53 - record types
A - maps a hostnane to ipv4
AAAA - maps a hostname to ipv6
CNAME - maps a hostname to another hostname ( the target is a domain name which must have an A or AAAA record)
NS - Name server for the Hosted zone (control how traffic is routed for a domain)

Alias - points a hostname to an AWS resource , TTL is automatically set by route53 we can not set it manually
You can not set an Alias record for an EC2 DNS name
we can set an Alias for 
- ELB
- cloudfront
- api gateway
- elastic beanstalk
- VPC interface Endpoints
- Global Accelator
- Route53(must be in same hosted zone)

# Route53 routing policies
- simple :
   route traffic to a single resource ,can specify multiple values in a single record, when alias enabled we can specify only one AWS resource and can't be associated with health checks
- weighted: 
  the more the weight is the more the traffic will send , can be associated with health checks
- failover
- latency based: 
  Redirect to the resource that has the least latency close to us, can be combined with health checks
- geolocation:
  based on users location
- Multi valued answer:
  Use when routing traffic to multiple resources
- Geoproximity:
  Route traffic to your resources based on the geographic location of users and resources
  the more the bias value the more the traffic will shifted , multi value is not a substitute for having a ELB , up to 8 healthy records are returned for each multi - value query

