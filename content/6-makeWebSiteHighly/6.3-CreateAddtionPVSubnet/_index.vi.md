---
title : "Tạo thêm 2 Private subnet"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 6.3 </b> "
---

#### Tạo thêm 2 Private subnet cho EC2 

1. Truy cập giao diện **AWS Management Console**

   - Tìm **VPC**
   - Chọn **VPC**
  
![Create VPC](/images/2/000.png?featherlight=false&width=90pc)

2. Trong giao điện VPC
- Chọn **Subnet**
- Chọn **Create Subnet**

![Create VPC](/images/6/add-2-subnet/001.png?featherlight=false&width=90pc)

3. Trong giao diện **Create Subnet**
- VPC, chọn **web-app-vpc**

![Create VPC](/images/6/add-2-subnet/002.png?featherlight=false&width=90pc)

4. Trong phần **Subnet settings**
- **Subnet name**, nhập **```Private subnet 3```**
- **Availability Zone**, chọn **ap-southeast-1a**
- **IPv4 subnet CIDR block**, nhập **```10.10.13.0/24```**
- Nhấn **Create subnet**

![Create VPC](/images/6/add-2-subnet/003.png?featherlight=false&width=90pc)

5. Tương tự như vậy, tạo  **```Private subnet 4```** với CIDR là **```10.10.14.0/24```**

![Create VPC](/images/6/add-2-subnet/004.png?featherlight=false&width=90pc)

6. Hoàn thành tạo thêm 2 private subnet 

![Create VPC](/images/6/add-2-subnet/005.png?featherlight=false&width=90pc)
