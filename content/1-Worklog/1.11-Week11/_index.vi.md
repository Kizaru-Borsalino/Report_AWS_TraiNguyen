---
title: "Tuần 11 - Kế hoạch triển khai JobGo lên AWS và kiểm thử phát hành"
date: 2026-08-24
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu

- Chuẩn bị phát hành JobGo trên hạ tầng AWS theo kiến trúc production giả lập.
- Hoàn thiện quy trình build, release, smoke test và theo dõi vận hành cơ bản.
- Xác nhận các luồng chính vẫn hoạt động đúng sau khi cấu hình môi trường cloud.

### Kế hoạch công việc

| Thứ | Công việc dự kiến | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Tạo ECR repository, build Docker image cho backend FastAPI và chuẩn bị task definition cho ECS Fargate. | 24/08/2026 | 24/08/2026 | [Amazon ECR User Guide](https://docs.aws.amazon.com/AmazonECR/latest/userguide/what-is-ecr.html), [Amazon ECS Developer Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html) |
| Thứ 3 | Tạo RDS PostgreSQL, security group, subnet group và cấu hình biến môi trường production cho backend. | 25/08/2026 | 25/08/2026 | [Amazon RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html) |
| Thứ 4 | Build frontend Vite, đưa static assets lên S3 và phân phối qua CloudFront bằng Origin Access Control. | 26/08/2026 | 26/08/2026 | [Hosting a static website on Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html), [CloudFront Developer Guide](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html) |
| Thứ 5 | Cấu hình private bucket cho CV, CORS, IAM role của task ECS và quyền đọc ghi file đính kèm. | 27/08/2026 | 27/08/2026 | [Amazon S3 security best practices](https://docs.aws.amazon.com/AmazonS3/latest/userguide/security-best-practices.html), [IAM best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html) |
| Thứ 6 | Thiết lập CloudWatch Logs, health check `/health`, alarm lỗi 5xx và smoke test cho các role guest, ứng viên, doanh nghiệp, admin. | 28/08/2026 | 28/08/2026 | [Using Amazon CloudWatch alarms](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html) |
| Thứ 7 | Kiểm tra end-to-end các luồng: xem việc làm, cập nhật hồ sơ, AI matching, ứng tuyển, duyệt tin và theo dõi trạng thái hồ sơ ứng tuyển. | 29/08/2026 | 29/08/2026 | [Application Load Balancer health checks](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/target-group-health-checks.html) |

### Kết quả kỳ vọng

- Kết thúc tuần 11, JobGo có thể được trình bày như một hệ thống đã sẵn sàng phát hành trên AWS với đầy đủ frontend, backend, database, file storage và logging.
- Đây là **kế hoạch triển khai** cho tuần `24/08/2026 - 29/08/2026`, nên nội dung được ghi theo hướng phát hành và kiểm thử dự kiến.



