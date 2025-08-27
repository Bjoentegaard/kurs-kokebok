# QUIZ Module 10 - Monitoring, Compliance, and the Governance in the AWS Cloud

> Q: An ecommerce company is hosting their customer application on multiple Amazon EC2 instances. The application experiences fluctuating traffic and occasional performance issues that are impacting the customer experience. 
> 
> How can Amazon CloudWatch help the customer? (Select THREE.)
> 
> A: 
>   - CloudWatch dashboards can be customized to visualize the metrics, alarms, and data in a consolidated view.
>   - CloudWatch alarms can be set up to alert when the Amazon EC2 utilization is too high for an extended period and automate more EC2 instances being created to share the load.
>   - CloudWatch logs can collect data on the EC2 instances and application logs. The logs can gain insights on performance issues or application errors.

---

> Q: A company wants to store the files that contain API activities for an AWS account in an Amazon S3 bucket. They want to retain these files for auditing and compliance. 
> 
> Which solution and feature would provide this capability?
> 
> A: AWS CloudTrail logs

---

> Q: Which tasks can you complete in AWS Artifact? (Select TWO.)
> 
> A:
>  - Access AWS compliance reports on demand.
>  - Review, accept, and manage agreements with AWS.

> Q: An enterprise customer with a large team of developers needs a way to ensure specific configuration guidelines for the developers when creating AWS resources. They want to assess and audit the AWS resources to make sure that the team is using the most cost-effective approved list of Amazon EC2 instances. 
> 
> Which AWS service would best fit the customer's need?
> 
> A: AWS Config

---

> Q: You are configuring service control policies (SCPs) in AWS Organizations. 
> 
> Which identities and resources can SCPs be applied to? (Select TWO.)
> 
> A:
> - An individual member account
> - An organizational unit (OU)

---

> Q: A government customer needs to set up and govern a secure, compliant, multi-account AWS environment. They want to make sure that employees comply with their approved requirements when creating new AWS accounts. 
> 
> Which AWS service would best fit the customer's need?
> 
> A: AWS Control Tower

---

> Q: An enterprise customer with a multi-Region AWS network is looking for ways to continuously evaluate and reduce costs while making sure that everything is secure and performing efficiently. They are also interested in learning AWS best practices to apply to their operations. 
> 
> Which solution would BEST meet their needs?
> 
> A: AWS Trusted Advisor

## ASSESSMENT

> Q: A financial company is looking for a solution to govern a curated set of AWS resources for their employees. When the employees need to select and start up a new AWS resource, they want to provide a self-service way to create, share, and deploy the AWS resources. 
> 
> Which AWS service would best meet their needs?
> 
> A: AWS Service Catalog
> 
> _With Service Catalog, you can create, share, and organize from a curated catalog of AWS resources. You can deploy baseline networking resources and security tools for new AWS accounts so that you can govern consistently._

> Q: A customer is using AWS Organizations to centrally manage their company's accounts for billing to optimize and organize costs. They want to set up rules or restrictions on the AWS services, resources, and individual API actions that the users can access. 
>  
> Which feature would meet their needs?
> 
> A: A service control policy (SCP)
> 
> _An SCP is a policy that lets you place restrictions on the AWS services, resources, and individual API actions that users and roles in each account can access. SCPs can be applied to either OUs or individual member accounts._

> Q: Which AWS service provides a no-cost, on-demand access to AWS security and compliance reports and select online agreements?
> 
> A: AWS Artifact 
> 
> _AWS Artifact is a self-service portal that provides on-demand access to AWS security and compliance documentation, including reports._

> Q: A sportswear company is hosting their application on Amazon EC2 instances. They want to collect metrics on their EC2 instances, and they would like notifications when utilization passes thresholds. They also want to have an action configured to automate scaling up the number of EC2 instances when utilization surpasses their threshold. 
> 
> Which AWS service would best meet their needs?
> 
> A: Amazon CloudWatch
> 
> _CloudWatch can collect the metrics on the EC2 instances, provide insights using dashboards, set alarms on thresholds, and automate the additional EC2 instances._

> Q: A research customer with a large team of developers needs a way to ensure specific configuration guidelines for the developers when creating AWS resources. They want a way to assess and audit the AWS resources to ensure that the team is using the most cost-effective approved list of compute resources. 
> 
> Which solution or feature would meet their needs?
> 
> A: AWS Config
> 
> _AWS Config is the best choice because it will assess, audit, and evaluate the configurations of the developer's AWS resources._

> Q: An enterprise customer has grown rapidly and is struggling to manage billing of their AWS resources and accounts. Every employee has created independent accounts with no centralized management or hierarchical groupings of accounts. The customer wants to roll up billing and centralize management into organizational units. 
> 
> Which AWS service would best meet this customer's need?
> 
> A: AWS Organizations
> 
> _With Organizations, you can centrally manage your environment as you scale your AWS resources. It can be used to centralize management, consolidate billing, and implement hierarchical groupings of accounts._

> Q: A financial company with a hybrid cloud solution wants to track changes made to their AWS resources both in the cloud and on premises. Specifically, they want to know who did what, and when.
> 
> Which AWS service would best meet their needs?
> 
> A: AWS CloudTrail
> 
> _CloudTrail is an AWS service that uses APIs to track who did what, when the action occurred, and on which AWS services and resources._

> Q: Which AWS service provides continuous evaluation and checks of your AWS resources, and provides suggestions to optimize costs, performance, security, and resilience?
> 
> A: AWS Trusted Advisor
> 
> _Trusted Advisor helps you optimize costs, increase performance, improve security and resilience, and operate at scale in the cloud._

> Q: Where can customers go to find resources on AWS compliance—for example, information on customer compliance stories, answers to key compliance questions, and an auditing security checklist?
> 
> A: Customer Compliance Center
> 
> _The Customer Compliance Center provides resources to help you learn more about AWS compliance. You can read customer compliance stories to discover how companies in regulated industries have solved various compliance, governance, and audit challenges._

> Q: What is the purpose of an AWS Control Tower landing zone?
> 
> A: It is the enterprise-wide container that holds all your organizational units (OUs), accounts, users, and resources that you want to regulate for compliance.
> 
> _A landing zone is a well-architected multi-account environment that is based on security and compliance best practices. It is the container where you hold all the resources that you want to regulate for compliance._

> Q: A customer is moving from on premises to the cloud and has decided to use the Bring Your Own License model (BYOL) approach for cost savings. They are concerned about managing the licenses, want a way to reduce the risk of noncompliance, and want to enforce license usage limits. 
> 
> Which solution would best meet their needs?
> 
> A: AWS License Manager
> 
> _License Manager helps reduce the risk of noncompliance by enforcing license usage limits, blocking new launches, and using other controls._
