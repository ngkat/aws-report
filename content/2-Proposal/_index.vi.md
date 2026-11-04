---
title: "Bản đề xuất"
date: 14-10-2026
weight: 2
chapter: false
pre: "  2  "
---


# Hệ Thống RAG Tư vấn Pháp luật Tự động (Nghị định 13/2023/NĐ-CP)
## Giải pháp Serverless Kết hợp LLM cho Tra cứu và Phân tích Dữ liệu Pháp lý Thời gian Thực

### 1. Tóm tắt điều hành  
Hệ thống Tư vấn Pháp luật Tự động (Legal RAG Platform) được thiết kế nhằm hỗ trợ người dùng và các thành viên trong đội ngũ tra cứu, phân tích nhanh chóng các quy định pháp luật phức tạp tại Việt Nam, đặc biệt tập trung vào **Nghị định 13/2023/NĐ-CP về bảo vệ dữ liệu cá nhân**. Hệ thống ứng dụng kiến trúc **Serverless** toàn diện trên nền tảng AWS kết hợp với mô hình ngôn ngữ lớn mạnh mẽ từ **Groq API (qwen/qwen3.8-27b)**. Giải pháp mang lại khả năng truy vấn dữ liệu chính xác dựa trên ngữ cảnh thực tế, loại bỏ tình trạng bịa đặt thông tin (hallucination) của AI, đồng thời tối ưu hóa chi phí vận hành ở mức tối thiểu ($0 nhờ tận dụng AWS Free Tier).  

### 2. Tuyên bố vấn đề  
### Vấn đề hiện tại
* Các văn bản pháp luật như Nghị định 13/2023/NĐ-CP rất dài, khô khan và khó tra cứu thủ công đối với người không chuyên.
* Các công cụ AI tổng quát thông thường (như ChatGPT bản free) thường thiếu dữ liệu chuyên sâu về luật pháp Việt Nam hoặc dễ đưa ra các câu trả lời chung chung, thiếu căn cứ pháp lý chính xác.
* Việc xây dựng một hệ thống AI tự túc thường tốn kém chi phí phần cứng và phức tạp trong khâu vận hành máy chủ.

### Giải pháp
* Xây dựng luồng **RAG (Retrieval-Augmented Generation)** tự động: Khi người dùng đặt câu hỏi, hệ thống sẽ quét cơ sở dữ liệu để lấy các điều khoản luật chính xác nhất, sau đó tiêm (inject) vào System Prompt để LLM xử lý và đưa ra câu trả lời có trích dẫn điều khoản rõ ràng.
* Sử dụng **Amazon DynamoDB** làm kho lưu trữ các điều khoản luật (`LegalArticles`) đã được trích xuất.
* Sử dụng **AWS Lambda** làm tầng xử lý logic backend, kết hợp với **Amazon API Gateway** để cung cấp điểm cuối (API Endpoint) ổn định.
* Tích hợp **Groq API** với mô hình `qwen/qwen3.8-27b` để sinh câu trả lời thông minh, mạch lạc.
* Giao diện web tĩnh lưu trữ trên **Amazon S3 Static Website** giúp người dùng tương tác trực quan qua khung chat.

### Lợi ích và hoàn vốn đầu tư (ROI)
* **Độ chính xác cao:** Câu trả lời luôn bám sát ngữ cảnh văn bản luật được cung cấp, minh bạch và có căn cứ.
* **Tối ưu chi phí:** Vận hành hoàn toàn theo mô hình Serverless, tận dụng tối đa AWS Free Tier với chi phí duy trì hàng tháng gần như **$0**.
* **Dễ dàng mở rộng:** Kiến trúc tách rời (Decoupled Architecture) giúp dễ dàng bổ sung thêm các bộ luật mới (như Luật An toàn thông tin mạng, Luật Công nghệ thông tin) vào DynamoDB trong tương lai.

### 3. Kiến trúc giải pháp  
Hệ thống áp dụng mô hình kiến trúc Serverless, kết nối khép kín từ Frontend đến Backend và LLM bên ngoài. 

### Dịch vụ AWS sử dụng
- **Amazon S3 Static Website:** Lưu trữ và phục vụ giao diện trang web tĩnh (`index.html`, CSS, JS) cho người dùng. 
- **Amazon API Gateway:** Cung cấp HTTP/REST API công khai, xử lý cơ chế CORS, làm cổng tiếp nhận request từ client chuyển đến Lambda.  
- **AWS Lambda (Python):** Thực thi mã nguồn backend xử lý logic RAG, gọi dữ liệu từ DynamoDB và tương tác với Groq API.  
- **Amazon DynamoDB (`LegalArticles`):** Lưu trữ cấu trúc các điều khoản luật, hỗ trợ truy vấn từ khóa tốc độ cao.  
- **Groq API (`qwen/qwen3.8-27b`):** Đảm nhận nhiệm vụ tổng hợp và phân tích ngôn ngữ tự nhiên dựa trên ngữ cảnh luật được truyền vào.

