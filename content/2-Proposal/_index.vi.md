---
title: "Bản đề xuất"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

## 1. Tóm tắt dự án

Dự án xây dựng một cổng thông tin thực tập cho sinh viên trên nền tảng cloud. Hệ thống hỗ trợ sinh viên tạo hồ sơ, tải CV, tìm kiếm vị trí thực tập và nộp đơn. Doanh nghiệp có thể đăng tin tuyển thực tập, xem danh sách ứng viên và cập nhật trạng thái hồ sơ. Admin quản lý người dùng, duyệt bài đăng, quản lý kỹ năng, vị trí tuyển dụng và nội dung cộng đồng.

Mục tiêu của dự án là tạo một web application hoàn chỉnh có frontend, backend, database, file storage, authentication, logging và khả năng triển khai lên AWS.

## 2. Problem

Sinh viên thường phải tìm thông tin thực tập qua nhiều nguồn rời rạc như mạng xã hội, email, website công ty hoặc các biểu mẫu thủ công. Điều này gây khó khăn trong việc theo dõi trạng thái ứng tuyển, quản lý CV và đánh giá cơ hội phù hợp.

Ở phía doanh nghiệp, việc nhận hồ sơ qua nhiều kênh khiến quá trình lọc ứng viên, cập nhật trạng thái và phản hồi thiếu tập trung. Nhà trường hoặc đơn vị quản trị cũng khó kiểm soát chất lượng bài đăng, tài khoản người dùng và dữ liệu thống kê về nhu cầu tuyển dụng.

Các vấn đề chính:

- Thiếu một nền tảng tập trung cho sinh viên và doanh nghiệp.
- CV và thông tin ứng tuyển chưa được quản lý an toàn, có phân quyền.
- Quy trình duyệt bài tuyển dụng chưa rõ ràng.
- Không có dashboard để theo dõi số lượng bài đăng, ứng viên, kỹ năng và vị trí tuyển dụng phổ biến.
- Việc triển khai thủ công trên máy cá nhân không đáp ứng yêu cầu vận hành thực tế.

## 3. Solution

Giải pháp là xây dựng **Student Internship Portal** theo mô hình web application triển khai trên AWS:

- **Frontend ReactJS + Vite** cung cấp giao diện cho student, company và admin.
- **Backend FastAPI** cung cấp REST API, xử lý nghiệp vụ và phân quyền.
- **JWT Authentication** bảo vệ API và phân tách quyền theo vai trò.
- **Amazon RDS PostgreSQL** lưu dữ liệu người dùng, hồ sơ, bài đăng, đơn ứng tuyển, kỹ năng, thông báo và diễn đàn.
- **Amazon S3** lưu CV trong private bucket; backend chỉ lưu object key và tạo presigned URL tạm thời khi người dùng hợp lệ cần xem file.
- **EC2** chạy backend FastAPI.
- **S3 Static Website Hosting hoặc CloudFront** phục vụ frontend production build.
- **CloudWatch Logs** thu thập log backend và hỗ trợ theo dõi lỗi khi vận hành.

## 4. Kiến trúc tổng quan

```text
User Browser
  -> Frontend React on S3/CloudFront
  -> FastAPI Backend on EC2
  -> Amazon RDS PostgreSQL
  -> Amazon S3 private bucket for CV files
  -> Amazon CloudWatch Logs
```

Luồng chính của hệ thống:

1. Người dùng đăng ký hoặc đăng nhập.
2. Backend xác thực tài khoản và trả JWT.
3. Student cập nhật hồ sơ, upload CV và ứng tuyển vào bài đăng đã được duyệt.
4. Company tạo hồ sơ công ty, đăng vị trí thực tập và xem danh sách ứng viên.
5. Admin duyệt bài đăng, quản lý người dùng, kỹ năng và vị trí tuyển dụng.
6. Khi trạng thái ứng tuyển hoặc bài đăng thay đổi, hệ thống tạo notification cho người liên quan.

## 5. Lợi ích

- Tập trung hóa quá trình tìm kiếm và quản lý thực tập.
- Tăng tính minh bạch nhờ trạng thái ứng tuyển rõ ràng.
- Bảo vệ CV bằng private S3 bucket và presigned URL.
- Dễ mở rộng database và backend khi lượng người dùng tăng.
- Phù hợp với chủ đề **Application Development on AWS** vì ứng dụng có đủ lớp frontend, backend, database, storage và monitoring.
