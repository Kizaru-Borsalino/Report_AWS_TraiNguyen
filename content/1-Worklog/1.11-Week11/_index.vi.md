---
title: "Tuần 11 - Củng cố triển khai AWS và vận hành"
date: 2026-08-24
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu

- Hoàn thiện cấu hình production trên AWS cho frontend, backend, database và storage.
- Tăng cường quan sát, bảo mật cấu hình và khả năng backup cơ bản.
- Chuẩn bị pipeline build và checklist triển khai.

### Công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Rà soát ECS service, autoscaling policy, health check và rollback strategy cho backend JobGo. | 24/08/2026 | 24/08/2026 | ECS operations checklist |
| Thứ 3 | Chuẩn hóa secrets bằng Systems Manager Parameter Store hoặc Secrets Manager. | 25/08/2026 | 25/08/2026 | Secrets management notes |
| Thứ 4 | Thiết lập CloudWatch Logs, metric filter và alarm cho các lỗi backend quan trọng. | 26/08/2026 | 26/08/2026 | CloudWatch alarms guide |
| Thứ 5 | Kiểm tra snapshot policy của RDS và versioning cho S3 bucket chứa CV. | 27/08/2026 | 27/08/2026 | RDS backup, S3 versioning docs |
| Thứ 6 | Hoàn thiện checklist triển khai: build frontend, push image ECR, update ECS service và clear CloudFront cache. | 28/08/2026 | 28/08/2026 | Deployment runbook |
| Thứ 7 | Chạy smoke test production-like và xác nhận guest, student, company, admin đều hoạt động đúng. | 29/08/2026 | 29/08/2026 | Production smoke test checklist |

### Kết quả đạt được

- Kiến trúc triển khai trên AWS đã sẵn sàng cho trình diễn cuối kỳ với mức độ vận hành thực tế cao hơn.
- Các thành phần hạ tầng đã có quy trình giám sát và kiểm soát thay đổi rõ ràng hơn.
