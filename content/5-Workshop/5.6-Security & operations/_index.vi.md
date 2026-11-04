---
title : "Bảo mật và vận hành"
date : 15-10-2026
weight : 6 
chapter : false
pre : "  5.6  "
---

#### Tổng quan

| Mục | Nội dung |
| --- | -------- |
| Mục đích | Nắm hiện trạng bảo mật, giám sát hoạt động và chi phí, và lập kế hoạch cải tiến |
| Dịch vụ AWS | CloudWatch, AWS Budgets, IAM |

#### 5.6.1. Hiện trạng bảo mật

| Hạng mục | Hiện trạng | Rủi ro | Khuyến nghị |
| -------- | ---------- | ------ | ----------- |
| API Gateway | Công khai, chưa xác thực | AAi có URL cũng gọi được và làm cạn quota Groq | Throttling + usage plan / API key; Cognito sau |
| CORS | Access-Control-Allow-Origin: * | Mọi website đều gọi được API từ trình duyệt | Giới hạn theo origin của trang S3 sau demo |
| Groq API key | Biến môi trường của Lambda | Lộ nếu bị commit hoặc chụp màn hình | Chuyển sang SSM Parameter Store (SecureString); đổi key nếu lộ |
| S3 website | Đọc công khai, chỉ HTTP | Lưu lượng không được mã hóa | Đặt CloudFront phía trước để có HTTPS nếu cần |
| Dữ liệu gửi tới Groq | Câu hỏi rời khỏi AWS | Dữ liệu khách hàng thật có thể ra ngoài tài khoản | Chỉ dùng câu hỏi mẫu; xem chính sách dữ liệu của Groq; cân nhắc Bedrock |
| CloudWatch | Đã bật log Lambda | Log có thể chứa câu hỏi người dùng | Đặt thời gian lưu (7-14 ngày); tránh log nội dung nhạy cảm |

#### 5.6.2. Giám sát và kiểm soát chi phí

**Mục tiêu**
Phát hiện sớm lỗi và chi phí bất thường.

**Các bước**
1. Đặt thời gian lưu log cho log group của Lambda.
2. Tạo alarm cho lỗi Lambda (tùy chọn).
3. Thường xuyên xem trang Free Tier usage trong Billing và giữ cảnh báo Budget ở mục 5.2.

[ CHÈN ẢNH CHỤP ]
Log group / alarm trong CloudWatch
5.6-Security/cloudwatch-dashboard.png

**Kiểm tra**

Request thử nghiệm xuất hiện trong log; cảnh báo Budget đang hoạt động.

#### 5.6.3. Lộ trình siết bảo mật

1. Thêm throttling và usage plan cho API để bảo vệ quota Groq (ưu tiên cao, không phải sửa frontend).
2. Chuyển Groq key sang SSM Parameter Store và chỉ cấp cho Lambda quyền đọc đúng parameter đó.
3. Giới hạn CORS theo origin của website.
4. Thêm đăng nhập Cognito nếu hệ thống ra khỏi chế độ demo.
5. Kiểm thử: gọi API với tốc độ cao để xác nhận throttling; thử câu hỏi prompt injection; quét repository tìm secret.

[ CHÈN ẢNH CHỤP ]
Kết quả kiểm thử bảo mật
5.6-Security/pentest.png