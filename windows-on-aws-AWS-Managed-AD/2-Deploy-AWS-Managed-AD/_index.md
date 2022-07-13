- If you have not ready for the infrastructure, please refer to this link for basic setup: [Basic Windows On AWS](https://github.com/minhhung1706/Windows-On-AWS-Series/tree/main/Windows-On-AWS-Basic)
- Let assumed that you are fully prepared to deep-dive into AWS Services - AWS Directory Service
- Reminding about the basic setup to prepare for deploying the AWS Managed AD:
  - VPC, Subnet, Internet Gateway, NAT Gateway must be created
  - Availability Zone must be from 2 zones and more
  - IAM Role with all of neccessary permissions must be created
  - Your AWS Account should have enough permission to perform this lab. Recommended to use your own AWS Account
---
### Deploy AWS Managed Directory Service
1. AWS Management Console => Search for Directory Service
2. At AWS Directory Service management console => Set up directory
  ![setup directory](images/setup-ad-1.jpg)
3. Choose AWS Managed Microsoft AD => Next
   ![setup directory](images/setup-ad-2.jpg)
4. Depends on your business needs. Manually choose the right Directory Service. For this lab purpose, choose Standard Edition
5. Then, fill in all of required information: Fully Qualified Domain Name (FQDN), NetBios Name, Description (optional), password
   - By default, the AWS Managed AD account is Admin (case sensitive)
   - Do not worry about the price, the lab last long 2~4hrs. Do not cost too much. However, remember to delete the resources included this Directory Service after completed the lab
  ![setup directory](images/setup-ad-3.jpg)
  ![setup directory](images/setup-ad-3-a.jpg)
6. Then click Next
7. Choose the right VPC and Subnet. Remember, at least 2 subnet in 2 different availability zone (az).
8. Must be private subnet for security best practices. Then click NEXT
  ![setup directory](images/setup-ad-4.jpg)
9. Double check all of the required information => Create Directory
  ![setup directory](images/setup-ad-5.jpg)
10. The directory creation might take a bit long, roundly 40 minutes. 
11. After finished, we will see our directory has been created
  ![setup directory](images/setup-ad-6.jpg)
12. We are done for setting up AWS Managed AD 
---
### Deploy EC2
- Let assumed that we are all know how to deploy EC2. 
- However, the basic guide has already mentioned about the EC2 Management Console
- The NEW EC2 Management Console is still under development. Hence, it will not let us join domain and some other setup
1. Switch back to the OLD EC2 Management Console => Top right: Opt-out to the old experience
  ![setup ec2](images/ec2-setup-1.jpg)
2. This is the OLD UI which we familiar with
  ![setup ec2](images/ec2-setup-2.jpg)
3. Follow up the step 
   - Choose / fill in the right option / information and click NEXT
   - Remember to attach the IAM Role which have some of the required permissions to be able to work with Directory Service
   - After click **Next Add Storage**, those further steps are exactly the same with the basic guide about how to setup an EC2.  

  ![setup ec2](images/ec2-setup-3.jpg)
4. The EC2 should be:
    - 1 EC2: t2.micro | Bastion host | Public subnet | Auto-assign Public IP: Enable
    - 1 EC2: t2.2xlarge | AD-Manager | Private subnet | Auto-assign Public IP: Disable
5. Finally, we will have some running EC2 look like this:
  ![setup ec2](images/ec2-setup-4.jpg)
6. We are done for setting up EC2

