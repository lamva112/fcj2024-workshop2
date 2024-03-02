---
title : "Tạo 2 EC2 instance mới từ IMAs"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 6.4 </b> "
---

#### stop EC2 isntance hiên tại

1. Truy cập **AWS Management Console**

   - Tìm **EC2**
   - Chọn **EC2**

![Create AMIs](/images/3/create-ec2/001.png?featherlight=false&width=90pc)


2. Trong giao điện EC2
   - Chọn **Instances**
   - Chọn **Webserver**
   - Chọn **Instance state**
   - Chọn **Stop instance**

![Create AMIs](/images/6/create-2-ec2/001.png?featherlight=false&width=90pc)


{{% notice note %}}
Hiên tại chúng ta không dùng đến Webserver nữa vì toàn bộ cấu hình và cài đặt cho ứng dụng web đã được lưu ở IMAs. Chúng ta sẽ dùng IMAs để tạo Webserver1 và Webserver2 trong private subnet
{{% /notice %}}

#### Tạo 2 EC2 instance mới từ IMAs

3. Trong giao diện  **Instances** chọn **launh instance**

![Create AMIs](/images/6/create-2-ec2/002.png?featherlight=false&width=90pc)

4. Trong giao diện **Launch an instance** với **Name and tags  Info** nhập **```Webserver1```**
   
![Create AMIs](/images/6/create-2-ec2/003.png?featherlight=false&width=90pc)

5. Trong phần **Amazon Machine Image**
   - Chọn tab **My AMIs** và chọn **Owned by me**
   - Chọn **WebserImage**

![Create AMIs](/images/6/create-2-ec2/004.png?featherlight=false&width=90pc)

6. Thực hiện chọn **Instance type**
   - Chọn **t2.micro (default)**
   - Chọn **key pair** đã tạo trước đó

![Create AMIs](/images/6/create-2-ec2/005.png?featherlight=false&width=90pc)

7.  Thực hiện cấu hình **Network**

    - **VPC**, chọn **web-app-vpc**
    - **Subnet**, chọn **Private Subnet 3**
    - **Auto-assign public IP**, chọn **disable**
    - **Firewall (Security Group)**, chọn **Select existing security group**
    - Chọn **Private server -SG**
    - Chọn **Launch instance**

![Create AMIs](/images/6/create-2-ec2/006.png?featherlight=false&width=90pc)

7.  Tương tự như trên tạo  **```Webserver2```** với cấu hình **network** như sau:
   

![Create AMIs](/images/6/create-2-ec2/007.png?featherlight=false&width=90pc)

8. Hoàn thành tạo 2 EC2 instance mới

![Create AMIs](/images/6/create-2-ec2/008.png?featherlight=false&width=90pc)

