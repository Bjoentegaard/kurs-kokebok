# QUIZ Module 4 - Going Global


> Q: A cloud engineer for a government agency is tasked with selecting an AWS Region to deploy the agency's resources. 
> 
> Which factors are MOST important to consider when selecting a Region? (Select TWO.)
>
> A: Any regulatory compliance standards the agency requires / Proximity to users

---

> AWS Region - A Physical location around the world where AWS operates multiple data centers
>
> Availability Zone - Separate, distinct locations with one or more data centers that are engineered to be isolated from failures in other areas
> 
> Edge location - Locations that cache content to deliver data, video, and applications to users with lower latency

---

> Q: A rapidly growing tech startup company is planning to launch a new web application that will require a complex infrastructure setup, including multiple Amazon EC2 instances, Elastic Load Balancing, and Auto Scaling groups. The application must be deployed consistently across different environments. 
> 
> Would AWS CloudFormation be a good solution for managing the company's infrastructure?
>
> A: CloudFormation would be ideal because it supports infrastructure as code (IaC), enabling consistent, repeatable deployments across different environments.
> 
> _CloudFormation is designed to handle complex infrastructure setups. It defines infrastructure as code to help make sure that deployments are consistent across different environments such as development, testing, and production._


## ASSESMENT


> Q: Which answer BEST describes the purpose and benefits of AWS edge locations?
>
> A: Edge locations cache content to deliver data with lower latency and higher transfer speeds to end users.


> Q: Which answer describes the key features and benefits of AWS CloudFormation?
>
> A: With CloudFormation, users can model and set up their AWS resources using code to automate provisioning and the management of infrastructure. This method can help to reduce errors and maintain consistency across environments.


> Q: What BEST describes key benefits of using multiple AWS Regions and multiple Availability Zones? (Select TWO.)
>
> A: High availability and fault tolerance /  Low latency for end users
> 
> _By using multiple AWS Regions, a company can place their resources closer to their end users, which reduces the distance that the data must travel. This results in lower latency and a better user experience. By using multiple Availability Zones within a Region, the company enhances the fault tolerance of their applications. If one zone fails, their application can continue to operate from another zone, maintaining high availability._


> Q: A team at a biomedical tech company is tasked with deploying a new medical application across multiple AWS Regions to help maintain high availability and fault tolerance. The application consists of several components, including a web server, a database, and a message queue. The deployment needs to be consistent and repeatable and should minimize manual errors through automation. 
> 
> Which approach is BEST suited for deploying this application according to the needs of automation and consistency?
>
> A: Using an Infrastructure as Code (IaC) service such as AWS CloudFormation to deploy the application


> Q: Which answer BEST describes the relationship between AWS Regions, Availability Zones, and edge locations?
>
> A: AWS Regions are physical locations around the world where AWS has multiple Availability Zones. Edge locations are located outside of AWS Regions and cache frequently accessed content.


> Q: A nonprofit organization is migrating all of their resources to the AWS Cloud. They are trying to decide which AWS Region to deploy their resources to. 
> 
> Which option lists the factors the organization needs to consider when deciding where to place their cloud resources?
>
> A: Compliance, proximity to customers, feature availability, and pricing
> 
> _When deciding where to place cloud resources, companies must consider multiple factors. Compliance refers to the Region meeting legal or regulatory requirements. Proximity to customers helps reduce latency and improve user experience. Feature availability makes sure that the required AWS services are supported in the chosen Region. Pricing varies by Region, so cost-efficiency is also a critical factor._
