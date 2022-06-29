### Access to Public Windows Instance
To gain access to our instance, we need to understand that we have 2 instance:
- Bastion instance: deployed at Public Subnet
- server-2022: deployed at Private Subnet
---

1. Click to **Choose the right** security group => Inbound => Edit Inbound Rule 
  ![EC2](images/ec2-7.jpg)
2. Add Rule => All Traffic (ONLY FOR LAB PURPOSE) => 0.0.0.0/0 => Save Rule
  ![EC2](images/ec2-8.jpg)
3. Navigate back again to EC2 Management Console => Instances => Choose bastion => Click Connect at top right 
  ![EC2](images/ec2-9.jpg)
4. Choose RDP Client => Click Get Password => Browse your keypair => Decrypt    Password => save the password
  ![EC2](images/ec2-10.jpg)
  ![EC2](images/ec2-11.jpg)
5. Back to the instance console => choose bastion => Details tab => copy the Public IP 
  ![EC2](images/ec2-12.jpg)
   - Paste to your remote desktop client (already built-in in windows) => click connect => you will be prompt for account and password: 
   - Account: Administrator (this is the default for most of Windows instances)
   - Password: paste the decrypt password above. Password IS NEVER the same for all the EC2 instances. It does not matter that your instance in the same subnet or az, the password is always different between the ec2 instances
   - This is a fully working Windows Server on AWS. The Windows Server is fully functional and not difference from your on-premise system
  ![EC2](images/ec2-13.jpg)

