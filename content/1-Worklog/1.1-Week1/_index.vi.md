---
Title: "Worklog Tuần 1"
Date: 14-09-2026
Weight: 1
Chapter: false
pre: " 1.1 "
---

### Mục tiêu tuần 1:

* Kết nối, làm quen với các thành viên trong First Cloud AI Journey.
* Hiểu dịch vụ AWS cơ bản, cách dùng console & CLI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu về AWS IAM (User, Group, Policy, Role) <br> - **Thực hành:** <br>&emsp; + Tạo IAM Group & IAM User <br>&emsp; + Tạo IAM Role & Operator User <br> &emsp; + Cấu hình & Sử dụng Switch Role <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                                                                                             | 14/09/2026   | 14/09/2026      | <https://000002.awsstudygroup.com>
| 3   | - Tìm hiểu về Amazon VPC & AWS Site-to-Site VPN (Subnet, Route Table, IGW, NAT Gateway, Security Group, NACL) <br> - **Thực hành:** <br>&emsp; + Khởi tạo VPC, Subnet, Internet Gateway & Route Table <br>&emsp; + Cấu hình Security Group & VPC Flow Logs <br>&emsp; + Triển khai EC2 Instance, NAT Gateway & SSM Session Manager <br>&emsp; + Cấu hình kết nối AWS Site-to-Site VPN <br>&emsp; + Cấu hình VPN nâng cao với Strongswan & Transit Gateway (Tùy chọn) <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                                            | 15/09/2025   | 15/09/2026      | <https://000003.awsstudygroup.com> |
| 4   | - Tìm hiểu về Amazon EC2 (Elastic Compute Cloud) <br> - **Thực hành:** <br>&emsp; + Chuẩn bị VPC & Security Group cho Linux và Windows <br>&emsp; + Khởi tạo & Kết nối Microsoft Windows Server 2025 Instance <br>&emsp; + Khởi tạo & Kết nối Amazon Linux Instance <br>&emsp; + Các thao tác EC2 cơ bản (Đổi Instance Type, quản lý EBS Snapshot, Custom AMI, khôi phục quyền truy cập) <br>&emsp; + Triển khai ứng dụng quản lý người dùng trên Amazon Linux (LAMP Stack / Node.js) <br>&emsp; + Triển khai ứng dụng Node.js trên Windows Server (XAMPP / Node.js) <br>&emsp; + Cấu hình IAM để quản trị chi phí & giới hạn sử dụng tài nguyên EC2 <br>&emsp; + Dọn dẹp tài nguyên (Clean up) | 16/09/2026   | 16/09/2026      | <https://000004.awsstudygroup.com> |
| 5   | - Tìm hiểu EC2 cơ bản: <br>&emsp; + Instance types <br>&emsp; + AMI <br>&emsp; + EBS <br>&emsp; + ... <br> - Các cách remote SSH vào EC2 <br> - Tìm hiểu Elastic IP   <br>                  | 17/09/2026   | 17/09/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành:** <br>&emsp; + Tạo EC2 instance <br>&emsp; + Kết nối SSH <br>&emsp; + Gắn EBS volume                                                                                         | 18/09/2026   | 18/09/2026      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 1:

* Hiểu AWS là gì và nắm được các nhóm dịch vụ cơ bản: 
  * Compute
  * Storage
  * Networking 
  * Database
  * ...

* Đã tạo và cấu hình AWS Free Tier account thành công.

* Làm quen với AWS Management Console và biết cách tìm, truy cập, sử dụng dịch vụ từ giao diện web.

* Cài đặt và cấu hình AWS CLI trên máy tính bao gồm:
  * Access Key
  * Secret Key
  * Region mặc định
  * ...

* Sử dụng AWS CLI để thực hiện các thao tác cơ bản như:

  * Kiểm tra thông tin tài khoản & cấu hình
  * Lấy danh sách region
  * Xem dịch vụ EC2
  * Tạo và quản lý key pair
  * Kiểm tra thông tin dịch vụ đang chạy
  * ...

* Có khả năng kết nối giữa giao diện web và CLI để quản lý tài nguyên AWS song song.
* ...


