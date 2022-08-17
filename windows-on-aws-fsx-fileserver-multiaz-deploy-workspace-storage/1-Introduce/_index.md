### Introduction
---
First of all, we need to understand that what is Amazon FSx. Amazon FSx is a file system that allow us to deploy and configure so that become a storage service for our organization. There are so many benefit which FSx has brought to the storage industry:
- Simple to deploy and fully manage: we do not take to much time and effort to deploy FSx. In comparision with the traditional storage system, Amazon has already done all of the critical tasks in the background at Amazon Datacentre. Hence, we only need to make an AWS account and search for Amazon FSx Service and give it a try
- Fast and flexible: Amazon FSx support all type of enterprise work-load with low latency. Furthermore, Amazon FSx has also designed so that it can scale automatically when the storage exceeded the pre-configuration. Hence, we do not need to have the plan to purchase the physical HDD/SSD when planning for the storage service. That lead to cost saving for the business 
- Affordable: due to the scalable ability, Amazon FSx is not for enterprise business, it is also suitable for medium, small and start-up business. We only pay for the storage capacity that we need.
- High availability and durable: Amazon FSx has autobackup so that our data will be safe. Furthermore, it has also be able to deploy with High-Availability infrastructure; what does it mean, it means we can deploy FSx in multiple availability-zone (multi-az deployment) to ensure that our critical data always safe. Additionally, Amazon has also guaranty about the durability of the underlined hardware which used to build the Amazon FSx. So that, we do not have to worry about the hardware failure. 
- Secure and compliant: Amazon FSx brings to you a secured and global certified storage system. Amazon FSx has passed and met all of the requirement to archive the crucial globle recognized certificate for datacentre and storage services. Amazon FSx is designed to meet the highest security standards and has been assessed to comply with ISO, PCI-DSS, and SOC certifications, and is HIPAA eligible.
- Integration with AWS services: Amazon FSx is working perfectly with most of AWS services such as: able to join to the AWS Managed AD, S3, Cloud Watch, Cloud Trail, Sage Maker, etc. 
- For more information about Amazon FSx, please visit the link: [Amazon FSx](https://aws.amazon.com/fsx/)

---
### Architect Diagram  

![FSx Windows File Server](/images/fsx-workspace-storage.jpg)  

---
### Infrastructure Explanation

It is nothing too fancy, beside those friendly familiar services, we have new service as FSx For Windows. The infrastructure can be understood as followed:
- Amazon FSx for Windows Server will join into the AWS Managed AD. 
- As can be seen from the architecture diagram, the Amazon FSx is deployed as multi-az to perform high-availability and fail tolerance. This is the recommended infrastructure for most of enterprise business to keep the data safe and accessible. 
- However, due to the lab purpose, we only need to deploy FSx in single AZ, it help to save the cost for our cloud learning as well as saving time. Multi AZ deployment will cost more time to be finished. For this lab, we do not need to take much time to avoid overcharged out of learning-budget. 
- We will have the familiar WorkSpaces simulate as client. 
- WorkSpaces will be deploy FSx as a file storage for users
- User will need to install the WorkSpace application to connect to WorkSpaces. Or, user can log-in into WorkSpaces via website. To maximize the WorkSpace experiences, WorkSpaces client need to be installed as a recommendation.
- All of the connection is secured