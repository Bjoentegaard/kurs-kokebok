# AWS Cloud Practitioner Essentials
[AWS Cloud Practitioner Essentials](https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7?parentId=Y4YASRJEVX)

## Module 1 - Introduction to the cloud
- `Cloud Computing` - On-demand delivery of IT resources over the internet with a Pay-as-you-go pricing
- `Cloud-based deployment:` Resources and applications are hosted entirely in the cloud and accessed over the internet.
- `On-premises deployment:` Resources and infrastructure are hosted and managed locally within the organization's data center.
- `Hybrid deployment`: A combination of on-premises and cloud environments, offering balance between control and scalability.
- `Six key benefits of cloud computing`
  - Trade fixed expense for variable expense
  - Benefit from massive economies of scale
  - Stop guessing capacity
  - Increase speed and agility
  - Stop spending money to run and maintain data centers
- `AWS Regions` - Physical locations around the world that contain groups (AZ) of data centers (Min 3)
- `Availability Zones (AZ)` - Consists of one or more data centers with redundant power, networking, and connectivity
- `Customer responsibilites` - Security IN the cloud (applications, data, access control)
- `Shared responsibilites` - Varies by service
- `AWS Responsibilities` - Security OF the cloud (hardware, infrastructure)

### Recap

In this section of the training, you learned fundamental concepts of cloud computing. You explored the definition and benefits of the cloud, and you were introduced to AWS Global Infrastructure. You also explored the AWS Shared Responsibility Model to clarify the division of responsibilities between AWS and customers.

## Module 2 - Compute in the cloud
- `Compute in the cloud` - Compute in the cloud means creating virtual machines with a cloud provider to run applications and tasks over the internet
- `Elastic Compute Cloud (EC2)` - Virtual Server/Machine in the AWS Cloud that provides on-demand, scalable computing capacity
- `EC2 Instances types`
  - General purpose - Balanced resources 
  - Compute optimized - Compute intensive tasks
  - Memory optimized - Provide fast performance for memory-heavy workloads
  - Accelerated computing - Uses HW acceleators to efficiently handle tasks
  - Storage optimized - Designed for workloads that require high performance for lacally stored data
- `AWS Management Console` - Web interface for managing AWS services
- `AWS Command Line Interface (CLI)` - Managing multiple AWS services directly from the command line.
- `AWS Software Development Kit (SDK)` - Simplifies integrating AWS services into your applications by providing APIs for various programming languages.
- `Amazon Machine Images (AMI)` - AMIs are pre-built VM that have the basic components for what is needed to start an instance.
  - It provides a consistent image to launch new instances.
  - With an _unmanaged_ service like EC2, you are responsible for configuring and managing security.
- `EC2 Pricing`
  - On-Demand Instances - Pay only for the compute capacity you consume with no upfront payment or long-term commitments required.
  - Reserved Instances - Get a saving of up to 75 percent by committing to a 1-year or 3-year term for predictable workloads using specific instance families and AWS Regions
  - Spot Instances - Bid on a spare compute capacity at up to 90 percent of the On-demand price, with the flexibility to be interrupted when AWS reclaims the instance
  - Savings Plans - Save up to 72 percent across a variety of instance types and services by commiting to a consistent usage level for 1 or 3 year.
  - Dedicated Hosts - Reserve an entire physical server for your exclusive use. This option offers full control and is ideal for workloads with strict security or licensing needs
  - Dedicated Instances - Pay for instances running on HW dedicated solely to your account. This option provides isolation from other AWS customers.
- `Cost optimization`
  - Saving Plans - Good for Predictable workloads
  - Capacity Reservation - Good for Critical workloads with strict capacity requirements
  - Reserved Instance flexibility - Good gor Steady-state workloads with predictable usage
- `Scalability` - Adding Resources
  - Scaling Up (Vertical) - Adding more power to existing machines
  - Scaling Out (Horizontal) - Adding more machines
- `Elasticity` - Abilitiy to automatically scale resources up or down in response to real-time demand
- `EC2 Auto Scaling` - automatically adjusts the number of EC2 instances based on changes in application demand, providing better availability. It offers two approaches. 
  - Dynamic scaling adjusts in real time to fluctuations in demand. 
  - Predictive scaling preemptively schedules the right number of instances based on anticipated demand.
- `Auto Scaling Group` - Configured with three key settings (**min, desired and max** capacity)
  -   - A load balancer serves as the single point of contact for all incoming web traffic to an Auto Scaling group.
- `Elastic Load Balancing (ELB)` - automatically distributes incoming application traffic across multiple resources, such as EC2 instances, to optimize performance and reliability.
  - Regional application
- `ELB Benefits`
  - Efficient traffic distribution - ELB evenly distributes traffic across EC2 instances, preventing overload on any single instance and optimizing resource utilization.
  - Automatic Scaling - ELB scales with traffic and automatically adjusts to changes in demand for a seamless operation as backend instances are added or removed.
  - Simplified management - ELB decouples front-end and backend tiers and reduces manual synchronization. It also handles maintenance, updates, and failover to ease operational overhead.
- `ELB Routing Methods`
  - Round Robin - Distributes traffic evenly across all available servers in a cyclic manner.
  - Least Connections - Routes traffic to the server with the fewest active connections, maintaining a balanced load.
  - Ip Hash - Uses the client’s IP address to consistently route traffic to the same server.
  - Least Response Time - Directs traffic to the server with the fastest response time, minimizing latency.
- `Monolitich Applications` - Applications consist of multiple components that work together to transmit data, fulfill requests, and keep the application running smoothly.
- `Microservices Applications` - Application components are loosely coupled. The communication between components remains intact, and the failure of a single component does not impact the entire system.
- `EventBridge` - A serverless service that helps connect different parts of an application using events, helping to build scalable, event-driven systems. 
  - With EventBridge, you route events from sources like custom apps, AWS services, and third-party software to other applications. 
- `Amazon Simple Queue Service (Amazon SQS)` - A message queuing service that facilitates reliable communication between software components.
  - It can send, store, and receive messages at any scale, making sure messages are not lost and that other services don't need to be available for processing
- `Payload` - Data contained within a message
- `SQS queues` - Where messages are placed until they are processed
- `Amazon Simple Notification Service (Amazon SNS)` - A publish-subscribe service that publishers use to send messages to subscribers through SNS topics.
- `SNS topic` - A channel for messages to be delivered

### Recap

In these lessons about compute, you learned how Amazon EC2 and cloud resources help scale applications. You gained knowledge of EC2 instance types, pricing options, and how to choose the best instance types for your unique business needs. You also became familiar with using AWS tools and services like Elastic Load Balancing, Amazon EC2 Auto Scaling, Amazon SQS, and Amazon SNS to manage traffic and communication.

## Module 3 - Exploring Compute Service
- `Unmanaged services` - (EX: EC2) AWS takes care of the underlying physical infrastructure, but you're responsible for setting up, securing, and maintaining the operating system, network configurations, and applications on your instances.
- `Managed services` - Managed services, on the other hand, reduce the amount of infrastructure you need to manage.
- `Fully-managed services` - like serverless ones—take abstraction even further, eliminating the need to provision or manage any servers at all.
- `Serveless` - You cannot see or access the underlaying infrastructure
- `Lambda` - a serverless compute service that runs code in response to events without the need to provision or manage servers
  - Maximum duration is 15 minutes
- `How Lambda works`
  - Upload code to Lambda
  - Set code to trigger from an event source 
  - Run code when triggered 
  - Pay only for the compute time used 
- `Containers` - provide a reliable way to package your application’s code and dependencies into a single, portable unit, making them ideal for workflows that require high security, reliability, and scalability.
  - Faster and lighter than virtual machines (VMs) because they share the host computer’s operating system.
