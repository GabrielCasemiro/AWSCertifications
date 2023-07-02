# EC2 (Elastic compute Cloud)

## EC2
- Iaas
- It mainly consists in the capability of:
  - Renting virtual machines (EC2)
  - Storing data on virtual drives (EBS)
  - Distributing load across machines (ELB)
  - Scaling the services using an auto-scaling group (ASG)

## EC2 sizing & configuration options
- OS: Linux, Windows or Mac OS
- How much compute power & cores (CPU)
- How much RAM
- How much storage space:
    - Network-attached (EBS & EFS)
    - hardware (EC2 Instance Store)
- Network card: speed of the card, Public IP address
- Firewall rules: security group
- Boostrap script (configure at first launch)

## EC2 User Data
- With this feature we can lauching commands when a machine starts. This is called boostrap.
- Run using root user.

## EC2 instance types
- Naming conventions:
- Ex: m5.2xlarge
  - m: instance class
  - 5: generation
  - 2xlarge: size within the instance class
- T series
  - Generail pourposes
- R series
  - Recommend for softwares that process large data sets in memory
- C series
  - Recommended for sofwtare that needs a high CPU power.
  - Example: Games, Machine learning and so on.
- I, G or H series
  - Great for storage-intensive tasks that require high, sequential read and write access to large data sets on local stores.
  - Examples: Relational and NoSQL databases, ache for in-memory databases (Redis), data warehouse

## EC2 Security Groups (Firewalls)
- Control how the traffic is allowed into or out EC2 instances
- They regulate:
  - Access to Ports
  - Authorised IP ranges - IPv4 and IPv6
  - Control of inbound network
  - Control of outbound network
- You can attach the security group to multiple instances
- Default: You are allowed to access anything out the instance but if you want to allow something out the instance, you need to create the role.
  - All inbound traffic is blocked
  - All outbound traffic is authorised
- It's good to maintain one separate security group for SSH access
- You can authorize inbound traffic from other security groups rather than use IP

## EC2 Security Group: Common errors:
  - If your application is not accessible (time out), then it's a security group issue
  - If your application gives a "connection refused" error, then it's an application error or it's not launched

## EC2 Instance Connect
  - SSH for all plataforms (Windows, Linux or MacOS)
  - Use browser

## EC2 Instances Purchasing Options
  - On-Demand Instances 
    - short workload
    - predictable princing
    - pay by second
  - Reserved (1 & 3 years)
    - long workloads
    - Convertible Reserved Instances
  - Savings Plans (1 & 3 years)
    - commitment to an amount of usage
    - long workload
    - "I want to spend 10$/hour for 1 or 3 years"
  - Sport Instances
    - short workloads
    - cheap 
    - can lose instances (less reliable)
  - Dedicated Hosts
    - book an entire physical server
    - control instance placement
  - Dedicated Instances
    - no other customers will share your hardware
  - Capacity Reservations
    - reserve capacity in a specific AZ for any duration



# EBS
- Storage for EC2
- Must be in the same AZ of the EC2 instance
- Allow to attach only to one instance but one instance can have more than one volume
- As default, the option "Delete on termination" and that will make your volume to be deleted  the instance is deleted.

## EBS snapshots
- Backup 
- Allow to restore
- Can copy snapshots accross AZ or Region
- EBS Snapshot Archive
  - 75% cheaper
  - Takes whithin 24 to 72 for restoring

## EBS recycle bin
- Allows you to recover from accidental deletion
- You must specify the retion from 1 day to 1 year


## AMI
- Amazon machine image
- It's a customazation of an EC2 instance
- Many vendors sell AMI's in the marketplace and you can launch a EC2 from the marketplace with all the specific configurations


## EC2 Image Builder
- Used to automate the creation of Virtual Machines or container images
- Automatically build, test and distribute AMIs

# EC2 Instance Store
- Alternative to EBS
- High performance
- Good for cache
- Lost if our instance stopped/terminated

# EFS
- Network File System
- Can be mounted on many EC2 instances at the same time
- Only for Linux
- Multi-AZ


##