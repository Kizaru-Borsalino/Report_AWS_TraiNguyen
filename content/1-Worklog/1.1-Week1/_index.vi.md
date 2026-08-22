---
title: "Tuần 1 - Khởi động dự án và phân tích nhu cầu"
date: 2026-06-15
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu

- Hiểu rõ bài toán nghiệp vụ của cổng tuyển dụng JobGo cho khách, ứng viên, doanh nghiệp và quản trị viên.
- Phân rã yêu cầu thành use case, user flow và phạm vi MVP trước khi viết SRS chi tiết.
- Định hình hướng triển khai hệ thống trên AWS ngay từ giai đoạn khởi động để tránh tư duy local-only.

### Công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Khảo sát nhu cầu của hệ thống tuyển dụng: luồng xem việc làm công khai, đăng ký tài khoản, tạo hồ sơ, ứng tuyển, duyệt tin và quản trị dữ liệu dùng chung. | 15/06/2026 | 15/06/2026 | [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) |
| Thứ 3 | Phân tích actor, use case và pain point của từng vai trò để xác định ranh giới chức năng cho guest, ứng viên, doanh nghiệp và admin. | 16/06/2026 | 16/06/2026 | [AWS Prescriptive Guidance - Microservice decomposition](https://docs.aws.amazon.com/prescriptive-guidance/latest/modernization-decomposing-monoliths/welcome.html) |
| Thứ 4 | Chốt phạm vi MVP cho giai đoạn 1 gồm: xác thực, hồ sơ ứng viên, hồ sơ công ty, đăng tin tuyển dụng, ứng tuyển, phê duyệt và AI matching cơ bản. | 17/06/2026 | 17/06/2026 | [Amazon Cognito features](https://docs.aws.amazon.com/cognito/latest/developerguide/features.html) |
| Thứ 5 | Phác thảo tài liệu SRS đầu tiên, định nghĩa các trường dữ liệu chính, các điều kiện kiểm tra và các trạng thái nghiệp vụ quan trọng. | 18/06/2026 | 18/06/2026 | [IBM - Software requirements specification](https://www.ibm.com/think/topics/software-requirements-specification) |
| Thứ 6 | Dựng sơ đồ kiến trúc đích trên AWS gồm CloudFront, S3, ALB, ECS Fargate, RDS PostgreSQL, S3 private cho CV và CloudWatch cho logging. | 19/06/2026 | 19/06/2026 | [AWS Architecture Center](https://aws.amazon.com/architecture/), [AWS Architecture Icons](https://aws.amazon.com/architecture/icons/) |
| Thứ 7 | Chuyển kết quả phân tích thành backlog kỹ thuật: chia module frontend, backend, master data, CV storage, matching engine và admin workflow. | 20/06/2026 | 20/06/2026 | [FastAPI documentation](https://fastapi.tiangolo.com/), [Vite Guide](https://vite.dev/guide/) |

### Kết quả đạt được

- Tuần đầu được dùng để **khởi động dự án đúng quy trình**: bắt đầu từ phân tích nhu cầu, actor, use case và phạm vi nghiệp vụ trước khi đi vào viết SRS chi tiết.
- Đã hình thành nền tảng để các tuần sau triển khai SRS, thiết kế dữ liệu, API và kế hoạch triển khai JobGo trên AWS.



