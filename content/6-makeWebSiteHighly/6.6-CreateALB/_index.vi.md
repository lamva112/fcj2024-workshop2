---
title : "Tạo Application Load Balancer"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 6.6 </b> "
---

#### Tạo Application Load Balancer 

1.  Trong giao điện EC2
   - Chọn **Load Balancers**
   - Chọn **Create load balancers**

![Create TG](/images/6/create-alb/001.png?featherlight=false&width=90pc)

2. Trong giao diện **Compare and select load balancer type**
-  Chọn **Create** trong trường **Application Load Balancer** 
  
![Create TG](/images/6/create-alb/002.png?featherlight=false&width=90pc)

3. Trong giao diện **Create Application Load Balancer**
- Với **Load balancer name**, nhập **```MyALB```**
- Với **Scheme**, chọn **Internet-facing**
- Với **IP address typeInfo**, chọn **IPv4**

![Create TG](/images/6/create-alb/004.png?featherlight=false&width=90pc)

4. Tiếp tục cấu hình **Network mapping**
- VPC, chọn **Web-app-vpc**
- Với **ap-southeast-1a (apse1-az2)**, chọn **Public Subnet 1**
- Với **ap-southeast-1b (apse1-az1)**, chọn **Publuc Subnet 2**

![Create TG](/images/6/create-alb/005.png?featherlight=false&width=90pc)

5. Trong phần **Security groups**
- chọn **ALB-SG**

![Create TG](/images/6/create-alb/006.png?featherlight=false&width=90pc)

5. Trong phần **Listeners and routing**
- Với **Default actionInfo**, ta chọn target group là **ALB-TG**

![Create TG](/images/6/create-alb/007.png?featherlight=false&width=90pc)

6. Nhấn **Create** để hoàn tất tạo Application Load Balancer

![Create TG](/images/6/create-alb/008.png?featherlight=false&width=90pc)
