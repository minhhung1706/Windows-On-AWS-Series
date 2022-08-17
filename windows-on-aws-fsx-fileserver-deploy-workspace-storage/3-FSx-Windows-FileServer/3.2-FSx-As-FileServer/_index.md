### FSx As File Server
---

1. Connect into EC2 Functional Server  

2. Open the File Explorer => Copy and paste the FSx DNS => Bu default, there is a share folder insde the FSx. We can make another folder as wished incase of we have some of different departments / branches / offices    
![fsx-as-fileserver](../../images/fsx-as-fileserver-2.jpg)
![fsx-as-fileserver](../../images/fsx-as-fileserver-4.jpg)    

3. Right click to the share folder => **Map Network Drive**
![fsx-as-fileserver](../../images/fsx-as-fileserver-5.jpg)  

4. Then click **Finished**
![fsx-as-fileserver](../../images/fsx-as-fileserver-6.jpg)  

5. Now, we will have the FSx at shared via the network
![fsx-as-fileserver](../../images/fsx-as-fileserver-7.jpg)  

6. Let's make 2 folder. Name as your desired. This is my 2 folders
![fsx-as-fileserver](../../images/fsx-as-fileserver-8.jpg)  

7. Open the Active Directory User and Computer:
   - Create 2 Groups 
   - Add 2 users which are created when we deploy the WorkSpaces. Each user belong to a group
![fsx-as-fileserver](../../images/fsx-as-fileserver-9.jpg)  



