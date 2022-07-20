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

**Similarities of 2 Sites:**  
- They are both on AWS  
- They are both in the same region
- They are both able to connect to the internet
- They are both can communicate with each other in either IP Address or Computer Name (of course, we need to configure them)  
- All of the services inside a VPC can work/communicate together. Additionallly, it is also depends on the real case scenario.  

**Differences of 2 Sites:**  
- The 2 Sites are localed in different Availability Zone
- The 2 Sites have different IP Address Range
- The 2 Sites are designed in differnt VPC
- The 2 Sites might not share the same Network Infrastructure and Network Design due to the reality of this lab and the real-world scenario. It is also depends on what does your business needs.  

The reason why we can simulate the Local Site and AWS Site both on AWS because of the VPC. By AWS VPC's definition: VPC is logically separate all of the infrastructure inside it. Which is mean that even though the infrastructures are located in the same region, they are still be isolated if we did not configure the VPC Peering to link all VPCs together.  

By that reason, we can completely simulate the real world case study about the Local Site and the AWS Cloud Site and implement to our work.

---

**Things to understand before doing this lab**

- [Creating Your AWS Account](https://000001.awsstudygroup.com/)
- [Setting up Budget for your Cloud Journey](https://000007.awsstudygroup.com/)
- [VPC - Virtual Private Cloud - Introducing and Getting to know](https://000003.awsstudygroup.com/)
- [EC2 - Introducing and Getting to know](https://000004.awsstudygroup.com/)
---
If you have not ready for the deep-dive into AWS Services - Windows On AWS. Please refer to this link for [Basic Windows On AWS](https://github.com/minhhung1706/Windows-On-AWS-Series/tree/main/Windows-On-AWS-Basic)

Once you have done all of those labs, i understand that you are ready to deep dive into the cloud. Let's get your hand dirty !

