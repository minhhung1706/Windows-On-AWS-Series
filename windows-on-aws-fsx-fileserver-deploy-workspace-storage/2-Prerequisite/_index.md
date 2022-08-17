### Preperation
---
![FSx Windows File Server](../images/fsx-workspace-storage.jpg)  

---
- 1 VPC
- 2 Public Subnet
- 2 Private Subnet
- 1 Internet Gateway
- 1 NAT Gateway
- 1 AWS Managed AD
- 1 FSx: Single AZ deployed (lab purpose)
- 1 EC2: Bastion | Public Subnet | Public IP enable: YES | Joined AWS Managed AD (optional)
- 1 EC2: Functional Server: AD Manager and File Server (lab purpose only) | Private Subnet | Public IP enable: NO | Joined AWS Managed AD
- 1 ~ 2 WorkSpaces: Joined Domain
- WorkSpaces Client installed on your place