---
title : "Launch the cutover instances"
date :  "`r Sys.Date()`" 
weight : 7
chapter : false
pre : " <b> 7. </b> "
---

#### Launch the cutover instances

1. Go back to the MGN interface and select Replication
- Select Mark as "Ready for cutover"

![Application Migration Service](/images/5/0001.png?featherlight=false&width=90pc)

2. Select **Continue**

![Application Migration Service](/images/5/0002.png?featherlight=false&width=90pc)

3. After about 5 minutes you will see the switch to **Ready for cutover**

![Application Migration Service](/images/5/0003.png?featherlight=false&width=90pc)

4. View job details

![Application Migration Service](/images/5/0004.png?featherlight=false&width=90pc)

5. Then only **Replication Server** remains

![Application Migration Service](/images/5/0005.png?featherlight=false&width=90pc)

6. Complete the job.

![Application Migration Service](/images/5/0006.png?featherlight=false&width=90pc)

7. Return to the MGN interface

- Select **Replication**
- Select **Launch cutover instances**

![Application Migration Service](/images/5/0007.png?featherlight=false&width=90pc)

8. Select **Launch**

![Application Migration Service](/images/5/0008.png?featherlight=false&width=90pc)

9. You will see **Cutover in progress** status

![Application Migration Service](/images/5/0009.png?featherlight=false&width=90pc)

10. Complete the jobs.

![Application Migration Service](/images/5/00010.png?featherlight=false&width=90pc)

11. Perform SSH preparation into EC2.

![Application Migration Service](/images/5/00011.png?featherlight=false&width=90pc)

12. SSH successful.

![Application Migration Service](/images/5/00012.png?featherlight=false&width=90pc)

13. Perform application startup.

![Application Migration Service](/images/5/00013.png?featherlight=false&width=90pc)

14. Access the application.

![Application Migration Service](/images/5/00014.png?featherlight=false&width=90pc)