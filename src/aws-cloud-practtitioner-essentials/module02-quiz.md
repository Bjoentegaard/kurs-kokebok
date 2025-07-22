# Module 2 - Compute in the Cloud


> Q: How does EC2 compare to running servers on premises?
> 
> A:  It is more flexible, cost-effective, and quicker to get started

> Q: What is multi-tenancy in the context of EC2 instances
> 
> A: Each vm is isolated but shares resources from a host machine.

> Q: A company uses EC2 instance to deploy their application, what whould happen if they need to stop or terminate the EC2 instances?
> 
> A: You pay only for running instances, not for stopped ord terminated ones.

> Q: What must be specified when preparing to launch an EC2 instance?
> 
> A: The types of instance and the OS

--- 
> Q: Which Amazon EC2 instance type is best suited for fast real-time analytics of large datasets?
> 
> A: Memory optimized

> Q: Which Amazon EC2 instance type is best suited for fast, consistent access to large locally stored datasets?
>
> A: Storage Optimized

---
> Q: What is a primary advantage of using the AWS CLI over the AWS Management Console?
> 
> A: It uses automation and scripting, which reduces manual steps and errors.

> Q: What is the customer's responsibility when using compute services like EC2 according to the AWS shared responsibility model?
> 
> A: The customer is responsible for configuring, securing, and managing the OS, networking, and applications on their EC2 instances.

---

> Q: What are the required configurations when launching an Amazon EC2 instance for a web server (3)
> 
> A: Amazon Machine Image (AMI) / Instance type / Storage

> Q: What is an Amazon Machine Image (AMI) used for when launching an Amazon EC2 instance
> 
> A: To pre-configure the OS and software

---

> Q: How can a financial services company run sensitive, regulation-compliant applications with full control over physical server placement and resource allocation?
> 
> A: Dedicated Hosts

> Q: How can a startup reduce costs for an interruptible batch processing workload by using unused Amazon EC2 capacity?
>
> A: Spot Instances

> Q: How can a customer build a new application with uncertain usage patterns and future growth without making a long-term commitment?
>
> A: On Demand

---

> Q: What is the primary benefit of scalability and elasticity in AWS
>
> A: The ability to grow and shrink resources dynamically based on real-time demand

> Q: What is the main reason for deploying Amazon EC2 instances across multiple Availability Zones?
>
> A: To provide high availability by allowing instances in different Availability Zones to handle traffic if one Availability Zone fails

> Q: How does AWS make sure that a business can meet fluctuating demand without over-provisioning resources?
>
> A: By allowing businesses to provision resources that automatically scale based on demand
 
---

> Q: How does Elastic Load Balancing (ELB) improve scalability in AWS?
>
> A: It automatically routes traffic to instances based on various routing methods.

> Q: Which task does Elastic Load Balancing (ELB) perform?
>
> A: Distributes a workload across several Amazon EC2 instances.

---

> Q: What BEST describes the key difference between tightly coupled and loosely coupled architectures?
>
> A: In a tightly coupled architecture, components are tightly connected and dependent on each other, whereas in a loosely coupled architecture, components can operate independently.

> Q: In a banking system, when customers transfer money, the transaction details are sent from the transaction service to a fraud detection service for verification. Sometimes, the fraud detection service is temporarily down. 
> 
> What is the MAIN advantage of using Amazon Simple Queue Service (Amazon SQS) in this banking scenario?
>
> A: It stores transaction details until the fraud detection service can process them, even if the service is down.


## ASSESMENT


> Q: What does multi-tenancy refer to in the context of Amazon EC2?
>
> A: Multiple users sharing the same EC2 instance while maintaining isolation

> Q:A university research team is running climate modeling simulations that require substantial CPU power to process complex algorithms and analyze large datasets.
> 
> Why are compute optimized Amazon EC2 instances ideal for this task?
>
> A: They are ideal for tasks that require significant CPU power to perform computations.

> Q: How do Amazon EC2 Auto Scaling and Elastic Load Balancing (ELB) work together in AWS?
>
> A: Amazon EC2 Auto Scaling adjusts the number of instances, whereas ELB distributes traffic evenly across them.

> Q: A manufacturing company is running a set of predictable workloads for the next 3 years and wants to optimize costs.
>
> Which option should they choose?
>
> A: Reserved Instances

> Q: A software development company needs to notify the engineering team whenever a new bug is reported in their bug tracking system. Some team members need to be notified immediately, whereas others can process the bug reports later. 
> 
> Which service should the software development company choose based on the requirements?
>
> A: Amazon Simple Notification Service (Amazon SNS)

> Q: Which tool can be used to interact with AWS services through a graphical user interface (GUI)?
>
> A: AWS Management Console

> Q: What is the primary role of an Amazon Machine Image (AMI) when scaling applications?
>
> A: It provides a consistent image to launch new instances.

> Q: A media company is working on a project that involves rendering complex visual effects and simulations. The rendering process requires significant computational power and hardware accelerators to handle the intense workload efficiently. 
> 
> Which Amazon EC2 instance type would be the BEST choice for this task?
>
> A: Accelerated computing

> Q: A marketing agency is developing a new web application and expects steady growth, but is unsure of traffic in the early months. They want flexibility without a long-term commitment. 
> 
> Which pricing option should they use?
>
> A: On-Demand

> Q: A startup company is building a new web application and chooses general purpose Amazon EC2 instances to host the application. 
>
> Why did they choose this instance type?
>
> A: It provides a balanced mix of compute, memory, and networking resources while keeping costs efficient as they scale their user base.

> Q: A company has critical steady-state workloads and batch jobs that are not time-sensitive.
>
> How should they optimize costs using Amazon EC2 Savings Plans and Spot Instances?
>
> A: Use Savings Plans for critical workloads and Spot Instances for jobs that are not time-sensitive to maximize savings.

> Q: How does Amazon EC2 Auto Scaling work in AWS?
>
> A: Amazon EC2 Auto Scaling automatically adds or removes instances based on performance data and application metrics.

> Q: What happens if one component fails in a loosely coupled architecture?
>
> A: The system can continue to function as other components are independent.

> Q: Which option BEST describes how compute resources are provisioned and managed in the cloud?
>
> A: Resources are provisioned based on demand, allowing for scaling and management.
