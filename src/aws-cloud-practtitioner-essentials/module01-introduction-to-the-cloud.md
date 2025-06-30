# Module 1 - Introduction to the Cloud

## INTRODUCTION

- You will learn:
  - Describe the client-server model at a fundamental level.

> **Test your skills**
>
> Which scenario BEST describes how the client-server model works in this analogy?
> - [ ] The customer takes a cup of coffee from a self-serve station without informing the barista. This describes how a client and server do not interact.
> - [ ] The barista proactively prepares a coffee and brings it to the customer without being asked. This describes how the client does not need to submit a request to the server.
> - [ ] The customer makes their own coffee using the coffee shop equipment without interacting with the barista. This describes how the client does not require the server.
> - [x] The customer goes to the barista and places an order for a coffee. The barista prepares the coffee and hands it back to the customer. This describes how the client places the request, and the server responds.

---
## THE AWS CLOUD

### What is Cloud Computing?

- You will learn:
  - Define cloud computing
  - Describe and differentiate between cloud deployment types

On-demand delivery of IT resources over the internet with pay-as-you-go pricing

- **Cloud deployment types**
    - Cloud-based deployment
    - On-premises deployment
    - Hybrid deployment

> **Test your skills**
>
> You work for a local charity organization. Your organization has sensitive data that must remain within your country for compliance reasons.
> However, you also need a solution that can scale quickly to handle seasonal spikes in demand.
> You decide to keep on-premises resources for compliance and use cloud-based resources for dynamic scaling.
>
> Which type of cloud deployment does this situation describe?
>
> - [ ] On-premises deployment
> - [ ] Public cloud deployment
> - [x] Hybrid deployment
> - [ ] Data-compliance deployment

### Benefits of the AWS Cloud

- You will learn:
  - Describe the six benefits of cloud computing

The six key benefits of the AWS Cloud are as follows:

1. Trade fixed expense for variable expense
2. Benefit from massive economies of scale
3. Stop guessing capacity
4. Increase speed and agility
5. Stop spending money to run and maintain data centers
6. Go global in minutes

> **Test your skills**
>
> A retail business plans to launch a new line of clothing, but they are struggling with accurately predicting how much server capacity they will need to support the launch.
>
> Which benefit of the AWS Cloud is most relevant to this situation?
>
> - [ ] Stop spending money to run and maintain data centers.
> - [x] Stop guessing capacity.
> - [ ] Trade upfront expense for variable expense.
> - [ ] Go global in minutes.

### Introduction to the AWS Global Infrastructure

- You will learn
  - Define AWS Regions and Availability Zones (AZ)
  - Explain the benefits of high availability and fault tolerance

- AWS Regions
  - Physical locations around the world that contain groups of data centers.
  - These groups of data centers are called Availability Zones
  - Each AWS Region consists of a minimum of three physically separate AZ within a geographic area.
- Availability Zone consists of one or more data centers with redundant power, networking, and connectivity.
  - Regions and AZ are designed to provide low-latency, fault-tolerant access to services for users within a given area.

> **Test your skills**
>
> You just joined a tech start-up, and the business is growing rapidly. 
> Your new company decides that they need to design a resilient and scalable infrastructure on AWS to handle increased traffic and help ensure high availability.
>
> Which statement BEST describes the AWS Global Infrastructure benefit of high availability?
>
> - [ ] AWS stores all of your website’s data in a single AWS storage bucket to centralize data management.
> - [ ] AWS has many customer support options to make sure the answers to your questions are highly available on its website.
> - [x] AWS provides multiple data centers across different geographic regions so your website can remain operational even if one location faces issues.
> - [ ] AWS offers a single, highly secure data center that can handle all your traffic, which makes sure that your website is available.

### The AWS Shared Responsibility Model

- You will learn:
  - Describe and differentiate between customer responsibilities, AWS responsibilities, and shared responsibilities.
  - Describe the components of the AWS Shared Responsibility Model


