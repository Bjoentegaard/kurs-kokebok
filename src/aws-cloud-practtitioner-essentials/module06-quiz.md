# Module 5 - Networking

> Q: A developer is building an application that processes large amounts of data and requires high I/O performance. After processing the data for an operation, the results are displayed to the user and do not need to be retained long-term. Unfortunately, the application's current storage solution is experiencing performance bottlenecks during peak processing times. 
> 
> How could implementing an EC2 instance store improve the performance of the application?
> 
> A: EC2 instance store provides high I/O performance for temporary storage needs.

> Q: AnyCompany Finance is designing an application that requires consistent and low-latency access to financial data. They're looking for a storage solution that provides persistent block storage. 
> 
> Why would Amazon EBS be suitable to store data in this scenario?
> 
> A: Amazon EBS provides high availability and durability by automatically replicating volumes within the same Availability Zone.

> Q: AnyCompany Software is migrating their on-premises application architecture to AWS. They are particularly concerned about data persistence because in their current environment, they have experienced data loss when virtual machines (VMs) crashed. They want to understand how Amazon Elastic Block Store (Amazon EBS) can help address their data persistence requirements when they move their workloads to Amazon EC2 instances. 
> 
> How does Amazon EBS solve the data persistence issue described in this scenario?
> 
> A: Amazon EBS volumes exist independently from the instance and persist even after the instance is terminated.

---

> Q: AnyCompany Commerce operates an online trading platform experiencing rapid growth. Their development team frequently needs to create test environments that mirror production for testing new features, but setting up these environments has become time-consuming and error-prone.
> 
> What is the most significant benefit of using EBS snapshots in this scenario?
> 
> A: EBS snapshots enable rapid creation of new volumes from existing data, so you can quickly deploy identical test environments that mirror production.

> Q: AnyCompany Healthcare manages thousands of EBS volumes containing patient records. They need to ensure that this data is properly backed up, retained according to compliance requirements, and old snapshots are removed to control costs.
>
> Which problem does AWS Data Lifecycle Manager primarily solve in this scenario?
> 
> A: Automating the creation, retention, and deletion of EBS snapshots and EBS backed Amazon Machine Images (AMIs) according to a schedule

---

> Q: AnyCompany Mobile is evaluating cloud storage solutions for their new mobile application. They need a reliable service that can handle various types of data storage requirements as their user base grows. 
> 
> Based on this scenario, what is an aspect of Amazon S3 that they could use in this scenario?
> 
> A: Storing and distributing mobile application content and user-generated media files

> Q: AnyCompany Marketing has created an Amazon S3 bucket to host images for their new website. The images need to be accessible to anyone visiting the website without authentication. After uploading the images to the bucket, users report they cannot access them, even though the bucket policy is set to allow public access. 
> 
> What is the most likely cause of this access issue?
> 
> A: Block public access settings are enabled at the account or bucket level.

> Q: AnyCompany Media is looking for a new cloud storage solution. They distribute large video files to users around the world, and are looking for a service that is highly durable, scalable, and offers various access control mechanisms. 
> 
> Based on this scenario, which Amazon S3 feature would be particularly beneficial?
> 
> A: Amazon S3 offers 99.999999999 percent (11 nines) of durability for objects stored across multiple Availability Zones. This maintains highly available for their video content and protects it against data loss.

---

> Q: AnyCompany Business stores a growing amount of customer data in Amazon S3. Their manager is concerned about storage costs and asks IT to implement a solution to move older data to cheaper storage. The data is frequently accessed for the first 30 days, occasionally accessed for the next 60 days, and rarely accessed after 90 days. 
> 
> What should they do in this situation to optimize costs while maintaining appropriate access to the data?
> 
> A: Create a lifecycle rule to transition objects to S3 Standard-Infrequent Access (S3 Standard-IA) after 30 days, transition to S3 Glacier after 90 days.

> Q: Which statement BEST describes S3 Lifecycle?
> 
> A: A feature used to define rules to automatically transition objects between different storage classes, or delete them based on age or usage patterns.

