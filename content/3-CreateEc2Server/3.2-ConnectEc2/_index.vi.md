---
title : "Kiểm tra kết nối"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 3.2 </b> "
---

#### Kiểm tra kết nối
{{% notice note %}}
Có nhiều cách kết nối EC2, các bạn có thể tham khảo [kết nối EC2 trên windown bằng **PuTTY**](https://000004.awsstudygroup.com/vi/4-launchlinuxinstance/4.2-connectlinuxinstance/). Trong bài lab, chúng ta sử dụng termial để kết nối EC2
{{% /notice %}}

1. Mở Terminal và chạy lệnh sau với đường dẫn chính xác cho tệp khóa .pem

![Conect EC2](/images/3/connect-ec2/001.png?featherlight=false&width=90pc)

2. Truy cập vào trang **EC2**

   - Chọn **Instances**
   - Chọn **Webserver**
   - Chọn **Connect**

![Conect EC2](/images/3/connect-ec2/002.png?featherlight=false&width=90pc)

3. Trong giao diện **Connect to instance**

   - Chọn **SSH Client**
   - Copy đường dẫn **Example**

![Conect EC2](/images/3/connect-ec2/003.png?featherlight=false&width=90pc)

4. Trong termial đã mớ trước đó
   - Pass đường dẫn  **Example**
   - Nhập **yes**

![Conect EC2](/images/3/connect-ec2/004.png?featherlight=false&width=90pc)

5. Kết nối thành công.

![Conect EC2](/images/3/connect-ec2/005.png?featherlight=false&width=90pc)

6. Kiểm tra kết nối tới internet của EC2 Public, ta thực hiện lệnh:

```
ping amazon.com -c5
```

![Conect EC2](/images/3/connect-ec2/006.png?featherlight=false&width=90pc)
