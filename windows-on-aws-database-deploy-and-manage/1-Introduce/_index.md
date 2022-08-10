### Introduction
---
What is Amazon RDS Service?, it is stand for Amazon Relational Database Service (RDS). This is a database service which is build by Amazon so that we can use to create and manage database server

There are some benefit that Amazon RDS service can bring to the business over the in-house (on-premise) database service:
- Wide-range support DB Engine: Amazon RDS Service is supporting some of most popular Database Engines such as: MySQL, Oracle, Postgre SQL, Microsoft SQL, Maria DB, and the cloud-native database Aurora
- Instance Size: Amazon RDS service is supporting so many instance size so that we can choose to meet the business's needs
- Editions: Amazon RDS service is built-in licence and supported some kind of editions for database so that to suitable our need. Let take Microsoft SQL as an example, Amazon RDS Service is supporting for: SQL Express Edition, SQL Standard Edition, SQL Web Edition, SQL Enterprise Edition 
- Version: For Microsoft SQL, Amazon RDS Service is currently support from SQL Server 2014 up to SQL Server 2019 with latest build.
- Auto Scale: the Amazon RDS Service is supporting for storage auto scaling; which means that we do not have to worry about the storage to be run-out. As we are hardly to do it on-premise. For now, just one-click and Amazon RDS Service will take care about the underlied-hardware(storage) for us - as AWS's cusomter.
- Back-up: for database, we are all understand that back-up is the most critical task to perform. Hence, at Amazon RDS Service, we can enable Automatic Back-up so that Amazon will take care and create a point-in-time (PIT) back-up for our database server
- Auto Minor Update: by enabling this function, AWS RDS Service will run task so that to catch-up the lastest minor update and update to our database server. 
- Accessing Underlied RDS Service OS Host: There is a special option named **"Amazon RDS Custom"** which is grant to customer some privilegdes to access into the RDS host OS so that we can fully conifgure the Amazon RDS Service as we want to.
- Join to a Domain: We can managed the Amazon RDS to join into a domain. However, the limitation of this is about we cannot join the Amazon RDS into the on-premise domain. Instead, we can only join the Amazon RDS to AWS Managed Directory Service
---
### Architect Diagram
![Deploy and Manage Amazon RDS](/images/windows-on-aws-database.jpg)

---
### Infrastructure Explanation
For this architect diagram, the infrastructure has Amazon RDS Service as a new entity. Basically, there is not any difficult to understand the infrastructure as we have already familiar with. Hence, i am going to do a quick explanation as follow:
- Functional Server: For the lab purpose, this EC2 will take roles in: AD-Manager and Database service for logging into the Amazon RDS instance. Infact, by the reality situation, we should not do this. We must separate to another EC2 Databse Service in a private subnet for security purpose as well as easy to work with and to maintain  
- Amazon RDS: this is a new entity in our infrastructure. The Amazon RDS will join into the AWS Managed Directory Service. Also, we will use the functional server as a database service bastion to log into the Amazon RDS instance.
---
**Things to understand before doing this lab**

- [Creating Your AWS Account](https://000001.awsstudygroup.com/)
- [Setting up Budget for your Cloud Journey](https://000007.awsstudygroup.com/)
- [VPC - Virtual Private Cloud - Introducing and Getting to know](https://000003.awsstudygroup.com/)
- [EC2 - Introducing and Getting to know](https://000004.awsstudygroup.com/)
---
If you have not ready for the deep-dive into AWS Services - Windows On AWS. Please refer to this link for [Basic Windows On AWS](https://github.com/minhhung1706/Windows-On-AWS-Series/tree/main/Windows-On-AWS-Basic)

Once you have done all of those labs, i understand that you are ready to deep dive into the cloud. Let's get your hand dirty !

--- 