- `VMs` use a hypervisor to run full, separate operating systems, which makes them less resource-efficient and have longer startup times.
- `Amazon Elastic Container Service (ECS)` - Scalable container orchestration service for running and managing containers on AWS, like Docker containers.
  - Streamlined and integrated
  - Define some parameters
  - Fully managed service
- `Amazon Elastic Kubernetes Service (EKS)` - A fully managed service for running Kubernetes on AWS. It simplifies deploying, managing, and scaling containerized applications using open-source Kubernetes.
  - Open source platform
  - More complex
  - More control and flexibility
- `Amazon Elastic Container Registry (ECR)` - Where you can store, manage, and deploy container images. It supports container images that follow the Open Container Initiative (OCI) standards.
  - Fully managed Docker registry
  - Stores container images
- `AWS Fargate` - a serverless compute engine for containers. It works with both Amazon ECS and Amazon EKS. 
  - Fargate is a container hosting platform, unlike Amazon ECS and Amazon EKS, which are both container orchestration services.
- `AWS Elastic Beanstalk` - A fully managed service that streamlines the deployment, management, and scaling of web applications.
  - Developers can upload their code, and Elastic Beanstalk automatically handles the provisioning of infrastructure, scaling, load balancing, and application health monitoring.
  - _Good for_: Deploying and managing web applications, RESTful APIs, mobile backend services, and microservices architectures, with automated scaling and simplified infrastructure management
- `AWS Batch` - A fully managed service that you can use to run batch computing workloads on AWS.
  - It automatically schedules, manages, and scales compute resources for batch jobs, optimizing resource allocation based on job requirements.
  - _Good for_: Processing large-scale, parallel workloads in areas like scientific computing, financial risk analysis, media transcoding, big data processing, machine learning training, and genomics research
- `Amazon Lightsail` - A cloud service offering virtual private servers (VPSs), storage, databases, and networking at a predictable monthly price.
  - It’s ideal for small businesses, basic workloads, and developers seeking a straightforward AWS experience without the complexity of the full AWS Management Console.
  - _Good for_: Basic web applications, low-traffic websites, development and testing environments, small business websites, blogs, and learning cloud services
- `AWS Outposts Family`- a fully managed hybrid cloud solution that extends AWS infrastructure and services to on-premises data centers.
  - It provides a consistent experience between on premises and the AWS Cloud, offering compute, storage, and networking components.
  - _Good for_: Low-latency applications, data processing in remote locations, migrating and modernizing legacy applications, and meeting regulatory compliance or data residency requirements

### Recap 
This module gave you a practical understanding of AWS compute services, so you can choose the right tools for your applications. You learned when to use fully managed options like Lambda or Fargate, and when full control with Amazon EC2 made sense. You explored how containers solve deployment consistency issues and how AWS services, like Amazon ECS and Amazon EKS, simplify managing and scaling containerized applications. You also discovered services like Elastic Beanstalk, AWS Batch, Lightsail, and Outposts, and how each supported specific use cases, from basic web hosting to large-scale batch processing or hybrid cloud environments.

## Module 4 - Going Global
- `AWS edge locations` - Edge locations cache items like images, videos, and other resources, so that users can access the content they need with lower latency.
  - Edge locations offer multiple services to run closer to end users, including AWS networking services like Amazon CloudFront
- `CloudFormation` - A service that lets you define and provision AWS infrastructure as code using templates.
- `Infrastructure as code (IAC)` - the practice of managing and provisioning infrastructure using code and automation instead of manual processes.
- `Key consideration when choosing Regions`
  1. Compliance - Different geographical locations have varying regulatory requirements and data protection laws that organizations must follow.
  2. Proximity - Regions closer to your user base minimize data travel time, which reduces latency and enhances application responsiveness.
  3. Features - AWS is constantly expanding features and services to multiple locations, but not all Regions contain all AWS offerings.
  4. Pricing - Some Regions have lower operational costs than others. These operational costs can impact the overall expenses for hosting applications and services.
- `Multi-Region and Multi-AZ` - deploying your cloud resources to multiple Regions and multiple Availability Zones
  - High availability: High availability refers to the capability of a system to operate continuously without failing
  - Agility: Agility refers to the ability to quickly adapt to changing requirements or market conditions.
  - Elasticity: Elasticity refers to the ability of a system to scale resources up or down automatically in response to changes in demand.
- `Amazon Cloudfront` - a content delivery network 
- `Content Delivery Network` - A distributed network of servers that delivers content to users from the closest location for faster performance and lower latency.
- `Route 53` - Domain name system (DNS)
- `Outpost` - Make it possible to run AWS services on-prem
- `Key elements of AWS Global Infrastructure`
  - Regions - Each Region consists of multiple, isolated locations known as Availability Zones. Each Region has three or more Availability Zones.
  - Availability Zone - Are distinct locations within a Region, each designed as an independent zone with its own power, networking, and connectivity.
  - Edge Locations - are strategically placed sites around the world that cache content to deliver data, video, and applications with lower latency and higher transfer speeds.

### Recap
In this section of the training, you learned more about the AWS Global Infrastructure. You learned about choosing a Region, the value of edge locations, and how to use services such as CloudFormation to streamline and automate deployment.

## Module 5 - Networking
- `Networking` - The term networking refers to interconnected devices that can exchange data and resources.
- `Amazon Virutal Private Cloud (Amazon VPC)` - Lets you provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define.
- `Subnet` - Is a section of a VPC in which you can group resources based on security or operational needs.
  - Private subnet - Contain resources that should be accessible only through your private network, such as a database that contains customers’ personal information and order histories.
  - Public subnet - Contain resources that need to be accessible by the public, such as an online store’s website.
- `Architectural diagrams` - A schematic or map of your network in the AWS Cloud
  - A picture is worth a thousand words. With a quick glance, you can see if the network was built for redundancy, security, and even scalability. It can also serve as a blueprint so you don't forget important connections when building your solutions.
- `Internet gateway` - A doorway that is open to the public.
- `Virtual private gateway` -  it allows you to create a VPN connection between a private network, like your on-premises data center or internal corporate network to your VPC.
- `AWS Direct Connect` - lets you establish a completely private, dedicated fiber connection from your data center to AWS. It ensures both security and consistent high performance.
- `Difference between similar network components`
  - Virtual Private Cloud (VPC) - Is used to establish boundaries around your AWS resources.
  - Virtual private gateway - Allows protected internet traffic to enter into the VPC.
  - Virtual private network (VPN) connection - A VPN encrypts your internet traffic, helping protect it from anyone who might try to intercept or monitor it.
- `AWS Client VPN` - Is a networking service you can use to connect your remote workers and on-premises networks to the cloud. 
  - It is a fully managed, elastic VPN service that automatically scales up or down based on user demand.
  - Benefits: AWS Client VPN provides advanced authentication, remote access. It is elastic and fully managed. 
  - Use case: It can be used to quickly scale remote-worker access.
- `AWS Site-to-Site VPN` - Creates a secure connection between your data center or branch offices and your AWS Cloud resources.
  - No dedicated hardware link (unlike AWS Direct Connect), which makes it cost-effective.
  - Benefits: Site-to-Site VPN provides high availability, secure and private sessions, and accelerates applications. 
  - Use cases: It can be used for application migration and secure communication between remote locations.
- `AWS PrivateLink` - Is a highly available, scalable technology that you can use to privately connect your VPC to services and resources as if they were in your VPC.
  - Benefits: AWS PrivateLink helps you secure your traffic and connect with simplified management rules.
  - Use case: It is used for connecting your clients in your VPC to resources, other VPCs, and endpoints.
  - _Traffic jams are possible because you’re using the same connection as other clients._
