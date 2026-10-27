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
| 4   | -  | 21/10/2026   | 21/10/2026      |
| 5   | -                   | 22/10/2026   | 22/10/2026      |
| 6   | -                                                                                          | 23/10/2026   | 23/10/2026      |


### Kết quả đạt được tuần 6:
* Thiết lập AWS Lambda Python 3.x runtime thành công.
* Cấu hình biến môi trường bảo mật (GROQ_API_KEY) trên AWS Lambda.
* Khắc phục thành công lỗi Error 1010 / 403 do Cloudflare chặn dải IP của AWS Lambda.
* Tích hợp thành công header giả lập trình duyệt (User-Agent) trong mã nguồn Python urllib để vượt tường lửa.
* Xác định và thử nghiệm các model hoạt động ổn định trên Groq Free Tier (llama-3.1-8b-instant, openai/gpt-oss-120b, v.v.).
* Chuyển đổi thành công sang model chuẩn xác, tốc độ cao qwen/qwen3.8-27b (ngữ cảnh 131K token) hoàn toàn miễn phí và không bị gián đoạn.
* Kiểm tra thành công kết nối đầu ra (Status Code 200 OK).
* Thời gian phản hồi (Latency) tối ưu dưới 2 giây.
* Xử lý cấu trúc JSON trả về (ai_response) hỗ trợ tiếng Việt có dấu rõ ràng (ensure_ascii=False).
* Đã nạp thành công các điều luật thực tế (Điều 9, Điều 13 Nghị định 13/2023/NĐ-CP).
* Đã tích hợp thành công boto3 trong Lambda để quét, trích xuất dữ liệu pháp lý và bơm vào prompt cho Groq API (qwen/qwen3.8-27b).


