---
title : "Tạo Security Group"
date :  "`r Sys.Date()`" 
weight : 5 
chapter : false
pre : " <b> 3.5 </b> "
---

#### Tạo Security Group

#### Tạo Security Group cho máy chủ nằm trong Public subnet

1. Trong giao diện **VPC**

   - Chọn **Security Group**
   - Chọn **Cretae security group**

![Create SG](/images/2/sg-group/001.png?featherlight=false&width=90pc)

2. Thực hiện cấu hình **Security group**

   - **Security Group name**, nhập **```Public server - SG```**
   - **Description**, nhập **Allow SSH and Ping for servers in public subnet.**
   - Chọn **web-app-vpc** VPC 

![Create SG](/images/2/sg-group/002.png?featherlight=false&width=90pc)

3. Thực hiện cấu hình **Inbound rules**

   - Trong **Inbound rules**, click **Add rule**.

   - Chọn **Type**: **SSH** và **Source**: **My IP**. **Anywhere** Cho phép ping từ bất kì địa chỉ IP nào.

   - Chọn  **Add rule** để thêm 1 rule mới.

   - Chọn **Type**: **HTTP** và **Source**: **Anywhere**. cho phép các instances trong Security Group đó giao tiếp qua giao thức HTTP với bên ngoài.

![Create SG](/images/2/sg-group/003.png?featherlight=false&width=90pc)

4. Kiểm tra **Outbound rules** và chọn **Create security group**

![Create SG](/images/2/sg-group/004.png?featherlight=false&width=90pc)

5. Hoàn thành tạo security group cho máy chủ nằm trong Public subnet

![Create SG](/images/2/sg-group/005.png?featherlight=false&width=90pc)
