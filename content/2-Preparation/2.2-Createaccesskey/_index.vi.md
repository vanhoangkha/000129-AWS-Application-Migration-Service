---
title : "Tạo Access key"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

#### Tạo Access key

Trong phần này chúng ta sẽ tạo IAM user và access key dành cho MGN.

1. Truy cập AWS Console.

   - Tìm và chọn **IAM**
   - Chọn **Users**
   - Chọn **Add users**

![Application Migration Service](/images/2/0001.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

2. Chúng ta thực hiện điền thông tin user.

   - Nhập tên user vào trường **User name**
   - Chọn **Provide user access to the AWS Management Console -optional**
   - Chọn **I want to create an IAM user**
   - Đối với **Console password**, chọn **Custom password** và nhập password bạn chọn.
   - Chọn **Users must create a new password at next sign-in (recommended)**
   - Chọn **Next**


![Application Migration Service](/images/2/0002.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

3. Đối với **Permission**

   - Chọn **Attach policies directly**
   - Tìm và chọn **AWSApplicationMigrationAgentInstallattionPolicy**
   - Chọn **Next**

![Application Migration Service](/images/2/0003.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

4. Chọn **Next** và sau đó chọn **Create user**. Giao diện tạo user thành công.

![Application Migration Service](/images/2/0004.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

5. Sau khi tạo user thành công.

- Chọn User đã tạo thành công.
- Chọn **Security credentials**
- Chọn **Create access key**.


![Application Migration Service](/images/2/0005.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

6. Chọn **Command Line Interface (CLI)**

- Chọn **I understand the above recommendation and want to proceed to create an access key**
- Chọn **Next**.


![Application Migration Service](/images/2/0006.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

7. Chọn **Create access key**

![Application Migration Service](/images/2/0007.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

8. Hoàn thành tạo Access key.

![Application Migration Service](/images/2/0008.png?featherlight=false&width=90pc?featherlight=false&width=90pc)





