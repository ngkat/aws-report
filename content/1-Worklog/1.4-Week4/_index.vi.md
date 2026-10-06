---
title: "Worklog Tuần 4"
date: 05-10-2026
weight: 1
chapter: false
pre: "  1.4  "
---


### Mục tiêu tuần 4:

* Hiểu và thực hành xây dựng các quy trình trích xuất, biến đổi và nạp dữ liệu tự động (ETL Pipeline) với AWS Glue.
* Nắm vững cách truy vấn, phân tích dữ liệu không cấu trúc và bán cấu trúc trên S3 bằng ngôn ngữ SQL với Amazon Athena.
* Thành thạo việc điều phối quy trình tự động hóa (Workflow Orchestration) đa dịch vụ bằng AWS Step Functions.
* Hiểu kiến trúc kho dữ liệu đám mây (Cloud Data Warehouse) và kỹ thuật nạp/truy vấn dữ liệu hiệu năng cao với Amazon Redshift.
* Nắm vững cách khởi tạo và quản lý các cụm xử lý dữ liệu lớn (Big Data Frameworks như Apache Spark, Hadoop, Hive) trên Amazon EMR.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm hiểu về AWS Glue (Serverless Data Integration Service) <br> - **Thực hành:** <br>&emsp; + Khởi tạo AWS Glue Data Catalog & Cấu hình Glue Crawler để tự động phát hiện Schema dữ liệu <br>&emsp; + Tạo và cấu hình AWS Glue Database & Tables <br>&emsp; + Xây dựng và khởi chạy tác vụ ETL (Extract, Transform, Load) bằng AWS Glue Job <br>&emsp; + Thực hiện biến đổi dữ liệu (Data Transformation) và lưu kết quả vào S3 / Redshift / DynamoDB <br>&emsp; + Tự động hóa và lập lịch chạy ETL Jobs bằng AWS Glue Triggers / Workflows <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                                                                                             | 05/10/2026   | 05/10/2026      | <https://000092.awsstudygroup.com>
| 3   | - Tìm hiểu về Amazon Athena (Interactive Query Service) - **Thực hành:** <br>&emsp; + Cấu hình vị trí lưu kết quả truy vấn (Query Result Location) trên S3 <br>&emsp; + Khởi tạo Database và Table trong Athena từ dữ liệu lưu trữ trữ trên Amazon S3 <br>&emsp; + Thực thi các truy vấn SQL để phân tích và khám phá dữ liệu trực tiếp trên S3 <br>&emsp; + Cấu hình Partitioning và định dạng dữ liệu tối ưu (Parquet / ORC) để nâng cao hiệu năng và giảm chi phí truy vấn <br>&emsp; + Tích hợp Athena với AWS Glue Data Catalog để quản lý Schema dữ liệu tự động <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                                            | 06/10/2026   | 06/10/2026      | <https://000094.awsstudygroup.com> |
| 4   | - Tìm hiểu về AWS Step Functions (Serverless Visual Workflow) <br> - **Thực hành:** <br>&emsp; + Khởi tạo State Machine trên AWS Step Functions bằng Visual Workflow Studio hoặc Amazon States Language (ASL) <br>&emsp; + Cấu hình các trạng thái cơ bản (Task, Choice, Parallel, Map, Pass, Fail) <br>&emsp; + Tích hợp Step Functions với các dịch vụ AWS khác (AWS Lambda, Amazon SQS, Amazon SNS, DynamoDB) <br>&emsp; + Thực thi State Machine, truyền dữ liệu đầu vào (Input/Output Processing) và theo dõi luồng điều khiển <br>&emsp; + Cấu hình Error Handling (Retry & Catch) để xử lý ngoại lệ trong quy trình <br>&emsp; + Dọn dẹp tài nguyên (Clean up) | 07/10/2026   | 07/10/2026      | <https://000130.awsstudygroup.com> |
| 5   | - Tìm hiểu về Amazon Redshift (Cloud Data Warehouse) <br> - **Thực hành:** <br>&emsp; + Khởi tạo Amazon Redshift Cluster / Redshift Serverless <br>&emsp; + Cấu hình hạ tầng mạng VPC, Security Group & IAM Role kết nối dữ liệu từ S3 <br>&emsp; + Khởi tạo Database, Schema và Tables tối ưu hóa với Distribution Keys & Sort Keys <br>&emsp; + Thực hiện nạp dữ liệu từ Amazon S3 vào Redshift bằng lệnh COPY <br>&emsp; + Thực thi các truy vấn SQL phân tích dữ liệu hiệu năng cao <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                  | 08/10/2026   | 08/10/2026      | <https://000093.awsstudygroup.com> |
| 6   | - Tìm hiểu về Amazon EMR (Elastic MapReduce - Managed Big Data Framework) <br> - **Thực hành:** <br>&emsp; + Khởi tạo EMR Cluster với các framework xử lý dữ liệu lớn (Apache Spark / Hadoop / Hive) <br>&emsp; + Cấu hình IAM Roles, EC2 Instance Types và Subnet cho Cluster <br>&emsp; + Chuẩn bị và tải dữ liệu/kịch bản xử lý (Spark / PySpark job) lên Amazon S3 <br>&emsp; + Gửi tác vụ xử lý dữ liệu (Submit Steps / Jobs) tới EMR Cluster <br>&emsp; + Theo dõi quá trình thực thi, lưu trữ kết quả đầu ra vào S3 và quản lý vòng đời EMR Cluster <br>&emsp; + Dọn dẹp tài nguyên (Clean up)                                                                                         | 09/10/2026   | 09/10/2026      | <https://000095.awsstudygroup.com> |