---

> Q: AnyCompany Financial needs to implement a new data application that will analyze market data. The application must be able to scale compute resources up or down to match traffic demand while maintaining access to the same datasets. 
> 
> What is a benefit of using Amazon EFS as the storage solution for the application described in this scenario?
> 
> A: Amazon EFS provides elastic storage capacity, automatically scaling up and down as files are added and removed, with no disruption to applications.

> Q: AnyCompany Retail is planning to migrate their on-premises file storage to AWS. They need a solution that allows their global development teams to collaborate on the same set of files simultaneously. 
> 
> Which feature of Amazon EFS makes it a good fit for this scenario?
> 
> A: Amazon EFS provides shared access for thousands of Amazon EC2 instances, with consistent low latencies.

---

> Q: AnyCompany Media wants to migrate its file shares to AWS while maintaining compatibility with existing applications. They need a solution that supports Server Message Block (SMB) protocol and integrates with Microsoft Active Directory. 
> 
> Which AWS service should they implement in this scenario?
> 
> A: Amazon FSx for Windows File Server

---

> Q: AnyCompany has a large collection of files stored on-premises that needs to be backed up to the AWS Cloud. They want to maintain local access to frequently used files while using cloud storage for cost savings. They also want to minimize changes to their existing file-sharing workflows and applications. 
> 
> Which AWS Storage Gateway type BEST addresses these requirements?
> 
> A: Amazon S3 File Gateway

> Q: AnyCompany Manufacturing stores CAD files that need to be accessed frequently by engineers at their on-premises data center. They want to maintain local access to this data while also benefiting from AWS Cloud storage capabilities. They plan to implement a solution that provides low-latency access to frequently used files while backing up data to AWS. 
> 
> Which AWS Storage Gateway configuration should they choose?
> 
> A: Implement Storage Gateway in Cached Volume mode to keep frequently accessed data local while storing the complete dataset in Amazon S3.

---

> Q: AnyCompany Telecommunications is concerned about potential downtime after experiencing an outage last quarter. They want to implement a disaster recovery solution for their on-premises server fleet but have limited IT staff. The CEO is particularly concerned about maintaining exact replicas of production servers and minimizing recovery time. 
> 
> What is a key benefit of using AWS Elastic Disaster Recovery in this scenario?
> 
> A: Continuous block-level replication with frequent backup intervals, providing near-instant recovery of servers at the target AWS Region

---

## ASSESSMENT

> Q: What is the primary function of Amazon S3 storage classes?
> 
> A: To provide different storage options optimized for different use cases and access patterns

> Q: Which statement BEST describes Amazon S3?
> 
> A: A scalable object storage service that is used to store and retrieve any amount of data from anywhere on the web.

> Q: AnyCompany Manufacturing maintains a large amount of engineering drawings and design files that their teams need to access daily from their on-premises applications. They want to gradually migrate these files to AWS to reduce their local storage costs while maintaining low-latency access for frequently used files. 
> 
> The solution needs to meet the following criteria:
>
> - Integrate with existing file-based workflows.
> - Provide a seamless path to cloud storage without disrupting current operations.
> - Maintain local, low-latency access to frequently used files.
>
> Which AWS storage service should they use based on these requirements?
> 
> A: AWS Storage Gateway – File Gateway

> Q: AnyCompany Software is deploying a critical production application on Amazon EC2 instances with several Amazon Elastic Block Store (Amazon EBS) volumes containing application code and customer data. The team is looking for an AWS service they can use to back up the data for their application.
>
> The solution needs to meet the following criteria:
> 
> - Create regular data backups. 
> - Create duplicate environments for testing. 
> - Create a disaster recovery strategy. 
> - Create full or incremental backups without impacting application performance. 
> - Provide cost-effective for long-term storage. 
>
> Which AWS service or feature would BEST meet the requirements in the scenario?
> 
> A: EBS snapshots

