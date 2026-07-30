---
title: "Project"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Đây là phần mô tả dự án thực tiễn được nhóm xây dựng để ứng dụng kiến thức backend, frontend và AWS vào một bài toán gần với nhu cầu thực tế của sinh viên.

### Các phần chính

1. [Backend API](3.1-Blog1/)
2. [Frontend Application](3.2-Blog2/)
3. [Luồng nghiệp vụ và kiểm thử](3.3-Blog3/)
4. [Các bài blog đã đăng](3.4-BlogsPosted/)

## Công nghệ sử dụng

| Thành phần | Công nghệ |
| --- | --- |
| Frontend | ReactJS, Vite, lucide-react |
| Backend | FastAPI, SQLAlchemy, Pydantic |
| Authentication | JWT, refresh token |
| Database local | SQLite |
| Database production | Amazon RDS PostgreSQL |
| File storage | Amazon S3 |
| Deployment | EC2, S3 Static Website Hosting/CloudFront |
| Monitoring | CloudWatch Logs |

## Chức năng chính

### Sinh viên

- Đăng ký, đăng nhập.
- Tạo và cập nhật hồ sơ cá nhân.
- Upload CV.
- Xem và tìm kiếm vị trí thực tập.
- Tìm kiếm công ty theo tên, mô tả hoặc địa điểm.
- Nộp đơn ứng tuyển.
- Xem trạng thái ứng tuyển và nhận thông báo khi trạng thái thay đổi.
- Xem thông tin phân tích thị trường như kỹ năng, vị trí, lương và địa điểm tuyển dụng phổ biến.

### Doanh nghiệp

- Đăng ký, đăng nhập.
- Tạo hồ sơ công ty.
- Đăng bài tuyển thực tập.
- Xem danh sách ứng viên.
- Xem CV ứng viên thông qua presigned URL.
- Cập nhật trạng thái ứng tuyển: `Pending`, `Reviewed`, `Interview`, `Accepted`, `Rejected`.
- Nhận thông báo khi admin duyệt hoặc từ chối bài đăng.

### Admin

- Quản lý tài khoản người dùng.
- Khóa hoặc mở khóa tài khoản.
- Duyệt, từ chối, đóng hoặc xóa bài đăng thực tập.
- Quản lý danh sách kỹ năng và vị trí tuyển dụng.
- Quản lý diễn đàn cộng đồng.
- Xem dashboard thống kê tổng quan.
