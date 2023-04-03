---
title : "Launch the test instances"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 6. </b> "
---

#### Launch the test instances

1. Return to the MGN interface and observe that it is in the Ready for testing state.

![Application Migration Service](/images/4/00021.png?featherlight=false&width=90pc)

2. Select "Replication", then select "Launch test instance".

![Application Migration Service](/images/4/00023.png?featherlight=false&width=90pc)

3. The status will change to Test in progress.

![Application Migration Service](/images/4/00024.png?featherlight=false&width=90pc)

4. If you check the EC2 instance, you will see a Replication server.

![Application Migration Service](/images/4/00025.png?featherlight=false&width=90pc)


5. View job details.

![Application Migration Service](/images/4/00026.png?featherlight=false&width=90pc)

6. Go back to check the EC2 instance. You will see an additional Conversion Server appear.

![Application Migration Service](/images/4/00027.png?featherlight=false&width=90pc)

7. Go back and check the detailed next steps of the job.

![Application Migration Service](/images/4/00028.png?featherlight=false&width=90pc)

8. You will see an instance being created.

![Application Migration Service](/images/4/00029.png?featherlight=false&width=90pc)

9. After the EC2 instance state transitions to 2/2 checks passed, you copy the Public IPv4.

![Application Migration Service](/images/4/00030.png?featherlight=false&width=90pc)

10. Use MobaXterm to SSH into an EC2 instance.
- Enter the Remote host information.
- For the username, enter the user that was created, for example: fcjuser
- Select OK.

![Application Migration Service](/images/4/00031.png?featherlight=false&width=90pc)

11. Password and SSH successfully entered.

![Application Migration Service](/images/4/00032.png?featherlight=false&width=90pc)

12. Perform a check on the database file configuration in the .env file and start the application by running:

```
npm start
```
![Application Migration Service](/images/4/00033.png?featherlight=false&width=90pc)

13. Access the public IP and port 5000:

```
IP:5000
```
