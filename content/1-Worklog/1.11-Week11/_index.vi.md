---
title: "Worklog Tuần 11"
date: 23-11-2026
weight: 2
chapter: false
pre: "  1.11  "
---

### Mục tiêu tuần 11:

* Tìm hiểu Hands-on Tutorial của AWS.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Xây dựng ứng dụng web không máy chủ bằng Generative AI | 16/11/2026 | 16/11/2026 | https://docs.aws.amazon.com/hands-on/latest/build-serverless-web-app-lambda-amplify-bedrock-cognito-gen-ai/build-serverless-web-app-lambda-amplify-bedrock-cognito-gen-ai.html |
| 3 | - Host một web tĩnh | 17/11/2026 | 17/11/2026 | https://docs.aws.amazon.com/hands-on/latest/host-static-website/host-static-website.html?ref=gsrchandson |
| 4 | - Xây dựng web application cơ bản | 18/11/2026 | 18/11/2026 | https://docs.aws.amazon.com/hands-on/latest/build-web-app-s3-lambda-api-gateway-dynamodb/build-web-app-s3-lambda-api-gateway-dynamodb.html?ref=gsrchandson |
| 5 | - Amazon RDS Backup & dùng AWS Backup để khôi phục | 19/11/2026 | 19/11/2026 | https://docs.aws.amazon.com/hands-on/latest/amazon-rds-backup-restore-using-aws-backup/amazon-rds-backup-restore-using-aws-backup.html?ref=gsrchandson |
| 6 | - Gửi email với Amazon SES | 20/11/2026 | 20/11/2026 | https://docs.aws.amazon.com/hands-on/latest/send-an-email-with-amazon-ses/send-an-email-with-amazon-ses.html?ref=gsrchandson |


### Kết quả đạt được tuần 11:

* Định cấu hình AWS Amplify để lưu trữ ứng dụng giao diện người dùng (frontend) của bạn với tính năng triển khai liên tục (continuous deployment) được tích hợp sẵn.
* Định cấu hình Amplify Auth và kích hoạt quyền truy cập vào các mô hình nền tảng (foundation models) trên Amazon Bedrock.
* Xây dựng phần phụ trợ (backend) cho ứng dụng để xử lý các yêu cầu từ ứng dụng web của bạn.
* Sử dụng Amplify Data để gọi phần phụ trợ không máy chủ (serverless backend).
* Kết nối ứng dụng với phần phụ trợ.

* Lưu trữ một trang web tĩnh bằng AWS Amplify thông qua AWS Management Console. AWS Amplify cung cấp dịch vụ lưu trữ được quản lý toàn diện cho các trang web tĩnh và ứng dụng web. Giải pháp lưu trữ của Amplify tận dụng Amazon CloudFront và Amazon S3 để phân phối các tài nguyên trang web của bạn thông qua mạng phân phối nội dung (CDN) của AWS.
* Thiết lập triển khai liên tục: Amplify cung cấp quy trình làm việc dựa trên Git với tính năng triển khai liên tục, cho phép bạn tự động triển khai các bản cập nhật cho trang web của mình mỗi khi có mã nguồn mới được đẩy lên (commit).

* **Lưu trữ (Host):** Xây dựng và triển khai ứng dụng React trên mạng phân phối nội dung (CDN) toàn cầu của AWS.
* **Xác thực (Authenticate):** Thêm tính năng xác thực vào ứng dụng để cho phép người dùng đăng nhập và đăng xuất.
* **Cơ sở dữ liệu (Database):** Tích hợp API thời gian thực, cơ sở dữ liệu và hàm không máy chủ (serverless function).
* **Hàm (Function):** Triển khai một hàm Lambda, hàm này sẽ được kích hoạt khi người dùng đăng ký tài khoản trong ứng dụng.

* Tạo tác vụ sao lưu theo yêu cầu (on-demand backup job) cho cơ sở dữ liệu Amazon RDS.
* Sử dụng kế hoạch sao lưu (backup plan) để sao lưu các tài nguyên Amazon RDS – thông qua AWS Backup, bạn có thể tự động hóa việc sao lưu theo lịch trình.
* Thêm tài nguyên vào kế hoạch sao lưu hiện có bằng cách sử dụng thẻ (tags).
* Khôi phục dữ liệu từ bản sao lưu.

* Xác minh địa chỉ email.
* Xác minh tên miền.
* Gửi email thông qua bảng điều khiển Amazon SES.