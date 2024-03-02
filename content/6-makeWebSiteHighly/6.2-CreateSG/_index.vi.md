---
title : "Tạo security group"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 6.2 </b> "
---

#### Tạo security group cho EC2 instance mới

Như thiết kế ban đầu. EC2 instance được đưa vào private subnet nên chúng ta cần phải đảm bảo rằng các security groups được áp dụng cho EC2 instance cho phép kết nối từ các tài nguyên trong cùng một VPC.

1. Trong giao diện EC2 chọn **Security Groups**
-  Chọn **Create security group**

![Create VPC](/images/6/create-sg/001.png?featherlight=false&width=90pc)

2. Trong giao diện **Create security group** với phần **Basic details**
   - **Security group name**, nhập **```Private server - SG```**
   - **Description**, nhập **```Allow inbound HTTP traffic on port 80 inside VPC```**
   - **VPC**, chọn **web-app-vpc**

![Create VPC](/images/6/create-sg/002.png?featherlight=false&width=90pc)

3. Thực hiện cấu hình **Inbound rules**

   - Trong **Inbound rules**, click **Add rule**.

   - Chọn **Type**: **HTTP** và **Source**: **```10.10.0.0/16```**. cho phép các instances trong Security Group đó giao tiếp qua giao thức HTTP bên trong VPC.

![Create VPC](/images/6/create-sg/003.png?featherlight=false&width=90pc)


4. Nhấn **Create security group** để hoàn thành tạo VPC

![Create VPC](/images/6/create-sg/004.png?featherlight=false&width=90pc)

#### Tạo security group cho Application Load Balancer 

5. Trong giao diện EC2 chọn **Security Groups**
-  Chọn **Create security group**

![Create VPC](/images/6/create-sg/001.png?featherlight=false&width=90pc)

6. Trong giao diện **Create security group** với phần **Basic details**
   - **Security group name**, nhập **```ALB-SG```**
   - **Description**, nhập **```Allow inbound HTTP traffic on port 80 from internet```**
   - **VPC**, chọn **web-app-vpc**

![Create VPC](/images/6/create-sg/006.png?featherlight=false&width=90pc)

7. Thực hiện cấu hình **Inbound rules**

   - Trong **Inbound rules**, click **Add rule**.

  - Chọn **Type**: **HTTP** và **Source**: **Anywhere** .Cho phép các instances trong Security Group đó giao tiếp qua giao thức HTTP với bên ngoài.

![Create VPC](/images/6/create-sg/007.png?featherlight=false&width=90pc)

8. Chọn **Create security group** và hoành thành tạo security group

![Create VPC](/images/6/create-sg/008.png?featherlight=false&width=90pc)
