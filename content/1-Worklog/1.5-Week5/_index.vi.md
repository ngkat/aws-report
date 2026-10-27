---
title: "Worklog Tuần 5"
date: 12-10-2026
weight: 1
chapter: false
pre: "  1.5  "
---


### Mục tiêu tuần 5:

* Tiến hành làm việc với project nhóm.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - Tìm concept chính cho project <br> - Thảo luận nhóm, trao đổi ý kiến và ý tưởng giữa các thành viên <br> - Sàng lọc, cân nhắc và chọn ra concept cuối cùng                                                                                             | 12/10/2026   | 12/10/2026      |
| 3   | - Brainstorm, xây dựng định hướng cho project <br> - Tạo bộ khung nền tảng để vận hành <br> - Phân công công việc sơ bộ cho các thành viên                                            | 13/10/2026   | 13/10/2026      |
| 4   | - Set up Backend với AWS Console <br>&emsp; + API Gateway <br>&emsp; + Lambda | 14/10/2026   | 14/10/2026      |
| 5   | - Set up Backend với AWS Console <br>&emsp; + Request validation <br>&emsp; + Session ID                  | 15/10/2026   | 15/10/2026      |
| 6   | - Set up Backend với AWS Console <br>&emsp; + Conversation history <br>&emsp; + Dynamo DB <br>&emsp; + Gọi RAG                                                                                         | 16/10/2026   | 16/10/2026      |


### Kết quả đạt được tuần 5:

* Tạo thành công Lambda legal-ai-chat-lambda (Runtime Python 3.12)
* Tạo thành công REST API legal-ai-chat-api
* Tạo Resource /chat và Method POST với Lambda Proxy Integration
* Đã Deploy API lên Stage prod và có Invoke URL
* Đã đính kèm Policy AmazonDynamoDBFullAccess cho IAM Role của Lambda
* Đã cập nhật mã nguồn Lambda có chứa boto3 để đọc/ghi DynamoDB
* Đã cập nhật code Lambda hỗ trợ tạo session_id tự động và xử lý GET /history/{session_id}
* Tạo thành công resource /history/{session_id} với method GET trên API Gateway