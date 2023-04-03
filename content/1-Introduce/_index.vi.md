---
title : "Giới thiệu về AWS Application Migration Service"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
#### Tổng quan 


AWS Application Migration Service (MGN) là một giải pháp chuyển đổi nâng cao tự động hóa (rehost) giúp đơn giản hóa, nhanh chóng và giảm chi phí cho quá trình di chuyển ứng dụng lên AWS. Nó cho phép các công ty nâng cao và di chuyển một lượng lớn các máy chủ vật lý, ảo hoặc đám mây mà không gặp vấn đề tương thích, gián đoạn hiệu suất hoặc thời gian chuyển đổi dài. MGN sao chép máy chủ nguồn vào tài khoản AWS của bạn. Khi bạn sẵn sàng, nó tự động chuyển đổi và khởi chạy máy chủ của bạn trên AWS để bạn có thể nhanh chóng tận dụng các lợi ích về tiết kiệm chi phí, năng suất, sự bền vững và tính linh hoạt của đám mây. Sau khi ứng dụng của bạn đang chạy trên AWS, bạn có thể tận dụng các dịch vụ và khả năng của AWS để dễ dàng tái nền tảng hoặc đổi mới các ứng dụng đó - điều này làm cho việc nâng cao và di chuyển trở thành một con đường nhanh chóng để hiện đại hóa.


AWS Application Migration Service cần được khởi tạo trên giao diện của dịch vụ bằng cách tạo mẫu sao chép (replication template) khi sử dụng lần đầu tiên.

- Sau khi bạn đã tạo mẫu sao chép, quá trình khởi tạo sẽ tự động diễn ra.

- **Chỉ có người dùng Admin của tài khoản AWS của bạn mới có thể khởi tạo Application Migration Service.**

#### Tạo IAM role 
Trong quá trình khởi tạo, các IAM role  sau sẽ được tạo ra:

- AWSServiceRoleForApplicationMigrationService

- AWSApplicationMigrationReplicationServerRole

- AWSApplicationMigrationConversionServerRole

- AWSApplicationMigrationMGHRole

- AWSApplicationMigrationLaunchInstanceWithDrsRole

- AWSApplicationMigrationLaunchInstanceWithSsmRole

- AWSApplicationMigrationAgentRole

#### Additional policies

Bạn có thể tạo ra các vai trò với quyền hạn chi tiết cho Application Migration Service. Dịch vụ đi kèm với các chính sách quản lý IAM đã được định nghĩa trước như sau:

- AWSApplicationMigrationFullAccess - Policy cung cấp quyền truy cập vào tất cả các API công cộng của AWS Application Migration Service (MGN), cũng như quyền truy cập để đọc thông tin chìa khóa KMS.

- AWSApplicationMigrationEC2Access - Policy cho phép các hoạt động Amazon EC2 cần thiết để sử dụng Application Migration Service (MGN) để khởi chạy các máy chủ đã di chuyển như các trường hợp EC2.

- AWSApplicationMigrationSSMAccess - Policy cho phép các hoạt động Amazon SSM cần thiết để sử dụng Application Migration Service (MGN) để chạy các tài liệu SSM sau khi di chuyển các máy chủ nguồn.

- AWSApplicationMigrationReadOnlyAccess - Chính sách chỉ cho phép người dùng xem tất cả dữ liệu có sẵn trong giao diện của Application Migration Service, nhưng không cho phép họ sửa đổi bất kỳ dữ liệu nào hoặc thực hiện bất kỳ hành động nào. Policy cũng bao gồm một số quyền chỉ đọc EC2.

- AWSApplicationMigrationAgentPolicy - Policy cho phép người dùng cài đặt AWS Replication Agent. 

- AWSApplicationMigrationAgentInstallationPolicy - Policy cho phép người dùng cài đặt AWS Replication Agent.