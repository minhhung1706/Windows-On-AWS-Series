### EC2 Configuration 
---

We are now going to configure EC2 on both **AWS Site** and **Local Site**

---

**I. AWS Site**  
If you were not ready, then back to the basic guide before doing this lab. I assumed you have already leveled up your skills:  

In this site, what we need to do are:  
- Edit Computer Name
- Edit the IP Address
- Edit hosts file
- Install the neccessary Administrator Tools (basic guide)
- Test the communication between EC2 Bastion and EC2 AD-Manager  

![EC2 Configuration](../../images/ec2-configuration-1.jpg)  
![EC2 Configuration](../../images/ec2-configuration-2.jpg)  
![EC2 Configuration](../../images/ec2-configuration-4.jpg)  

---

**II. Local Site**  
We need to upgrade the EC2 in the private network to Domain Controller   

1. Open Server Mamanger to perform the tasks  
![EC2 Configuration](../../images/ec2-configuration-3.jpg)  
![EC2 Configuration](../../images/ec2-configuration-5.jpg)  
![EC2 Configuration](../../images/ec2-configuration-6.jpg)  
![EC2 Configuration](../../images/ec2-configuration-7.jpg)  
![EC2 Configuration](../../images/ec2-configuration-8.jpg) 
![EC2 Configuration](../../images/ec2-configuration-9.jpg)  
  
2. Promote the server to become a Domain Controller  
![EC2 Configuration](../../images/ec2-configuration-10.jpg)  
![EC2 Configuration](../../images/ec2-configuration-11.jpg)  
![EC2 Configuration](../../images/ec2-configuration-12.jpg)  
![EC2 Configuration](../../images/ec2-configuration-13.jpg)  
![EC2 Configuration](../../images/ec2-configuration-14.jpg)  

3. After the installation finished, the server will restart. Then, login again to check the server has become a Domain Controller  
![EC2 Configuration](../../images/ec2-configuration-15.jpg)  

4. Double check the IP Address of the Domain Controller. After restart, the DNS will be flushed and added a loopback address. Then re-configure it again  
![EC2 Configuration](../../images/ec2-configuration-16.jpg)  

5. Checking the Servers communication
![EC2 Configuration](../../images/ec2-configuration-17.jpg)  
![EC2 Configuration](../../images/ec2-configuration-18.jpg)  

---

**III. Testing Server Communication on both sites**
![EC2 Configuration](../../images/ec2-configuration-19.jpg)  
![EC2 Configuration](../../images/ec2-configuration-20.jpg)  
![EC2 Configuration](../../images/ec2-configuration-21.jpg)  
![EC2 Configuration](../../images/ec2-configuration-22.jpg)  






 

 





