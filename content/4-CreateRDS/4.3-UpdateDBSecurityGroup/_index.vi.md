---
title : "Cập nhật DB security group"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 4.3 </b> "
---

#### Cập nhật DB security group cho phép traffic từ VPC CIDR

1. Trong giao diện **Amazon RDS**
- Chọn **Database**
- Mở **webapp-db**

![Create VPC](/images/4/db-sg/001.png?featherlight=false&width=90pc)

2. Trong giao diện **webapp-db** 
- Chọn **Connectivity & Security** 
- Nhấp vào liên kết VPC Security groups (điều này sẽ mở bảng điều khiển EC2 với DB security group được chọn)

![Create VPC](/images/4/db-sg/002.png?featherlight=false&width=90pc)
![Create VPC](/images/4/db-sg/003.png?featherlight=false&width=90pc)

3. Mở **webapp-db-security-group**
   - Chọn **Inbound rules**
   - Chọn **Edit inbound rules**
 - 
![Create VPC](/images/4/db-sg/004.png?featherlight=false&width=90pc)

4. Trong giai diện **Edit inbound rules**
- Cập nhật source thành **```10.10.0.0/16```**
- Chọn **Save rules**

![Create VPC](/images/4/db-sg/006.png?featherlight=false&width=90pc)