- `AWS Direct Connect` - Is a service that makes it possible for you to establish a dedicated private connection between your network and VPC in the AWS Cloud.
  - Benefits: AWS Direct Connect reduces network costs and increases amount of bandwidth.
  - Latency-sensitive applications - Direct Connect bypasses the internet and provides a consistent, low-latency network experience.
  - Large-scale data migration or transfer - Direct Connect helps ensure smooth and reliable data transfers at massive scale for real-time analysis, rapid data backup, or broadcast media processing.
  - Hybrid cloud architectures - You can use Direct Connect to link your AWS and on-premises networks to build applications that span environments without compromising performance.
- `Additional gateway services`
  - AWS Transit Gateway - Is used to connect your Amazon VPCs and on-premises networks through a central hub.
  - Network Address Translation (NAT) Gateway - You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services can't initiate a connection with those instances.
  - Amazon API (Application Programming Interface) Gateway - An API defines how different software systems can interact and communicate with each other. The Amazon API Gateway is an AWS service for creating, publishing, maintaining, monitoring, and securing APIs at any scale.
- `Security Groups` - Control inbound and outbound traffic at the resource level
  - Security groups perform stateful packet filtering. They remember previous decisions made for incoming packets.
  - By default, a security group denies all inbound traffic and allows all outbound traffic.
  - _Note_: If you have multiple Amazon EC2 instances within the same VPC, you can associate them with the same security group or use different security groups for each instance.
  - **Feature:**
    - Scope - Instance level (attached to EC2 instances)
    - State - Stafeul (remember state)
    - Rule types - Only allow type rules
    - Return traffic - Return traffic is automatically allowed if inbound traffic is allowed
    - Uses - Fine-grained control of traffic for individual EC2 instances
