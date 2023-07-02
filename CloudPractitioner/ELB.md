# Scalability
Means that an application/system can handle greater loads by adapting
- There are two kinds of scalability
  - Vertical Scalability
  - Horizontal Scalability (= elasticity)
- Scalability is linked but different to High Availability
  
## Vertical Scalability
- Increase size of the instance
- For example: t2.micro to t2.large
- There's a limit to how much you can scale
  
## Horizontal 
- Increase the number of instances/systems for you application

# High availability
- Means running your application/system in at least 2 Availability Zones

# Load balancer
- LB are servers that forward internet traffic to multiple services (EC2 instances).
- Advantages:
  - Expose a single point of DNS to your application
  - Provide SSL
  - High Availability accross zones
  - Do regular health checks to your instances
  - Seamlessly handle failures of downstram instances
  - Spread load across multiple instances

# ELB (Elastic load balancer)
- Managed by AWS
- 4 kinds of load balancers offered by AWS
  - Application Load Balancer (HTTP/HTTPS)
  - Network load balacer
  - Gateway Load Balancer
  - Classisc Load Balancer (Replaced by ALB)
  

## Application Load Balancer
- HTTP/HTTPS/gRPC protocols (Layer 7)
- HTTP routing features
- Static DNS (URL)

## Network Load Balancer
- TCP/ UDP (layer 4)
- High Performance millions of requests per seconds
- Static IP

## Gateway Load Balancer
- GENEVE Protocol on IP Packets (Layer 3)
- Rout traffic to firewals that you manage on EC2 instances
- Instrusion detection

# Auto Scaling Group
- Allow you to scale out  (add EC2 instances) to match the increased load and allow you to scale in (remove EC2 instances) to match a decreased load
- Ensure we have a minimum and a maximum number of machines running
- Automatically register new instances to a load balancer
- Repalce unhealthy instances
Sumarry: save costs