---
title : "AWS Replication Agents "
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

#### AWS Replication Agents 

1. Chúng ta sẽ thêm source server. Chọn **Add server**

![Application Migration Service](/images/4/0003.png?featherlight=false&width=90pc)

2. Nếu bạn chưa tạo **Access key**. Bạn có vào **User**. Để tạo một access key Trong phần Access keys, chọn Create access key. Nếu bạn đã có hai access key, nút này sẽ bị vô hiệu hóa và bạn phải xóa một access key trước khi tạo một key mới.

![Application Migration Service](/images/4/0004.png?featherlight=false&width=90pc)

3. Trên trang Access key best practices & alternatives, chọn trường hợp sử dụng của bạn để tìm hiểu về các tùy chọn bổ sung có thể giúp bạn tránh việc tạo một access key dài hạn. Nếu bạn xác định rằng trường hợp sử dụng của bạn vẫn yêu cầu một access key, chọn Other và sau đó chọn Next.

![Application Migration Service](/images/4/0005.png?featherlight=false&width=90pc)

4. (Tùy chọn) Thiết lập giá trị thẻ mô tả cho access key. Điều này thêm một cặp khóa giá trị thẻ vào người dùng IAM của bạn. Điều này có thể giúp bạn xác định và xoay các access key sau này. Khóa thẻ được thiết lập thành id access key. Giá trị thẻ được thiết lập thành mô tả access key mà bạn chỉ định. Khi bạn hoàn thành, chọn Create access key.


![Application Migration Service](/images/4/0006.png?featherlight=false&width=90pc)

5. Trên trang Retrieve access keys, chọn Show để hiển thị giá trị access key bí mật của người dùng của bạn hoặc chọn Download .csv file. Đây là cơ hội duy nhất của bạn để lưu giữ access key bí mật của mình. Sau khi bạn đã lưu giữ access key bí mật của mình ở một vị trí an toàn, hãy chọn Done.

![Application Migration Service](/images/4/0007.png?featherlight=false&width=90pc)

6. Sao chép Access key vào và copy chạy các lệnh mục 4 và 5 lên terminal.

- Đảm bảo rằng các service role cần thiết đã được tạo bằng cách nhấp vào nút Reinitialize service permissions trên trang cài đặt Replication của Console Dịch vụ Di chuyển Ứng dụng. Bạn phải có các quyền cần thiết để tạo ra các IAM role để thực hiện thao tác này thành công.

- Tải xuống trình cài đặt Agent với lệnh wget trên máy chủ nguồn Linux của bạn. Lệnh wget này sẽ tải xuống tệp cài đặt Agent - aws-replication-installer-init.py vào máy chủ của bạn.

- Trình cài đặt Agent có định dạng như sau: https://aws-application-migration-service-<region>.s3.<region>.amazonaws.com/latest/linux/aws-replication-installer-init.py . Thay thế <region> bằng AWS Region mà bạn đang sao chép.

- Dưới đây là ví dụ về lệnh wget đầy đủ cho us-east-1:

```
wget -O ./aws-replication-installer-init.py https://aws-application-migration-service-us-east-1.s3.us-east-1.amazonaws.com/latest/linux/aws-replication-installer-init.py
```

- Dòng lệnh sẽ cho biết khi nào trình cài đặt đã được tải xuống thành công.

- Sau khi trình cài đặt Agent đã tải xuống thành công, bạn hãy sao chép và nhập lệnh cài đặt vào dòng lệnh trên máy chủ nguồn của bạn để chạy tập lệnh cài đặt.

```
sudo python3 aws-replication-installer-init.py
```

- Nếu bạn cần tùy chỉnh thêm, bạn có thể thêm nhiều tham số khác nhau vào tập lệnh cài đặt để điều khiển cách cài đặt Agent trên máy chủ của bạn. Thêm các tham số vào cuối tập lệnh cài đặt.

![Application Migration Service](/images/4/0008.png?featherlight=false&width=90pc)

7. Terminal sẽ yêu cầu bạn nhập tên AWS Region của bạn, AWS Access Key ID, AWS Secret Access Key (và AWS Session Token nếu có thích hợp) mà bạn đã tạo trước đó. Nhập đầy đủ tên AWS Region (ví dụ: eu-central-1), đầy đủ AWS Access Key ID và đầy đủ AWS Secret Access Key.

- Sau khi bạn đã nhập thông tin đăng nhập của mình, trình cài đặt sẽ xác định các ổ đĩa cần được sao chép. Trình cài đặt sẽ hiển thị các đĩa đã được xác định và yêu cầu bạn chọn các đĩa mà bạn muốn sao chép.
- Để sao chép một số ổ đĩa, nhập đường dẫn của các ổ đĩa, cách nhau bằng dấu phẩy, như được minh họa trong trình cài đặt (ví dụ: /dev/sda, /dev/sdb, v.v.). Để sao chép tất cả các ổ đĩa, nhấn Enter. Trình cài đặt sẽ xác định các ổ đĩa đã chọn và in ra kích thước của chúng.
- Trình cài đặt sẽ xác nhận rằng tất cả các đĩa đã được xác định thành công.

![Application Migration Service](/images/4/0009.png?featherlight=false&width=90pc)