- `Network Access Control Lists (ACL)` - Is a virtual firewall that controls inbound and outbound traffic at the subnet level.
  - ACLs perform stateless packet filtering. They remember nothing and check packets that cross the subnet border each way: inbound and outbound.
  - Default network ACL in each AWS account allows all inbound/outbound traffic by default; you can modify or create custom ACLs for your VPC.
  - **Feature:**
    - Scope - Subnet level (associated with subnets)
    - State - Stateless (don't remember state)
    - Both allow and deny type rules
    - Return traffic must be implicitly allowed in both directions
    - Broad control of traffic in and out of subnets
- `AWS Shared Responsibility Model` -  Network ACLs and security groups are the customers responsibility
- `Domain Name System (DNS)` - DNS resolution is the process of translating a domain name to an IP address and vice versa.
- `Amazon route 53` - Route 53 is a highly available and scalable cloud DNS service.
  - Latency-based routing
  - Geolocation DNS
  - Weighted round-robin
- `Amazon CloudFront` - CloudFront is a CDN service that delivers your content with low latency and high speeds.
- `AWS Global Accelerator` - Global Accelerator is a service that uses the AWS global network to improve application availability, performance, and security.

### Recap 
In this networking module, you identified core networking components and how they connect in the AWS Cloud. We covered the basics of a VPC, the way that you isolate your workload in AWS, gateways, network ACLs, and security groups. You also reviewed ways to connect to AWS through a VPN and Direct Connect, secure connections that are either encrypted over the public internet or exclusive connections used by you and you alone.

You also learned about AWS edge locations, Route 53 for DNS, and CloudFront to cache content closer to consumers.

## Module 6: Storage
- `Block storage` - Provides persistent, low-latency block-level storage volumes that attach to EC2 instances like physical hard drives.
  - `Amazon EC2 instance store`- An unmanaged non-persistent, high-performance block storage directly attached to EC2 instances for temporary data.
    - Is best for temporary memory-based storage needs like buffers, caches, and scratch data. It is not recommended for applications that require data retention.
    - Automatically available storage - Instance store volumes are temporary, high‑performance block storage physically attached to the host, included at no extra cost on many EC2 instance types and erased when the instance stops.
    - Cost effective - Is included in the instance price, making it ideal for temporary data like caches or buffers and helping reduce costs for workloads that don’t need persistent storage.´
    - EC2 instance store provides ultra‑low latency and high I/O performance by being directly attached to the host server, making it ideal for temporary fast‑processing data.
  - `Amazon Elastic Block Store (EBS)` - A managed service that provides persistent block storage volumes for EC2 instances, offering various types for different workloads
    - EBS volumes act like external hard drives, offering consistent and low-latency performance for workloads like databases and file systems.
    - Use cases - Some practical use cases of Amazon EBS include database hosting, backup storage for applications, and rapid deployment of development environments using volume snapshots.
    - Data migration - EBS volumes can be easily migrated between Availability Zones using snapshots. The snapshots provide a simple way to move data across regions or create copies.
    - Instance type changes - EBS volumes are separate from EC2 instances, so you can easily attach them to other instance types and change sizes without losing data.
    - Disaster recovery - EBS snapshots offer reliable, automated backups that can be restored across regions for fast recovery during emergencies.
    - Cost optimization - EBS volumes can be resized or changed to different types without downtime, letting you match storage to usage needs.
    - Performance tuning - Amazon EBS provides multiple volume types and adjustable performance to suit varying workload and IOPS requirements.
- `Object storage` - is a data storage architecture that manages data as objects in a flat address space. 
  - It offers unlimited scalability so you can store vast amounts of unstructured data without worrying about capacity constraints.
  - Object storage provides enhanced metadata capabilities to provide more efficient data management, search, and analytics across massive datasets.
  - **`Amazon Simple Storage Service (S3)` - A fully managed scalable object storage service for storing and retrieving any amount of data from anywhere.**
    - Store data as objects -> Store object in buckets
    - Upload a maximum size of 5 TB
    - Create multiple buckets
    - Offers features like versioning, lifecycle management, and various storage classes to optimize costs.
    - Each object typically includes the data itself, metadata, and a unique identifier, or key.
    - Each Amazon S3 object is uniquely identified within a bucket by its key, which is essentially its file name.
    - Objects also have properties like version ID, access control information, and user-defined metadata.
- `File storage` - file storage services provide shared file systems accessible over networks, so multiple users and applications can access the same data simultaneously.
  - They offer scalability and flexibility so you can expand storage capacity as needs grow without managing physical infrastructure.
  - `Amazon Elastic File System (EFS)` - A fully managed, scalable NFS file system for use with AWS Cloud services and on-premises resources.
    - Multiple instances reading and writing simultaneously
    - EFS is designed to support a wide variety of workloads and can be accessed by multiple EC2 instances simultaneously.
    - Benefits:
      - Multi-AZ redundancy - automatically replicates data across multiple Availability Zones in a region for high availability.
      - Shared access - supports thousands of concurrent NFS connections, so multiple EC2 instances can access the same file system simultaneously.
      - Elastic storage - automatically grows and shrinks as you add and remove files, with no need to provision or manage storage capacity.
  - `Amazon FSx` - A fully managed file storage services for popular file systems like Windows, Lustre, and NetApp ONTAP.
    - Benefits:
      - File system integration - Supports industry-standard file system protocols, allowing convenient integration with your existing applications, workflows, and development tools.
      - Managed infrastructure - Reduces the complexity of managing infrastructure while delivering the features and capabilities of traditional file systems.
      - Scalable storage - Adjusts resources dynamically, eliminating the need for complex capacity planning and manual infrastructure management.
      - Cost effective - has a pricing model and automated tiering options that optimize costs by charging only for used storage and moving infrequently accessed data to lower-cost tiers.
- `NFS` - Network File System
- `AWS Storage Gateway` - A fully managed, hybrid-cloud storage service that provides on-premises access to virtually unlimited cloud storage.
- `AWS Elastic Disaster Recovery` - A fully managed service that streamlines the recovery of your physical, virtual, and cloud-based servers into AWS.
- `Amazon EBS Snapshots` - Point-in-time backups of EBS volume. They can be used for disaster recovery, data migration, volume resizing, and for creating consistent backups of production workloads.
  - EBS snapshots are incremental, so they only save the blocks on the volume that have changed after your most recent snapshot.
  - Can be used to create multiple new volumes, and new volumes created from a snapshot are an exact copy of the original volume at the time the snapshot was taken.
  - Snapshots of EBS volumes are stored redundantly in multiple Availability Zones using Amazon S3.
  - Benefits
    - Data protection and recovery - Enable fast data recovery from corruption, accidental deletion, or system failures using point-in-time backups.
    - Operational flexibility - Enable operations like cross-Region data migration, volume resizing, volume cloning, and sharing data across AWS accounts.
    - Cost effective - Use incremental backup technology, storing only changed blocks after the initial backup, reducing storage costs and backup time.
- `Amazon Data Lifecycle Manager` - You can automate the creation, retention, and deletion of EBS snapshots using Amazon Data Lifecycle Manager.
  - Schedule automatic snapshot creation
  - Set retention policies
  - Manage snapshot lifecycle
  - Apply consistent backup policies
- `AWS S3 Benefits`
  - Virtually unlimited storage - no fixed storage limit, scaling automatically to accommodate any amount of data you need to store.
  - Object lifecycle management - lifecycle policies automatically move objects between storage classes based on your defined rules, optimizing costs over time.
  - Broad range of use cases - supports a wide range of use cases for both cloud-based applications and traditional on-premises workloads. Amazon S3 is commonly used for content distribution, hosting static websites, and delivering media files.
- `S3 Security and privacy management`
  - Everything you store in Amazon S3 is private by default
  - **Bucket policies** - Resource-based policies that can only be attached to S3 buckets. An S3 bucket policy specifies which actions are allowed or denied on the bucket, in addition to every object in that bucket.
  - **Identity-based policies** - Permissions that control what actions users, groups, or roles can perform on S3 resources are attach directly to identities rather than to the S3 resources themselves
  - **Encryption** - Provides encryption capabilities to protect data both at rest and in transit.
- `Amazon S3 storage classes and uses cases`
  1. `S3 Standard` - General-purpose storage for cloud applications, dynamic websites, content distribution, mobile and gaming applications, and big data analytics
  2. `S3 Intelligent-Tiering` - This tier is useful if your data has unknown or changing access patterns. Stores objects in three tiers: a frequent, an infrequent, and an archive instant access tier.
  3. `S3 Standard Infrequent Access (Standard-IA)` - For infrequently accessed data that still needs fast retrieval. Provides the same durability, throughput, and low latency as S3 Standard, but at a lower storage cost with a retrieval fee—ideal for long-term backups and disaster recovery.
  4. `S3 One Zone Infrequent Acces (One Zone-IA)` - Stores data in a single Availability Zone, reducing costs compared to S3 Standard-IA, which uses three zones.
  5. `S3 Express One Zone` - It was purpose-built to deliver consistent single-digit millisecond data access for your most frequently accessed data and latency-sensitive applications. Delivers data access speed up to 10x faster and request costs up to 80% lower than S3 Standard.
  6. `S3 Glacier Instant Retrieval` - Archiving data that is rarely accessed and requires millisecond retrieval.
  7. `S3 Glacier Flexible Retrieval` - Offers low-cost storage for archived data that is accessed 1–2 times per year. With S3 Glacier Flexible Retrieval, your data can be accessed in as little as 1–5 minutes using an expedited retrieval.
  8. `S3 Glacier Deep Archive` - is S3’s lowest-cost storage class, built for long-term retention (7–10+ years) and regulatory compliance. Ideal for rarely accessed data—retrieval takes about 12 hours—such as archives in finance, healthcare, or public sectors.
  9. `S3 Outpost` - Delivers object storage to your on-premises AWS Outposts environment using Amazon S3 APIs and features, and serves workloads with local data residency requirements.
- `S3 Lifecycle` - Automating object storage tier config
  - _Transition actions_: define when objects should transition to another storage class.
  - _Expiration actions_: define when objects expire and should be permanently deleted.
  - Use cases
    - _Periodic logs_: If you upload periodic logs to a bucket, your application might need them for a week or a month. After that, you might want to delete them.
    - _Data that changes in access frequency_: Some documents are frequently accessed for a limited period of time. After that, they are infrequently accessed. At some point, you might not need real-time access to them.
- `Amazon EFS storage classes`
  - Standard Storage Classes - Offer Multi-AZ resilience and the highest levels of durability and availability.
  - One Zone Storage Classes - Provide additional savings by saving your data in a single Availability Zone.
  - Archive Storage Class - Is cost-optimized for data that is accessed only a few times a year or less and that does not need the sub-millisecond latencies of EFS Standard.
- `EFS Lifecycle` - You can create lifecycle policies that determine when and how files transition between different storage tiers.
  - Transition to IA - This policy instructs lifecycle management when to move files into the Infrequent Access storage, which is cost-optimized for data that is accessed only a few times each quarter.
  - Transition to Archive - This policy instructs lifecycle management when to move files into the Archive storage class, which is cost-optimized for data that is accessed only a few times each year or less.
  - Transition to Standard - This policy instructs lifecycle management whether to transition files out of IA or Archive and back into Standard storage when the files are accessed in the IA or Archive storage.
- `Amazon FSx file systems`
  - Windows File Server
  - NetApp ONTAP
  - OpenZFS
  - Lustre
- `AWS Storage Gateway` - Is a hybrid cloud storage service that makes it possible to seamlessly integrate on-premises environments with AWS Cloud storage.
  - Benefits
    - Seamless integration
    - Improved data management
    - Local caching
    - Cost optimization
- `Gateway types` - offers three distinct types of gateways to meet different hybrid storage needs
  - Amazon S3 File Gateway - Bridges your local environment with Amazon S3. It provides on-premises applications with access to virtually unlimited cloud storage through familiar file protocols.
  - Volume Gateway - Lets you create virtual storage volumes with local access, bridging on-premises infrastructure and AWS Cloud by presenting cloud data as iSCSI volumes.
  - Tape Gateway - Makes it possible to replace physical tape infrastructure with virtual tape capabilities while benefitting from the durability and scalability of AWS Cloud storage.
- `Elastic Disaster Recovery` - replicates critical workloads to AWS with minimal downtime. Your servers' block-level data is continuously replicated to AWS, making it ideal for uses that require robust disaster recovery solutions.
  - Supports both physical and virtual servers
  - Benefits:
    - Business resilience - Maintain business operations with continuous block-level data replication and the ability to recover workloads within minutes during disruptions.
    - Streamlined disaster recovery - Automate disaster recovery processes through an intuitive console, reducing complex manual configurations and minimizing the risk of human error.
    - Cost optimization - Eliminate expensive secondary data centers and pay only for what you use, with minimal upfront investment and no standby infrastructure costs.
  - Use cases
    - Healthcare data protection
    - Financial services continuity
    - Manufacturing operations recovery

### Recap
In this module, you learned about the diverse storage options available in AWS, starting with block storage services like Amazon EC2 Instance Store and Amazon EBS. You learned how Amazon EBS provides persistent block storage volumes for EC2 instances, while EC2 instance store offers temporary block-level storage. You learned how to use EBS snapshots and AWS Data Lifecycle Manager for automated backup management and data protection.

You then examined Amazon S3, a highly scalable object storage service that serves as a foundation for many cloud storage needs. You delved into file storage solutions, including Amazon Elastic File System (Amazon EFS) for Linux-based workloads and Amazon FSx for Windows, Lustre, OpenZFS, and NetAPP ONTAP file systems. Finally, you learned about AWS Storage Gateway, which bridges on-premises environments with AWS storage services to enable hybrid cloud storage architectures.

## Module 7: Databases
- `Relational Databases` - store data in a way that relates it to other pieces of data, and they use structured query language, or SQL, to manage and query data.
- `Amazon Relational Database Service (Amazons RDS)` - Managed relational database service that handles routine database tasks such as backups, patching, and hardware provisioning.
  - Supports multiple database instance class types that optimize for memory, performance, or input/output (I/O).
  - Supports different database engines, including Amazon Aurora, MySQL, PostgreSQL, Microsoft SQL Server, MariaDB, and Oracle Database.
  - Benefits:
    - Cost optimization - Eliminates the high upfront costs of purchasing and maintaining database hardware infrastructure. You only pay for the compute and storage resources that you consume through a flexible pay-as-you-go model.
    - Multi-AZ deployment - Improves database reliability through Multi-AZ deployments. It automatically replicates data to a standby instance in a different Availability Zone.
    - Perfomance optimization - enhances database performance through automated management of resource allocation, monitoring, and optimization tasks.
    - Security controls - enhances database security through multiple layers of protection, including VPC isolation as well as encryption at rest and in transit.
- `AWS Database Migration Service (AWS DMS)` - Helps you migrate databases quickly and securely to AWS with minimal downtime by continuously replicating data during the migration process.
- `Amazon Aurora` - Managed relational database designed to help reduce unnecessary I/O operations. It's compatible with MySQL and PostgreSQL, provides high performance and availability, and automatically scales alongside your workloads.
  - High performance and availability - Delivers up to five times the throughput of standard MySQL and three times the throughput of PostgreSQL. It uses a distributed storage system across multiple nodes to provide high performance and availability.
  - Automated storage and backup management - Automatically grows storage from 10 GB to 128 TB based on your actual data usage, which eliminates guesswork in capacity planning.
  - Advanced replication and fault tolerance - Replicates data across three Availability Zones with six copies of data, and provides 99.99% availability. It automatically detects database failures and redirects traffic to healthy replicas without data loss.
- `Querying Relation Data` - Involves retrieving, manipulating, and managing information stored in relational databases.
  - MySQL
  - PostgreSQL
  - Microsoft SQL Server
- `Structured Query Language (SQL)` - Is a programming language for storing and processing information in a relational database
- `NoSQL databases` - are sometimes referred to as non-relational databases. Instead of row and column relationships, NoSQL databases build a structure for the data that they contain using key-value pairs instead
  - With key-value pairs, data is organized into items identified by unique keys.
- `Amazon DynamoDB` - is a fully managed NoSQL database service that provides fast and predictable performance for both document and key-value data structures.
  - Data = items = set of attributes
  - Attribute = name + value
  - Add/remove attribute any time
  - Benefits:
    - Scalability with provisioned capacity - Automatically scales throughput up or down based on actual usage, which ensures consistent performance without manual intervention.
    - Consistent high perfomance - Delivers single-digit millisecond response times at any scale, which makes it ideal for high-performance applications.
    - High availability and durability - Delivers 99.999% data availability by replicating data across three distinct facilities within each AWS Region.
    - Data encryption - Offers comprehensive encryption capabilities to protect information both at rest and in transit. All data is automatically encrypted behind the scenes before being written to the storage layer.
- `In-memory caches` - Is a high-speed storage layer that temporarily stores frequently accessed data in a computer's main memory, or RAM.
- `Amazon ElastiCache` - Is a fully managed in-memory caching service that was built to help reduce the complexity of administering in-memory caching systems.
  - It automatically detects and replaces failed nodes, which makes it ideal for applications that need consistent high performance.
  - Benefits:
    - High performance for Redis, Valey, or Memchached instances - simplifies deploying and managing in-memory caches with automated provisioning, patching, monitoring, and seamless scalability.
    - High availability - Provides high availability by constantly monitoring primary nodes for potential failures.
    - Replication across multiple AZ - Enables automatic replication across multiple Availability Zones to protect against infrastructure failures.
    - Data encryption - Supports data encryption mechanisms to safeguard sensitive information throughout its lifecycle. 
- `There is no one-size-fits-all database for all purposes`
- `Amazon DocumentDB` - is fully managed service designed to handle semistructured data, which is information that doesn't conform to rigid relational schemas.
  - is a MongoDB-compatible database, so it manages JSON-like documents with dynamic schemas.
  - is perfect for applications requiring frequent schema changes and document-oriented data. Unlike relational databases or nonrelational databases, you can quickly iterate without relying on predefined schemas.
  - Use cases:
    - Content management systems
    - Catalog
    - Inventory management, and user profile and personalization systems.
  - Benefits:
    - MongoDB compability - Is fully compatible with MongoDB workloads and supports MongoDB APIs, drivers, and tools.
    - Performance and scalability - Automatically scales storage up to 64 TB in 10 GB increments based on your application needs.
    - Increased read throughput - Improves read throughput for high-volume applications by creating up to 15 replica instances that share underlying storage.
- `AWS Backup` - Streamlines data protection across various AWS resources and on-premises deployments by providing a single dashboard for monitoring and managing backups.
  - It eliminates the complexity of managing multiple backup strategies by supporting multiple storage types, including Amazon EBS volumes, Amazon EFS file systems, and various databases.
  - Benefits:
    - Centralized backup management - Provides a single dashboard to manage backups across multiple AWS services and accounts.
    - Cross-region backup redundancy - Enables automatic replication of backup data across different AWS Regions for disaster recovery purposes.
    - Streamlined regulatory compliance - Maintains detailed audit logs and reports to demonstrate compliance with regulatory requirements.
- `Amazon Neptune` - is a fully managed, purpose-built graph database service that manages highly connected data sets, like those used in social networking applications.
  - It excels at understanding complex relationships that are difficult to identify in traditional relational databases like user connections, friend networks, and interaction patterns.
  - Benefits:
    - Purpose-built for complex relationships - It supports both property graph and resource description framework, or RDF, models making it ideal for relationship mapping and pattern matching applications.
    - High performance and scalability - Delivers consistent performance at scale, processing billions of relationships in milliseconds. It automatically grows storage up to 64 TB based on your application needs.

### Recap
In this module, we explored the managed relational database capabilities of Amazon RDS and Amazon Aurora. You learned how AWS DMS facilitates seamless database migrations, and DynamoDB provides insights into NoSQL database solutions for scalable applications.

We covered the in-memory caching capabilities of ElastiCache and the MongoDB-compatible document database features of Amazon DocumentDB. We examined the comprehensive data protection strategy across AWS services offered by AWS Backup. And finally, we concluded with the powerful graph database capabilities of Neptune for complex relationship queries.

## Module 8 - AI/ML and Data Analytics
- `Artificial Intelligence (AI)` - A broad field focused on the development of intelligent computer systems capable of performing humanlike tasks.
- `Machine learning (ML)` - is a type of AI for training machines to perform complex tasks without explicit instructions.
  - Machine learning training finds the patterns hidden in vast amounts of historical data to produce an ML model.
- `Common ML business use cases` - ML models power the Amazon.com e-commerce recommendations engine. But, ML can solve for lots of other business use cases, such as the following:
  - Predict trends - such as future stock prices.
  - Make decisions - like routing callers to the right department
  - Detect anomalies - such as bank fraud.
- `AWS AI/ML solutions` - stack is composed of the following three tiers of solutions:
  - AI services - pre-built models that are already trained to perform specific functions
  - ML services - a more customized approach with Amazon SageMaker AI where you build, train, and deploy your own ML models with fully managed infrastructure.
  - ML frameworks and infrastructure - a completely custom approach to building models using purpose-built chips that integrate with popular ML frameworks.
- `Tier 1: Pre-built AWS AI services` - The AWS AI services tier is made up of pre-built models that are already trained to perform specific functions
  - These managed services help you quickly address diverse business needs across three groups of AWS AI services.
    - Language services - are great for when you need to interpret text or speech and transform it into something meaningful.
      - `Amazon Comprehend` - uses natural language processing to extract key insights from documents.
        - Use cases: Content classification, customer sentiment analysis, and compliance monitoring
      - `Amazon Polly` - converts text into lifelike speech. It supports multiple languages, different genders, and a variety of accents.
        - Use cases: Virtual assistants, e-learning applications, and accessibility enhancements for visually impaired users
      - `Amazon Transcribe` - converts speech into text. It supports multiple languages and offers features such as speaker identification, custom vocabulary, and real-time transcription.
        - Use Cases: Customer call transcription, automated subtitling, and metadata generation for media content.
      - `Amazon Translate` - is a text translation service. This service is ideal for global communication because it supports real-time and batch text translation across multiple languages.
        - Use cases: Document translation and multi-language application integrations
    - Computer vision and search services - ideal for answering questions and gathering insights from various types of content sources such as documents, images, videos, and more.
      - `Amazon Kendra` - uses natural language processing to search for answers within large amounts of enterprise content.
        - Use cases: Intelligent search, chatbots, and application search integration
      - `Amazon Rekognition` - is a video analysis service. It can identify objects, people, text, scenes, and activities within images and videos stored in Amazon S3.
        - Use cases: Content moderation, identity verification, media analysis, and home automation experiences
      - `Amazon Textract` - detects and extracts typed and handwritten text found in documents, forms, and even tables within documents.
        - Use cases: Financial, healthcare, and government form text extraction for quick processing
    - Conversational AI and personalization services - users can interact with your apps through text and voice conversations. You can also present your customers with product recommendations personalized just for them.
      - `Amazon Lex` - you can add voice and text conversational interfaces to your applications. This service uses both natural language understanding (NLU) and automatic speech recognition (ASR) to create lifelike conversations.
        - Use cases: Virtual assistants, natural language search for FAQs, and automated application bots
      - `Amazon Personalize` - you can use historical data to build intelligent applications with personalized recommendations for your customers.
        - Use cases: Personalized streaming, product, and trending recommendations
- `Tier 2: ML services` - provides a more customized approach for customers who want a bit more control over their ML solutions without having to manage infrastructure
  - `Amazon SageMaker AI` - With this fully managed service, you can build, train, and deploy your own ML models without worrying about infrastructure
    - Key benefits:
      - Choice of ML tools - Increase innovation with different tool choices. Data scientists can use the IDE, and business analysts can use the no-code interface.
      - Fully managed infrastructure - Focus on ML model development while SageMaker AI provides you with high-performance, cost-effective infrastructure.
      - Repeatable ML workflows - Automate and standardize your MLOps practices and governance across your enterprise to support transparency and auditability.
- `Tier 3: ML frameworks and infrastructure` - Some organizations have highly specialized needs that require complete control over the ML training process. They can use in-house expertise, ML frameworks, and AWS infrastructure to develop their own ML solutions.
  - `ML frameworks` - is a software library or tool that provides experienced ML practitioners with pre-built, optimized components for building machine learning models
  - `AWS ML Infrastructure` - such as ML-optimized Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon EMR, and Amazon Elastic Container Service (Amazon ECS), can support these custom solutions.
- `Deep Learning (DL)` - is a subset of machine learning where models are trained using layers of artificial neurons that mimic the human brain.
- `Generative AI` - is a type of deep learning powered by extremely large ML models known as foundation models (FMs). 
- `Foundation models (FMs)` - FMs are pre-trained on vast collections of data.
- `Large language models (LLMs)` - are a popular type of FM trained to use human language. Foundation models can also be used to create videos, images, music, and more.
- `Generative AI on AWS` - AWS offers the following types of generative AI solutions
  - `Amazon SageMaker JumpStart` - An ML hub with FMs and pre-built ML solutions deployable with a few clicks.
    - Rapid ML model deployments - Deploy pre-trained models without extensive ML expertise.
    - Custom fine-tuned solutions - Pre-trained FMs with your domain-specific data
    - ML experiments and prototypes - Compare performance for different models before committing to a specific approach.
  - `Amazon Bedrock` - A fully managed service for adapting and deploying FMs from Amazon and other leading AI companies.
    - Enterprise-grade AI - Build production-ready generative AI applications with enterprise-level security, privacy, and scalability.
    - Multimodal content generation - Create applications that can generate multiple content types, such as text and images.
    - Advanced conversational AI - Develop advanced conversational agents that connect to your enterprise data to provide accurate responses.
  - `Amazon Q` - An interactive AI assistant that can be integrated with a company's information repositories.
    - `Amazon Q Business` - can answer pressing questions, help solve problems, and take actions using the data and expertise found in your company's information repositories.
      - Use cases: Information requests, automated workflows, and insight extraction
    - `Amazon Q Developer` - provides code recommendations to accelerate development for coding languages including C#, Java, JavaScript, Python, and TypeScript applications.
      - Use cases: Faster code generation, improved reliability and security, and automated code reviews
- `Data pipelines for ETL Process` - AI/ML and traditional data analytics need clean and accessible data in a format that's usable by analytics tools and AI algorithms.
  1. _Extract_ the data from various sources and store it.
  2. _Transform_ it into a consistent, usable format for downstream tools to consume.
  3. _Load_ it into a destination system, like a data warehouse or analytics platform.
- `Data analytics` - is when analysts transform raw historical data to uncover valuable insights and trends.
  - Loan companies explaining lending decisions to customers.
  - Medical researches analyzing clinical trial data through hypothesis testing.
  - Insurance companies making their risk assessment models transparent for regulators.
  - Data ingestion services - involves moving data from source systems into your chosen storage solution.
    - `Amazon Kinesis Data Streams` - Real-time ingestion of terabytes of data from applications, streams, and sensors. This serverless service even provides automatic provisioning and scaling in on-demand mode.
    - `Amazon Data Firehouse` - An option for data ingestion in near real-time. This fully managed service provides automatic provisioning and scaling. It also delivers data within seconds to data lakes, warehouses, and analytics services.
  - Data storage services - Data can come from many different sources. To gain insights, data is commonly consolidated into a single location.
    - `Amazon S3` - This object storage service can securely house virtually any amount of structured or unstructured data. Amazon S3 is also fully elastic, automatically scaling as you add and remove data.
    - `Amazon Redshift` - is a fully managed data warehouse service that can store petabytes of structured or semistructured data. With the scalability and pay-as-you-go pricing model, organizations can cost-effectively analyze large datasets.
  - Data cataloging services - Cataloging your data with metadata provides an inventory of your organization's data.
    - `AWS Glue Data Catalog` - provides a centralized, scalable, and managed metadata repository that enhances data discovery.
  - Data processing services - Data processing services clean and transform your data so it's ready to be analyzed.
    - `AWS Glue` - is a fully managed ETL service that makes data preparation simpler, faster, and cost-effective.
    - `Amazon EMR` - is ideal for large-scale data processing and organizations with existing big data expertise. It automatically handles infrastructure provisioning, cluster management, and scaling.
  - Data analysis and visualization services - Queries and visualization tools help you to develop important insights about your data.
    - `Amazon Athena` - you can run SQL queries to analyze data in relational, nonrelational, object, and custom data sources
      - This fully managed serverless service can access data hosted on Amazon S3, on premises, or even in multi-cloud environments.
      - It offers a cost-effective solution for data analysis because you only pay for the queries you run.
    - `Amazon Redshift` - is a fully managed data warehouse solution. Its columnar storage and massively parallel processing architecture make it ideal for analyzing large datasets.
      - You can use it to perform complex SQL queries on large datasets for frequent, high-performance analytical workloads.
    - `Amazon Quicksight` - both technical and non-technical users can quickly create modern interactive dashboards and reports from various data sources without managing infrastructure
      - Amazon Q in QuickSight provides natural language queries so business analysts and users can build, discover, and share meaningful insights in seconds.
    - `Amazon OpenSearch Service` - you can search for relevant content through precise keyword matching or natural language queries.
      - Unified dashboards provide real-time data visualization as you analyze and monitor logs, traces, and metrics for various applications.

### Recap
AI/ML and data analytics are two fields that use high-quality data to analyze past events and innovate for the future. In the previous lessons, you learned how AWS AI/ML solutions help to predict future trends and automate processes. And you learned how AWS solutions can be used to analyze historical trends and develop insights from data.

## Module 9 - Security
- `Authentication` - Verifying the identity of a user or entity through credentials.
  - Is the process of verifying the identity of a user or entity through credentials like a username and password combination.
  - Use case: An employee logs in to an employee portal.
- `Authorization` - Granting authenticated users with certain access rights and permissions.
  - Grants users certain access rights and permissions that determine which actions they can perform in a system or application.
  - Use case: An employee can only access their own employee records inside the employee portal.
- `Data privacy and protection` - Maintains customer trust and prevents fraud.
- `AWS security controls` - AWS offers multiple security mechanisms to help protect your cloud resources and achieve the following:
  - Prevent security incidents through proper permission and access management
  - Protect networks, application, and data
  - Detect and respond to security incidents as they occur.
- `AWS Identity and Access Managemen (IAM)` - Securely manage identities and access to AWS services and resources.
  - By default, all actions are denied.
- `Principle of least privilege` - Dictates that you should only give people and systems access to what they need and nothing else.
- `Root user` - The root user is the account owner and has permission to do anything inside the AWS account.
- `IAM user` - Represents a person or application that interacts with AWS services and resources. It consists of a name and credentials.
- `IAM Group` - Is a collection of IAM users. When you assign permissions to a group, all users in the group inherit the permissions.
- `IAM Roles` - An IAM role is a temporary identity with specific permissions. When assumed, previous permissions are dropped, and the user gains only those of the new role.
- `IAM policies` - is a JSON document that allows or denies permission to access AWS services and resources. IAM policies can also define the level of access to resources.
- `Resource` - Which AWS resource the API call is for
- Additional access management services
  - `AWS IAM Identity Center` - centralizes identity and access management across AWS accounts and applications
    - _Federated identity management is a system that allows users to access multiple applications, services, or domains using a single set of credentials._
  - `AWS Secrets Manager` - provides a secure way to manage, rotate and retrieve database credentials, API keys, and other secrets throughout their lifecycle.
    - _Secrets are confidential or private information intended to be known only to specific individuals or groups. Examples include passwords, database credentials, and API keys._
  - `AWS Systems Manager` - provides a centralized view of nodes across your organization's accounts and Regions and multi.cloud and hybrid environments.
    - _Nodes are connection points in a network, system, or structure._
- `AWS network and application protection` - automatically protects against low-level, brute-force attacks, such as DDoS, through its built-in infrastructure and network architecture.
- `AWS protection through infrastructure`
  - Security groups - only allow in proper request traffic. They operate at the AWS network level so they can shrug off massive attacks using the entire AWS Region's capacity
  - Elastic Load Balancing (ELB) - handles traffic first before handing it off, so your frontend server is not overwhelmed. Like security groups, it runs at the Region level.
  - AW Regions - The enormous capacity of Regions makes them extremely difficult to overwhelm.
- AWS protection through services
  - `AWS Shield` - designed to automatically protect AWS customers from the most common, frequently occurring types of DDoS attacks at no cost
  - `AWS WAF` - is a web application firewall that monitors network requests that come into your web applications. When a request comes into AWS WAF, it checks the IP address against a web access control list (web ACL). 
- `Data Encryption` - Securing data in a way that only authorized parties can access it
  - Data encryption works like a lock and key mechanism. If you have the right key, you can access the encrypted data.
  - At rest - The data is idle and not moving, like when it's stored in a database.
  - At transit - The data is moving between locations, like when it's being sent from a database to an application. SSL/TLS certificates are used to establish encrypted network connections from one system to another.
- AWS built-in data protection
  - `Amazon S3` - all new S3 buckets have encryption configured, and all uploaded objects are encrypted at rest.
  - `Amazon EBS` - EBS volumes and snapshots can be encrypted at rest, including both boot and data volumes of an Amazon EC2 instance.
  - `Amazon DynamoDB` - Server-side encryption at rest is enabled on all DynamoDB table data using encryption keys stored in AWS Key Management Service (AWS KMS).
- `AWS Key Management Service (AWS KMS)` - use AWS KMS to create and manage cryptographic keys. These keys can then be used to encrypt and decrypt your data. 
  - You can also control the use of keys across a wide range of services and in your applications.
  - _A cryptographic key is a random string of digits used for locking (encrypting) and unlocking (decrypting) data._
- `Amazon Macie` - you can monitor your sensitive data at rest to make sure it's safe. Macie uses machine learning (ML) and automation to discover sensitive data stored in Amazon S3
- `AWS Certificate Manager (ACM)` - Centralizes the management of your SSL/TLS certificates that provide data encryption in transit. It can be used to protect various AWS services and your connected on-premises resources.
  - SSL/TLS certificates are used to establish encrypted network connections from one system to another.
- Detection and response services
  - `Amazon Inspector` - Helps improve the security and compliance of applications by running automated security assessments for Amazon EC2 instances, containers, and Lambda functions.
  - `Amazon GuardDuty` - Provides intelligent threat detection across your infrastructure and resources. GuardDuty identifies threats by continuously monitoring streams of your account metadata and network activity in your environment.
  - `Amazon Detective` - After a threat has been detected, you can use Amazon Detective to further investigate the root cause. Detective helps you analyze threats with interactive visualizations contained in a unified AWS Management Console view.
  - `Amazon Security Hub` - Brings multiple security services together into a single place and format. With this service, you can quickly see your security and compliance state in one comprehensive view.

### Recap 
Building and maintaining a secure environment in the cloud is an important responsibility. AWS shares this responsibility with its customers. In the previous lessons, you learned about important security concepts, mechanisms, and services that help protect your cloud resources.

## Module 10 - Monitoring, Compliance and Governance in the AWS Cloud
- `Monitoring your resources in the AWS Cloud`
  1. Secure - Protect data, systems, and infrastructure from unauthorized access, use, disclosure, disruption, modification, or destruction
  2. Monitor - Continuously observe and analyze system activity, network traffic, and security events to detect potential threats or anomalies
  3. Audit - Periodically review and assess the effectiveness of security controls and check that all requirements are met and security policies and procedures are adhered to
  4. Compliance - Help ensure that an organization's security practices and controls meet the requirements of relevant regulations, industry standards, and contractual obligations
- `Importance of monitoring` - It provides a way for you to continuously observe and analyze system activity, network traffic, and security events to detect potential threats or anomalies.
  -  Monitoring and observability are critical components for ensuring the security, availability, reliability, and performance of your cloud-based workloads and data.
- `Benefits of monitoring your cloud resources`
  - Maintain security
  - Respond proactively
  - Ensure reliability
  - Monitor costs
  - Improve performance
- `Metrics` - Variables tied to your resources
- 
- `Amazon CloudWatch` - monitors your AWS resources and the applications that you run on AWS in real time.
  - you gain system-wide visibility into resource utilization, application performance, and operational health.
  - `CloudWatch metrics` - CloudWatch collects metrics from all your AWS resources, applications, and services that run on AWS and on-premises servers.
  - `CloudWatch alarms` - You can define thresholds on CloudWatch metrics and send notifications or automatically make changes to the resources.
  - `CloudWatch dashboards` - Dashboards are customizable home pages in the CloudWatch console that you can use to monitor your resources in a single view.
  - `CloudWatch logs` - Logs centralize the logs from all the systems, applications, and AWS services that you use.
  - **Benefits**: CloudWatch helps you visualize and analyze your resources, operate efficiently with automation, use an integrated view, proactively monitor, and gain insights.
- `AWS CloudTrail` - tracks user activity and API usage in the AWS Cloud, on premises, and even with other cloud providers. CloudTrail provides a detailed history of API calls, so you can track changes and identify who made them and when.
  - **Benefits**: CloudTrail provides auditing, security monitoring, and operational troubleshooting. It also helps you prove compliance and improve your security posture.
  - **Use cases:** It can be used for compliance and auditing, identifying security incidents, troubleshooting operational issues.
  - `CloudTrail events` - Event history provides a viewable, searchable, downloadable, and immutable record of the past 90 days of management events in an AWS Region. There are no CloudTrail charges for viewing event history.
  - `CloudTrail logs` - Monitors events and delivers those events as log files to your Amazon Simple Storage Service (Amazon S3) bucket. Because CloudTrail logs are securely stored, they can be used to prove compliance with regulations such as Payment Card Industry (PCI) and Healthcare Insurance Portability and Accountability Act (HIPAA).
  - `CloudTrail Insights` - Analyzes your normal patterns of API call volume and API error rates.
- `Benefits of compliance with AWS`
  - Inheriting the latest security controls that AWS uses on its own infrastructure
  - Third-party validation for thousands of global requirements
  - Streamlining and automating compliance
  - On-demand compliance reports
- `AWS Artifact` - a service that provides no-cost, on-demand access to AWS security and compliance reports and select online agreements.
  - Benefits: AWS Artifact helps you manage at scale, save time with on-demand access to compliance reports, and deploy with more confidence.
  - Use cases: It can be used to manage select online agreements and assess third-party security and compliance.
  - `AWS Artifact Agreements` - you can review, accept, and manage agreements for an individual account and for all your accounts in AWS Organizations.
  - `AWS Artifact Reports` - provide compliance reports from third-party auditors. These auditors have tested and verified that AWS is compliant with a variety of global, regional, and industry-specific security standards and regulations.
- `AWS Compliance` - contains resources to help you learn more about AWS compliance. You can read customer compliance stories to discover how companies in regulated industries have solved various compliance, governance, and audit challenges.
- `AWS Config` - a service that you can use to assess, audit, and evaluate the configurations of your AWS resources.
  - **Benefits:** AWS Config helps evaluate configurations against a desired state, manage resource configuration changes, and simplify troubleshooting and remediation.
  - **Use cases:** It can be used to continually audit security monitoring and analysis and to streamline operational troubleshooting and change management.
- `AWS Audit Manager` - A service that continually audits your AWS usage to simplify risk and compliance assessment. It helps collect evidence and manage audit data.
  - **Benefits:** Audit Manager saves time with automated evidence collection, streamlines collaboration across teams, and helps ensure integrity of audits with read-only permissions.
  - **Use case:** It can be used to automate evidence collection, continually audit to assess compliance, and deploy internal risk assessments.
- `AWS Organizations` - helps you centrally manage and govern your environment as you grow and scale your AWS resources. It helps you manage policies for groups of accounts and automate account creation.
  - Organizations provides several benefits like quickly scaling your environment by programmatically creating new AWS accounts for resources and teams.
  - It also helps by simplifying permission management through SCPs and managing and optimizing costs across your AWS accounts and resources.
- `Key concepts of Organizations`
  - `Managament account` - The management account is the central AWS account that creates and manages the organization. Responsible for overall control and governance 
  - `Organizational Units (OU)`- Logical grouping of accounts in an AWS Organization. OUs can contain member accounts or nested OUs.
  - `Service Control Policies (SCP)` - a policy that lets you place restrictions on the AWS services, resources, and individual API actions that users and roles in each account can access. SCPs can be applied to either OUs or individual member accounts.
  - `Member account not in an OU` - If you have a member account that has unique requirements that do not overlap with those of an organizational unit, you can add them to the organization. They do not have to be placed under an OU.
- `AWS Control Tower` - a service you can use to enforce and manage governance rules for security, operations, and compliance at scale across all your organizations and accounts in the AWS Cloud.
  - Benefits: AWS Control Tower can help you save time while providing governance. It uses preconfigured controls, which can help you to quickly set up multi-account environments, automation with built-in governance, and integration of third-party software at scale.
  - Use cases: Use AWS Control Tower to quickly deploy applications and provision compliant AWS accounts.
- `AWS Service Catalog` - you can create, share, and organize from a curated catalog of AWS resources. You can deploy baseline networking resources and security tools for new AWS accounts so you can govern consistently.
  - Benefits: Service Catalog saves time by making it quick to find and deploy approved, self-service cloud resources. It also helps you stay agile while improving governance over resources across multiple accounts.
  - Use cases: Use it to provision resources across AWS accounts, apply access controls, and accelerate provisioning of continuous integration and continuous delivery (CI/CD) pipelines.
- `AWS License Manager` - a service that helps you manage your software licenses and fine-tune your licensing costs.
  - Benefits: License Manager helps with visibility and control, tracking and managing licenses, and reducing the risk of noncompliance with licenses.
  - Use cases: Use it to streamline license management and to simplify the Microsoft License Mobility through Software Assurance experience. You can also use it to automate the distribution and activation of software entitlements across AWS accounts for end users.
- `AWS Bring Your Own License model (BYOL)` - use existing software licenses purchased directly from vendors, such as Microsoft, on AWS services like Amazon EC2 Dedicated Hosts and Amazon WorkSpaces.
- Three governance services
  - `AWS Control Tower` - A service you can use to set up and govern a secure, compliant, multi-account AWS environment based on best practices
  - `AWS Service Catalog` - A service you can use to create, share, and organize AWS services and resources from a curated catalog that you define
  - `AWS License Manager` - A service that helps you manage your software licenses and fine-tune licensing costs
- `AWS Health` - is the go-to data source for events and changes affecting the health of your AWS Cloud resources. It notifies you about service events, planned changes, and account notifications to help you manage and take actions.
- `AWS Health Dashboard` - you can view account-specific health information and get AWS Health event updates. You can also use AWS Health programmatically using the AWS Health API, which is available with AWS Premium Support.
  - Benefits: AWS Health Dashboard provides valuable information as a data source for events and changes. It gives you timely and actionable guidance to remedy issues. It also helps manage service health and is integrated and automated to use at scale.
  - Use cases: Use AWS Health Dashboard to view account-specific health information. You can also use it to plan for lifecycle events or troubleshoot an incident. 
- `AWS Trusted Advisor` - a service that provides real-time recommendations to help you optimize your AWS environment for cost, performance, security, and fault tolerance.
  - Benefits: Trusted Advisor helps you align with AWS best practices, prioritize recommendations, and optimize your AWS resources at scale.
  - Use cases: It can be used to optimize cost, efficiency, security, improve performance, and track service limits.
- `AWS IAM Access Analyzer` - provides capabilities to set, verify, and refine permissions by analyzing external access and validating that your policies match your corporate security standards.
  - Benefits: IAM Access Analyzer provides benefits like refining permissions, validating IAM policies, helping you meet your least privilege goals, and automating IAM policy reviews.
  - Use cases: It can be used to set fine-grained permissions, verify who can access what, remediate unused access, and refine and remove broad access.

### Recap 
In this module, you learned the progression of securing, monitoring, auditing, compliance, and governance in the AWS Cloud. You identified services that aid in monitoring with metrics, alarms, and dashboards. You also learned about services for auditing, such as CloudTrail, and compliance, such as AWS Artifact. You reviewed several other governance and compliance services and identified the role of AWS Trusted Advisor in continuously evaluating for cost, security, performance, and more.

