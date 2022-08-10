### Connect To Amazon RDS
---
1. To be able to connect into Amazon RDS, we need to download Microsoft SQL Server Management Studio and/or DBeaver
    - [Microsoft SQL Server Management Studio](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16)
    - [DBeaver](https://dbeaver.io/)  

2. Install both Microsoft SQL Server Management Studio and DBeaver. Just do the installation task as same as the other software, nothing special. The reason why i listed 2 DB tools just because of making more choice for everyone to choose the most suitable one to work with  

3. After installed both of the Database connection tool. Open Microsoft SQL Server Management Studio
![Database Connection](../../images/configure-db-connect-1.jpg)  

4. At the Object Explorer => Connect => Database Engine
![Database Connection](../../images/configure-db-connect-2.jpg)  

5. Back to the RDS Management Console => choose the created databse => copy the database endpoint
![Database Connection](../../images/configure-db-connect-3.jpg)  

6. Paste the End-point into the Server Name => choose the SQL Server Authentication => fill-in the user name and password => Click Connect
![Database Connection](../../images/configure-db-connect-4.jpg)  

7. We connected to the Amazon RDS successfully
![Database Connection](../../images/configure-db-connect-5.jpg)  

8. Right-click to Database => New Database => We are trying to create a new database to see double check the database is working perfectly
![Database Connection](../../images/configure-db-connect-6.jpg)
![Database Connection](../../images/configure-db-connect-7.jpg)  

9. We created our test_db successfully
![Database Connection](../../images/configure-db-connect-8.jpg)  

10. Close the SQL Server Management Studio. Open the DBeaver and do the connection to our Amazon RDS and double check if we see the test_db or not
![Database Connection](../../images/configure-db-connect-9.jpg)  

11. Fill-in the information and click finished
![Database Connection](../../images/configure-db-connect-10.jpg)  

12. We might be prompted to download some required data/file to be able to perform the connection. Just download them
![Database Connection](../../images/configure-db-connect-11.jpg)  

13. We successfully connected to Amazon RDS by using DBeaver
![Database Connection](../../images/configure-db-connect-12.jpg)  


