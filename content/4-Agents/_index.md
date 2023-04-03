---
title : "AWS Replication Agents "
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

#### AWS Replication Agents 

1. We will add a source server. Select Add server.

![Application Migration Service](/images/4/0003.png?featherlight=false&width=90pc)

2. If you have not created an Access key yet, you can go to your User settings and create one. Under the Access keys section, select Create access key. If you already have two Access keys, this button will be disabled, and you must delete one Access key before creating a new one.

![Application Migration Service](/images/4/0004.png?featherlight=false&width=90pc)

3. On the Access key best practices & alternatives page, select your use case to learn about additional options that can help you avoid creating a long-term access key. If you determine that your use case still requires an access key, select "Other" and then select "Next".

![Application Migration Service](/images/4/0005.png?featherlight=false&width=90pc)

4. (Optional) Set a description tag value for the access key. This adds a key-value pair tag to your IAM user. This can help you identify and rotate the access keys in the future. The tag key is set to the access key ID. The tag value is set to the access key description you specify. Once you're done, select Create access key.

![Application Migration Service](/images/4/0006.png?featherlight=false&width=90pc)

5. On the Retrieve access keys page, select Show to display your user's secret access key value or select Download .csv file. This is your only chance to keep your secret access key. Once you have securely saved your secret access key, select Done.

![Application Migration Service](/images/4/0007.png?featherlight=false&width=90pc)

6. Copy the Access key and run commands 4 and 5 on the terminal.
- Make sure that the necessary service roles have been created by clicking the Reinitialize service permissions button on the Replication setup page of the Application Migration Service Console. You must have the necessary permissions to create IAM roles to successfully perform this operation.

- Download the Agent installer using the wget command on your source Linux server. This wget command will download the Agent installation file - aws-replication-installer-init.py to your server.

- The Agent installer is formatted as follows: https://aws-application-migration-service-<region>.s3.<region>.amazonaws.com/latest/linux/aws-replication-installer-init.py. Replace <region> with the AWS Region you are copying to.

Below is an example of the full wget command for us-east-1:

```
wget -O ./aws-replication-installer-init.py https://aws-application-migration-service-us-east-1.s3.us-east-1.amazonaws.com/latest/linux/aws-replication-installer-init.py
```

- The command line will indicate when the installer has been successfully downloaded.

- After the Agent installer has been downloaded successfully, copy and enter the installation command on the command line of your source server to run the installation script.

```
sudo python3 aws-replication-installer-init.py
```

- If you need further customization, you can add various parameters to the installation script to control how the Agent is installed on your server. Add the parameters to the end of the installation script.

![Application Migration Service](/images/4/0008.png?featherlight=false&width=90pc)

7. The terminal will prompt you to enter your AWS Region name, AWS Access Key ID, AWS Secret Access Key (and AWS Session Token if appropriate) that you have created previously. Enter the full name of your AWS Region (e.g., eu-central-1), full AWS Access Key ID, and full AWS Secret Access Key.
After you have entered your login information, the installer will determine which drives need to be copied. The installer will display the identified disks and ask you to select the disks that you want to copy.

   - To copy specific drives, enter the path of the drives, separated by commas, as illustrated in the installer (e.g., /dev/sda, /dev/sdb, etc.). To copy all drives, press Enter. The installer will identify the selected drives and print their sizes.

   - The installer will confirm that all disks have been successfully identified.

![Application Migration Service](/images/4/0009.png?featherlight=false&width=90pc)