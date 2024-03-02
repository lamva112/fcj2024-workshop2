---
title : "Tạo máy chủ EC2"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 3.1 </b> "
---

#### Tạo EC2 nằm trong Public subnet

1. Truy cập **AWS Management Console**

   - Tìm **EC2**
   - Chọn **EC2**

![Create EC2](/images/3/create-ec2/001.png?featherlight=false&width=90pc)

2. Trong giao diện **EC2**

   - Chọn **Instances**
   - Chọn **Launch instances**

![Create EC2](/images/3/create-ec2/002.png?featherlight=false&width=90pc)

3. **Name and tags** của instance, nhập **```Webserver```**

![Create EC2](/images/3/create-ec2/003.png?featherlight=false&width=90pc)

4. Thực hiện chọn **AMI**

   - Chọn **Quick Start**
   - Chọn **Amazon Linux (default)**
   - Chọn AMI **Amazon Linux 2023 AMI – Free tier eligible**

![Create EC2](/images/3/create-ec2/004.png?featherlight=false&width=90pc)

5. Thực hiện chọn **Instance type**
   - Chọn **t2.micro (default)**
   - Chọn **Create key pair**

![Create EC2](/images/3/create-ec2/005.png?featherlight=false&width=90pc)

6. Trong giao diện **Create key pair**

   - **Key pair name**, nhập **```aws-keypair```** (tên tùy chọn, bạn có thể đặt bất kỳ).
   - **Key pair type**, chọn **RSA**
   - **Private key file format**, chọn **.pem**

![Create EC2](/images/3/create-ec2/006.png?featherlight=false&width=90pc)

7.  Thực hiện cấu hình **Network**

    - **VPC**, chọn **ASG**
    - **Subnet**, chọn **Public Subnet 1**
    - **Auto-assign public IP**, chọn **Enable**
    - **Firewall (Security Group)**, chọn **Select existing security group**
    - Chọn **Public server -SG**
    - Chọn **Launch instance**

![Create EC2](/images/3/create-ec2/007.png?featherlight=false&width=90pc)

8. Hoàn thành tạo instance

![Create EC2](/images/3/create-ec2/008.png?featherlight=false&width=90pc)

9. Đợi khoảng 5 phút **Status check** sẽ chuyển sang **2/2 checks passed**

![Create EC2](/images/3/create-ec2/009.png?featherlight=false&width=90pc)
