---
title : "Dọn dẹp tài nguyên"
date :  "`r Sys.Date()`" 
weight : 9
chapter : false
pre : " <b> 9. </b> "
---

#### Dọn dẹp tài nguyên

1. Trên giao diện MGN, bạn sẽ thấy **Migration lifecycle** có trạng thái **Cutover ccomplete**.
2. Chọn **Actions** và chọn **Mark as archived.**
3. Khi **Archive X server** xuất hiện, chọn **Archive.**
   
#### Terminate instance

1. Truy cập vào EC2
2. Chọn Instances
3. Chọn các instance liên quan bài lab
4. Chọn Instance state
5. Chọn Terminate instance

#### Xóa Security group
1. Truy cập vào EC2
2. Chọn Security Group
3. Chọn các security group liên quan đến bài lab
4. Chọn Actions
5. Chọn Delete security group

#### Xóa Keypair
1. Truy cập EC2
2. Chọn Key Pairs
3. Chọn Actions
4. Chọn Delete

#### Xóa VPC
1. Truy cập VPC
2. Chọn Your VPCs
3. Chọn các vpc liên quan bài lab
4. Chọn Actions
5. Chọn Delete VPC


