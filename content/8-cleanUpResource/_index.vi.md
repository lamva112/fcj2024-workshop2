---
title : "Dọn dẹp tài nguyên"
date :  "`r Sys.Date()`" 
weight : 8
chapter : false
pre : " <b> 8. </b> "
---
#### Dọn dẹp tài nguyên

Chúng ta sẽ tiến hành xóa các tài nguyên theo thứ tự sau

### Terminate các EC2 Instance.
1. Terminate EC2 instance.
    - Truy cập Amazon EC2 console 
    - Trên thanh điều hướng bên trái, chọn Intances
    - Chọn tất cả EC2 Instance liên quan tới bài lab.
    - Chọn **Instance state**
    - Chọn **Terminate instance**

![Create TG](/images/7/clean-up/001.png?featherlight=false&width=90pc)

2. Xác nhận terminate.
   
![Create TG](/images/7/clean-up/002.png?featherlight=false&width=90pc)

#### Xóa Load balancer
3. Xoá Load balancer
    - Truy cập Amazon EC2 console 
    - Trên thanh điều hướng bên trái, chọn Load balancer
    - Chọn Load balancer liên quan tới bài lab.
    - Chọn **Action**
    - Chọn **Delete load balancer**
