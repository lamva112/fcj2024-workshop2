---
title : "Kiểm tra target heath và truy cập ứng dụng web"
date :  "`r Sys.Date()`" 
weight : 8
chapter : false
pre : " <b> 6.8 </b> "
---

#### Kiểm tra target heath

1.  Trong giao điện EC2
   - Chọn **Target Groups**
   - Chọn **ALB-TG**

![Create TG](/images/6/review/001.png?featherlight=false&width=90pc)

2. Trong **Target group: ALB-TG**
   - Chọn **Targets**

{{% notice info %}}
 Dựa vào target group chúng ta có thể thấy rằng cả 2 EC2 instance đều hoạt động tốt
{{% /notice %}}
![Create TG](/images/6/review/002.png?featherlight=false&width=90pc)

#### Truy cập vào ứng dụng web

3.  Trong giao điện EC2
   - Chọn **Load Balancers**
   - Chọn **MyALB**

![Create TG](/images/6/review/003.png?featherlight=false&width=90pc)

4. Với **Load balancer: MyALB**
   - copy **DNS name** và mở trên trình duyệt

![Create TG](/images/6/review/004.png?featherlight=false&width=90pc)
![Create TG](/images/6/review/005.png?featherlight=false&width=90pc)

5. Truy cập vào trang web với đường dẫn **DNS name/corp.php**

![Create TG](/images/6/review/006.png?featherlight=false&width=90pc)
