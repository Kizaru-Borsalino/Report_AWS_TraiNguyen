---
title: "AI Code Review với AWS Security Agent: Phát hiện lỗ hổng bảo mật trước khi ứng dụng được triển khai"
date: 2026-07-03
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

## Chủ đề bài viết

**Series:** AWS Security Agent - Phần 2  
**Link bài đăng:** [Xem bài viết trên Facebook](https://www.facebook.com/groups/660548818043427?multi_permalinks=2228768907888069)

## Giới thiệu chung

Nếu bài viết đầu tiên tập trung vào bảo mật từ thiết kế, thì bài viết thứ hai đi sâu vào giai đoạn lập trình và rà soát mã nguồn. Trọng tâm của bài là: **một ứng dụng chạy đúng nghiệp vụ chưa chắc đã an toàn**. Nhiều lỗ hổng chỉ lộ ra khi nhìn hệ thống dưới góc độ secure coding, authorization, validation và kiểm soát dữ liệu nhạy cảm.

Bài viết giới thiệu cách **AI Code Review** với AWS Security Agent có thể hỗ trợ đội phát triển phát hiện sớm các rủi ro trước khi mã nguồn được merge hoặc trước khi ứng dụng được triển khai.

## Nội dung chính

### 1. Vì sao code đúng chưa đủ

Bài viết mở đầu bằng một tình huống quen thuộc: API đăng nhập của hệ thống hoạt động đúng, người dùng nhập email và mật khẩu, hệ thống xác thực thành công rồi trả về JWT token. Nhìn theo kiểm thử chức năng, mọi thứ đều ổn.

Tuy nhiên, dưới góc nhìn bảo mật thì vẫn còn hàng loạt câu hỏi:

- Có giới hạn số lần đăng nhập thất bại hay chưa?
- JWT có thời gian hết hạn hợp lý không?
- Mật khẩu có được băm bằng thuật toán phù hợp không?
- API có ghi log chứa thông tin nhạy cảm không?
- Có thể brute force bằng cách thử mật khẩu liên tục hay không?

Điểm mạnh của bài viết là làm rõ khác biệt giữa **functional correctness** và **security correctness**.

### 2. AI Code Review là gì

Trong bài, em mô tả AI Code Review là quá trình dùng trí tuệ nhân tạo để:

- Phân tích mã nguồn.
- Nhận diện các rủi ro bảo mật.
- Giải thích lý do tại sao đó là rủi ro.
- Gợi ý hướng khắc phục phù hợp.

Khác với các công cụ chỉ kiểm tra cú pháp, AI Code Review cố gắng hiểu ngữ cảnh xử lý của ứng dụng, luồng dữ liệu, logic xác thực và phân quyền.

### 3. AWS Security Agent hỗ trợ quy trình review như thế nào

Bài viết mô tả bốn bước chính:

1. Đọc và phân tích phần mã mới.
2. Xác định các điểm có nguy cơ gây mất an toàn.
3. Giải thích nguyên nhân và mức độ ảnh hưởng.
4. Đề xuất hướng khắc phục hoặc đoạn mã thay thế.

Nhờ đó, lập trình viên có thể xử lý vấn đề bảo mật sớm ngay ở giai đoạn pull request, thay vì chờ đến lúc đã lên production.

### 4. Các ví dụ gắn với JobGo

#### API đăng nhập

Bài viết nêu rõ một lỗi rất thực tế: nếu hệ thống trả về hai thông báo khác nhau như:

- "Email không tồn tại"
- "Sai mật khẩu"

thì kẻ tấn công có thể lợi dụng điều này để dò tài khoản hợp lệ. Giải pháp tốt hơn là dùng một thông báo chung như:

- "Email hoặc mật khẩu không chính xác"

#### API tải CV

Với tính năng tải CV, bài viết đặt ra những kiểm tra quan trọng:

- Có giới hạn loại tệp không?
- Có giới hạn kích thước không?
- Tên tệp có được chuẩn hóa không?
- Có kiểm tra nội dung thật của tệp hay chỉ dựa vào phần mở rộng?

Đây là ví dụ rất sát với nghiệp vụ JobGo vì hệ thống cho phép ứng viên tải hồ sơ lên trực tiếp.

#### API quản lý tin tuyển dụng

Một rủi ro khác là chỉ kiểm tra người dùng đã đăng nhập, nhưng không kiểm tra họ có thật sự sở hữu bài đăng tuyển dụng đó hay không. Nếu thiếu bước xác minh này, một doanh nghiệp có thể chỉnh sửa hoặc xóa dữ liệu của doanh nghiệp khác.

### 5. Giá trị của việc giải thích, không chỉ cảnh báo

Một ý rất hay trong bài là AWS Security Agent không chỉ nói "đoạn code này có vấn đề", mà còn giải thích:

- Vì sao đó là rủi ro.
- Nếu bị khai thác thì hậu quả là gì.
- Kẻ tấn công có thể tận dụng ra sao.
- Hướng sửa nào phù hợp với ngữ cảnh ứng dụng.

Điều này rất có ích cho các nhóm phát triển chưa có nhiều kinh nghiệm secure coding, vì mỗi nhận xét đều trở thành một bài học thực tế.

### 6. Bài học rút ra

Bài viết nhấn mạnh rằng các chức năng như đăng nhập, tải CV và quản lý tin tuyển dụng đều có thể trở thành điểm tấn công nếu thiếu cơ chế bảo vệ phù hợp. Ứng dụng chạy đúng chưa bao giờ là điều kiện đủ để kết luận ứng dụng an toàn.

## Ý nghĩa của bài viết

Bài viết này giúp em củng cố tư duy rằng bảo mật cần xuất hiện trong chính vòng đời phát triển phần mềm, đặc biệt ở giai đoạn review code. Với dự án JobGo, điều đó rất quan trọng vì hệ thống xử lý nhiều loại dữ liệu nhạy cảm như tài khoản, CV, hồ sơ ứng viên và thông tin tuyển dụng.

Ngoài ra, việc viết bài cũng giúp em hệ thống hóa được nhiều tình huống bảo mật thực tế hơn thay vì chỉ học lý thuyết chung chung. Đây là trải nghiệm hữu ích để sau này em có thể review code kỹ hơn, đặt câu hỏi đúng hơn và chủ động phòng tránh lỗ hổng ngay từ sớm.

## Tài liệu tham khảo

- AWS Security Agent: <https://aws.amazon.com/vi/security-agent/>
