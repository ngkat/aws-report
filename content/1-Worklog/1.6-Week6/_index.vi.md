---
title: "Worklog Tuần 6"
date: 19-10-2026
weight: 1
chapter: false
pre: "  1.6  "
---


### Mục tiêu tuần 6:

* Tiếp tục hoàn thiện project nhóm.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Set up Backend với AWS Console <br>&emsp; + Gọi Groq API(dùng model `qwen/qwen3.8-27b`)                                                                                             | 19/10/2026   | 19/10/2026      |
| 3   | - Set up Backend với AWS Console <br>&emsp; + Xây dựng quy trình RAG                                            | 20/10/2026   | 20/10/2026      |
| 4   | - Set up Backend với AWS Console <br>&emsp; + Xây dựng Amazon API Gateway  | 21/10/2026   | 21/10/2026      |
| 5   | - Set up Backend với AWS Console <br>&emsp; + Input Validation <br>&emsp; + Standardized Error Handling                  | 22/10/2026   | 22/10/2026      |
| 6   | - Set up Backend với AWS Console <br>&emsp; + Xây dựng giao diện Web Chat (Frontend)                                                                                         | 23/10/2026   | 23/10/2026      |


### Kết quả đạt được tuần 6:
* Cấu hình biến môi trường bảo mật (GROQ_API_KEY) trên AWS Lambda.
* Khắc phục thành công lỗi Error 1010 / 403 do Cloudflare chặn dải IP của AWS Lambda.
* Tích hợp thành công header giả lập trình duyệt (User-Agent) trong mã nguồn Python urllib để vượt tường lửa.
* Đã tích hợp thành công boto3 trong Lambda để quét, trích xuất dữ liệu pháp lý và bơm vào prompt cho Groq API (qwen/qwen3.8-27b).
* Đã cấu hình route POST /chat liên kết trực tiếp tới hàm AWS Lambda xử lý RAG.
* Đã thiết lập thành công stage mặc định ($default) và lấy thành công Invoke URL công khai.
* Đã kích hoạt cấu hình CORS (Access-Control-Allow-Origin: *, Methods: POST, Headers: Content-Type) để sẵn sàng cho Frontend gọi API.
* Đồng bộ hóa cấu trúc HTTP Response cho toàn bộ hệ thống kèm đầy đủ tiêu đề CORS.
* Xử lý lỗi thiếu biến môi trường cấu hình GROQ_API_KEY.
* Xử lý lỗi timeout mạng khi đường truyền gặp vấn đề.