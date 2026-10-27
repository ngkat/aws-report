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

### 3. Dọn dẹp tài nguyên không sử dụng

Các tài nguyên "rác" hoặc tài nguyên độc lập thường là nguyên nhân phát sinh chi phí ẩn:

* **Tắt hoặc xóa EC2 instance:** Dừng các máy chủ thử nghiệm khi không làm việc.
* **Lưu ý Elastic IP:** Elastic IP chỉ miễn phí khi được gán vào một EC2 instance đang ở trạng thái Running. Nếu ngắt kết nối hoặc gán vào instance đang Stopped, bạn vẫn sẽ bị tính phí duy trì.
* **Xóa Unattached EBS Volumes & Snapshots:** Khi xóa EC2 instance, một số EBS volume hoặc snapshot tự động tạo có thể vẫn tồn tại độc lập và tiếp tục tính phí lưu trữ.

---

### 4. Theo dõi chi tiết với AWS Cost Explorer

* **Công cụ trực quan:** AWS Cost Explorer cung cấp biểu đồ phân tích chi phí theo thời gian, theo dịch vụ hoặc theo Tag.
* **Định kỳ kiểm tra:** Thói quen xem báo cáo chi phí 1-2 lần/tuần giúp bạn nhanh chóng phát hiện các dịch vụ đang tiêu tốn ngân sách bất thường.

---

### 5. Tổng kết

Tối ưu và kiểm soát chi phí là một phần không thể thiếu trong tư duy làm việc với Cloud Computing. Thiết lập hạ tầng an toàn ngay từ đầu sẽ giúp bạn thoải mái học tập và thử nghiệm các dịch vụ AWS mà không phải lo lắng về vấn đề chi phí.

---

![alt text](<../../images/aws cost optimization.png>)

https://www.facebook.com/groups/awsstudygroupfcj/posts/2317495209015438/?notif_id=1793075766463069&notif_t=group_post_approved&ref=notif