---
title: "Tuần 9 - EC2 và deploy backend"
date: 2024-01-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu

- Tìm hiểu cách đưa FastAPI backend lên Amazon EC2.
- Cấu hình network và security group cơ bản.

### Công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| 2 | Tạo EC2 instance<br>Chuẩn bị môi trường Linux cho backend | 06/10/2025 | 06/10/2025 | Amazon EC2 Docs / IAM Docs |
| 3 | Cài Python, venv, dependencies<br>Backend có thể chạy bằng Uvicorn | 07/10/2025 | 07/10/2025 | Amazon EC2 Docs / IAM Docs |
| 4 | Mở port kiểm thử<br>Cho phép truy cập API qua port 8000 tạm thời | 08/10/2025 | 08/10/2025 | Amazon EC2 Docs / IAM Docs |
| 5 | Kiểm tra health endpoint<br>`/health` trả trạng thái service | 09/10/2025 | 09/10/2025 | Amazon EC2 Docs / IAM Docs |

### Kết quả đạt được

Backend có quy trình deploy rõ ràng trên EC2. Nhóm hiểu hơn về security group, inbound rule, SSH và cách chạy service backend trong môi trường cloud.
