---
title : "Khởi tạo EC2"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

#### Khởi tạo EC2


Sau khi đã chuẩn bị tất cả về mặt networking, chúng ta sẽ khởi tạo EC2 và cài đặt Agent đồng thời cũng triển khai ứng dụng.

1. Truy cập vào AWS Management Console

   - Tìm và chọn **EC2**
   - Chọn **Instances**
   - Chọn **Launch instances**

![Application Migration Service](/images/3/0001.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

2. Thực hiện cấu hình EC2, nhập **Name and tag**. Ví dụ như **App - Source**

![Application Migration Service](/images/3/0002.png?featherlight=false&width=90pc?featherlight=false&width=90pc)


3. Chọn **AMI** là **Ubuntu Server 20.04 LTS...** 

![Application Migration Service](/images/3/0003.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

4. Chọn **Instance type** và tạo **Key pair** 

![Application Migration Service](/images/3/0004.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

5. Cấu hình và điền thông tin về key pair.

![Application Migration Service](/images/3/0005.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

6. Sau khi tạo **EC2** thành công. Chúng ta sẽ SSH vào EC2 bằng MobaXterm. 

- Bạn có thể tham khảo thêm cách SSH vào EC2 tại [đây](https://000004.awsstudygroup.com/vi/4-launchlinuxinstance/4.2-connectlinuxinstance/)

![Application Migration Service](/images/3/0006.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

7. Thêm user vào để thực hiện login bằng user không sử dụng keypair. Sử dụng lệnh sau:

```
sudo adduser fcjuser
```
- Và chọn **Enter** ở các bước tiếp theo.



![Application Migration Service](/images/3/0007.png?featherlight=false&width=90pc?featherlight=false&width=90pc)


8. Cấp quyền cho user:

```
sudo usermod -aG sudo fcjuser
```

![Application Migration Service](/images/3/0008.png?featherlight=false&width=90pc?featherlight=false&width=90pc)


9. Điều chỉnh phương thức đăng nhập bằng password.

```
sudo vi /etc/ssh/sshd_config
```

- Sau đó thay đổi **PasswordAuthentication** thành **yes**

- Sau đó gõ **Esc** và nhập **:wq!**

![Application Migration Service](/images/3/0009.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

10. Sau đó, restart server ssh.

```
sudo systemctl restart ssh.service
```

![Application Migration Service](/images/3/00010.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

11. Bạn sẽ lựa chọn optional đăng nhập.

![Application Migration Service](/images/3/00011.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

12. Sau đó bạn sẽ đăng nhập bằng user/password và không cần dùng keypair.

![Application Migration Service](/images/3/00012.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

