# QUIZ Module 9 - Security

> Q: After logging in to their online banking profile with their username and password, a customer attempts to transfer $10,000 from their savings to their checking account. The system checks if the customer has sufficient privileges to make transfers of this amount before proceeding. 
> 
> Which type of system check is this an example of?
> 
> A: Authorization

> Q: A healthcare company is preparing to deploy a web application on Amazon EC2 instances that will process sensitive patient data. The application will use Amazon RDS for database storage and Amazon S3 for file storage. The company's security team is discussing security responsibilities for the deployment. 
> 
> What is the customer's security responsibility in this scenario?
> 
> A:  Protecting sensitive patient data stored in Amazon S3 and Amazon RDS

---

> Q: An administrator who creates an AWS account is provided with the root user credentials. To secure this highly privileged account, they should immediately set a strong password and enable multi-factor authentication (MFA). 
> 
> What does MFA require users to do?
> 
> A: Provide two or more verification methods to gain access.

> Q: AWS Identity and Access Management (IAM) provides users, groups, roles, and policies so you can configure access based on your company’s specific operational and security needs. 
> 
> Which of these is specifically designed to provide temporary access to permissions?
> 
> A: IAM roles

> Q:A financial services company wants to give its accountants access to a particular Amazon S3 bucket. 
> 
> Which of these IAM controls is used to define this access?
> 
> A: IAM policy

---

> Q: A software development team needs to centrally manage its database credentials and API keys on AWS. 
> 
> Which of these services should the team choose?
> 
> A: AWS Secrets Manager

> Q: In a denial of service (DoS) attack, an attacker floods a web application with excessive network traffic. Legitimate customer requests are denied if the web application becomes overloaded and can no longer respond. 
> 
> How is a distributed denial of service (DDoS) attack different?
> 
> A: A DDoS attack uses multiple compromised computers and devices to launch the attack.

> Q: An online boutique has recently suffered a series of targeted distributed denial of service (DDoS) attacks. The owner wants to enhance the security of the boutique's web application using AWS infrastructure. 
> 
> Which components can the boutique use to protect the web application on AWS from DDoS attacks? (Select TWO.)
> 
> A: Security groups / Elastic Load Balancing (ELB)

--- 

> Q: Which processes involve locking and unlocking data with a special key so only authorized users can access it?
> 
> A: Encryption and decryption

> Q: A tax preparation company needs to secure sensitive customer data moving from its database to its web application on AWS.
> 
> Which of these services can help them secure the data in transit?
> 
> A: AWS Certificate Manager (ACM)

> Q: A security team at a legal firm has detected a threat to their AWS environment. To investigate the root cause over time, they need interactive visualizations of security data. 
> 
> Which AWS service is the BEST choice for this investigation?
> 
> A: Amazon Detective

> Q: A local government agency needs to prepare for an upcoming compliance audit. The agency needs to automatically aggregate security findings from multiple AWS services into one comprehensive view. 
> 
> Which of these services should the agency choose?
> 
> A: AWS Security Hub

## ASSESSMENT

> Q: With AWS Identity and Access Management (IAM) all actions are denied by default. When granting permissions, access should be provided only on a need-to-have basis. 
> 
> What is this concept called?
> 
> A: Principle of least privilege

> Q: What is the responsibility of AWS under the AWS shared responsibility model?
> 
> A: Managing physical security of data centers

> Q: A security team for a large ecommerce company needs a centralized way to create and manage the encryption keys that protect its data on AWS. 
> 
> Which of these services is the BEST fit for this team?
> 
> A: AWS Key Management Service (AWS KMS)

> Q: A small financial services company recently moved its online resources to AWS. The security team was concerned about protection from common, frequently occurring types of distributed denial of service (DDoS) attacks. 
> 
> Which AWS service automatically protects customers at no cost from DDoS attacks?
> 
> A: AWS Shield

> Q: An employee wants to check their company’s online employee portal to see how many vacation hours they have accrued. Before accessing their personal records, they enter their username and password to log in to the site. 
> 
> What happens during this login process?
> 
> A: Authentication

> Q: A security team for a large software development company needs to check multiple applications for security vulnerabilities and deviations from security best practices. The applications are running on Amazon EC2, AWS Lambda, and in containers. 
> 
> Which AWS service should they choose for the security assessments?
> 
> A: Amazon Inspector

> Q: A technology company is moving some of its resources to AWS. The company wants to provide single sign-on access for its employees on AWS using its existing identity source. 
> 
> Which service can help the company accomplish this?
> 
> A: AWS IAM Identity Center

> Q: A large marketing firm has a standard set of permissions used to grant designers access to certain Amazon S3 buckets. The firm added a new S3 bucket that all designers need to access. 
> 
> Which AWS Identity and Access Management (IAM) control can the firm use to assign permissions that will be inherited by all of its designers?
> 
> A: IAM group

> Q: All AWS accounts are given an AWS account root user. The root user is the account owner and has full permissions to perform any actions. 
> 
> What are some ways to protect this powerful account? (Select TWO.)
> 
> A: Associate a strong password with the account. /  Turn on multi-factor authentication (MFA).

> Q: Protecting sensitive customer data is a vital component of maintaining customer trust. This involves encrypting data at rest and in transit. 
> 
> What is used to encrypt data in transit?
> 
> A: SSL/TLS certificates

