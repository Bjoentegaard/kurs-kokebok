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

- IAM user permissions are managed through group memberships and attached policies.
- Removing a user from an admin group revokes their administrator access immediately.
- Policies can be attached directly to users or through groups, affecting their permissions.
- AWS IAM policies use JSON documents to define allowed actions and resources with fine-grained control.

## IAM MFA Overview
- Password policies enhance account security by enforcing strong password requirements.
- `Multi-Factor Authentication (MFA)` combines something you know (password) with something you own (security device) for stronger protection. 
- AWS supports various MFA devices including `virtual MFA apps`, `U2F security keys`, and `hardware key fobs`. 
- Protecting root and IAM user accounts with MFA significantly reduces the risk of unauthorized access.

## AWS Access Keys, CLI and SDK
- AWS can be accessed via three methods: `Management Console`, `CLI`, and `SDK`.
- Access keys are essential credentials for CLI and SDK access and must be kept secret.
- The AWS CLI allows command-line interaction with AWS services and supports scripting and automation.
- The AWS SDK provides language-specific libraries to programmatically access AWS services within applications.

## IAM Roles for AWS Services
- IAM Roles allow AWS services to perform actions on your behalf by assigning permissions.
- IAM Roles function like users but are intended for AWS services, not physical people.
- EC2 Instances and other AWS services like Lambda Functions use IAM Roles to access AWS resources securely.
- Creating and assigning IAM Roles is essential for managing permissions for AWS services.

## IAM Security Tools
- IAM Credentials Report provides an account-level overview of all users and their credential statuses.
- IAM Access Advisor offers user-level insights into granted service permissions and their last access times.
- Access Advisor helps enforce the principle of least privilege by identifying unused permissions.
- Utilizing these tools enhances security management within IAM.

## IAM Best Practices
- Avoid using the root account except during initial AWS setup.
- Each AWS user should correspond to a single physical user; do not share credentials.
- Manage security by assigning users to groups and applying permissions at the group level.
- Enforce strong password policies and use multifactor authentication (MFA) to enhance account security.
- Use roles when granting permissions to AWS services, including EC2 instances.
- Keep access keys secret and never share IAM user credentials or access keys.

## Shared Responsibility Model for IAM
- AWS is responsible for `the security of the cloud infrastructure`, including global network security and service compliance.
- Users are responsible for `managing IAM components` such as users, groups, roles, policies, and their monitoring.
- Enabling and enforcing Multi-Factor Authentication (MFA) is the user's responsibility, not AWS's.
- Users must regularly rotate keys, apply appropriate permissions using IAM tools, and review access patterns and permissions.

## IAM Summary
- IAM users should be mapped to actual physical users within your company.
- Users can be grouped, and policies attached to users or groups to define permissions.
- Roles can be created for AWS services like EC2 instances to assume identities.
- Security best practices include enabling multi-factor authentication and setting password policies.
- AWS services can be managed via CLI or SDK, with access keys for authentication.
- IAM usage can be audited using credentials reports and the IAM access advisor service.

## Quiz Section 4: IAM - Identity and Access Management

> Q: What is a proper definition of IAM Roles?
> 
> A: An IAM entity that defines a set of permissions for making AWS service requests, that will be used by AWS services

> Q: Which of the following is an IAM Security Tool?
> 
> A: IAM Credentials Report

> Q: Which answer is **INCORRECT** regarding IAM Users?
> 
> A: IAM Users access AWS with the root account credentials

> Q: Which of the following is an IAM best practice?
> 
> A: Don't use the root user account

> Q: What are IAM Policies?
> 
> A: JSON documents to define Users, Groups or Roles' persmissions

> Q: Under the shared responsibility model, what is the customer responsible for in IAM?
> 
> A: Assigning users proper IAM Policies

> Q: Which of the following statements is TRUE?
> 
> A: The AWS CLI can interact with AWS using commands in your command-line shell, while the AWS SDK can interact with AWS programmatically.

> Q: Which principle should you apply regarding IAM Permissions?
> 
> A: Grant least privilege

> Q: What should you do to increase your root account security?
> 
> A: Enable Multi-Factor Authentication (MFA)

# Section 5: EC2 - Elastic Compute Cloud

## EC2 Basics
- Amazon EC2 stands for `Elastic Compute Cloud` and provides Infrastructure as a Service on AWS.
- EC2 allows renting `virtual machines` called `instances` with customizable operating systems, CPU, RAM, storage, and networking.
- Bootstrapping EC2 instances is possible using User Data scripts that run once at first launch with root privileges.
- Various EC2 instance types exist to fit different application needs, with t2.micro included in the AWS free tier offering 750 hours per month.

