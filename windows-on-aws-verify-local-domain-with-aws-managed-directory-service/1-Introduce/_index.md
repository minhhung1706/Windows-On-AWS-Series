### Introduction
---
AWS Managed Directory Service has ability to work with the local domain. However, before they can work (verified) each other, we need to understand some of the concept about the infrastructure and then jump into the hands-on which will help us to gain more experiences about system and network integration.

Moreover, working with AWS in term of system-integrated, we do not have to build everything from scratch. What does it mean ?, this is mean that we can eliminate some works such as: network configuration, AWS assist us in this task via AWS built-in SDN (Software Defined Network). 

Our task is to use and to focus on our infrastructure and put all of AWS services to work together.

---
### Architect Diagram

![Verify Local Domain With AWS Managed Directory Service](../images/verified-local-domain-with-aws-directory-service.jpg)

---
### Infrastructure Explannation

As usual, we are so much familiar with the infrastructure which is pretty easy to understand and to work with. 

What we have here ==> 2 Sites:
**1. AWS Site:** 
We have EC2, NAT Gateway, Internet Gateway, AWS Managed Directory Service
**2. Local Site:**
We also have EC2, NAT Gateway, Internet Gateway  
**Similarity of 2 Sites:**
- They are both in the same region
- They are both able to connect to the internet
- They are both can communicate with each other in either IP Address or Computer Name (of course, we need to configure them)  
- All of the services inside a VPC can work/communicate together. Additionallly, it is also depends on the real case scenario.  
**Differences of 2 Sites:**  
- The 2 Sites are localed in different Availability Zone
- The 2 Sites have different IP Address Range
- The 2 Sites are designed in differnt VPC
- The 2 Sites might not share the same Network Infrastructure and Network Design due to the reality of this lab and the real-world scenario. It is also depends on what does your business needs. 


