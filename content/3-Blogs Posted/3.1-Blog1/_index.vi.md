---
title: "Xây dựng ứng dụng an toàn ngay từ bản thiết kế với AWS Security Agent"
date: 2026-07-02
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

## Chủ đề bài viết

**Series:** AWS Security Agent - Phần 1  
**Link bài đăng:** [Xem bài viết trên Facebook](https://www.facebook.com/groups/660548818043427?multi_permalinks=2227782947986665)

## Giới thiệu chung

Bài viết này tập trung vào một tư tưởng rất quan trọng trong phát triển phần mềm hiện đại: **bảo mật không nên bắt đầu sau khi ứng dụng hoàn thành, mà phải bắt đầu ngay từ giai đoạn thiết kế**. Thay vì đợi đến lúc hệ thống đã triển khai rồi mới kiểm tra lỗ hổng, em trình bày cách đưa tư duy security vào từ lúc xây kiến trúc, phân chia mạng, định nghĩa quyền truy cập và thiết kế luồng dữ liệu.

Từ đó, bài viết giới thiệu **AWS Security Agent** như một trợ lý AI có thể hỗ trợ đội phát triển đánh giá mức độ an toàn của hệ thống trước khi viết code hoặc trước khi đưa kiến trúc vào triển khai thực tế.

## Nội dung chính

### 1. Vì sao bảo mật cần xuất hiện từ bản thiết kế

Trong nhiều dự án, nhóm phát triển thường ưu tiên chức năng, hiệu năng và tiến độ. Tuy nhiên, rất nhiều rủi ro nghiêm trọng lại không xuất phát từ lỗi code nhỏ, mà đến từ các quyết định thiết kế ban đầu, ví dụ:

- Cơ sở dữ liệu đặt ở vùng mạng có thể truy cập từ Internet.
- Máy chủ ứng dụng mở nhiều cổng mạng không cần thiết.
- API nội bộ và API công khai không được tách biệt.
- Thành phần xử lý dữ liệu nhạy cảm không có vùng bảo vệ riêng.
- Quyền IAM được cấp rộng hơn nhu cầu thực tế.

Nếu các vấn đề này chỉ được phát hiện sau khi hệ thống đã hoàn thiện, chi phí sửa đổi sẽ cao hơn nhiều vì phải thay đổi lại kiến trúc, cấu hình mạng và các cơ chế bảo vệ.

### 2. AWS Security Agent là gì

Trong bài viết, em mô tả AWS Security Agent như một công cụ hỗ trợ đánh giá bảo mật bằng AI. Thay vì chỉ quét mã nguồn, công cụ này có thể hỗ trợ phân tích:

- Tài liệu thiết kế hệ thống.
- Sơ đồ kiến trúc.
- Luồng dữ liệu giữa các thành phần.
- Cấu hình triển khai trên AWS.
- Quan hệ truy cập giữa các dịch vụ.

Điểm quan trọng ở đây là chuyển tư duy từ **"sửa lỗi bảo mật"** sang **"thiết kế cho bảo mật"**.

### 3. Threat Modeling và cách nhìn hệ thống theo góc độ rủi ro

Một nội dung cốt lõi của bài viết là threat modeling. Em trình bày đây là quá trình trả lời bốn câu hỏi:

1. Hệ thống cần được bảo vệ trước những mối đe dọa nào?
2. Thành phần nào có nguy cơ bị tấn công?
3. Kẻ tấn công có thể khai thác hệ thống theo những con đường nào?
4. Cần thay đổi thiết kế ra sao để giảm thiểu rủi ro?

AWS Security Agent được nêu như một công cụ hỗ trợ nhóm phát triển nhìn ra sớm các điểm yếu kiến trúc trước khi chúng biến thành lỗ hổng thật trong sản phẩm.

### 4. Liên hệ với dự án JobGo

Để làm rõ hơn, bài viết liên hệ trực tiếp với kiến trúc của hệ thống JobGo, gồm các thành phần như:

- Amazon CloudFront
- Amazon S3
- Amazon EC2
- Amazon RDS PostgreSQL
- AWS IAM
- Amazon CloudWatch

Từ kiến trúc đó, bài viết đặt ra các câu hỏi bảo mật rất thực tế:

- Amazon RDS có nằm trong private subnet hay không?
- EC2 có mở SSH cho toàn bộ Internet không?
- Chỉ CloudFront được truy cập website hay người dùng vẫn có thể truy cập trực tiếp vào máy chủ?
- IAM role của EC2 có bị cấp quá quyền không?
- Dữ liệu trao đổi giữa các thành phần đã được mã hóa hay chưa?

### 5. Ví dụ thực tế được nêu trong bài

Một ví dụ nổi bật là trường hợp triển khai Amazon RDS với cấu hình public để thuận tiện cho giai đoạn phát triển. Về chức năng, hệ thống vẫn chạy bình thường, nhưng về bảo mật thì đây là bề mặt tấn công đáng kể. Bài viết phân tích các khuyến nghị phù hợp như:

- Đưa RDS vào private subnet.
- Chỉ cho phép EC2 truy cập thông qua security group.
- Loại bỏ truy cập trực tiếp từ Internet.
- Tách rõ tầng ứng dụng và tầng dữ liệu.

### 6. Lợi ích của việc đánh giá sớm

Bài viết kết luận rằng việc đánh giá bảo mật từ giai đoạn thiết kế giúp:

- Giảm chi phí sửa lỗi.
- Tạo kiến trúc an toàn hơn.
- Hỗ trợ đội phát triển chưa có nhiều kinh nghiệm bảo mật.
- Đặt nền tảng cho quy trình DevSecOps về sau.

## Ý nghĩa của bài viết

Bài viết này có ý nghĩa lớn với em ở hai khía cạnh.

Thứ nhất, nó giúp em nhìn lại dự án JobGo không chỉ như một ứng dụng web có đầy đủ chức năng, mà như một hệ thống cloud cần được bảo vệ theo tư duy thực tế.

Thứ hai, thông qua việc viết bài, em hiểu rõ hơn rằng bảo mật hiệu quả không nằm ở việc vá lỗi muộn, mà nằm ở chất lượng của các quyết định thiết kế ngay từ ban đầu. Đây là nền tảng quan trọng nếu sau này em tiếp tục làm các hệ thống triển khai trên AWS hoặc các môi trường production tương tự.

## Tài liệu tham khảo

- AWS Security Agent: <https://aws.amazon.com/vi/security-agent/>
