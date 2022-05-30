**Basic Infrastructure Explanation** 
- Region: this is AWS available regions which are can be considered as a physical AWS Datacentres. They are located around the globe
- Availability Zone: this is the available zone that can be used to deploy AWS resources. We can consider them as a datacentre in so many of AWS datacentre. 
- For example, we have a physical AWS Datacentre named A (AWS Region). Inside that A region, we have so many datacentres which are built by AWS. Each datacentra like this can be considered as an Availability Zone (AZ)  
- VPC - Virtual Private Cloud: This can be considered as a DMZ (Demilitary Zone) on on-premise infrastructure. By AWS, VPC is logically separated your infrastructure. Which mean, 2 VPC in the same AZ cannot communicate/connect to each other. Instead, we must setup and configure some services so that the 2 VPC can communicate to each other. 
- Public subnet: the subnet that exposed to the internet. In other word, for those of AWS resources which are deployed inside a public subnet can be connected to the internet
- Private subnet: the subnet that cannot connect to the internet.
- Internet Gateway (IGW): this is a special component of AWS service to let your infrastructures, which are deployed inside a public subnet can connect to the internet. Infact, the IGW transfers your private subnet become a public subnet. Because of by default, all of subnet inside a VPC is completely private, except we deploy an IGW.
- NAT Gateway (NGW): deploy inside a public subnet and route to internet. Private subnet will route to a NGW to be able to securely connect to the internet. The crucial thing about NGW: NGW by default only allow services which inside private subnet connect to internet. NOT TO allow in comming connection to the VPC=>Private Subnet.
- EC2 - Elastic Cloud Compute: this is the virtual server which is provisioned by AWS underline system. There are so many of EC2 families so that we can choose to use depends on what we need. For example: compute optimized, network optimized, graphical ec2, bare metal, hypervise/hypervisor, etc. There is a special EC2: t2.micro which is free to use and limited by 720hrs running. AWS EC2 is supports for most of available OS in the market: RedHat Fedora, Windows, Mac OSX (recently supported), Ubuntu, so many other Linux distroes. We can bring our own licence, using of AWS market, using of licenced AWS partner OS (Microsoft, for example). 
![Basic Diagram - Windows Server on AWS](images/windows-on-aws-basic-diagram.jpg)

**Detailed Infrastructure Explanation** 
- EC2 - Bastion Host: used as a remote desktop gateway (RDGW) which is deployed inside a public subnet. So that, we will use this instance to remotely connect to the private subnet
- EC2 - Windows Server 2022: an EC2 instance which is running Windows Server 2022
