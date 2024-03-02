---
title : "Tạo Target Groups"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 6.5 </b> "
---

#### Tạo target group

Trong Amazon Web Services (AWS), một target group là một nhóm các máy chủ đích mà các yêu cầu từ một dịch vụ được định tuyến đến. Target group thường được sử dụng trong các dịch vụ như Elastic Load Balancing (ELB) hoặc AWS Auto Scaling để định tuyến yêu cầu đến các máy chủ đích phù hợp.

Tron bài lab này chúng ta tạo một target group cho 2 EC2 instances, để xác định  các yêu cầu đến từ một dịch  load balancer  sẽ được định tuyến đến 2 EC2 instances này. Việc này giúp phân phối tải (load balancing) và tăng tính sẵn sàng và độ tin cậy của ứng dụng bằng cách chia sẻ tải làm việc giữa các máy chủ.

1.  Trong giao điện EC2
   - Chọn **Target Groups**
   - Chọn **Create target group**

![Create TG](/images/6/create-target-group/001.png?featherlight=false&width=90pc)

2. Trong giao diện **step 1** (**Specify group details**)
   - Với phần **Basic configuration**, chọn **target type** là **instance**

![Create TG](/images/6/create-target-group/002.png?featherlight=false&width=90pc)

3. Tiếp tục cấu hình target group
- Với **Target group name** nhập **```ALB-TG```**
- với **Protocol : Port** chọn **HTTP**
- Chọn **IP address type** là **IPv4**
- **VPC**, chọn **web-app-vpc**

![Create TG](/images/6/create-target-group/003.png?featherlight=false&width=90pc)

4. Tạo Health checks
- **Health check protocol**, Chọn **HTTP**
- **Health check path**, nhập **```corp.php```**

![Create TG](/images/6/create-target-group/004.png?featherlight=false&width=90pc)

Trong AWS, health checks trong target group được sử dụng để kiểm tra tình trạng của các instances hoặc targets mà target group đang quản lý. Mục tiêu của health checks là đảm bảo rằng chỉ những instance hoặc targets khỏe mạnh và sẵn sàng phục vụ yêu cầu mới sẽ nhận được lưu lượng từ load balancer hoặc các dịch vụ khác.

Dưới đây là một số mục đích chính của việc sử dụng health checks trong target group:

+ **Giữ cho Load Balancer chỉ định tuyến lưu lượng đến các instance hoạt động**: Health checks đảm bảo rằng chỉ có các EC2 instances hoặc targets đang hoạt động và khỏe mạnh mới nhận được lưu lượng từ Load Balancer. Điều này giúp ngăn chặn việc định tuyến lưu lượng đến các instance không hoạt động hoặc gặp sự cố.

+ **Tăng tính sẵn sàng và độ tin cậy của ứng dụng**: Bằng cách chấp nhận chỉ những instance hoạt động và khỏe mạnh vào target group, bạn đảm bảo rằng ứng dụng của mình luôn sẵn sàng phục vụ yêu cầu từ người dùng mà không gặp sự cố.

+ **Tự động phát hiện và xử lý các sự cố**: Nếu một EC2 instance hoặc target không vượt qua health check, load balancer hoặc các dịch vụ khác có thể tự động loại bỏ nó khỏi quá trình định tuyến lưu lượng. Điều này giúp tự động phát hiện và xử lý các sự cố mà không cần sự can thiệp thủ công.

5. Nhấn **next** để chuyển sang **step 2**

6. Trong **step 2** (**Register targets**)
- Chọn 2 instance **Webserver1** và **Webserver2**
- Chọn **Include as pendding below**

![Create TG](/images/6/create-target-group/005.png?featherlight=false&width=90pc)

7. Kiểm tra lại 2 instance đã được thêm vào target và nhấn **Create target group**

![Create TG](/images/6/create-target-group/006.png?featherlight=false&width=90pc)

8. Hoàn thành tạo target group

![Create TG](/images/6/create-target-group/007.png?featherlight=false&width=90pc)

