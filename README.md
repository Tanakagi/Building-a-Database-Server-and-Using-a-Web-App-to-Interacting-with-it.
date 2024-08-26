# Building-a-Database-Server-and-Using-a-Web-App-to-Interacting-with-it.

In this project, I created a highly available Relational Database Server and Interact with my DB Using a web App.

## In this Project I did the following:

<b>• Launch an Amazon RDS DB instance with high availability.</br>
<b>• Configure the DB instance to permit connections from your web server.</br>
<b>• Open a web application and interact with your database.</br>

## AWS services used:
<b> **• Amazon EC2** - used to host the web application.</br>
<b> **• Amazon RDS**: - used to connect to the web application and receive information from it.</br>
<b> **• Amazon VPC and subnets** - used to tell RDS which subnets can be used for the database.</br>
<b> **• Internet Gateway** - used to provide internet access for the web app.</br>
<b> **• NAT Gateway** - used to control and secure network routing.</br>
<img src="" height="80%" width="80%" />

# Project walk-through:

### Task 1: Creating a Security Group for the RDS DB Instance

<b>• In this task, I created a security group to allow my web server to access my RDS DB instance.</br> 
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
</br>
</br>
</br>

### Task 2: Creating a DB Subnet Group

<b>I  created a DB subnet group that is used to tell RDS which subnets can be used for the database.</br>
<b>Each DB subnet group required subnets in at least two Availability Zones to make it more available.</br>

<b>• In the AWS Management Console, I selected RDS under Database.</br>
<b>• In the left navigation pane, I clicked on Subnet groups.</br>
<img src="" height="50%" width="50%" />
</br>
</br>

<b>• In the Add subnets section for Availability zones, I selected the 2 AZ’s.</br>
<b>• For Subnets, I selected 2 subnets.</br>
<b>• This adds Private Subnet 1 (10.0.1.0/24) and Private Subnet 2 (10.0.3.0/24).</br>
<b>I will use this DB subnet group when creating the database in the next task.</br>
<b>• I then Created the DB subnet group.</br>
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
</br>
</br>
</br>

 ### Task 3: Creating an Amazon RDS DB Instance

<b>In this task, I configured and launched a Multi-AZ Amazon RDS for MySQL database instance named lab_db.</br>
<b>• In the Databases page I clicked create database.</br>
<img src="g" height="80%" width="80%" />
</br>
</br>

<b>• I configured the Database as follows:</br>
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
</br>
</br>


<b>• Under Instance configuration, I configured the following for the DB instance class:</br>
<b>• Under Storage, I configured the following:</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• Under Connectivity, I configured the following:</br>
<img src="" height="80%" width="80%" />
</br>
</br>


<b>• Under VPC security group I selected "Choose existing":</br>
<b>• Under "Existing VPC security groups" I did the following:</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• Under Monitoring, I expanded Additional configuration and then configured the following:</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I scroll down to the  Additional Configuration section and expand this option. I configured the following:</br>
<b>This will turn off backups, which is not normally recommended but will make the database deploy faster for this project.</br>
<b>• I then created the Database.</br>
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
</br>
</br>
</br>

 ### Task 4: Interacting with the Database

<b>In this task, I opened the web application running on my web server and configured it to use the database.</br>

<b>• I opened a new web browser tab and typed the WebServer IP address.</br>
<b>• At the top of the web application page, I clicked the RDS link.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I then configured the application to connect to my database.</br>
<b>• filled in the following lab_db information in the open fields, and clicked submit</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>A message  appeared explaining that the application is running a command to copy information to the database.</br>
<b>After a few seconds, the application displayed an Address Book.</br>
<b>The Address Book application uses the RDS database to store information.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I then clicked Save intent and Build to save the changes</br>
<b>• I then started the 3rd round of testing the chatbot.</br>
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I then tested the web application by adding, editing and removing contacts.</br>
<b>The data was persisted to the database and  automatically replicated to the second Availability Zone.</br>
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
</br>
</br>
</br>

## End of project.

This was the end of my project as I was able to successfully Build a Database Server and Interact with my DB Using the web App.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

