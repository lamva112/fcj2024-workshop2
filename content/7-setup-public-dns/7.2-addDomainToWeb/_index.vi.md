---
title : "Cài đặt Public DNS cho ứng dụng web"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 7.2 </b> "
---

#### Cài đặt Public DNS cho ứng dụng web

1. Trong giao diện **Route 53**
- Chọn **Hosted zones**
- Chọn **Hosted zone name** sử dụng cho website

![Create TG](/images/7/set-dns/001.png?featherlight=false&width=90pc)

2. Trong giao diện **Hosted zone** vừa được chọn
   - Chọn **Create record**

![Create TG](/images/7/set-dns/002.png?featherlight=false&width=90pc)

3. Trong giao diện **Create record**

- Bật **Alias**
- Với **Route traffic to**
  + Chọn **Alias to Aplication and Classic Load Balancer**
  + Chọn **Asia Pacific (Sigapore)**
  + Chọn **MyALB**
- Nhấn **Create record**

![Create TG](/images/7/set-dns/003.png?featherlight=false&width=90pc)

4. Hoàn thành tạo reacord

![Create TG](/images/7/set-dns/004.png?featherlight=false&width=90pc)

5. Mở trình duyệt và truy cập ứng dụng web của bạn bằng cách sử dụng **```http://YOUR_DOMAIN_NAME/corp.php```**

![Create TG](/images/7/set-dns/005.png?featherlight=false&width=90pc)

