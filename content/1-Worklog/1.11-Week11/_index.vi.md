---
title: "Tuần 11 - Deploy frontend"
date: 2024-01-01
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu

- Build React app cho môi trường production.
- Deploy frontend lên S3 Static Website Hosting hoặc CloudFront.
- Cấu hình CORS giữa frontend và backend.

### Công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Cấu hình `VITE_API_URL`<br>Frontend gọi đúng backend production | 20/10/2025 | 20/10/2025 | Amazon S3 Hosting / CloudFront Docs |
| 3 | Build frontend<br>Tạo thư mục `dist` bằng Vite | 21/10/2025 | 21/10/2025 | Amazon S3 Hosting / CloudFront Docs |
| 4 | Upload lên S3<br>Public static assets qua S3/CloudFront | 22/10/2025 | 22/10/2025 | Amazon S3 Hosting / CloudFront Docs |
| 5 | Cấu hình CORS backend<br>Chỉ cho phép frontend domain hợp lệ | 23/10/2025 | 23/10/2025 | Amazon S3 Hosting / CloudFront Docs |

### Kết quả đạt được

Frontend có thể truy cập từ trình duyệt thông qua AWS hosting. Ứng dụng kết nối được backend production và sẵn sàng cho luồng demo end-to-end.
