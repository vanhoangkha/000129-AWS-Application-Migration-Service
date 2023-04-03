---
title : "Chuẩn bị Networking"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

#### Chuẩn bị Networking


1. Trước hết, chúng ta sẽ chuẩn bị phần mạng cho MGN.

   - Để thực hiện việc này, hãy truy cập vào giao diện AWS.
   - Tìm kiếm **VPC**
   - Truy cập vào giao diện VPC.
   - Chọn **Your VPCs**
   - Chọn **Create VPC**

![Application Migration Service](/images/1/0001.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

2. Trong giao diện **Create VPC**:

   - Chọn **VPC and more**
   - Đối với **Name taf auto-generation**, bạn có thể nhập tùy chọn.
   - Các tham số khác để mặc định.


![Application Migration Service](/images/1/0003.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

3. Sau đó, kiểm tra lại và chọn **Create VPC**.

![Application Migration Service](/images/1/0004.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

4. Tạo VPC cho **Source server** thành công.

![Application Migration Service](/images/1/0005.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

5. Bạn xem chi tiết trong phần **Resource map**

![Application Migration Service](/images/1/0006.png?featherlight=false&width=90pc?featherlight=false&width=90pc)


6. Bạn chọn subnet để kiểm tra subnet dành cho source server.

![Application Migration Service](/images/1/0007.png?featherlight=false&width=90pc?featherlight=false&width=90pc)


7. Thực hiện chỉnh sửa thành **Public subnet**

- Chọn **subnet** vừa tạo, chọn **Edit subnet settings**

![Application Migration Service](/images/1/0008.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

8. Trong giao diện chỉnh sửa subnet

- Chọn **Enable auto-assign public subnet IPv4 address**

![Application Migration Service](/images/1/0009.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

9. Bước tiếp theo, bạn phải tạo Security group cho source server.

   - Chọn **Security group**
   - Chọn **Create secuirty group**

![Application Migration Service](/images/1/00010.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

10. Đặt tên cho SG và chọn đúng VPC vừa tạo.

![Application Migration Service](/images/1/00011.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

11. Thực hành cấu hình như hình minh họa.

![Application Migration Service](/images/1/00012.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

12. Kiểm tra lại cấu hình và chọn **Create security group**

![Application Migration Service](/images/1/00013.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

13. Xem lại security group đã tạo.

![Application Migration Service](/images/1/00014.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

#### Chuẩn bị networking ở Target region

1. Chuyển sang region mới và thực hiện tạo VPC.

![Application Migration Service](/images/1/00015.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

2. Cấu hình và chọn **Create VPC**

![Application Migration Service](/images/1/00016.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

3. Hoàn thành tạo VPC sau đó bạn chỉnh sửa subnet như phần **Source Region**

![Application Migration Service](/images/1/00017.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

4. Tương tự, tạo SG cho **target server**.

![Application Migration Service](/images/1/00018.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

