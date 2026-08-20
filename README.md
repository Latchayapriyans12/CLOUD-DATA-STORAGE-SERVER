
## NAME: Latchaya priyan S
## REG NO: 212224230139

## Aim

To create and configure an Amazon Relational Database Service (Amazon RDS) instance as a cloud data storage server, configure the required security settings, connect it to a web application, and perform database operations using the application.

## Algorithm / Steps

1. Create a Security Group for the RDS database.
2. Add an inbound rule to allow MySQL (Port 3306) access from the Web Security Group.
3. Create a DB Subnet Group using two Availability Zones.
4. Launch an Amazon RDS MySQL database instance.
5. Configure the database with the required identifier, username, password, storage, and instance class.
6. Associate the database with the created Security Group and Subnet Group.
7. Wait until the database status becomes **Available**.
8. Copy the RDS endpoint.
9. Open the web application using the provided Web Server IP address.
10. Enter the RDS endpoint, database name, username, and password.
11. Connect the application to the database.
12. Verify the connection by adding, editing, and deleting records in the Address Book application.


## Program

### Security Group Configuration

* Security Group Name: **DB Security Group**
* Inbound Rule: **MySQL/Aurora (3306)**
* Source: **Web Security Group**

### DB Subnet Group

* Name: **DB-Subnet-Group**
* VPC: **Lab VPC**

### Amazon RDS Configuration

* Engine: **MySQL**
* Template: **Dev/Test**
* Availability: **Multi-AZ**
* DB Instance Identifier: **lab-db**
* Username: **main**
* Password: **lab-password**
* Instance Class: **db.t3.micro**
* Storage: **20 GB (General Purpose SSD)**

### Connect the Application

```text
Endpoint : <RDS Endpoint>
Database : lab
Username : main
Password : lab-password
```

After submitting the above details, perform Add, Edit, and Delete operations on the Address Book application.

## Output

<img width="969" height="656" alt="image" src="https://github.com/user-attachments/assets/49735e6f-7b2d-4d36-8c24-7bc3f8c49170" />


<img width="968" height="604" alt="image" src="https://github.com/user-attachments/assets/d1573b6a-87f1-4b07-883c-e99638ddd247" />

<img width="978" height="663" alt="image" src="https://github.com/user-attachments/assets/efc42385-9522-4503-9eb5-1304241138dd" />


<img width="960" height="646" alt="image" src="https://github.com/user-attachments/assets/33778b1b-c2e8-41bd-a5ce-68b4e8a07d82" />


<img width="971" height="199" alt="image" src="https://github.com/user-attachments/assets/a5c62792-2d1b-4eba-ac5c-d1bdd3a36c0a" />


<img width="891" height="279" alt="image" src="https://github.com/user-attachments/assets/702929fe-6c74-4f65-b723-9058c9d21a71" />



## Result

Thus, an Amazon RDS database instance was successfully created and configured as a cloud data storage server. The database was securely connected to a web application, and data operations such as inserting, updating, and deleting records were successfully performed through the application.

