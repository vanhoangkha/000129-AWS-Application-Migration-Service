---
title : "Launch Settings"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

#### Launch Settings

1. Please wait for about 5-10 minutes. You will see the Source server name.

![Application Migration Service](/images/4/00010.png?featherlight=false&width=90pc)

2. Configure the EC2 Launch Template

   - Select Source server name
   - Select Launch settings
   - Select Modify

![Application Migration Service](/images/4/00012.png?featherlight=false&width=90pc)

3. Select Modify.

![Application Migration Service](/images/4/00013.png?featherlight=false&width=90pc)

4. Maintain the AMI configuration.

![Application Migration Service](/images/4/00014.png?featherlight=false&width=90pc)

5. Keep the Instance type configuration unchanged.

- Select Create new key pair.

![Application Migration Service](/images/4/00015.png?featherlight=false&width=90pc)

6. Select Create key pair.

![Application Migration Service](/images/4/00016.png?featherlight=false&width=90pc)


7. Perform Networking configuration:
   - Choose the correct pre-defined subnet as shown in the Migrated Resource Subnet image.
   - Select Select existing security group.
   - Choose App Server Target.
   - For Auto-assign public IP, select Enable.

![Application Migration Service](/images/4/00017.png?featherlight=false&width=90pc)

8. Enter the description of the template version and then select Create template version.

![Application Migration Service](/images/4/00018.png?featherlight=false&width=90pc)

9. Select View launch templates.

![Application Migration Service](/images/4/00019.png?featherlight=false&width=90pc)

10. Select the recently created template. Then, choose Action and continue with selecting Set default version.

![Application Migration Service](/images/4/00020.png?featherlight=false&width=90pc)

11. Successfully changed the template version.

![Application Migration Service](/images/4/00022.png?featherlight=false&width=90pc)