---
title: "Blog 2"
date: 27-10-2026
weight: 1
chapter: false
pre: "  3.2  "
---

# GÓC HỌC TẬP AWS: MỚI HỌC AWS CẦN LƯU Ý GÌ ĐỂ KHÔNG "GIẬT MÌNH" VÌ HÓA ĐƠN CUỐI THÁNG?



Một trong những tình huống quen thuộc với người mới bắt đầu trải nghiệm AWS là lỡ tay bật một tài nguyên thử nghiệm rồi quên tắt, để rồi nhận hóa đơn bất ngờ vào cuối tháng. Việc kiểm soát chi phí không chỉ giúp bạn yên tâm thực hành mà còn là kỹ năng cơ bản quan trọng trong quản trị hạ tầng Cloud.

Dưới đây là các thiết lập và lưu ý quan trọng giúp quản lý ngân sách hiệu quả ngay từ những ngày đầu.

---

### 1. Thiết lập AWS Budgets & Billing Alerts

Đây là bước đầu tiên nên thực hiện ngay sau khi khởi tạo tài khoản AWS.

* **Cơ chế:** Cấu hình ngưỡng ngân sách an toàn (ví dụ: $5 hoặc $10). Khi chi phí thực tế hoặc chi phí dự báo vượt quá ngưỡng này, hệ thống sẽ tự động gửi email thông báo.
* **Lợi ích:** Tránh tình trạng tài nguyên chạy ngầm liên tục mà không được phát hiện kịp thời.

---

### 2. Tận dụng AWS Free Tier đúng cách

* **Giới hạn thời gian:** Ví dụ: EC2 cung cấp 750 giờ/tháng cho dòng `t2.micro` hoặc `t3.micro` (tùy Region). Nếu bật đồng thời 2 instance running liên tục, thời gian sử dụng sẽ bị tính gấp đôi và nhanh chóng vượt mức miễn phí.
* **Giới hạn dung lượng:** S3 hay EBS đều có quy định cụ thể về dung lượng lưu trữ và số lượng request. Hãy đọc kỹ điều kiện dịch vụ trước khi khởi tạo.

---

### 3. Đánh giá trải nghiệm thực tế

**Ưu điểm:**

* **Tốc độ triển khai tối ưu:** Đặc biệt phù hợp cho các dự án demo, đồ án môn học hoặc sản phẩm MVP (Minimum Viable Product).
* **Kiến trúc Serverless:** Không tốn chi phí và công sức duy trì hay quản lý máy chủ.
* **Hỗ trợ đa nền tảng:** Tích hợp tốt với các framework phổ biến như React, Next.js, Vue, Flutter, React Native...

**Hạn chế:**

* Khi quy mô ứng dụng mở rộng và yêu cầu tùy chỉnh sâu về hạ tầng (như cấu hình VPC riêng hay phân quyền IAM phức tạp), việc can thiệp vào các tài nguyên do Amplify tự động tạo ra sẽ cần thời gian nghiên cứu thêm.

---

### 4. Tổng kết

AWS Amplify là giải pháp hiệu quả giúp tối ưu hóa quy trình phát triển và đưa sản phẩm lên Cloud một cách chuẩn chỉnh, tiết kiệm thời gian.

---

...Hình ảnh...

...Link...

...Hướng dẫn...