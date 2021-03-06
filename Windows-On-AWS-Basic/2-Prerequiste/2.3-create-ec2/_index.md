### Create EC2

In this section, we will create a EC2. 
- AWS recently has been developing new EC2 Management Console. Hence, pay attention to the top of your browser to see if there is anything inform from AWS. Click to switch to new EC2 Management Console
- New EC2 Management Console will help you to choose: ec2 instance family, operating system, create/choose security group, tag, create/choose key pair, attach EBS, etc.
- However, the new EC2 Management Console WILL NOT let you to join domain incase of you have the AWS Managed Directory service created (will have lab for it)
- Currently, using the old EC2 Management Console is highly recommended
---
### Steps to create EC2 - Windows Server
1. At EC2 Management Console => Check to see if you are in the right region. If not, change to your desired region
2. Left hand-side menu => Instances => Launch Instances
  ![EC2](images/ec2-1.jpg)
3. This is the NEW EC2 Management Console. 
   - To pay attention on the top right, there is a button that can switch to OLD console which is fully functions and options
   - Name your EC2
   - Choose OS: Windows
   - Choose AMI (Amazon Machine Images): Windows Server 2022 Base - Free Tier Available
  ![EC2](images/ec2-2.jpg)
4. Follow those steps in the picture bellow to continue to configure EC2
  ![EC2](images/ec2-3.jpg)
   - Key pair: choose your keypair. If you did not have one, click Create Keypair
   - Follow this link for AWS Documentation about how to create a keypair in some different ways 
   - [AWS Doc - How to Create a Keypair](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/create-key-pairs.html)
   - Remember for Windows instance: RSA for keypair type and then save as PEM for remote desktop service
   - At the Network Settings, Click Edit to be able to access to the options.
   - Choose VPC 
   - Subnet: Public 
   - Auto Assigned Public IP: Enable => This is a bastion host, we need public ip to log-in from our place
   - Security Group: Choose the default one which coresponeded with your VPC. 
   - **If your AWS Account is new created, there is a default VPC and Security Group. Becareful to choose the one which is attached to your VPC, otherwise, you will not be able to connect to your ec2 instance**
5. Configure Storage and some other options as follow
  ![EC2](images/ec2-5.jpg)
   - The remainning options just do not configure, leave them as default as they are. Then, click Launch Instance
   - The OLD console will prompt you to choose a keypair when you click Launch Instance whereas the NEW console will not prompt you anything
   - Click View All Instances to see the instance is launching. Take a closer look to the **instance State**. It will change from Pending to Running
   - Then, take a closer look to **Status Check**. It will change from Initializing to 2/2 Checked Pass. Once your Status Check is 2/2 Checked Pass, you will be able to use your intance
  ![EC2](images/ec2-6.jpg)
6. Let's make another instance. However, change some option as follow:
  - Name: sever-2022 (or something you like)
  - Subnet: Private  
  - Auto Assigned Public IP: Disable => We do not want our important server to    be exposed to the internet
7. 
   - After finished, we will have 2 EC2 instance as followed: 
   - Bastion: used as remote desktop gateway | Public Subnet | has public ip 
   - Server (name as your desired): used as a main servers | Private Subnet | DOES NOT have public IP
  ![EC2](images/ec2-6-1.jpg)
