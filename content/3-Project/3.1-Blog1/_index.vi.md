---
title: "Backend API"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

Backend của dự án được xây dựng bằng **FastAPI**, chịu trách nhiệm cung cấp API cho frontend, xử lý nghiệp vụ, xác thực người dùng và kết nối database.

## Cấu trúc backend

```text
backend/
  app/
    routers/
      auth.py
      student.py
      company.py
      admin.py
      internships.py
      analytics.py
      forum.py
      common.py
    main.py
    models.py
    schemas.py
    database.py
    config.py
    auth.py
    services.py
  alembic/
  tests/
  requirements.txt
```

## Các module chính

- **Auth:** đăng ký, đăng nhập, kiểm tra người dùng hiện tại, refresh token.
- **Student:** quản lý hồ sơ sinh viên, upload CV, xem đơn ứng tuyển.
- **Company:** quản lý hồ sơ công ty, bài đăng thực tập, ứng viên và trạng thái hồ sơ.
- **Admin:** quản lý người dùng, duyệt bài đăng, quản lý kỹ năng, vị trí tuyển dụng và diễn đàn.
- **Internships:** hiển thị danh sách vị trí thực tập đã được duyệt.
- **Analytics:** thống kê kỹ năng, vị trí, địa điểm và khoảng lương phổ biến.
- **Forum:** cộng đồng trao đổi chuyên môn, bài viết, bình luận, like và lưu bài.

## Database

Các bảng chính gồm:

- `users`
- `student_profiles`
- `companies`
- `internship_posts`
- `job_positions`
- `applications`
- `skills`
- `notifications`
- `forum_categories`
- `forum_posts`
- `forum_comments`
- `forum_likes`
- `forum_saves`

Backend dùng SQLite khi chạy local và chuyển sang PostgreSQL trên Amazon RDS khi deploy production. Schema được quản lý bằng Alembic migration để dễ thay đổi và triển khai nhất quán.

## Bảo mật và phân quyền

Hệ thống chia người dùng thành ba role: `student`, `company`, `admin`. Mỗi API được bảo vệ theo quyền tương ứng để tránh việc người dùng truy cập dữ liệu hoặc thao tác không thuộc vai trò của mình.

CV không được lưu trực tiếp trong database. File được lưu ở S3 private bucket, database chỉ lưu đường dẫn/object key. Khi người dùng hợp lệ cần xem CV, backend tạo presigned URL có thời hạn ngắn.
