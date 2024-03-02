---
title : "Tạo AMIs"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 6.1 </b> "
---

#### Tạo AMIs

AMI cho phép chúng tạo bản sao lưu của máy ảo EC2, bao gồm cả hệ điều hành, ứng dụng và dữ liệu. Do đó chúng ta cần AIMS triển khai hai instance mới với cấu hình tương tự như máy ảo EC2 chúng ta đã tạo trước đó.

1. Truy cập **AWS Management Console**

   - Tìm **EC2**
   - Chọn **EC2**

![Create AMIs](/images/3/create-ec2/001.png?featherlight=false&width=90pc)


2. Trong giao điện EC2
   - Chọn **Instances**
   - Chọn **Webserver**
   - Chọn **Action**

![Create EC2](/images/6/001.png?featherlight=false&width=90pc)

3. Trong Action Popup
- Chọn **Image and template**
- Chọn **Create image**

![Create EC2](/images/6/002.png?featherlight=false&width=90pc)

4. Trong giao diện **Create Image**
   
- **Image name**, nhập **```WebserverImage```**
- Nhấn **Create**

![Create EC2](/images/6/003.png?featherlight=false&width=90pc)

5. Tạo Image thành công

![Create EC2](/images/6/004.png?featherlight=false&width=90pc)

