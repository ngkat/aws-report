---
title: "Blog 3"
date: --2026
weight: 1
chapter: false
pre: "  3.3  "
---

# GÓC HỌC TẬP AWS: XÂY DỰNG TRANG WEB TĨNH ĐƠN GIẢN, BẢO MẬT VỚI S3 + CLOUDFRONT + ROUTE 53


Khi hoàn thành một trang web tĩnh (HTML/CSS/JS thuần hoặc các bản build từ React, Vue, Next.js), bài toán tiếp theo là lựa chọn giải pháp lưu trữ và phân phối lên internet. Mục tiêu đặt ra thường là: chi phí tối ưu, tốc độ truy cập nhanh, hỗ trợ HTTPS an toàn và không tốn công quản lý server.

Bộ ba dịch vụ Amazon S3 + Amazon CloudFront + Route 53 là kiến trúc chuẩn chuẩn hóa giúp giải quyết bài toán này một cách tối ưu.

---

### 1. Kiến trúc giải pháp & Các bước thực hiện

**Bước 1: Lưu trữ tập tin với Amazon S3**

* Khởi tạo một S3 Bucket để chứa toàn bộ mã nguồn web tĩnh đã build.
* Cấu hình S3 Bucket Policy và cấp quyền truy cập hợp lý.
* Bật tính năng Static website hosting để thiết lập file truy cập mặc định (ví dụ: `index.html` và `404.html`).

**Bước 2: Tăng tốc & Bảo mật với Amazon CloudFront (CDN)**

* Khởi tạo một CloudFront Distribution và trỏ nguồn (Origin) về S3 Bucket vừa tạo.
* **Tăng tốc:** Dữ liệu web được lưu bản sao (cache) tại các Edge Location trên toàn cầu, giúp giảm độ trễ tối đa cho người dùng.
* **Bảo mật:** Tích hợp chứng chỉ SSL/TLS miễn phí từ AWS Certificate Manager (ACM) để kích hoạt giao thức HTTPS. Đồng thời, cấu hình OAC (Origin Access Control) để chặn truy cập trực tiếp vào S3 Bucket từ bên ngoài, chỉ cho phép traffic đi qua CloudFront.

**Bước 3: Định tuyến tên miền với Amazon Route 53**

* Tạo Hosted Zone cho tên miền cá nhân trên Route 53.
* Cấu hình bản ghi A Record (dạng Alias) để trỏ tên miền chính hoặc subdomain về địa chỉ CloudFront Distribution.

---

### 2. Giá trị kỹ thuật & Bài học rút ra

* **Tối ưu chi phí:** Kiến trúc Serverless hoàn toàn không tốn chi phí duy trì máy chủ (Nginx/Apache). Với lượng truy cập nhỏ hoặc các dự án cá nhân, chi phí hàng tháng gần như bằng 0.
* **Khả năng mở rộng (Scalability):** Mạng lưới CDN của CloudFront tự động xử lý khi lượng truy cập tăng đột biến mà không cần nâng cấp hạ tầng.
* **Đơn giản hóa vận hành:** Không cần bận tâm về việc vá lỗi hệ điều hành hay quản lý chứng chỉ SSL định kỳ.

---

### 3. Tổng kết

Đây là một trong những bài thực hành kinh điển nhưng rất quan trọng, giúp bạn nắm vững tư duy kết hợp các dịch vụ cơ bản trên AWS để tạo nên một hệ thống hoàn chỉnh, bảo mật và chuẩn công nghiệp.

---

![alt text](<../../images/aws static website.png>)

...Link...