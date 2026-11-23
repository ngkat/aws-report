---
title: "Worklog Tuần 12"
date: 30-11-2026
weight: 2
chapter: false
pre: "  1.12  "
---

### Mục tiêu tuần 12:

* Tìm hiểu Hands-on Tutorial của AWS.

### Các công việc cần triển khai trong tuần này:
| Day | Task | Start date | Completion date | Resource source |
| --- | ---- | ---------- | --------------- | --------------- |
| Mon | - Set up môi trường AWS | 30/11/2026 |30/11/2026 | https://docs.aws.amazon.com/hands-on/latest/setup-environment/setup-environment.html?ref=gsrchandson |
| Tue | - Tạo một dứng dụng iOS | 01/12/2026 | 01/12/2026 | https://docs.aws.amazon.com/hands-on/latest/build-ios-app-amplify/build-ios-app-amplify.html?ref=gsrchandson |
| Wed | - Tạo một Flutter Mobile App bằng AWS Amplify - Phần 2 | 02/12/2026 | 02/12/2026 | https://docs.aws.amazon.com/hands-on/latest/build-flutter-mobile-app-part-two/build-flutter-mobile-app-part-2.html?ref=gsrchandson |
| Thu | - Tạo Continuous Delivery Pipeline | 3/12/2026 | 03/12/2026 | https://docs.aws.amazon.com/hands-on/latest/create-continuous-delivery-pipeline/create-continuous-delivery-pipeline.html?ref=gsrchandson |
| Fri | - Triển khai ứng dụng .NET lên một phiên bản Windows Server 2022 trong Amazon Lightsail | 04/12/2026 | 04/12/2026 | https://docs.aws.amazon.com/hands-on/latest/host-net-web-app/host-net-web-app.html?ref=gsrchandson |


### Kết quả đạt được tuần 12:

* Quản lý backend đám mây không máy chủ (serverless) thông qua giao diện dòng lệnh.
* Thêm tính năng xác thực vào ứng dụng để cho phép người dùng đăng nhập và đăng xuất.
* Tích hợp GraphQL API, cơ sở dữ liệu và giải pháp lưu trữ.
* Chia sẻ backend giữa nhiều dự án khác nhau.

* Sao chép (clone) ứng dụng đã được xây dựng trong hướng dẫn trước đó từ GitHub.
* Sử dụng Amplify CLI để tạo backend Amplify cho ứng dụng này.
* Cập nhật ứng dụng để hiển thị các chuyến đi trước đây.
* Tạo mô hình dữ liệu cho các hoạt động trong chuyến đi và hồ sơ người dùng, đồng thời sử dụng GraphQL API để đồng bộ hóa với backend Amplify.

* Thiết lập kho lưu trữ (repository) trên GitHub cho mã nguồn ứng dụng.
* Tạo môi trường AWS Elastic Beanstalk để triển khai ứng dụng.
* Cấu hình AWS CodeBuild để xây dựng mã nguồn từ GitHub.
* Sử dụng AWS CodePipeline để thiết lập quy trình phân phối liên tục (continuous delivery), bao gồm các giai đoạn: lấy mã nguồn, xây dựng và triển khai.

* Cài đặt các vai trò và tính năng máy chủ cần thiết.
* Cấu hình Visual Studio 2022 Community edition để kết nối với instance của bạn.
* Xuất bản (publish) mẫu ứng dụng web ASP.NET Core lên instance của bạn.