---
title : "Khởi tạo test instances"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 6. </b> "
---

#### Khởi tạo test instances


1. Quay lại giao diện MGN, quan sát thấy đang ở trạng thái **Ready for testing**

![Application Migration Service](/images/4/00021.png?featherlight=false&width=90pc)

2. Chọn **Replication**, sau đó chọn **Launch test instance**

![Application Migration Service](/images/4/00023.png?featherlight=false&width=90pc)

3. Trạng thái sẽ chuyển sang **Test in progress**

![Application Migration Service](/images/4/00024.png?featherlight=false&width=90pc)

4. Bạn kiểm tra EC2 instance sẽ thấy một Replication server.

![Application Migration Service](/images/4/00025.png?featherlight=false&width=90pc)

5. Xem chi tiết job.

![Application Migration Service](/images/4/00026.png?featherlight=false&width=90pc)


6. Quay lại kiểm tra EC2 instance. Bạn sẽ thấy xuất hiện thêm một Conversion Server.

![Application Migration Service](/images/4/00027.png?featherlight=false&width=90pc)

7. Quay lại xem chi tiết các bước tiếp theo của job.

![Application Migration Service](/images/4/00028.png?featherlight=false&width=90pc)

8. Bạn sẽ thấy một instance được tạp ra.

![Application Migration Service](/images/4/00029.png?featherlight=false&width=90pc)

9. Sau khi trạng thái EC2 instance chuyển sang **2/2 checks passed**. Bạn thực hiện sao chép **Public IPv4**

![Application Migration Service](/images/4/00030.png?featherlight=false&width=90pc)

10. Sử dụng **MobaXterm** để SSH vào EC2 instance.

- Thực hiện điền **Remote host** 
- Đối với username. Điền user đã tạo, ví dụ: **fcjuser**
- Chọn **OK**

![Application Migration Service](/images/4/00031.png?featherlight=false&width=90pc)

11. Nhập mật khẩu và SSH thành công.

![Application Migration Service](/images/4/00032.png?featherlight=false&width=90pc)

12. Thực hiện kiểm tra cấu hình database file .env và thực hiện khởi động ứng dụng:

```
npm start
```

![Application Migration Service](/images/4/00033.png?featherlight=false&width=90pc)

13. Truy cập vào IP public và port 5000:

```
IP:5000
```

![Application Migration Service](/images/4/00034.png?featherlight=false&width=90pc)
