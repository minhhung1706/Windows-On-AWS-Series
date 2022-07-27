In this section, we will start to clean up all of the services to avoid unexpected charge from AWS  

---
1. Terminate all EC2  
![Clean Up Services](../images/clean-up-services-1.jpg)  
![Clean Up Services](../images/clean-up-services-2.jpg)  

2. Delete AWS Directory Service   
![Clean Up Services](../images/clean-up-services-4.jpg)  
![Clean Up Services](../images/clean-up-services-3.jpg)  

3. Delete ALl Security Group Rules: do for both inbound and outbound
![Clean Up Services](../images/clean-up-services-5.jpg)  
![Clean Up Services](../images/clean-up-services-6.jpg)  
![Clean Up Services](../images/clean-up-services-7.jpg)  

4. Delete Peering Connection
![Clean Up Services](../images/clean-up-services-8.jpg)  
![Clean Up Services](../images/clean-up-services-9.jpg)  

5. Delete NAT Gateway
   Due to the purpose of the lab, we had 2 VPCs; hence, we had 2 NAT Gateway. Just delete all of them
![Clean Up Services](../images/clean-up-services-10.jpg)  

6. Delete Internet Gateway
   Due to the lab purpose, we had 2 IGW. Just delete both of them
![Clean Up Services](../images/clean-up-services-11.jpg)  
![Clean Up Services](../images/clean-up-services-12.jpg)  
![Clean Up Services](../images/clean-up-services-13.jpg)  
![Clean Up Services](../images/clean-up-services-14.jpg)

7. Delete VPC
   Due to the lab purpose, we had 2 VPCs. Just delete both of them  
![Clean Up Services](../images/clean-up-services-15.jpg)  
![Clean Up Services](../images/clean-up-services-16.jpg)  

8. Delete Elastic IP:  
   If you left the un-used Elastic IP. You would be charged for the IP service
![Clean Up Services](../images/clean-up-services-17.jpg)  
