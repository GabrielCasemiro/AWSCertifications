# AWS Cloud Practitioner Exam Study Notes

## What is Cloud Computing?
- Cloud computing is the on-demand delivery of compute power, database storage, applications, and other IT resources over the internet.
- Pay-as-you-go pricing allows users to pay for only the resources they consume.
- Provisioning resources can be done based on specific requirements.
- Cloud resources can be accessed almost instantly, providing flexibility and scalability.

## Cloud Types
- **Private Cloud:**
    - Cloud services used by a single organization.
    - Offers complete control and security for sensitive applications.
    - Allows organizations to meet specific business needs.
  
- **Public Cloud:**
    - Cloud resources owned and operated by a third-party cloud service provider.
    - Delivered over the internet to multiple organizations.
    - Advantages of public cloud computing:
        1. Scalability: Easily scale resources up or down based on demand.
        2. Cost-effectiveness: Pay only for the resources you use.
        3. Reliability: Benefit from the cloud provider's infrastructure and redundancy.
        4. Security: Cloud providers implement robust security measures.
        5. Global reach: Access cloud services from anywhere in the world.
        6. Innovation: Cloud providers continuously introduce new services and features.

- **Hybrid Cloud:**
    - Combination of on-premises infrastructure and cloud services.
    - Allows organizations to keep sensitive assets on their private infrastructure.
    - Leverage the flexibility and cost-effectiveness of the public cloud for other resources.
  
## Five Characteristics of Cloud Computing
1. **On-demand self-service:**
    - Users can provision resources and use them without human interaction from the service provider.
    - Enables a self-service model, providing agility and quick access to resources.

2. **Broad network access:**
    - Cloud resources are available over the network and can be accessed by diverse client platforms.
    - Resources can be accessed using laptops, smartphones, or tablets from anywhere with an internet connection.

3. **Multi-tenancy and resource pooling:**
    - Multiple customers can share the same infrastructure and applications.
    - Ensures security and privacy through isolation mechanisms.
    - Allows efficient resource allocation and utilization.

4. **Rapid elasticity and scalability:**
    - Cloud resources can be automatically and quickly acquired and disposed of as needed.
    - Resources can be easily scaled up or down based on demand.
    - Enables organizations to optimize resource usage and cost efficiency.

5. **Measured service:**
    - Cloud usage is measured, providing transparency and accurate billing.
    - Users pay for the resources they consume, promoting cost control and accountability.
  
## Six Advantages of Cloud Computing
1. **CAPEX to OPEX:**
    - Cloud computing eliminates the need for upfront capital expenditure on hardware infrastructure.
    - Organizations can shift to operational expenditure, paying for cloud services on a pay-as-you-go basis.

2. **Benefit from massive economies of scale:**
    - Cloud providers leverage their vast infrastructure and customer base to offer services at lower costs.
    - Users can benefit from economies of scale without having to invest in building and maintaining their own infrastructure.

3. **Stop guessing capacity:**
    - With cloud computing, organizations can easily scale their resources up or down based on demand.
    - They no longer need to guess the capacity required in advance, ensuring optimal resource utilization.

4. **Increase speed and agility:**
    - Cloud computing enables rapid provisioning of resources, reducing the time to market for new applications and services.
    - Organizations can quickly respond to changing business needs, enabling faster innovation and gaining a competitive advantage.

5. **Stop spending money running and maintaining data centers:**
    - Cloud providers take care of infrastructure maintenance, security, and updates.
    - Organizations can focus their resources and expertise on core business activities, rather than managing data centers.

6. **Go global in minutes:**
    - Cloud computing provides global reach, with data centers located around the world.
    - Organizations can expand their operations to new regions quickly, serving customers in different geographical locations.
  
## Problems AWS Solved
- **Flexibility:** AWS offers a wide range of services and configurations, allowing organizations to tailor their infrastructure to specific needs.
- **Scalability:** AWS provides the ability to scale resources up or down quickly and automatically, based on demand.
- **Security:** AWS incorporates robust security measures, such as encryption, access control, and monitoring, to protect data and resources.
- **Reliability:** AWS infrastructure is designed for high availability and fault tolerance, ensuring minimal downtime and service disruptions.
- **Cost-effectiveness:** AWS offers a pay-as-you-go model, allowing organizations to optimize costs by paying for only the resources they use.
- **Innovation:** AWS continuously introduces new services and features, enabling organizations to leverage the latest technologies and trends.

## Types of Cloud Computing
- **On-Premises:** Infrastructure and applications are hosted and managed within an organization's own data centers.
- **IaaS (Infrastructure as a Service):** Provides virtualized computing resources, such as virtual machines, storage, and networks, over the internet.
- **PaaS (Platform as a Service):** Offers a platform for developing, testing, and deploying applications without the need for infrastructure management.
- **SaaS (Software as a Service):** Delivers fully functional software applications over the internet, eliminating the need for installation and maintenance.


## AWS Global Infrastructure

- AWS Regions
- AWS Availability Zones
- AWS Data Centers
- AWS Edge Locations/ Points of Presence

## AWS has global services
 - IAM
 - Route 53
 - Cloudfront 
 - WAF

## Most AWS services are Region-scoped
- EC2
- Elastic Beanstalk
- Lambda
- Reckognition

## Shared Resposability Model Diagram

- Customer
    - Responsible the security in the cloud
        - Users, Groups, Roles, Policies management and monitoring
        - Enable MFA on all accounts
        - rotate all your keys often
        - Use IAM tools to apply appropriate permissions
        - Analyze access patterns & review permissions
- AWS
    - Responsible the security of the cloud
        - Infrastructure (global network security)
        - Configuration and vulnerability analysis
        - Compliance validation
