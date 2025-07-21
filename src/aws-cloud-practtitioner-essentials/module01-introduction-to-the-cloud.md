# Module 1 - Introduction to the Cloud

## INTRODUCTION

_Objective:_
- Describe the client-server model at a fundamental level.
---

> Q: Which scenario BEST describes how the client-server model works in coffee-shop analogy?
> 
> A: The customer goes to the barista and places an order for a coffee. The barista prepares the coffee and hands it back to the customer. This describes how the client places the request, and the server responds.
---
## THE AWS CLOUD

### What is Cloud Computing?

_Objective:_
- Define cloud computing
- Describe and differentiate between cloud deployment types
---

>On-demand delivery of IT resources over the internet with pay-as-you-go pricing

**Cloud deployment types:**
- **Cloud-based deployment:** Resources and applications are hosted entirely in the cloud and accessed over the internet.
- **On-premises deployment:** Resources and infrastructure are hosted and managed locally within the organization's data center.
- **Hybrid deployment**: A combination of on-premises and cloud environments, offering balance between control and scalability.

> Q: Which deployment model balances compliance (on-premises) and scalability (cloud)?
> 
> A: Hybrid deployment

### Benefits of the AWS Cloud

_Objective:_
- Describe the six benefits of cloud computing
---

The six key benefits of the AWS Cloud are as follows:

1. Trade fixed expense for variable expense
2. Benefit from massive economies of scale
3. Stop guessing capacity
4. Increase speed and agility
5. Stop spending money to run and maintain data centers
6. Go global in minutes



> Q: A retail business plans to launch a new line of clothing but struggles with predicting the server capacity needed for the launch. Which AWS Cloud benefit helps address this challenge?
>
> A: Stop guessing capacity

### Introduction to the AWS Global Infrastructure

_Objective:_
- Define AWS Regions and Availability Zones (AZ)
- Explain the benefits of high availability and fault tolerance
---

**AWS Regions**
  - Physical locations around the world that contain groups of data centers.
  - These groups of data centers are called Availability Zones
  - Each AWS Region consists of a minimum of three physically separate AZ within a geographic area.

**Availability Zone**
  - consists of one or more data centers with redundant power, networking, and connectivity.
  - Regions and AZ are designed to provide low-latency, fault-tolerant access to services for users within a given area.

> Q: How does AWS Global Infrastructure ensure high availability?
>
> A: AWS provides multiple data centers across different geographic regions, so your website remains operational even if one location experiences issues.

### The AWS Shared Responsibility Model

_Objective_:
- Describe and differentiate between customer responsibilities, AWS responsibilities, and shared responsibilities.
- Describe the components of the AWS Shared Responsibility Model
---

**Customer responsibilities** (Security _IN_ the cloud)
- Customer data
- Client-side data encryption

**Shared responsibilities** (Varies by service)
- Server-side encryption
- Network traffic protection
- Platform and application management
- OS, network, firewall configuration

**AWS responsibilities** (Security _OF_ the cloud)
- Software for compute, storage, database, and networking
- Hardware, AWS Global Infrastructure

> Q: Which party is responsible for applying security patches to the OS that is running in the cloud?
>
> A: Your company is responsible for applying security patches to the OS.

---
## CLOUD IN REAL LIFE

### Applying Cloud Concepts to Real Life Use Cases

- _Objective_:
  - Explain how fundamentals cloud concepts, such as the AWS Global Infrastructure and AWS Shared Responsibility Model, work together to form real-world business solutions.
---

>**EXAMPLE**
>- An ecommerce company in Seattle, Washington seeks to expand globally. Greater distance from customers increases latency.
>- To improve reach, they deploy resources in global AWS Regions, starting with eu-west-1 (Ireland) for high availability.
>- Fault-tolerance and availability further improve by using two Availability Zones in the Region.
>- With a strong customer base in Asia, they also deploy resources in ap-southwest-1 (Singapore).

---
## MODULE 1 CONCLUSION

### Assessment

> Q: A finance company is interested in migrating to the cloud and is curious about who is responsible for securing the physical infrastructure of the cloud.
>
> A: AWS is responsible for securing the physical infrastructure, and the company can focus on securing their data and applications within the cloud.

---

> Q: A global web application needs to ensure performance and reliability by using AWS infrastructure. What are the key advantages of AWS infrastructure to meet these needs?
>
> A: 
>   - High availability 
>   - Fault tolerance.

---

> Q: A cloud architect explains the customer's responsibilities under the AWS Shared Responsibility Model. What responsibilities does the customer have in this model?
>
> A: 
>   - Managing OS patches 
>   - Encrypting client-side data.

---

> Q: A small business is concerned about fixed costs when considering migrating its IT infrastructure to the cloud. How does cloud computing address this concern?
>
> A: Cloud computing is a model for delivering IT resources over the internet. Businesses can rent services on a pay-as-you-go basis, which can help reduce fixed costs and allow for more flexible budgeting.

---

> Q: Your team lead has asked you to explain the client-server model and how cloud computing fits into this model. What is the best explanation?
>
> A: In the client-server model, the client sends requests to the server, which processes the requests and sends back responses. Cloud computing provides scalable server resources that can be accessed over the internet.

---

> Q: A large enterprise is looking to lower operational costs by reducing the overhead associated with managing its infrastructure. What is a key advantage of cloud computing in this case?
>
> A: Stop spending money running and maintaining data centers.

---

> Q: A government agency wants to maintain complete control over its IT infrastructure but plans to use AWS Cloud services for specific applications. Which deployment model is suitable for their needs?
>
> A: Hybrid deployment.

---

> Q: Your company is expanding globally and needs high availability. What is the difference between AWS Regions and Availability Zones?
>
> A: A Region is a geographical location that contains three or more Availability Zones. An Availability Zone is a distinct location within a Region that contains one or more discrete data centers.

---