> Q: AnyCompany AI is developing a machine learning application that requires extremely fast data processing for temporary model training datasets. The data is generated during training sessions and stored separately in persistent storage. The team is trying to determine the best storage solution to use alongside their application.
>
> The solution needs to meet the following criteria:
> - Highest possible I/O performance
> - Directly attached to their Amazon EC2 instances
> - Temporary storage – data does not persist when instances are stopped or terminated
>
> Which AWS service BEST meets the temporary storage needs described in this scenario?
> 
> A: Amazon EC2 instance store

> Q: Which statement BEST describes Amazon Elastic Block Store (Amazon EBS)?
> 
> A: A block-level storage service that provides persistent storage volumes for Amazon EC2 instances

> Q: Which statement BEST describes Amazon Elastic File System (Amazon EFS)?
> 
> A: A fully managed, elastic file system that scales automatically as files are added and removed

> Q: What is a key characteristic of Amazon S3 storage classes pricing?
> 
> A: Pricing varies based on storage costs, retrieval fees, and minimum storage durations.

> Q: AnyCompany Technology needs to implement a centralized storage solution for their development team that allows multiple Amazon EC2 instances to access the same file system simultaneously. 
> 
> The solution needs to meet the following criteria:
> - Provide a fully managed service. 
> - Automatically scale. 
> - Eliminate the need for capacity planning. 
> - Support Linux-based applications with standard file system interfaces. 
> - Maintain consistent low-latency access across development environments. 
> - Provide high durability without requiring complex replication setups. 
>
> Which AWS storage service is BEST suited for this scenario?
> 
> A: Amazon Elastic File System (Amazon EFS)

> Q: AnyCompany Commerce has recently migrated its main application to an Amazon EC2 instance in AWS. As their customer base expands, they are exploring storage solutions that can grow dynamically with the application's data needs. 
> 
> The solution needs to meet the following criteria:
> - Have persistent block storage that provides consistent low-latency performance. 
> - Be able to be attached to and detached from the EC2 instance as needed. 
> - Independently resize storage capacity without disrupting the instance. 
> - Create point-in-time backups to protect critical customer and inventory data. 
> 
> Which AWS storage service would BEST meet the requirements in the scenario?
> 
> A:  Amazon Elastic Block Store (Amazon EBS)

> Q: Which statement BEST describes AWS Elastic Disaster Recovery?
> 
> A: A service that minimizes downtime and data loss by providing fast, reliable recovery of on-premises and cloud-based applications using affordable storage, minimal compute, and point-in-time recovery

> Q: Which statement BEST describes AWS Storage Gateway?
> 
> A: A hybrid cloud storage solution that provides on-premises applications with access to virtually unlimited cloud storage

> Q: Which statement BEST describes Amazon FSx?
> 
> A: A fully managed service that provides cost-effective, scalable file storage built on widely used file systems

> Q: AnyCompany Marketing needs a storage solution that they can use to distribute large collections of high-resolution images, videos, and design files for their clients' campaigns. Some assets are accessed frequently, whereas others are archived for occasional reference.
>
> The solution needs to meet the following criteria:
> - Unlimited storage capacity 
> - High durability 
> - Easy file sharing through URLs 
> - Ability to organize assets by client and project 
> - Cost-efficient storage options 
> - Security controls to prevent unauthorized access for specific assets
>
> Which AWS service is BEST suited for the storage needs described in this scenario?
> 
> A: Amazon S3

> Q: AnyCompany Marketing needs to migrate their existing file shares to AWS to support their design teams who work with large creative files. They need help choosing a storage solution that can facilitate this migration. 
> The solution needs to meet the following requirements:
> - Provide a fully managed service.
> - Seamlessly integrate with Windows applications.
> - Support SMB protocol.
> - Offer Active Directory integration for user authentication.
> - Support data deduplication to optimize storage costs.
> - Provide consistent sub-millisecond latencies.
> - Provide high availability.
>
> Which AWS storage service BEST meets the requirements described in the scenario?
> 
> A: Amazon FSx for Windows File Server

