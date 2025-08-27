# QUIZ Module 3 - Exploring Compute Service


> Configure operating system, security patches, and network settings - UNMANAGED
> 
> Choose deployment options and configure environment settings - MANAGED
> 
> Focus only on writing and deploying code - FULLY MANAGED

---

> Q:A development team at a fintech startup is building a new customer-facing microservice using AWS Lambda. AWS takes care of the infrastructure, but the team is focused on meeting strict security and compliance requirements. 
> 
> Which task is still the team's responsibility when using Lambda?
> 
> A: Managing data access permissions


> Q: A photography company offers cloud-based photo editing and storage. To streamline operations, it uses AWS Lambda to automatically process photos—resizing images, applying filters, and organizing files—every time a client uploads a new image. 
> 
> Which key components are involved in running an automated photo processing workflow with Lambda? (3)
> 
> A: Lambda function / Triggers / Runtimes

---

> Q: A developer just finished building an application that runs flawlessly on their laptop. However, when their team tries to deploy it in a different environment, it crashes because of missing dependencies and configuration mismatches. 
> 
> How do containers help solve this problem?
> 
> A: By packaging the application and everything it needs to run into one consistent environment

> Amazon Elastic Container Service (Amazon ECS) - Scalable container orchestration service for running containers on AWS
> 
> Amazon Elastic Kubernetes Service (Amazon EKS) - Fully managed Kubernetes service for deploying and scaling containers
> 
> Amazon Elastic Container Registry (Amazon ECR) - Stores, manages, and deploys Open Container Initiative (OCI)-compliant container images
> 
> AWS Fargate - Serverless compute engine for containers—removes the need to manage servers

---

> AWS Elastic Beanstalk - A managed service for deploying and scaling web applications
> 
> AWS Batch - A fully managed service for batch computing workloads
> 
> Amazon Lightsail - A simplified service with virtual private servers (VPSs), storage, and networking
> 
> AWS Outposts - A hybrid cloud service extending AWS to on premises

> Q: A startup is building a web application and wants a simple way to deploy code without managing infrastructure. They need to have auto scaling and monitoring handled for them. 
> 
> Which AWS service should they use?
> 
> A: AWS Elastic Beanstalk

> Q: A financial company must run workloads on premises because of strict compliance requirements, but it wants to use AWS services and tools consistently across environments. 
> 
> Which service meets their needs?
> 
> A: AWS Outposts


## ASSESMENT


> Q: A developer is launching a new microservice and wants to focus only on writing and deploying code. They do not want to manage servers, handle scaling, or worry about infrastructure availability. 
> 
> Which AWS service model is BEST for this use case?
> 
> A: Serverless 

> Q: A development team at a travel company has stored their hotel booking system’s container image in Amazon Elastic Container Registry (Amazon ECR) and is ready to deploy it. They need a service that can automatically start and stop containers based on traffic, scale up or down with demand, and monitor the health of the system. 
> 
> Which service does the team need next?
> 
> A:  An orchestration service like Amazon Elastic Container Service (Amazon ECS) or Amazon Elastic Kubernetes Service (Amazon EKS)

> Q: Which scenario is the BEST fit for using AWS Lambda?
> 
> A: Automatically processing images as users upload them to an Amazon S3 bucket

> Q: A company is launching a containerized photo application and has built the container image, which needs to be stored securely. They plan to use Kubernetes for orchestration and prefer not to manage any servers. 
> 
> Which combination of AWS services BEST fits their needs?
> 
> A: Amazon Elastic Container Registry (Amazon ECR), Amazon Elastic Kubernetes Service (Amazon EKS), and AWS Fargate

> Q: A development team at an e-commerce company is working on a new website. The application runs fine on their local machines, but when they attempt to deploy it to a staging environment, it does not work as expected. The team wants to make sure that the application runs consistently across all development, testing, and production environments going forward. 
> 
> Which solution should the team use to make sure that the application runs the same across all environments?
> 
> A: Package the application in a container that includes all dependencies.

> Q: A pharmaceutical research company needs to run thousands of simulations to analyze protein folding. These compute-heavy tasks are run in parallel and do not require real-time interaction. The company wants the jobs to be automatically scheduled and scaled based on computing demand. 
> 
> Which AWS service BEST fits this workload?
> 
> A: AWS Batch

> Q: A freelance developer is building a blog for a client with minimal traffic. They want a basic, cost-effective solution that includes storage and compute in one package, without having to deal with complex configurations or scaling concerns. 
> 
> Which AWS service is the BEST fit?
> 
> A: Amazon Lightsail

> Q: What is the customer responsible for managing in a serverless service like AWS Lambda?
> 
> A: The application code