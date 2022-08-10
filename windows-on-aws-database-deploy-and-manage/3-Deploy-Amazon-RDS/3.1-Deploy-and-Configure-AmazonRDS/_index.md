### Deploy Amazon RDS
---
1. Navigate to the AWS Management console and search for Amazon RDS Service. This is the Amazon RDS Management Console
![Deploy Amazon RDS](../images/deploy-rds-1.jpg)  

2. At the left hand-side menu, click to the Database
![Deploy Amazon RDS](../images/deploy-rds-2.jpg)  

3. Then, click the Create Database
![Deploy Amazon RDS](../images/deploy-rds-3.jpg)  

4. Standard Create => Microsoft SQL => Amazon RDS
![Deploy Amazon RDS](../images/deploy-rds-4.jpg)  

5. Configure as follow:
   - SQL Server Standard Edition
   - Version: Drop-down menu => choose the latest available
   - Templates: Dev/Test => in the real world scenario, you can choose either production OR dev/test. All is based on what you need for your environment.
   - DB Instance Identifier: name your DB
![Deploy Amazon RDS](../images/deploy-rds-5.jpg)  

6. Credentials Setting:
   - Master Username: admin => default. You can change it if you want to
   - Master Password: create your desired password. Or you can choose auto generate password. Then, remember to save the password
   - Instance Class: Standard
   - Drop-down menu for instance size: choose the first one (lab purpose) which available in your region. My region might different from yours. In the real case, instance size should be depends on what your organization need
![Deploy Amazon RDS](../images/deploy-rds-6.jpg)  

7. Continue to set up
   - Storage type: General Purpose (GP2) => there are some other types of storage, but for the lab, we just choose GP2
   - Allocate Storage: db storage capacity => choose as much as you want. Remember, maximum is 16 TB (16,384 Gib)
   - Enable Auto Scaling
   - Maximum Storage Threshold: your db storage will auto scale up to the threshold. Remember, once you exceed the threshold, you will be charged for extra storage service. Planning wisely before setup. Understand your current DB workload so that you can avoid unecessary charge
   - Multi AZ Deployment: for this lab: NO | For your real environment: need to take into a consideration for high-availability and fail-over 
![Deploy Amazon RDS](../images/deploy-rds-7.jpg)  

8. Continue to set up
   - Do as follow the guide figure
   - For Availability Zone: Double check your subnet setting to see which zone that your subnet is configured. Then choose your db AZ followed by your subnet AZ
![Deploy Amazon RDS](../images/deploy-rds-8.jpg)  

9. Join the Amazon RDS instance to AWS Managed AD => then double check and click Create Databse
    **==>** Do not worry about the price. For the lab purpose only few hours. Then, you will not be charged as the price showed
![Deploy Amazon RDS](../images/deploy-rds-9.jpg)
![Deploy Amazon RDS](../images/deploy-rds-10.jpg)
![Deploy Amazon RDS](../images/deploy-rds-11.jpg)  

10. It takes about 30 to 40 minutes for the database to be created. For multi-az deployment, it should take a bit longer.  

11. After around about 40 minutes, our Amazon RDS instance has been successfully created. To pay attention to those information which is bordered. Especially the End-point. We will need it later
![Deploy Amazon RDS](../images/deploy-rds-12.jpg)  


   