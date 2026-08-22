---
title: "Xây dựng AI Application trên AWS: Developer thực sự cần những gì?"
date: 2026-07-04
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

## Chủ đề bài viết

**Link bài đăng:** [Xem bài viết trên Facebook](https://www.facebook.com/groups/awsstudygroupfcj/permalink/2228769511221342/?rdid=BHSRlBz1EoDanLJa)

## Giới thiệu chung

Bài viết thứ ba mở rộng khỏi phạm vi bảo mật để đi vào một chủ đề lớn hơn: **xây dựng AI Application trên AWS dưới góc nhìn của developer**. Mục tiêu của bài không phải là giới thiệu một mô hình AI đơn lẻ, mà là trả lời một câu hỏi thực tế:

> Tôi muốn xây dựng một ứng dụng AI trên AWS, vậy tôi thực sự cần chuẩn bị những gì?

Bài viết nhấn mạnh rằng một AI Application hoàn chỉnh không thể chỉ dừng ở việc gọi API của một mô hình ngôn ngữ lớn. Để hệ thống thực sự usable và production-ready, developer còn phải quan tâm tới dữ liệu, backend, authentication, RAG, security, evaluation, monitoring và kiến trúc triển khai.

## Nội dung chính

### 1. AI Application không chỉ là một model

Bài viết bắt đầu từ mô hình đơn giản:

`User -> LLM -> Answer`

Cách tiếp cận này phù hợp cho thử nghiệm ban đầu, nhưng chưa đủ cho ứng dụng thực tế. Khi đi vào sản phẩm thật, developer phải trả lời thêm nhiều câu hỏi:

- Model nào phù hợp với bài toán?
- Dữ liệu riêng của ứng dụng nằm ở đâu?
- Làm sao để model sử dụng dữ liệu đó?
- Làm sao ngăn model tạo nội dung không mong muốn?
- Làm sao đánh giá độ chính xác của câu trả lời?
- Làm sao monitor hệ thống khi chạy production?
- Chi phí sẽ thay đổi thế nào khi số lượng người dùng tăng?

### 2. Foundation Model và vai trò của Amazon Bedrock

Bài viết giới thiệu **Amazon Bedrock** như dịch vụ trung tâm trong hệ sinh thái AWS cho bài toán Generative AI. Bedrock cung cấp quyền truy cập được quản lý tới nhiều foundation models từ các nhà cung cấp khác nhau, giúp developer không cần tự vận hành hạ tầng model từ đầu.

Từ đó hình thành một kiến trúc dễ hiểu hơn:

`Application -> Amazon Bedrock -> Foundation Model`

Điểm quan trọng là developer có thể tập trung nhiều hơn vào application layer thay vì phải lo toàn bộ hạ tầng AI backend.

### 3. Developer cần hiểu gì khi chọn model

Bài viết không dừng ở chỗ "có model để gọi", mà nhấn mạnh rằng chọn model là một quyết định kỹ thuật cần cân nhắc nhiều chiều:

- **Chất lượng:** model có phù hợp với loại tác vụ không?
- **Latency:** ứng dụng cần phản hồi thời gian thực hay xử lý nền?
- **Cost:** có thực sự cần model lớn nhất cho mọi request không?
- **Context window:** ứng dụng cần đưa bao nhiêu thông tin vào prompt?

Đây là phần thể hiện tư duy thực tế hơn so với việc chỉ demo chatbot đơn giản.

### 4. RAG và nhu cầu dùng dữ liệu riêng

Một ý rất quan trọng trong bài là **LLM không tự động biết dữ liệu nội bộ của doanh nghiệp hay tổ chức**. Vì vậy, nếu muốn xây AI Assistant cho trường học hoặc doanh nghiệp, cần cơ chế đưa dữ liệu riêng vào quá trình sinh câu trả lời.

Bài viết giải thích khái niệm **RAG - Retrieval-Augmented Generation** qua luồng xử lý:

`User Question -> Retrieve Relevant Information -> Relevant Context -> Foundation Model -> Generated Answer`

Từ đó, bài liên hệ tới **Amazon Bedrock Knowledge Bases** như một managed RAG solution giúp developer giảm bớt công sức xây thủ công pipeline retrieval.

### 5. Các tầng kiến thức developer cần học

Bài viết chia lộ trình học thành 6 tầng, đây là phần có giá trị định hướng khá rõ:

#### Tầng 1 - Application Developer

- HTML / CSS / JavaScript
- React hoặc framework tương đương
- REST API
- Backend
- Database
- Authentication

#### Tầng 2 - AI Fundamentals

- LLM
- Prompt
- Tokens
- Context
- Embeddings
- Inference

#### Tầng 3 - Amazon Bedrock

- Foundation Models
- Model Invocation
- Prompting
- Knowledge Bases
- Guardrails

#### Tầng 4 - RAG

- Documents
- Chunking
- Embeddings
- Retrieval
- Context
- Generation

#### Tầng 5 - Production

- Security
- Evaluation
- Monitoring
- Logging
- Cost Optimization

#### Tầng 6 - Agentic AI

- Tools
- Agents
- Memory
- Multi-step workflows
- Agent evaluation
- Agent observability

### 6. Thông điệp chính của bài viết

Thông điệp mà bài viết truyền tải là: muốn xây AI Application thực tế thì cần tư duy hệ thống, không thể chỉ bắt đầu bằng một framework AI rồi sao chép chatbot mẫu. Cần hiểu ứng dụng ở cả ba lớp:

- Lớp sản phẩm và nghiệp vụ.
- Lớp dữ liệu và AI.
- Lớp vận hành production trên cloud.

## Ý nghĩa của bài viết

Bài viết này có ý nghĩa đặc biệt vì nó gắn trực tiếp với định hướng mở rộng của JobGo, nhất là khi hệ thống đã có tính năng **AI Matching** giữa hồ sơ ứng viên và tin tuyển dụng. Khi viết bài, em có cơ hội hệ thống lại kiến thức xem để một tính năng AI thực sự hữu ích thì backend, dữ liệu đầu vào, master data, đánh giá kết quả và vận hành trên AWS cần chuẩn bị ra sao.

Ngoài ra, bài viết cũng giúp em nhận ra rằng học AI trên AWS nên đi theo lộ trình từ application foundation đến production readiness, thay vì chỉ học mỗi phần mô hình. Đây là góc nhìn thiết thực nếu sau này em phát triển các sản phẩm AI có người dùng thật.

## Tài liệu tham khảo

- Amazon Bedrock overview: <https://aws.amazon.com/bedrock/>
- What is Amazon Bedrock: <https://docs.aws.amazon.com/bedrock/latest/userguide/what-is-bedrock.html>
- Amazon Bedrock Knowledge Bases: <https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html>
- How Knowledge Bases work: <https://docs.aws.amazon.com/bedrock/latest/userguide/kb-how-it-works.html>
- AWS Training - Artificial Intelligence: <https://aws.amazon.com/training/learn-about/ai/>
- AWS Dev Hour - Learn Gen AI from Scratch: <https://aws.amazon.com/training/twitch/aws-dev-hour-learn-gen-ai-from-scratch/>
