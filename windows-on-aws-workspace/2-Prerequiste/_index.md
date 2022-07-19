### Preparation  

1. 1 VPC 
2. 2 Private Subnets
3. 2 Public Subnets
4. AWS Directory Service: Deploy an AWS Managed Directory Service
5. NAT Gateway
6. Internet Gateway
7. 1 EC2 - Bastion host
   - Public Subnet
   - Assigned Public IP: **Enabled**
   - IAM Role: Attached
   - Domain: Joined Domain
   - Modify hosts file and Computer name: recommended to do but not required
   - Modify IP: YES 
8. 1 EC2 - AD Manager
   - Private Subnet
   - Assigned Public IP: **Disabled**
   - IAM Role: Attached
   - Domain: Joined Domain
   - Modify hosts file and Computer name: recommended to do but not required
   - Modify IP: YES

Refer to the architect diagram bellow to centralized and double check your preparation for the lab

![Amazon Workspace](../images/aws-workspace.jpg)