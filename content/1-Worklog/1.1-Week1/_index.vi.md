---
title: "Tuần 1 - Khảo sát yêu cầu và kiến trúc JobGo"
date: 2026-06-15
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu

- Nắm rõ phạm vi nghiệp vụ của cổng tuyển dụng JobGo cho ứng viên, doanh nghiệp và quản trị viên.
- Chuyển SRS thành backlog kỹ thuật và sơ đồ kiến trúc triển khai trên AWS.
- Thiết lập tiêu chuẩn môi trường phát triển, cấu trúc repo và quy ước API.

### Công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Phân tích tài liệu SRS, use case và actor để xác định phạm vi MVP của JobGo. | 15/06/2026 | 15/06/2026 | SRS JobGo, Use case backlog |
| Thứ 3 | Vẽ kiến trúc mục tiêu trên AWS gồm CloudFront, S3, ECS Fargate, ALB, RDS PostgreSQL và S3 private cho CV. | 16/06/2026 | 16/06/2026 | AWS Architecture Icons, ECS/RDS/S3 docs |
| Thứ 4 | Tạo backlog sprint đầu tiên cho authentication, profile, job posting và admin approval. | 17/06/2026 | 17/06/2026 | Sprint planning board |
| Thứ 5 | Khởi tạo cấu trúc monorepo cho frontend React và backend FastAPI. | 18/06/2026 | 18/06/2026 | Frontend/Backend project template |
| Thứ 6 | Thiết kế sơ bộ mô hình dữ liệu cho users, profiles, jobs, applications, resumes và master data. | 19/06/2026 | 19/06/2026 | ERD draft, PostgreSQL notes |
| Thứ 7 | Thống nhất chuẩn đặt tên API, phân quyền role và tiêu chí nghiệm thu cho sprint tiếp theo. | 20/06/2026 | 20/06/2026 | API conventions, acceptance checklist |

### Kết quả đạt được

- Hoàn thành bản thiết kế tổng quan cho JobGo trên AWS và xác định rõ các service chính dùng trong production.
- Sẵn sàng bước vào giai đoạn hiện thực hóa authentication, data model và API nền tảng.
