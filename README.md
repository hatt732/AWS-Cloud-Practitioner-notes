# Notes for AWS Certified Cloud Practitioner

# Contents

# Cloud Computing
- __on-demand delivery__ of compute power, database storage, applications, and other IT resources
- __pay-as-you-go pricing__
- __provision exactly the right type and size of computing__
- access as many resources __almost instantly__
- simple way to access __servers, storage, databases__ and a set of application services

## The Deployment Models of the Cloud
- Private Cloud
- Public Cloud
- Hybrid Cloud
<picture>
  <img alt="The Deployment Models of the Cloud" 
       src="https://user-images.githubusercontent.com/87024662/177539153-f8ae8fc6-4277-4c06-9ad0-16183e4b4306.png" 
       width=750px>
</picture>

## The Five Characteristics of Cloud Computing
- On-demand self service
- Broad network access
- Multi-tenancy and resource pooling
- Rapid elasticity and scalability
- Measured service

## Six Advantages of Cloud Computing
- Trade capital expense (CAPEX) for operational expense (OPEX)
- Benefit from massive economies of scale
- Stop guessing capacity
- Increase speed and agility
- Stop spending money running and maintaining data centers
- Go global in minutes

## Problems solved by the Cloud
- Flexibility
- Cost-Effectiveness
- Scalability
- Elasticity
- High-availability and fault-tolerance
- Agility

## Types of Cloud Computing
<picture>
  <img alt="Types of Cloud Computing" 
       src="https://user-images.githubusercontent.com/87024662/177539654-062f6a88-bcef-4166-ac5f-f73fa20144e8.png" 
       width=750px>
</picture>

- Infrastructure as a Service (IaaS)
  - Amazon EC2 (on AWS)
  - GCP, Azure, Rackspace, Digital Ocean, Linode
- Platform as a Service (PaaS)
  - Elastic Beanstalk (on AWS)
  - Heroku, Google App Engine (GCP), Windows Azure (Microsoft)
- Software as a Service (SaaS)
  - Many AWS services (ex: Rekognition for Machine Learning)
  - Google Apps (Gmail), Dropbox, Zoom


## Pricing of the Cloud
- Compute
- Storage
- Data transfer OUT of the Cloud

## AWS Global Infrastructure
![image](https://user-images.githubusercontent.com/87024662/177540993-e9c05d3c-ab56-41e4-adbd-38a0fb6c29cb.png)

- AWS Regions
  - all around the world (us-east-1)
  - cluster of data centers
  - __Most AWS services are region-scoped__
- AWS Availability Zones
  - many availability zones (usually 3, min is 2, max is 6) ap-southeast-2a
  - isolated from disasters
  - connected with high bandwidth, ultra-low latency networking
- AWS Data Centers
- AWS Edge Locations / Points of Presence
  - Content is delivered to end users with lower latency

## AWS Services Scope
- Global Services
  - Identity and Access Management (IAM)
  - Route 53 (DNS service)
  - CloudFront (Content Delivery Network)
  - WAF (Web Application Firewall)
- Region Services - Most AWS services

https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/

## Shared Responsibility Model
- CUSTOMER = Responsibility for the security __IN__ the cloud
- AWS = Responsibility for the security __OF__ the cloud

## AWS Acceptable Use Policy
- No Illegal, Harmful, or Offensive Use or Content
- No Security Violations
- No Network Abuse
- No E-Mail or Other Message Abuse

## Scalability Vs. Elasticity
<picture>
  <img alt="Scalability Vs. Elasticity" 
       src="https://user-images.githubusercontent.com/87024662/177538768-560097a9-9dc2-492a-8793-d54c0333e694.png" 
       width=750px>
</picture>

## Cloud Computing Vs. Mobile Computing

## Multi-tenancy
<picture>
  <img alt="Multi-tenancy" 
       src="https://user-images.githubusercontent.com/87024662/177539855-9ac597c6-2dd1-4fb6-b90a-5efcc793b7fd.png" 
       width=750px>
</picture>

# IAM Section

### Users
- Mapped to a physical user, has a password for AWS Console
### Groups
- Contains users only
### Policies
- JSON document that outlines permissions for users or groups
### Roles
- For EC2 instances or AWS services
### Security
- MFA + Password Policy
### AWS CLI
- Manage your AWS services using the command-line
### AWS SDK
- Manage your AWS services using a programming language
### Access Keys
- Access AWS using the CLI or SDK
### Audit
- IAM Credential Reports & IAM Access Advisor

## IAM Policies inheritance
<picture>
  <img alt="IAM Policies inheritance" 
       src="https://user-images.githubusercontent.com/87024662/178901938-887607de-e990-4737-95e7-ee08c1fae7e1.png" 
       width=750px>
</picture>


## IAM Guidelines & Best Practices
- Don’t use the __root__ account except for AWS account setup
- __One__ physical user = __One__ AWS user
- __Assign users to groups__ and assign permissions to groups
- Create a __strong password policy__
- Use and enforce the use of __Multi Factor Authentication (MFA)__
- Create and use __Roles__ for giving permissions to AWS services
- Use Access Keys for Programmatic Access (CLI / SDK)
- Audit permissions of your account with the IAM Credentials Report
- __Never share IAM users & Access Keys__

# EC2 Section



## EBS Vs. S3 Vs. EFS
- EBS is a high-performance per-instance block storage system designed to act as storage for a single EC2 instance (most of the time)
- EFS is a highly scalable file storage system designed to provide flexible storage for multiple EC2 instances
- S3 is an object storage system, designed to provide archiving and data control options and to interface with other services beyond EC2. It’s also useful for storing static html pages and shared storage for applications
<picture>
  <img alt="IAM Policies inheritance" 
       src="https://user-images.githubusercontent.com/87024662/178952472-85d09215-aec8-49f3-97e8-d0f9e4070d60.png" 
       width=750px>
</picture>

### EBS (Elastic Block Store) vs Instance Store in AWS
<picture>
  <img alt="IAM Policies inheritance" 
       src="https://user-images.githubusercontent.com/87024662/178956059-ae6fac61-6077-4887-938f-fa17d2ad1d9f.png" 
       width=750px>
</picture>

+ Amazon EFS Standard
+ Amazon EFS Standard-Infrequent Access (EFS Standard-IA)
+ Amazon EFS One Zone
+ Amazon EFS One Zone-Infrequent Access (EFS One Zone-IA)