- **Customer responsibilities** (Security _IN_ the cloud)
  - Customer data
  - Client-side data encryption
- **Shared responsibilities** (Varies by service)
  - Server-side encryption
  - Network traffic protection
  - Platform and application management
  - OS, network, firewall configuration
- **AWS responsibilities** (Security _OF_ the cloud)
  - Software for compute, storage, database, and networking
  - Hardware, AWS Global Infrastructure

> **Test your skills**
>
> You work for a startup company that is developing an application in the cloud. 
> A new security update is available for your operating system (OS), and you are tasked with verifying that the OS is patched accordingly.
> 
> Which statement BEST describes which party is responsible for applying security patches to the OS that is running in the cloud?
>
> - [ ] AWS is responsible for applying security patches to the OS.
> - [x] Your company is responsible applying security patches to the OS.
> - [ ] Both AWS and the customer apply separate patches.
> - [ ] The OS vendor applies the patches.

---
## CLOUD IN REAL LIFE

### Applying Cloud Concepts to Real Life Use Cases

- You will learn:
  - Explain how fundamentals cloud concepts, such as the AWS Global Infrastructure and AWS Shared Responsibility Model, work together to form real-world business solutions.

>**EXAMPLE**
>- This ecommerce company is based in Seattle, Washington in the United States.
>- The company wants to expand to global locations. However, the further the computing infrastructure is from their customers, the longer the latency. 
>- The company decides to expand to global AWS Regions to better reach their global customers.
>- The company deploys resources to the eu-west-1 Region in Ireland. Deploying in multiple Regions increases high availability. 
>- The company increases fault-tolerance and high availability even more by deploying to two Availability Zones in this Region.
>- The company has a significant customer base in Asia, too. So, they deploy resources to the ap-southwest-1 AWS Region in Singapore.

---
## MODULE 1 CONLUSION

### Assessment

#### Q1: Cloud Security Responsibility
A finance company is interested in migrating to the cloud and is curious about who is responsible for securing the physical infrastructure of the cloud.

**Best statement:**
- [x] AWS is responsible for securing the physical infrastructure, and the company can focus on securing their data and applications within the cloud.

---

#### Q2: AWS Global Infrastructure
A global web application needs to ensure performance and reliability by using AWS infrastructure.

**Correct answers (2):**
- [x] High availability
- [x] Fault tolerance

---

#### Q3: Customer's Security Responsibilities
A cloud architect explains the customer's responsibilities under the AWS Shared Responsibility Model.

**Customer responsibilities (2):**
- [x] Managing OS patches
- [x] Encrypting client-side data

---

#### Q4: Cloud Computing Cost Model
A small business is concerned about fixed costs when considering migrating its IT infrastructure to the cloud.

**Best statement:**
- [x] Cloud computing is a model for delivering IT resources over the internet. Businesses can rent services on a pay-as-you-go basis, which can help reduce fixed costs and allow for more flexible budgeting.

---

#### Q5: Client-server model
Your team lead has asked you to explain the client-server model and how cloud computing fits into this model

**Best statement:**
- [x] In the client-server model, the client sends requests to the server, which processes the requests and sends back responses. Cloud computing provides scalable server resources that can be accessed over the internet.

---

#### Q6: Advantage of the Cloud
A large enterprise is looking to lower operational costs. They are hoping to reduce the operational overhead associated with managing their own physical infrastructure.

**Best statement**
- [x] Stop spending money running and maintaining data centers

---

#### Q7: AWS Cloud services
A government agency wants to maintain complete control over its IT infrastructure, but plans to use AWS Cloud services for specific applications.

**Best statement**
- [x] Hybrid

---

#### Q8: Difference between Regions and AZ
Your company is expanding globally and needs high availability. Explain to your COO the difference between AWS Regions and Availability Zones.

**Best statement**
- [x] A Region is a geographical location that contains three or more Availability Zones. An Availability Zone is a distinct location within a Region that contains one or more discrete data centers.

---