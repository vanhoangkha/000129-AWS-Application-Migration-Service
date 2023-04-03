---
title : "Create an Access key"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

#### Create an Access key


In this section, we will create an IAM user and access key for MGN.

1. Access the AWS Console.

   - Search and select IAM
   - Select Users
   - Select Add users

![Application Migration Service](/images/2/0001.png?featherlight=false&width=90pc)

2. We perform filling in user information.

   - Enter the user name in the User name field
   - Select Provide user access to the AWS Management Console -optional
   - Select I want to create an IAM user
   - For Console password, select Custom password and enter the password you choose.
   - Select Users must create a new password at next sign-in (recommended)
   - Select Next

![Application Migration Service](/images/2/0002.png?featherlight=false&width=90pc)

3. Regarding Permission

   - Select Attach policies directly
   - Find and select AWSApplicationMigrationAgentInstallattionPolicy
   - Click Next

![Application Migration Service](/images/2/0003.png?featherlight=false&width=90pc)


4. Select Next and then select Create user. The user creation interface will appear indicating success.

![Application Migration Service](/images/2/0004.png?featherlight=false&width=90pc)

5. After successfully creating a user:

   - Select the user that has been created successfully.
   - Select Security credentials.
   - Select Create access key.

![Application Migration Service](/images/2/0005.png?featherlight=false&width=90pc)

6. Choose Command Line Interface (CLI)

   - Select I understand the above recommendation and want to proceed to create an access key
   - Click Next.

![Application Migration Service](/images/2/0006.png?featherlight=false&width=90pc)

7. Select Create access key.

![Application Migration Service](/images/2/0007.png?featherlight=false&width=90pc)

8. Complete the creation of Access key.

![Application Migration Service](/images/2/0008.png?featherlight=false&width=90pc)
