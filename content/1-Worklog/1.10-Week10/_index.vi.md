---
title: "Tuần 10 - RDS PostgreSQL"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu

- Chuyển database production sang Amazon RDS PostgreSQL.
- Kết nối backend EC2 với RDS an toàn.

### Công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Tạo RDS PostgreSQL<br>Database `internship_portal` cho production | 13/10/2025 | 13/10/2025 | Amazon RDS Docs / Alembic Docs |
| 3 | Cấu hình security group<br>Chỉ cho EC2 backend truy cập port 5432 | 14/10/2025 | 14/10/2025 | Amazon RDS Docs / Alembic Docs |
| 4 | Cập nhật `DATABASE_URL`<br>Backend kết nối RDS thay vì SQLite | 15/10/2025 | 15/10/2025 | Amazon RDS Docs / Alembic Docs |
| 5 | Chạy Alembic migration<br>Tạo schema production | 16/10/2025 | 16/10/2025 | Amazon RDS Docs / Alembic Docs |

### Kết quả đạt được

Database được tách khỏi server backend, phù hợp hơn với kiến trúc cloud. Việc dùng Alembic giúp schema giữa local và production nhất quán.
