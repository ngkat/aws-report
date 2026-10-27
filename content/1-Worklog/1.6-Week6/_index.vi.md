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
* Cấu hình biến môi trường bảo mật (GROQ_API_KEY) trên AWS Lambda.
* Khắc phục thành công lỗi Error 1010 / 403 do Cloudflare chặn dải IP của AWS Lambda.
* Tích hợp thành công header giả lập trình duyệt (User-Agent) trong mã nguồn Python urllib để vượt tường lửa.
* Đã tích hợp thành công boto3 trong Lambda để quét, trích xuất dữ liệu pháp lý và bơm vào prompt cho Groq API (qwen/qwen3.8-27b).


