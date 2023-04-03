---
title : "Prepare for Networking"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

#### Prepare for Networking.

1. First of all, we will prepare the network part for MGN.

   - To do this, access the AWS interface.
   - Search for VPC
   - Access the VPC interface.
   - Select Your VPCs
   - Choose Create VPC.

![Application Migration Service](/images/1/0001.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

2. In the Create VPC interface:

   - Select VPC and more
   - For Name tag auto-generation, you can enter an optional value.
   - Leave the other parameters at their default settings.

![Application Migration Service](/images/1/0003.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

3. Then, double-check and select Create VPC.

![Application Migration Service](/images/1/0004.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

4. Successfully create VPC for the Source server.

![Application Migration Service](/images/1/0005.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

5. Please refer to the Resource map section for more details.

![Application Migration Service](/images/1/0006.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

6. You select a subnet to test the subnet for the source server.

![Application Migration Service](/images/1/0007.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

7. Perform the modification to Public subnet.

- Select the newly created subnet, choose Edit subnet settings.

![Application Migration Service](/images/1/0008.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

8. In the subnet editing interface,

- Select Enable auto-assign public subnet IPv4 address.

![Application Migration Service](/images/1/0009.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

9. Next step, you need to create a Security group for the source server.

   - Select Security group
   - Choose Create security group.

![Application Migration Service](/images/1/00010.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

10. Name the SG and select the correct VPC that was just created.

![Application Migration Service](/images/1/00011.png?featherlight=false&width=90pc)

11. Configure as illustrated in the figure.

![Application Migration Service](/images/1/00012.png?featherlight=false&width=90pc)


12. Review the configuration and select "Create security group."

![Application Migration Service](/images/1/00013.png?featherlight=false&width=90pc)

13. Review the created security group.

![Application Migration Service](/images/1/00014.png?featherlight=false&width=90pc)

#### Prepare networking in Target region

1. Switch to the new region and create a VPC.

![Application Migration Service](/images/1/00015.png?featherlight=false&width=90pc)

2. Configure and select Create VPC.

![Application Migration Service](/images/1/00016.png?featherlight=false&width=90pc)

3. Complete the VPC creation and then modify the subnet as specified in the Source Region section.


![Application Migration Service](/images/1/00017.png?featherlight=false&width=90pc)

4. Similarly, create an SG for the target server.

![Application Migration Service](/images/1/00018.png?featherlight=false&width=90pc)