## EC2 Instance Type Basics
- EC2 instances come in various types optimized for different workloads, including `general purpose`, `compute optimized`,` memory optimized`, and `storage optimized`.
- AWS uses a naming convention for instances: `the instance class (e.g., M for general purpose)`, `generation number (e.g., 5)`, and `size (e.g., 2xlarge)`.
- General purpose instances `balance` `compute`, `memory`, and `networking`, suitable for `diverse workloads` like web servers.
- Compute optimized instances (C series) are ideal for `CPU-intensive tasks` such as `batch processing`, `media transcoding`, and` machine learning`.
- Memory optimized instances (R series) excel at `processing large in-memory data sets`, useful for `databases` and `real-time big data processing`.
- Storage optimized instances (I, D, H1 series) are designed for `high-frequency data access on local storage`, `supporting OLTP systems` and `data warehousing`.
- The website `ec2instances.info` is a useful resource to compare instance specifications and costs.

## Security Groups & Classic port Overview
- `Security groups` act as firewalls for EC2 instances, controlling `inbound` and `outbound` traffic with allow rules only.
- Security groups can reference IP addresses or other security groups, enabling flexible and secure communication between instances.
- By default, `all inbound traffic is blocked`, and `all outbound traffic is allowed`.
- Important ports to know include 22 for SSH (Linux), 21 for FTP, 80 for HTTP, 443 for HTTPS, and 3389 for RDP (Windows).

- Security groups control inbound and outbound traffic to EC2 instances.
- Inbound rules specify allowed incoming connections, such as SSH on port 22 and HTTP on port 80.
- Timeouts when connecting to EC2 instances often indicate incorrect security group rules.
- Multiple security groups can be attached to an EC2 instance, and one security group can be attached to multiple instances.

## EC2 Instance Purchasing Options
- `On-demand` EC2 instances provide flexible, pay-per-use pricing ideal for short workloads.
- `Reserved instances` offer significant discounts for long-term commitments with options for flexibility via convertible reserved instances.
- `Savings plans` allow committing to a specific spend amount for discounts, providing flexibility across instance sizes and operating systems.
- `Spot instances` offer the highest discounts but can be interrupted, suitable for fault-tolerant workloads.
- `Dedicated hosts` and dedicated instances provide physical hardware isolation for compliance or licensing needs.
- `Capacity reservations` guarantee instance availability in a specific availability zone without discounts.

## Shared Responsibility Model for EC2
- AWS is responsible for the security of the physical data centers and infrastructure.
- Users are responsible for security within the cloud, including configuring security groups and managing their EC2 instances.
- Users must maintain their operating system patches, updates, and installed software on EC2 instances.
- Proper assignment of IAM roles and securing data on EC2 instances are critical user responsibilities.

## EC2 Summary
- EC2 instances are composed of an Amazon Machine Image (AMI) defining the operating system, instance size specifying CPU and RAM, storage, security groups as firewalls, and user data scripts for initialization.
- Security groups act as external firewalls to EC2 instances, controlling allowed ports and IP addresses.
- EC2 User Data scripts run at the first start of an instance to configure it, such as setting up a web server.
- SSH allows terminal access to EC2 instances on port 22, and EC2 instance roles enable instances to interact with IAM securely.
- Multiple EC2 purchasing options exist: `on-demand`, `spot instances`, `reserved instances (standard or convertible)`, `dedicated hosts`, and `dedicated instances`.

## Quiz Section 5: EC2 - Elastic Compute Cloud

> Q: Which EC2 Purchasing Option can provide the biggest discount, but is not suitable for critical jobs or databases
> 
> A: Spot Instances

> Q: Which network security tool can you use to control traffic in and out of EC2 Instances?
> 
> A: Security Groups

> Q: Under the Shared Responsibility Model, who is responsible for operating-system patches and updates on EC2 Instances?
> 
> A: The customer

> Q: How long can you reserve an EC2 Reserved Instance?
> 
> A: 1 or 3 years

> Q: A company would like to deploy a high-performance computing (HPC) application on EC2, Which EC2 instance type should it choose?
> 
> A: Compute Optimized

> Q: Which of the following is **NOT** an EC2 Instance Purchasing Option?
> 
> A: Connect Instances

> Q: Which EC2 Purchasing Option should you use for an application you plan on running on a server continuously for 1 year
> 
> A: Reserved Instances

