---
title : "Tạo DB Subnet Group"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 4.1 </b> "
---

#### Tạo DB Subnet Group trên AWS

1. Truy cập **AWS Management Console**

   - Tìm **RDS**
   - Chọn **RDS**

![Create VPC](/images/4/db-subnet-group/001.png?featherlight=false&width=90pc)

2. Trong giao diện **RDS**

   - Chọn **Subnet groups**
   - Chọn **Create DB Subnet group**

![Create VPC](/images/4/db-subnet-group/002.png?featherlight=false&width=90pc)

3. Trong giao diện **Add subnets**
     - **Name**, nhập **```webapp-db-subnet-group```**
     - **Description**, nhập **```DB Subnet group```**
    - Select **web-app-vpc** VPC

![Create VPC](/images/4/db-subnet-group/003.png?featherlight=false&width=90pc)

4. Trong giao diện **Add subnets**
   - **Availability Zones**, chọn **ap-southeast-1a** và **ap-southeast-1b**
   - **Subnets**, chọn **10.10.11.0/24** cho  **ap-southeast-1a** và **10.10.12.0/24** cho **ap-southeast-1b**
   - Chọn **Create**

![Create VPC](/images/4/db-subnet-group/004.png?featherlight=false&width=90pc)

5. Hoàn thành tạo DB Subnet Group

![Create VPC](/images/4/db-subnet-group/005.png?featherlight=false&width=90pc)
