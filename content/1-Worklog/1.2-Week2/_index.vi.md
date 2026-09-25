---
title: "Worklog Tuần 2"
date: 21-09-2026
weight: 1
chapter: false
pre: "  1.2  "
---


### Mục tiêu tuần 2:

* Hiểu và thực hành lưu trữ dữ liệu đối tượng (Object Storage), lưu trữ lưu lượng truy cập cao và lưu trữ tĩnh trên Amazon S3.
* Nắm vững kiến thức và cách triển khai cơ sở dữ liệu quan hệ (Relational Database) với Amazon RDS.
* Sử dụng thành thạo giao diện dòng lệnh AWS CLI từ cơ bản đến nâng cao (quản lý profile, scripting, lọc dữ liệu JMESPath).
* Hiểu và thực hành quản trị cơ sở dữ liệu NoSQL hiệu năng cao với Amazon DynamoDB.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu về Amazon S3 (Object Storage) <br> - **Thực hành:** <br>&emsp; + Khởi tạo S3 Bucket & Tải dữ liệu lên Bucket <br>&emsp; + Bật tính năng Static Website, cấu hình Block Public Access & cấp quyền Public cho Object <br>&emsp; + Kiểm tra hoạt động của Website và Tối ưu hóa tốc độ bằng Amazon CloudFront <br>&emsp; + Cấu hình Bucket Versioning (Quản lý phiên bản) & Di chuyển Object <br>&emsp; + Thiết lập Replication Object đa Region (Multi-Region Replication) <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                                                                                             | 21/09/2026   | 21/09/2026      | <https://000057.awsstudygroup.com>
| 3   | - Tìm hiểu về Amazon RDS (Relational Database Service) <br> - **Thực hành:** <br>&emsp; + Chuẩn bị môi trường: Tạo VPC, Security Group & Database Subnet Group <br>&emsp; + Khởi tạo RDS Database Instance <br>&emsp; + Khởi tạo EC2 Instance & Triển khai ứng dụng (Application deployment) <br>&emsp; + Thực hiện Sao lưu và Khôi phục dữ liệu (Backup and Restore) <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                                            | 22/09/2026   | 22/09/2026      | <https://000005.awsstudygroup.com> |
| 4   | - Tìm hiểu về AWS Command Line Interface (AWS CLI) <br> - **Thực hành:** <br>&emsp; + Cài đặt AWS CLI trên hệ điều hành (Windows / Linux / macOS) <br>&emsp; + Cấu hình AWS CLI với Access Key & Secret Access Key <br>&emsp; + Sử dụng các câu lệnh AWS CLI cơ bản để quản trị dịch vụ AWS <br>&emsp; + Kiểm tra và xác nhận cấu hình tài khoản <br>&emsp; + Dọn dẹp tài nguyên (Clean up) | 23/09/2026   | 23/09/2026      | <https://000045.awsstudygroup.com> |
| 5   | - Tìm hiểu về AWS Command Line Interface (AWS CLI) nâng cao & Scripting <br> - **Thực hành:** <br>&emsp; + Cấu hình nhiều Profile (Named Profiles) trên AWS CLI <br>&emsp; + Thao tác quản lý tài nguyên nâng cao qua các câu lệnh AWS CLI <br>&emsp; + Tự động hóa tác vụ quản trị AWS bằng Scripting (Bash / PowerShell) <br>&emsp; + Cấu hình định dạng đầu ra (Output Format: JSON, Table, Text) & Lọc dữ liệu (JMESPath) <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                  | 24/09/2026   | 24/09/2026      | <https://000046.awsstudygroup.com> |
| 6   | - Tìm hiểu về Amazon DynamoDB (NoSQL Database) <br> - **Thực hành:** <br>&emsp; + Khởi tạo DynamoDB Table & Cấu hình Partition Key / Sort Key <br>&emsp; + Thực hiện các thao tác dữ liệu (Create, Read, Update, Delete - CRUD) <br>&emsp; + Cấu hình Secondary Indexes (LSI / GSI) để tối ưu truy vấn <br>&emsp; + Kết nối và thao tác với DynamoDB từ EC2 / Lambda <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                                                                                         | 25/09/2026   | 25/09/2026      | <https://000006.awsstudygroup.com> |


### Kết quả đạt được tuần 2:

* Thành thạo dịch vụ lưu trữ Amazon S3: 
  * Tạo S3 Bucket, lưu trữ và quản lý đối tượng dữ liệu.
  * Cấu hình Static Website, cấp quyền truy cập công khai và tăng tốc độ phân phối dữ liệu qua Amazon CloudFront.
  * Thiết lập quản lý phiên bản (Bucket Versioning) và sao chép dữ liệu đa vùng (Multi-Region Replication).

* Triển khai và quản trị cơ sở dữ liệu Amazon RDS:
  * Thiết lập hạ tầng mạng (VPC, Subnet Group, Security Group) tối ưu cho cơ sở dữ liệu.
  * Khởi tạo, kết nối ứng dụng và thực hiện sao lưu/khôi phục dữ liệu (Backup and Restore) trên Amazon RDS.

* Sử dụng AWS CLI chuyên nghiệp và tự động hóa:
  * Cài đặt, cấu hình Access Key và quản lý nhiều Profile (Named Profiles) trên máy cục bộ.
  * Tự động hóa các tác vụ quản trị AWS bằng kịch bản lệnh (Bash / PowerShell).
  * Tùy biến định dạng đầu ra (JSON, Table) và lọc dữ liệu bằng câu lệnh JMESPath.

* Làm chủ cơ sở dữ liệu NoSQL Amazon DynamoDB:
  * Khởi tạo DynamoDB Table, thiết lập Partition Key, Sort Key và các chỉ mục phụ (LSI / GSI).
  * Thực hiện thành thạo các thao tác xử lý dữ liệu CRUD (Create, Read, Update, Delete) và kết nối DynamoDB với ứng dụng.

* Tối ưu chi phí bằng cách thực hiện dọn dẹp (Clean up) tài nguyên sau mỗi bài thực hành.