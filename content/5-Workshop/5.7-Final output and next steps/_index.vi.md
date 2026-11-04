---
title : "Thành quả cuối cùng và hướng phát triển"
date : 15-10-2026
weight : 7 
chapter : false
pre : "  5.7  "
---

#### Thành quả

* Hệ thống serverless backend hoàn chỉnh, tự co giãn và, theo ghi nhận của nhóm, tốn $0 nhờ nằm trong AWS Free Tier.
* Luồng RAG vận hành được: mỗi request tra cứu điều luật từ DynamoDB và kết hợp với LLM để đưa ra câu trả lời có căn cứ.
* Một API endpoint ổn định, sẵn sàng cho website tĩnh và để các thành viên kiểm thử.

#### Hạn chế đã biết

* Tra cứu theo từ khóa có thể bỏ sót điều luật liên quan.
* Câu trả lời là văn bản thuần; chưa có mức rủi ro có cấu trúc.
* LLM chạy ngoài AWS và API chưa có xác thực.

#### Hướng phát triển

* Phản hồi có cấu trúc với mức rủi ro (Low / Medium / High / Insufficient evidence), điều khoản, bằng chứng và nguồn.
* Báo cáo sự cố có người xác nhận kèm cảnh báo email qua Amazon SNS (chỉ tóm tắt, không có dữ liệu nhạy cảm).
* Lịch sử hội thoại trong DynamoDB có TTL.
* Đánh giá Amazon Bedrock và Bedrock Knowledge Bases để giữ toàn bộ dữ liệu trong AWS (kiểm tra giá hiện hành và region hỗ trợ trước).