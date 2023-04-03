---
title : "Clean up resources"
date : "`r Sys.Date()`"
weight : 9
chapter : false
pre : " <b> 9. </b> "
---

#### Clean up resources

1. On the MGN interface, you will see **Migration lifecycle** with status **Cutover ccomplete**.
2. Select **Actions** and select **Mark as archived.**
3. When **Archive X server** appears, select **Archive.**
   
#### Terminate instance

1. Access to EC2
2. Select Instances
3. Select the instances related to the lab
4. Select Instance state
5. Select Terminate instance

#### Delete Security group
1. Access to EC2
2. Select Security Group
3. Select the security groups related to the lab
4. Select Actions
5. Select Delete a security group

#### Remove Keypair
1. EC2 Access
2. Select Key Pairs
3. Select Actions
4. Select Delete

#### Remove VPC
1. Access VPC
2. Choose Your VPCs
3. Select the vpc related to the lab
4. Select Actions
5. Select Delete VPC