### Kết quả đạt được tuần 4:

* Xây dựng quy trình tích hợp và biến đổi dữ liệu tự động với AWS Glue:
  * Khởi tạo Glue Crawler để tự động quét và phát hiện Schema, lưu trữ vào AWS Glue Data Catalog.
  * Thiết lập AWS Glue Database/Tables và tạo kịch bản ETL biến đổi dữ liệu lưu trữ vào S3 / Redshift / DynamoDB.
  * Tự động hóa và lập lịch chạy ETL Jobs bằng Glue Triggers và Workflows.

* Truy vấn dữ liệu tức thì trên S3 với Amazon Athena:
  * Khởi tạo Database/Table trong Athena kết nối trực tiếp với dữ liệu trên Amazon S3.
  * Thực thi các câu lệnh SQL để phân tích dữ liệu trực tiếp không cần khởi tạo hạ tầng máy chủ.
  * Tối ưu hóa chi phí và tốc độ truy vấn bằng kỹ thuật Phân vùng (Partitioning) và chuyển đổi sang định dạng cột (Parquet / ORC).

* Điều phối luồng công việc phức tạp với AWS Step Functions:
  * Thiết kế State Machine trực quan bằng Visual Studio hoặc Amazon States Language (ASL).
  * Tích hợp thành công Step Functions điều phối đa dịch vụ (Lambda, SQS, SNS, DynamoDB).
  * Cấu hình cơ chế xử lý ngoại lệ, thử lại (Retry & Catch) và kiểm soát luồng dữ liệu truyền qua các bước.

* Triển khai kho dữ liệu phân tích quy mô lớn với Amazon Redshift:
  * Khởi tạo Redshift Cluster / Serverless kết nối an toàn trong VPC.
  * Thiết lập Distribution Keys và Sort Keys để tối ưu hóa truy vấn dữ liệu lớn.
  * Sử dụng lệnh COPY để nạp nhanh lượng lớn dữ liệu từ Amazon S3 vào Redshift.

* Xử lý dữ liệu lớn bằng Big Data Framework với Amazon EMR:
  * Triển khai EMR Cluster cấu hình các công cụ Spark, Hadoop, Hive.
  * Gửi và quản lý các tác vụ xử lý dữ liệu (Spark/PySpark Jobs) từ kịch bản lưu trên S3.
  * Lưu trữ kết quả phân tích về S3 và tối ưu chi phí bằng cách tắt cụm sau khi hoàn thành công việc.

* Tối ưu chi phí bằng cách thực hiện dọn dẹp (Clean up) tài nguyên sau mỗi bài thực hành.