### Thiết kế thành phần
- **Giao diện Người dùng (Frontend):** Người dùng truy cập trang web từ S3, nhập câu hỏi vào khung chat. Trình duyệt gửi HTTP POST Request chứa câu hỏi qua HTTPS tới API Gateway.
- **Cổng giao tiếp (API Gateway):** Tiếp nhận request, kiểm tra bảo mật CORS và chuyển tiếp payload dữ liệu tới hàm Lambda.
- **Truy vấn Dữ liệu (Retrieval - DynamoDB):** Hàm Lambda thực hiện hàm `retrieve_legal_context` để quét và tìm kiếm các điều khoản liên quan trong bảng `LegalArticles` (ví dụ: quy định xử lý vi phạm liên quan đến CCCD, dữ liệu cá nhân theo Nghị định 13).
- **Tăng cường & Sinh văn bản (Augmentation & Generation - Groq API):** Lambda đóng gói câu hỏi của người dùng kèm theo ngữ cảnh luật vừa lấy được vào một System Prompt có ràng buộc nghiêm ngặt (chỉ trả lời dựa trên ngữ cảnh được cung cấp), sau đó gọi sang Groq API.
- **Phản hồi (Response Flow):** Groq trả kết quả về Lambda, Lambda định dạng lại cấu trúc JSON chuẩn và trả về qua API Gateway để hiển thị lên khung chat của người dùng.

### 4. Triển khai kỹ thuật  
**Các giai đoạn triển khai**
1. **Định hình Prompt & Cơ chế RAG:** Xây dựng System Prompt định hướng vai trò chuyên gia luật, thiết lập ràng buộc ngữ cảnh (Context Constraint) tuyệt đối không bịa đặt thông tin.
2. **Triển khai Backend & Database:**
* Tạo bảng DynamoDB LegalArticles.
* Viết mã Python trên AWS Lambda tích hợp hàm truy xuất dữ liệu và gọi Groq API.
* Cấu hình API Gateway, bật CORS Headers và xây dựng tầng bắt lỗi chuẩn hóa (mã 400, 502/504, và xử lý mã 429 khi quá giới hạn Groq API).
3. **Kiểm thử & Hoàn thiện:** Sử dụng lệnh `curl` gửi HTTP POST test hoặc test trực tiếp trên giao diện web, kiểm tra log trên Amazon CloudWatch.


### 5. Lộ trình & Mốc triển khai  
- **Giai đoạn Nghiên cứu & Thiết kế:** Xác định phạm vi luật (Nghị định 13/2023/NĐ-CP) và thiết kế luồng dữ liệu RAG.
- **Giai đoạn Lập trình & Triển khai:** Xây dựng cơ sở dữ liệu DynamoDB, hoàn thiện hàm Lambda và cấu hình API Gateway.
- **Giai đoạn Tích hợp & Kiểm thử:** Kết nối giao diện S3 Static Website với API Gateway, test độ chính xác của câu trả lời từ Groq LLM và tối ưu hóa xử lý lỗi.

### 6. Ước tính ngân sách  

- **AWS Infrastructure:**
* Amazon S3: Miễn phí (trong hạn mức Free Tier).
* Amazon API Gateway: Miễn phí (trong hạn mức 1 triệu request đầu tiên/tháng).
* AWS Lambda: Miễn phí (trong hạn mức 1 triệu request/tháng).
* Amazon DynamoDB: Miễn phí (25GB storage, 25 WCU / 25 RCU).
- **Groq API:** Sử dụng gói miễn phí cho mô hình mã nguồn mở (`qwen/qwen3.8-27b`).

*Tổng*: 0 USD

### 7. Đánh giá rủi ro  
#### Rủi ro quá tải API (Rate Limit từ Groq API - Lỗi 429):
- Giải pháp: Xây dựng cơ chế bắt lỗi (Error Handling) và thông báo thân thiện tới người dùng trên giao diện chat khi hệ thống vượt quá tần suất gọi tạm thời.

#### Rủi ro AI trả lời sai lệch (Hallucination):
- Giải pháp: Thắt chặt System Prompt với quy tắc bắt buộc chỉ được sử dụng ngữ cảnh luật được cung cấp từ DynamoDB, tuyệt đối không tự suy diễn ngoài luồng.

#### Rủi ro lỗi CORS trên trình duyệt:
- Giải pháp: Cấu hình đầy đủ CORS Headers (`Access-Control-Allow-Origin: *, POST, OPTIONS`) trực tiếp trên API Gateway.

### 8. Kết quả kỳ vọng  
#### Thành quả kỹ thuật:
Xây dựng thành công một hệ thống Serverless Backend hoàn chỉnh, tự động co giãn, hoạt động ổn định và tối ưu chi phí tuyệt đối ($0).
#### Giá trị thực tiễn:
Cung cấp một cổng giao tiếp API chuẩn hóa và giao diện chat trực quan giúp tra cứu nhanh chóng, chính xác các quy định pháp luật cốt lõi trong Nghị định 13/2023/NĐ-CP, phục vụ hiệu quả cho học tập và nghiên cứu.