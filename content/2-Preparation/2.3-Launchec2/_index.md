---
title : "Launch the EC2"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

#### Launch the EC2

After preparing everything in terms of networking, we will launch an EC2 instance and install the Agent while also deploying the application.

1. Access the AWS Management Console

   - Find and select EC2
   - Choose Instances
   - Select Launch instances

![Application Migration Service](/images/3/0001.png?featherlight=false&width=90pc)

2. Configure EC2 by entering the Name and tag. For example, App - Source.

![Application Migration Service](/images/3/0002.png?featherlight=false&width=90pc)

3. Choose AMI as Ubuntu Server 20.04 LTS...

![Application Migration Service](/images/3/0003.png?featherlight=false&width=90pc)

4. Select the Instance type and create a Key pair.

![Application Migration Service](/images/3/0004.png?featherlight=false&width=90pc)

5. Configure and fill in information about the key pair.

![Application Migration Service](/images/3/0005.png?featherlight=false&width=90pc)

6. After successfully creating the EC2, we will SSH into it using MobaXterm.

![Application Migration Service](/images/3/0006.png?featherlight=false&width=90pc)

7. Add a user to perform login without using a keypair. Use the following command:

```
sudo adduser fcjuser
```

- Then choose Enter for the subsequent steps.

![Application Migration Service](/images/3/0007.png?featherlight=false&width=90pc)

8. Grant permission to the user:

```
sudo usermod -aG sudo fcjuser
```
![Application Migration Service](/images/3/0008.png?featherlight=false&width=90pc)

9.  Adjust the password login method.

```
sudo vi /etc/ssh/sshd_config
```

- Then change PasswordAuthentication to yes.

- Then press Esc and enter :wq!.

![Application Migration Service](/images/3/0009.png?featherlight=false&width=90pc)

10. Then, restart the SSH server.

```
sudo systemctl restart ssh.service
```
![Application Migration Service](/images/3/00010.png?featherlight=false&width=90pc)

11. You will have the option to choose to log in optionally.

![Application Migration Service](/images/3/00011.png?featherlight=false&width=90pc)

12. After that, you will log in using a user/password and won't need to use a keypair.

![Application Migration Service](/images/3/00012.png?featherlight=false&width=90pc)
