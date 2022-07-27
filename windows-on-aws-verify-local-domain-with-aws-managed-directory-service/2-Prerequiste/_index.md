### Preparation
---
**I. General Preparation:**  
Both of **AWS Site** and **Local Site** are located on AWS in the same region.  

**II. AWS Site**  
- 1 VPC  
- 2 Public Subnet  
- 2 Private Subnet 
- Recommended Instance size: t3.xlarge => For better network performance (Up to 5 Gigabit Network Performance) 
- 1 EC2: Bastion  
- 1 EC2: Active Directory Manager  
- 1 NAT Gateway  
- 1 Internet Gateway  
- 1 AWS Managed Directory Service:   
  => Standard Edition  
  => High Availability Congifured: Desinged and Implemented on 2 Private Subnet  
  => Inside the AWS Site VPC  

**III. Local Site**  
- 1 VPC  
- 2 Public Subnet  
- 2 Private Subnet 
-  Recommended Instance size: t3.xlarge => For better network performance (Up to 5 Gigabit Network Performance)  
- 1 EC2: Bastion  
- 1 EC2: Built our own Active Directory  
- 1 NAT Gateway  
- 1 Internet Gateway  

**IV. VPC Peering:**  
- Quantity: 1  
- Setup: VPC Peering is setup and configured so that both of the VPC can communicate together  

---

![Verify Local Domain With AWS Managed Directory Service](../images/verified-local-domain-with-aws-directory-service.jpg)
