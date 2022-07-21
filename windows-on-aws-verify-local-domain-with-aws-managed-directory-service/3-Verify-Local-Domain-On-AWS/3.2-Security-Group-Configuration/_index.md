### Security Group Configuration
---

We need to understand this before continue to configure the Security Group:  
- For quick and easy due to the **lab purpose**, we only have 3 Security Groups; however, in real world case study, we might have 30 Security Groups with stricly policies
- Those Security Groups are: 
  => 1 Default Security Group: AWS Site
  => 1 AWS Managed Directory Service Security Group: AWS Site
  => 1 Default Security Group: Local Site
![Security Group](/images/sg-1.jpg)
---

**Configure Security Group**  

1. Save/Copy the SG id of the other 2 SG of **AWS Site** so that we can work with it
![Security Group](/images/sg-2.jpg)  

2. At the SG Inbound:
   - Click Add Rule
   - Type: All Traffic
   - Paste the copied SG ID to the search box => choose it 
   - Do 1 by 1 SG ID, you cannot add 2 SG at the same time.
   - Check your result after finished to match the figure bellow. The SG ID in my case will be different from yours. But should be enough 2 SG IDs from the AWS-Site
   - Save Rule
![Security Group](/images/sg-3.jpg)  

3. You will want to do the same thing for the other 2 of AWS-Site SG. Then check the result so that:
   - **Local Site SG Inbound:** Added the 2 SG of **AWS Site**  
   - **AWS Site Default SG Inbound:** Added **Local Site SG** and **d_controller** (SG from AWS Managed Directory Service)  
   - **d_controller SG:** Added **AWS Site Default SG** and **Local Site SG**
   - You can name your SG so that we can understand which SG we are working on  
![Security Group](/images/sg-4.jpg)  
![Security Group](/images/sg-5.jpg)  
![Security Group](/images/sg-6.jpg)    

 
