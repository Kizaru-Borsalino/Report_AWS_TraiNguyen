---
title : "Kiểm thử backend API"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.4.3. </b> "
---

## Health check

Mở endpoint:

```text
http://<ec2-public-ip>:8000/health
```

Kết quả mong đợi:

```json
{
  "status": "ok",
  "service": "Student Internship Portal"
}
```

## Swagger docs

FastAPI tự tạo API documentation tại:

```text
http://<ec2-public-ip>:8000/docs
```

## Kiểm thử luồng chính

1. Login bằng tài khoản demo.
2. Company tạo bài đăng thực tập.
3. Admin duyệt bài đăng.
4. Student upload CV và apply.
5. Company cập nhật trạng thái ứng tuyển.
6. Kiểm tra notification của student.

## Kết quả

Nếu các endpoint hoạt động đúng, backend đã kết nối được RDS, đọc ghi dữ liệu thành công và có thể xử lý nghiệp vụ chính của project.
