### Cleaning up the resources

1. EC2 Management console => Choose Instances => Click to choose All Instances => Choose instance state => Terminate
![Clean-up](images/cleanup-1.jpg)

2. For the lab purpose, just click Terminate
![Clean-up](images/cleanup-2.jpg)

3. Pay attention to Instance State, it will change from **Shutting down** to **Terminated**. Once the instance state at Terminated, this is mean your instance(s) has completely deleted => **No Extra cost** will be charged from now.
![Clean-up](images/cleanup-3.jpg)  
![Clean-up](images/cleanup-4.jpg)
    - **If there were ONLY Stopped at instance state, which mean you still be charged for storage service due to the attached EBS (Elastic Block Storage)**
    - **Carefully choose the right option depends on your need if you would like to STOP or TERMINATE the instance(s)**
  
4. Navigate to VPC management console 
   - Route Table
   - Choose Public Route
   - Remove the IGW (internet gateway) from the public route
![Clean-up](images/cleanup-7.jpg)  
![Clean-up](images/cleanup-8.jpg)

5. We do the same thing for the Private routes. However, we will remove the NAT Gateway. Do for both our private routes
![Clean-up](images/cleanup-9.jpg)
![Clean-up](images/cleanup-10.jpg)

6. Removing the NAT Gateway
![Clean-up](images/cleanup-11.jpg)
![Clean-up](images/cleanup-12.jpg)
    - It takes a while (3 mins) for the NAT Gateway to be deleted
![Clean-up](images/cleanup-13.jpg)  

7. Removing Internet Gateway
   - Detach IGW from VPC
   - Delete Internet Gateway
![Clean-up](images/cleanup-5.jpg)
![Clean-up](images/cleanup-6.jpg)
![Clean-up](images/cleanup-14.jpg)  

8. Deleting VPC
   - Navigate to VPC 
   - Choose the VPC you want to (need to) delete
   - Action => Delete VPC => Confirm Delete
   - As can be seen, everything included the route tables, subnets and vpc will be deleted
![Clean-up](images/cleanup-15.jpg)  
![Clean-up](images/cleanup-16.jpg)  

9. Deleting Elastic IP
    - If you left the Elastic IP UN-USED => you will be charged for the IP service
    - If Elastic IP is IN-USED => you will not be charged
    - Choose the right Elastic IP that need to be deleted
![Clean-up](images/cleanup-17.jpg)  
![Clean-up](images/cleanup-18.jpg)

---

## Finished all cleaning up the services. Do not forget this step, otherwise, you will be charged for the AWS Services

