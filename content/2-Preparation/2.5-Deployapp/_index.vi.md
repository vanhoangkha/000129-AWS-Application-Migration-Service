---
title : "Triển khai ứng dụng"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 2.5 </b> "
---

#### Triển khai ứng dụng

1. Triển khai ứng dụng.Thực hiện clone repository code ứng dụng.

```
git clone https://github.com/First-Cloud-Journey/000004-EC2.git
```

![Application Migration Service](/images/3/00022.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

2. Đến thư mục của bài lab 000004-EC2

```
cd 000004-EC2
```

Sau khi kết nối EC2 instance thành công. Bạn sẽ thực hiện các bước chuẩn bị để triển khai ứng dụng:

- Cài đặt Nodejs trên EC2 instance.

- Cài đặt node version manager (nvm) ) bằng cách nhập nội dung sau vào dòng lệnh sau:

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
```

- Kích hoạt nvm bằng cách nhập nội dung sau vào dòng lệnh:

```
. ~/.nvm/nvm.sh
```

- Sử dụng nvm để cài đặt phiên bản mới nhất của Node.js bằng cách nhập nội dung sau vào dòng lệnh:

```
nvm install 16
```

- Kiểm tra đã cài đặt nodejs thành công

```
node -v
npm -v
```

![Application Migration Service](/images/3/00023.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

3. NPM là viết tắt của Node package manager là một công cụ tạo và quản lý các thư viện lập trình Javascript cho Node.js. Sử dụng npm init khởi tạo project sẽ tạo ra file package.json mẫu.

```
npm init
```

Tiếp theo chúng ta thực hiện dependencies installation

- express
- Dotenv
- express-handlebars
- body-parser
- mysql

```
npm install express dotenv express-handlebars body-parser mysql
```

![Application Migration Service](/images/3/00024.png?featherlight=false&width=90pc?featherlight=false&width=90pc)

4.  Thực hiện tạo 1 file mội trường .env và dùng lệnh vi để chỉnh sửa. Thực hiện cấu hình database:

```
DB_HOST = 'localhost'
DB_NAME = 'awsfcjuser'
DB_USER = 'root'
DB_PASS = '123456789@Aws'
```

- Trong đó, DB_HOST là Enpoint của DB instance
- DB_NAME là tên database đã được tạo trong DB instance
- DB_USER là tên người dùng database đã được tạo trong DB instance
- DB_PASS là mật khẩu database đã được tạo trong DB instance

Khởi động lại Express server. Sử dụng Nodemon để tiết kiệm thời gian

```
npm install --save-dev nodemon
```

![Application Migration Service](/images/3/00025.png?featherlight=false&width=90pc?featherlight=false&width=90pc)


5. Khởi động local server

```
npm start
```

![Application Migration Service](/images/3/00026.png?featherlight=false&width=90pc?featherlight=false&width=90pc)


6. Vào giao diện EC2

   - Chọn Instances
   - Chọn instance mà bạn host ứng dụng.
   - Sao chép Public IPv4 address
   - Sử dụng Public IPv4 address dán vào trình duyệt và cổng 5000 để kiểm tra ứng dụng.

```
<Public IPv4 address>:5000
```

Ví dụ: 3.91.32.39:5000

![Application Migration Service](/images/3/00027.png?featherlight=false&width=90pc)
