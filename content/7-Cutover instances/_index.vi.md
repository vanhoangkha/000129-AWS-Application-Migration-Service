---
title : "Khởi tạo cutover instances"
date :  "`r Sys.Date()`" 
weight : 7
chapter : false
pre : " <b> 7. </b> "
---

#### Khởi tạo cutover instances

1. Quay lại giao diện MGN, Chọn **Replication**

- Chọn **Mark as "Ready for cutover"**

![Application Migration Service](/images/5/0001.png?featherlight=false&width=90pc)

2. Chọn **Continue**

![Application Migration Service](/images/5/0002.png?featherlight=false&width=90pc)

3. Sau khoảng 5 phút bạn sẽ thấy chuyển sang **Ready for cutover**

![Application Migration Service](/images/5/0003.png?featherlight=false&width=90pc)

4. Xem chi tiết job

![Application Migration Service](/images/5/0004.png?featherlight=false&width=90pc)

5. Sau đó chỉ còn **Replication Server**

![Application Migration Service](/images/5/0005.png?featherlight=false&width=90pc)

6. Hoàn thành job.

![Application Migration Service](/images/5/0006.png?featherlight=false&width=90pc)

7. Quay lại giao diện MGN

- Chọn **Replication**
- Chọn **Launch cutover instances**

![Application Migration Service](/images/5/0007.png?featherlight=false&width=90pc)

8. Chọn **Launch**

![Application Migration Service](/images/5/0008.png?featherlight=false&width=90pc)

9. Bạn sẽ thấy trạng thái **Cutover in progress**

![Application Migration Service](/images/5/0009.png?featherlight=false&width=90pc)

10. Hoàn thành các job.

![Application Migration Service](/images/5/00010.png?featherlight=false&width=90pc)

11. Thực hiện chuẩn bị SSH vào EC2.

![Application Migration Service](/images/5/00011.png?featherlight=false&width=90pc)

12. SSH thành công.

![Application Migration Service](/images/5/00012.png?featherlight=false&width=90pc)

13. Thực hiện khởi động ứng dụng.

![Application Migration Service](/images/5/00013.png?featherlight=false&width=90pc)

14. Truy cập vào ứng dụng.

![Application Migration Service](/images/5/00014.png?featherlight=false&width=90pc)
