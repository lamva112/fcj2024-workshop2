---
title : "Tạo Route53 Public hosted zone"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 7.1 </b> "
---

#### Tạo Route53 Public hosted zone

{{% notice warning %}}
Ở phần lab này chúng ta cần phải có 1 public domain. Bạn ta có thể mua domain ở bất kỳ nhà cung cấp nào.
{{% /notice %}}

1. Truy cập **AWS Management Console**

   - Tìm **Route53**
   - Chọn **Route53**

![Create TG](/images/7/domain/001.png?featherlight=false&width=90pc)

2. Trong giao diện **Route 53 Dashboard**
   - Chọn **Create hosted zone**

![Create TG](/images/7/domain/002.png?featherlight=false&width=90pc)

3. Trong giao diện **Create hosted zone**
   - **Domain name**, nhập **your domain**. Ví dụ learnaws.click
   - **type**, chọn **Public hosted zone**
   - Chọn **Create hosted zone**
  
![Create TG](/images/7/domain/003.png?featherlight=false&width=90pc)

4. Hoàn thành tạo hosted zone

![Create TG](/images/7/domain/004.png?featherlight=false&width=90pc)

5. Trong giao diện hosted zone vừa tạo
   - Copy tất cả **Value/Route traffic to** với type **NS** vừa được Route53 tạo ra

![Create TG](/images/7/domain/006.png?featherlight=false&width=90pc)

6. Truy cập vào website quản lý domain 
   - Tìm **DNS & Nameserver** 

![Create TG](/images/7/domain/007.png?featherlight=false&width=90pc)

7. Thêm **Value/Route traffic to** vào Nameserver

![Create TG](/images/7/domain/008.png?featherlight=false&width=90pc)


8. Hoàn thành Thêm **Value/Route traffic to** vào Nameserver

![Create TG](/images/7/domain/009.png?featherlight=false&width=90pc)

