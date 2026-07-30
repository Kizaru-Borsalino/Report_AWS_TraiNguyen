---
title: "Frontend Application"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

Frontend được xây dựng bằng **ReactJS + Vite**, cung cấp giao diện riêng cho từng nhóm người dùng: sinh viên, doanh nghiệp và admin.

## Cấu trúc frontend

```text
frontend/
  src/
    api/
    components/
    hooks/
    pages/
    utils/
    main.jsx
    styles.css
  index.html
  package.json
```

## Các nhóm màn hình

### Student

- `/student/home`: dashboard sinh viên.
- `/student/jobs`: danh sách vị trí thực tập.
- `/student/companies`: danh sách công ty.
- `/student/applications`: các đơn đã ứng tuyển.
- `/student/profile`: hồ sơ cá nhân và CV.
- `/student/insights`: phân tích thị trường tuyển dụng.
- `/student/forum`: diễn đàn cộng đồng.

### Company

- `/company/home`: dashboard doanh nghiệp.
- `/company/jobs`: quản lý bài đăng thực tập.
- `/company/applicants`: danh sách ứng viên.
- `/company/profile`: hồ sơ công ty.

### Admin

- `/admin/home`: dashboard tổng quan.
- `/admin/users`: quản lý người dùng.
- `/admin/posts`: duyệt bài thực tập.
- `/admin/job-positions`: quản lý vị trí tuyển dụng.
- `/admin/skills`: quản lý kỹ năng.
- `/admin/forum`: quản lý diễn đàn.

## Kết nối backend

Frontend gọi API thông qua module `src/api/client.js`. Khi chạy local, frontend mặc định kết nối backend ở port `8000`. Khi deploy production, biến môi trường `VITE_API_URL` được dùng để trỏ tới domain API thật.

Thiết kế frontend tập trung vào luồng thao tác rõ ràng: đăng nhập theo role, chuyển hướng đến dashboard phù hợp, hiển thị dữ liệu từ API và phản hồi trạng thái loading/error cho người dùng.
