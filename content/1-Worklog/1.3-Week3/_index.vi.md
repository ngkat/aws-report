---
title: "Worklog Tuần 3"
date: 28-09-2026
weight: 1
chapter: false
pre: "  1.3  "
---


### Mục tiêu tuần 3:

* Hiểu và thực hành tối ưu hóa phân phối nội dung toàn cầu với Amazon CloudFront.
* Nắm vững kiến thức mô hình Serverless Compute với AWS Lambda và xây dựng RESTful API bằng Amazon API Gateway.
* Hiểu và cấu hình dịch vụ phân giải tên miền (DNS), quản lý định tuyến và kiểm tra sức khỏe tài nguyên với Amazon Route 53.
* Thành thạo công cụ giám sát (Monitoring), ghi nhật ký (Logging) và kiểm toán hệ thống (Auditing) với Amazon CloudWatch & AWS CloudTrail.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu về Amazon CloudFront (Content Delivery Network - CDN) <br> - **Thực hành:** <br>&emsp; + Khởi tạo CloudFront Distribution <br>&emsp; + Cấu hình Origin là S3 Bucket hoặc Custom Origin (EC2/ALB) <br>&emsp; + Cấu hình Origin Access Control (OAC) để bảo mật S3 Bucket <br>&emsp; + Thiết lập chính sách Caching, Behavior và HTTPS/SSL Certificate <br>&emsp; + Tối ưu hóa phân phối nội dung và kiểm tra vô hiệu hóa Cache (Invalidation) <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                                                                                             | 28/09/2026   | 28/09/2026      | <https://000008.awsstudygroup.com>
| 3   | - Tìm hiểu về AWS Lambda & Serverless Compute <br> - **Thực hành:** <br>&emsp; + Khởi tạo Lambda Function bằng AWS Console / CLI <br>&emsp; + Viết và thực thi kịch bản xử lý dữ liệu (Node.js / Python) <br>&emsp; + Cấu hình Trigger tự động từ các dịch vụ AWS (S3, API Gateway, DynamoDB) <br>&emsp; + Cấu hình Environment Variables & IAM Role cấp quyền cho Lambda <br>&emsp; + Giám sát và kiểm tra Log hoạt động qua Amazon CloudWatch Logs <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                                            | 29/09/2026   | 29/09/2026      | <https://000010.awsstudygroup.com> |
| 4   | - Tìm hiểu về Amazon API Gateway (REST API & HTTP API) <br> - **Thực hành:** <br>&emsp; + Khởi tạo API Gateway (REST API / HTTP API) <br>&emsp; + Cấu hình Resources, Methods (GET, POST, PUT, DELETE) & Integration Types <br>&emsp; + Tích hợp API Gateway với AWS Lambda Function (Serverless Backend) <br>&emsp; + Cấu hình CORS (Cross-Origin Resource Sharing) & Authentication / Authorization <br>&emsp; + Triển khai API lên Stage (Dev / Prod) & Kiểm tra gọi API <br>&emsp; + Dọn dẹp tài nguyên (Clean up) | 30/09/2026   | 30/09/2026      | <https://000011.awsstudygroup.com> |
| 5   | - Tìm hiểu về Amazon Route 53 (Domain Name System - DNS) <br> - **Thực hành:** <br>&emsp; + Đăng ký tên miền hoặc cấu hình Hosted Zone trên Amazon Route 53 <br>&emsp; + Tạo và quản lý các bản ghi DNS (A, CNAME, MX, TXT) <br>&emsp; + Cấu hình Routing Policies (Simple, Weighted, Latency-based, Failover, Geolocation) <br>&emsp; + Thiết lập Route 53 Health Checks để giám sát trạng thái tài nguyên <br>&emsp; + Tích hợp Route 53 với CloudFront / Application Load Balancer (ALB) / S3 Static Website <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                  | 01/10/2026   | 01/10/2026      | <https://000060.awsstudygroup.com> |
| 6   | - Tìm hiểu về Amazon Route 53 Routing Policies nâng cao (Weighted, Latency-Based, Failover, Geolocation, Geoproximity, Multi-value Answer) <br> - **Thực hành:** <br>&emsp; + Khởi tạo môi trường đa Region với EC2 / Application Load Balancer (ALB) <br>&emsp; + Cấu hình các loại Routing Policy để điều hướng truy cập tối ưu theo vị trí địa lý và độ độ trễ <br>&emsp; + Thiết lập Failover Routing Policy kết hợp Route 53 Health Checks để tự động chuyển hướng khi hệ thống gặp sự cố <br>&emsp; + Kiểm tra và kiểm thử điều hướng lưu lượng truy cập thực tế <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                                                                                         | 02/10/2026   | 02/10/2026      | <https://000061.awsstudygroup.com> |


### Kết quả đạt được tuần 3:

* Tối ưu hóa và bảo mật phân phối nội dung qua Amazon CloudFront:
  * Tạo và quản lý CloudFront Distribution tích hợp với Origin (S3 Bucket / ALB / EC2).
  * Bảo mật S3 Bucket bằng Origin Access Control (OAC) và cấu hình chính sách Caching/Behavior tối ưu.

* Xây dựng kiến trúc Serverless với AWS Lambda & API Gateway:
  * Khởi tạo, viết code xử lý dữ liệu (Node.js / Python) và gán IAM Role cho AWS Lambda.
  * Cấu hình Trigger tự động từ các dịch vụ AWS và giám sát qua CloudWatch Logs.
  * Tạo REST API / HTTP API trên Amazon API Gateway, tích hợp với Lambda Function làm Serverless Backend.
  * Cấu hình CORS, Authentication/Authorization và triển khai API lên các môi trường (Dev / Prod).

* Quản trị tên miền và định tuyến mạng với Amazon Route 53:
  * Khởi tạo Hosted Zone, đăng ký và quản lý các bản ghi DNS (A, CNAME, MX, TXT).
  * Làm chủ các chính sách định tuyến (Simple, Weighted, Latency-based, Failover, Geolocation) và cấu hình Health Checks giám sát tài nguyên.
  * Tích hợp thành công Route 53 với CloudFront, Load Balancer và S3 Static Website.

* Giám sát, cảnh báo và kiểm toán hệ thống với CloudWatch & CloudTrail:
  * Xây dựng CloudWatch Dashboards để theo dõi các chỉ số hoạt động (Metrics) của tài nguyên.
  * Thiết lập CloudWatch Alarms kết hợp Amazon SNS để tự động gửi cảnh báo khi có sự cố.
  * Quản lý Log Group, Log Stream, Metric Filters và cấu hình EventBridge xử lý sự kiện tự động.
  * Kích hoạt AWS CloudTrail để ghi chép và kiểm toán toàn bộ nhật ký thao tác API trong tài khoản.

* Tối ưu chi phí bằng cách thực hiện dọn dẹp (Clean up) tài nguyên sau mỗi bài thực hành.