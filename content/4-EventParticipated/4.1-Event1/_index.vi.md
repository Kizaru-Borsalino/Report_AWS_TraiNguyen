---
title: "Chung kết cuộc thi Cloud Architect"
date: 2026-07-11
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

## Thông tin sự kiện

| Nội dung | Chi tiết |
|---|---|
| Tên sự kiện | **Chung kết cuộc thi Cloud Architec t và hai bài thuyết trình về công nghệ** |
| Thời gian | 09:00 - 12:00, ngày 11/07/2026 |
| Địa điểm | Tầng 26, Bitexco Financial Tower |
| Vai trò | Người tham dự |

## Hình ảnh sự kiện

![Hình ảnh Chung kết cuộc thi Cloud Architect](/images/event1.jpg)

## Nội dung tham gia

Trong sự kiện, em tham dự vòng chung kết cuộc thi Cloud Architect với sự tranh tài của hai đội có kết quả nổi bật nhất. Phần thi được thiết kế dưới dạng các câu hỏi trắc nghiệm xoay quanh AWS Cloud, kiến trúc hệ thống, bảo mật, quản lý tài nguyên và các tình huống triển khai thực tế.

Các đội phải trả lời 10 câu hỏi trong thời gian giới hạn, đồng thời sử dụng chiến thuật hợp lý thông qua các quyền hỗ trợ như **Nhân đôi số điểm** hoặc **Rủi ro thấp nhất**. Điều này làm cho phần thi không chỉ kiểm tra kiến thức kỹ thuật mà còn yêu cầu khả năng phân tích, đánh giá mức độ chắc chắn và đưa ra quyết định nhanh.

Qua phần thi, em nhận thấy vai trò Cloud Architect không chỉ dừng lại ở việc ghi nhớ tên dịch vụ AWS. Người làm kiến trúc cần hiểu rõ chức năng, ưu điểm, hạn chế của từng dịch vụ và biết cách kết hợp chúng để xây dựng hệ thống có hiệu năng tốt, khả năng mở rộng, tính sẵn sàng cao, bảo mật và tối ưu chi phí.

## Nội dung chia sẻ về AWS Security

Bên cạnh phần thi, sự kiện còn có phần chia sẻ về bảo mật trên AWS. Nội dung nhấn mạnh rằng khi triển khai ứng dụng trên cloud, bảo mật phải được xem là một phần của kiến trúc ngay từ đầu thay vì chỉ bổ sung sau khi hệ thống đã hoàn thành.

Một nội dung quan trọng là mô hình **Shared Responsibility Model**. AWS chịu trách nhiệm bảo vệ hạ tầng cloud bên dưới, còn người dùng chịu trách nhiệm cấu hình tài khoản, phân quyền truy cập, bảo vệ dữ liệu, thiết lập mạng và giám sát hoạt động của tài nguyên trong môi trường của mình.

### Bảo vệ tài khoản và quyền truy cập

Em được nhắc lại các nguyên tắc cơ bản khi sử dụng IAM, bao gồm không dùng root account cho công việc hằng ngày, bật MFA cho tài khoản quan trọng, cấp quyền theo nguyên tắc least privilege và tránh tạo access key cho root user. Đây là các bước đơn giản nhưng có ảnh hưởng lớn đến mức độ an toàn của hệ thống.

### Bảo vệ mạng

Phần chia sẻ cũng đề cập đến cách sử dụng VPC và Security Group để kiểm soát lưu lượng truy cập. Với một ứng dụng web, hệ thống chỉ nên mở các cổng cần thiết như HTTP/HTTPS, giới hạn SSH theo địa chỉ IP quản trị và đặt database trong private subnet. Database Security Group chỉ nên cho phép kết nối từ backend thay vì mở trực tiếp ra Internet.

### Bảo vệ dữ liệu

Đối với dữ liệu, các cấu hình như S3 Block Public Access, mã hóa dữ liệu khi lưu trữ và khi truyền tải, không đưa secret vào source code hoặc GitHub là những điểm cần đặc biệt chú ý. Khi chạy ứng dụng trên EC2, nên sử dụng IAM Role để cấp quyền truy cập AWS thay vì lưu access key trực tiếp trên server.

### Theo dõi và phát hiện nguy cơ

Sự kiện cũng giới thiệu một số dịch vụ hỗ trợ giám sát và phát hiện rủi ro như CloudTrail, GuardDuty, Security Hub và AWS Shield Standard. CloudTrail giúp theo dõi lịch sử API call, GuardDuty hỗ trợ phát hiện hành vi bất thường, Security Hub tổng hợp các cảnh báo bảo mật, còn Shield Standard giúp bảo vệ cơ bản trước các cuộc tấn công DDoS đối với những dịch vụ được hỗ trợ.

## Bài học rút ra

Sau khi tham gia sự kiện, em hiểu rõ hơn cách một Cloud Architect tư duy khi thiết kế hệ thống trên AWS. Kiến trúc tốt cần cân bằng giữa hiệu năng, bảo mật, khả năng mở rộng, độ tin cậy và chi phí vận hành.

Ngoài ra, phần chia sẻ về AWS Security giúp em nhận ra rằng các cấu hình bảo mật cơ bản như IAM, MFA, Security Group, S3 Block Public Access và theo dõi log là nền tảng quan trọng khi triển khai bất kỳ ứng dụng nào lên cloud. Những kiến thức này hỗ trợ trực tiếp cho project của nhóm khi thiết kế và triển khai hệ thống backend, database và lưu trữ file trên AWS.
