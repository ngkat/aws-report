---
Title: "Worklog Tuần 1"
Date: 14-09-2026
Weight: 1
Chapter: false
pre: " 1.1 "
---

### Mục tiêu tuần 1:

* Hiểu và thực hành phân quyền, quản lý truy cập an toàn trên AWS bằng IAM (User, Group, Policy, Role, Switch Role).
* Hiểu cấu trúc mạng ảo Amazon VPC, các thành phần định tuyến, bảo mật và thiết lập kết nối AWS Site-to-Site VPN.
* Nắm vững cách khởi tạo, quản lý và triển khai ứng dụng thực tế trên dịch vụ máy chủ ảo Amazon EC2 (Linux & Windows).
* Biết cách cấp quyền cho ứng dụng truy cập dịch vụ AWS an toàn thông qua IAM Role và sử dụng môi trường AWS CloudShell.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu về AWS IAM (User, Group, Policy, Role) <br> - **Thực hành:** <br>&emsp; + Tạo IAM Group & IAM User <br>&emsp; + Tạo IAM Role & Operator User <br> &emsp; + Cấu hình & Sử dụng Switch Role <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                                                                                             | 14/09/2026   | 14/09/2026      | <https://000002.awsstudygroup.com>
| 3   | - Tìm hiểu về Amazon VPC & AWS Site-to-Site VPN (Subnet, Route Table, IGW, NAT Gateway, Security Group, NACL) <br> - **Thực hành:** <br>&emsp; + Khởi tạo VPC, Subnet, Internet Gateway & Route Table <br>&emsp; + Cấu hình Security Group & VPC Flow Logs <br>&emsp; + Triển khai EC2 Instance, NAT Gateway & SSM Session Manager <br>&emsp; + Cấu hình kết nối AWS Site-to-Site VPN <br>&emsp; + Cấu hình VPN nâng cao với Strongswan & Transit Gateway (Tùy chọn) <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                                            | 15/09/2025   | 15/09/2026      | <https://000003.awsstudygroup.com> |
| 4   | - Tìm hiểu về Amazon EC2 (Elastic Compute Cloud) <br> - **Thực hành:** <br>&emsp; + Chuẩn bị VPC & Security Group cho Linux và Windows <br>&emsp; + Khởi tạo & Kết nối Microsoft Windows Server 2025 Instance <br>&emsp; + Khởi tạo & Kết nối Amazon Linux Instance <br>&emsp; + Các thao tác EC2 cơ bản (Đổi Instance Type, quản lý EBS Snapshot, Custom AMI, khôi phục quyền truy cập) <br>&emsp; + Triển khai ứng dụng quản lý người dùng trên Amazon Linux (LAMP Stack / Node.js) <br>&emsp; + Triển khai ứng dụng Node.js trên Windows Server (XAMPP / Node.js) <br>&emsp; + Cấu hình IAM để quản trị chi phí & giới hạn sử dụng tài nguyên EC2 <br>&emsp; + Dọn dẹp tài nguyên (Clean up) | 16/09/2026   | 16/09/2026      | <https://000004.awsstudygroup.com> |
| 5   | - Tìm hiểu về cấp quyền ứng dụng truy cập dịch vụ AWS qua IAM Role <br> - **Thực hành:** <br>&emsp; + Tạo IAM Role cấp quyền truy cập dịch vụ AWS <br>&emsp; + Cấu hình & Gán IAM Role cho ứng dụng (EC2/Lambda) <br>&emsp; + Kiểm tra quyền truy cập của ứng dụng tới dịch vụ AWS <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                  | 17/09/2026   | 17/09/2026      | <https://000048.awsstudygroup.com> |
| 6   | - Tìm hiểu về AWS CloudShell (Command-line environment) <br> - **Thực hành:** <br>&emsp; + Khởi tạo môi trường AWS CloudShell <br>&emsp; + Các lệnh Linux cơ bản & Thao tác với tệp <br>&emsp; + Quản lý tài nguyên bằng AWS CLI trên CloudShell <br>&emsp; + Upload / Download tệp giữa CloudShell và máy cục bộ <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                                                                                         | 18/09/2026   | 18/09/2026      | <https://000049.awsstudygroup.com> |


### Kết quả đạt được tuần 1:

* Hiểu và thực hành quản lý truy cập với AWS IAM: 
  * Hiểu và thực hành quản lý truy cập với AWS IAM:
  * Cấu hình IAM Role & Operator User.
  * Thực hành Switch Role để chuyển đổi vai trò truy cập an toàn. 

* Thành thạo khởi tạo và cấu hình mạng Amazon VPC:
  * Khởi tạo VPC, Subnet, Internet Gateway & Route Table.
  * Thiết lập bảo mật với Security Group & giám sát với VPC Flow Logs.
  * Triển khai NAT Gateway, SSM Session Manager và kết nối AWS Site-to-Site VPN.
  * Cấu hình VPN nâng cao với Strongswan & Transit Gateway.

* Nắm vững quản trị và sử dụng máy chủ ảo Amazon EC2:
  * Khởi tạo, cấu hình và kết nối thành công với Microsoft Windows Server 2025 & Amazon Linux.
  * Thực hiện các thao tác quản trị EC2: Đổi Instance Type, quản lý EBS Snapshot, Custom AMI, khôi phục quyền truy cập.
  * Triển khai ứng dụng quản lý người dùng (Node.js/LAMP Stack) trên cả hai môi trường Linux và Windows.
  * Áp dụng chính sách IAM để kiểm soát chi phí và giới hạn sử dụng tài nguyên EC2.

* Cấp quyền cho ứng dụng và thao tác trên AWS CloudShell:
  * Tạo và gán IAM Role cho ứng dụng (EC2/Lambda) để truy cập dịch vụ AWS an toàn.
  * Sử dụng thành thạo môi trường CLI trên AWS CloudShell (thao tác lệnh Linux, quản lý tài nguyên qua AWS CLI, Upload/Download tệp).

* Thực hiện dọn dẹp (Clean up) tài nguyên sau mỗi bài thực hành để tối ưu chi phí.