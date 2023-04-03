---
title : "Launch Settings"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

#### Launch Settings


1. Đợi khoảng 5 - 10 phút sau. Bạn sẽ thấy **Source server name**

![Application Migration Service](/images/4/00010.png?featherlight=false&width=90pc)

2. Thực hiện cấu hình **EC2 Launch Template**

    - Chọn **Source server name**
    - Chọn **Launch settings**
    - Chọn **Modify**

![Application Migration Service](/images/4/00012.png?featherlight=false&width=90pc)

3. Chọn **Modify**

![Application Migration Service](/images/4/00013.png?featherlight=false&width=90pc)

4. Giữ cấu hình **AMI**

![Application Migration Service](/images/4/00014.png?featherlight=false&width=90pc)

5. Giữ nguyên cấu hình **Instance type**. 

- Chọn **Create new key pair**

![Application Migration Service](/images/4/00015.png?featherlight=false&width=90pc)

6. Chọn **Create key pair**

![Application Migration Service](/images/4/00016.png?featherlight=false&width=90pc)

7. Thực hiện cấu hình **Networking**

    - Chọn đúng subnet đã chuẩn như hình **Migrated Resource Subnet**.
    - Chọn **Select existing security group**
    - Chọn **App Server Target**
    - Đối với **Auto-assign public IP**, chọn **Enable**.

![Application Migration Service](/images/4/00017.png?featherlight=false&width=90pc)

8. Nhập mô tả template version sau đó chọn **Create template version**

![Application Migration Service](/images/4/00018.png?featherlight=false&width=90pc)

9. Chọn **View launch templates**

![Application Migration Service](/images/4/00019.png?featherlight=false&width=90pc)

10. Chọn template vừa tạo. Sau đó, chọn **Action** tiếp tục chọn **Set default version**

![Application Migration Service](/images/4/00020.png?featherlight=false&width=90pc)

11. Đổi template version thành công.

![Application Migration Service](/images/4/00022.png?featherlight=false&width=90pc)