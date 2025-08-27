[UDEMY COURSE 2025](https://www.udemy.com/course/aws-certified-cloud-practitioner-new/?couponCode=25BBPMXINACTIVE)

(Section 1 and 2: Intro)

# Section 3: What is Cloud Computing

## Traditional IT Overview
- Websites operate by clients using networks to send requests to servers identified by IP addresses.
- Servers consist of CPU, RAM, storage, and networking components essential for processing and data management.
- Traditional IT involved hosting servers physically in homes or data centers, which posed challenges in scaling, maintenance, and disaster recovery.
- Cloud computing externalizes infrastructure management, providing scalable and on-demand resources.

## What is Cloud Computing ?
- Cloud computing provides on-demand delivery of computing resources with pay-as-you-go pricing.
- It offers flexibility to provision exactly the right type and size of resources instantly.
- There are different cloud deployment models: `private`, `public`, and `hybrid clouds`.
- Cloud computing delivers benefits such as `scalability`, `cost efficiency`, `agility`, and `high availability`.

## The Different Types of Cloud Computing
- Cloud computing is categorized into `Infrastructure as a Service (IaaS)`, `Platform as a Service (PaaS)`, and `Software as a Service (SaaS)`.
- `IaaS` provides raw building blocks such as networking, computers, and data storage, offering high flexibility.
- `PaaS` removes the need to manage underlying infrastructure, allowing focus on application deployment and management.
- `SaaS` delivers fully managed products run by service providers, requiring no management from users.
- AWS and other providers offer services corresponding to each cloud computing type.
- Cloud pricing follows a `pay-as-you-go model`, `charging based on compute time`, `storage used`, and `outbound data transfer`.

## AWS Cloud Overview
- AWS was launched internally in 2002 and publicly in 2004 with SQS, expanding to S3 and EC2 in 2006.
- AWS operates globally with multiple `regions` and `availability zones`, enabling scalable and sophisticated applications.
- Choosing an AWS region depends on factors like `compliance`, `latency`, `service availability`, and `pricing`.
- AWS has over 400 points of presence (400+ edge locations) worldwide to deliver content with low latency.

## Shared Responsibility Model & AWS Acceptable Policy
- The Shared Responsibility Model defines the division of security responsibilities between AWS and the customer.
- Customers are responsible for `security "in" the cloud`, `including data`, `operating systems`, `network`, and `firewall configurations`.
- AWS is responsible for `security "of" the cloud`, including `infrastructure`, `hardware`, `software`, and `internal security`.
- Users must comply with AWS's Acceptable Use Policy, prohibiting illegal, harmful, offensive, or abusive activities.

## Quiz Section 3: What is Cloud Computing

> Q: You ONLY want to manage Applications and Data. Which type of Cloud Computing model should you use?
> 
> A: Platform as a Service (PaaS)

> Q: What is the pricing model of Cloud Computing?
> 
> A: Pay-as-you-go pricing

> Q: Which Global Infrastructure identity is composed of one or more discrete data centers with redundant power, networking, and connectivity, and are used to deploy infrastructure?
> 
> A: Availability Zones

> Q: Which of the following is **NOT** one of the Five Characteristics of Cloud Computing?
> 
> A: Dedicated Support Agent to help you deploy applications

> Q: Which are the 3 pricing fundamentals of the AWS Cloud?
> 
> A: Compute, Storage, and Data transfer out of the AWS Cloud

> Q: Which of the following options is **NOT** a point of consideration when choosing an AWS Region?
> 
> A: Capacity availability

> Q: Which of the following is **NOT** an advantage of Cloud Computing?
> 
> A: Train your employees less

> Q: AWS Regions are composed of?
> 
> A: Three or more Availability Zones

> Q: Which of the following services has a global scope?
> 
> A: IAM (Identity Access Manager)

> Q: Which of the following is the definition of Cloud Computing?
> 
> A: On-demand availability of computer system resources, especially data storage (cloud storage) and computing power, without direct active management by the user.

> Q: What defines the distribution of responsibilities for security in the AWS Cloud?
> 
> A: The Shared Responsibility Model

> Q: A company would like to benefit from the advantages of the Public Cloud but would like to keep sensitive assets in its own infrastructure. Which deployment model should the company use?
> 
> A: Hybrid Cloud

> Q: What is **NOT** authorized to do on AWS according to the AWS Acceptable Use Policy?
> 
> A: Run analytics on stolen content




# Section 4: IAM - Identity and Access Management

## IAM Introduction: Users, Groups, Policies
- IAM stands for `Identity and Access Management` and is a global AWS service for managing users and groups.
- The root user is created by default and should only be used for initial account setup, not for daily use or sharing.
- Users represent individual people in an organization and can be grouped logically; groups contain only users, not other groups.
- Permissions are assigned to users or groups via `JSON policy documents` following the `least privilege principle` to ensure security and cost control.

## IAM Users & Groups
- IAM is a global AWS service without region selection.
- Root user access is not recommended; create IAM users for safer account management.
- Users can be grouped to manage permissions efficiently.
- Customizing the AWS sign-in URL with an account alias simplifies access.

## IAM Policies
- IAM policies can be attached at different levels: `groups`, `users (inline policies)`, and `multiple groups`.
- Users inherit policies from all groups they belong to, combining permissions.
- IAM policy structure includes version, ID, and statements with key elements: Sid, Effect, Principal, Action, Resource, and optional Condition.
- Understanding Effect, Principal, Action, and Resource is essential for managing AWS permissions effectively.

