# Glocal Application

A global application is an application deployed in multiple geographies
- On AWS: this could be Regions and / or Edge Locations
- Benefits:
  - Decreased Latency
  - Disaster Recovery
  - Attack protection 
    - It's make harder to attack many regions at the same time


## Route 53
Route53 is a managed DNS (Domain Name System)
- DNS is a collection of rules and records which helps clients understand how to reach a server through URLs
- Great to route users to the closest deployment with least latency
- Great for disaster recovery strategies

### Simple Routing Policy
- No health checks

### Weighted Routing Policy
Allows us to distribute the traffic across multiple EC2 instances

### Latency Routing Policy
Allow us minimize the latency by making the users connect to the closest server

### Failover Routing Policy
The DNS will do a health check to the primary and in case of failure, the dns will redirect to the failover instance
- Help with disaster recovery

## CloudFront (CDN)
Improves read performance, content is cached at the edge
- 216 Point of presence globally (edge locations)
- DDos protection, integration with Shield and AWS Web Application Firewall 
- Replicate part of your application to AWS Edge Locations 
  - This decrease latency
- Cache common requests
  - Improved user experience and decreased latency

### Origins
- S3 bucket
  - For distributing files and caching them at the edge
  - Enchanced securty with CloudFront Origin Access Control (OAC)

- Custom Origin (HTTP)
  - Application Load Balancer
  - EC2 Instance
  - S3 website
  - Any HTTP backend you wat

## S3 Transfer Acceleration
Accelerate global uploads & downloads into Amazon S3. Increase transfer speed by transferring file to an AWS edge location which will forward the data to the S3 bucket in the target region


## AWS Global Accelerator
Improve global application availability and performance using the AWS global network
- Leverage the AWS internal network to optimize the route to your application (60% improvement)
- Does not cache anything

## AWS outposts
- AWS servers racks in your data center and you can use some services

