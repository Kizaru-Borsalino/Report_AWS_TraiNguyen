---
title: "Tuần 2 - Xây nền tảng backend và xác thực"
date: 2026-06-22
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu

- Hoàn thiện backend skeleton với FastAPI, SQLAlchemy và migration.
- Xây luồng đăng ký, đăng nhập và phân quyền theo ba vai trò.
- Chuẩn bị database PostgreSQL cho môi trường AWS.

### Công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Khởi tạo FastAPI app, cấu hình settings, dependency injection và module router. | 22/06/2026 | 22/06/2026 | [FastAPI - Bigger Applications](https://fastapi.tiangolo.com/tutorial/bigger-applications/), [FastAPI Project Generation](https://fastapi.tiangolo.com/project-generation/) |
| Thứ 3 | Tạo schema users, role enum, password hashing và JWT authentication. | 23/06/2026 | 23/06/2026 | [FastAPI - OAuth2 with JWT](https://fastapi.tiangolo.com/tutorial/security/oauth2-jwt/) |
| Thứ 4 | Viết API đăng ký cho ứng viên và doanh nghiệp, đồng thời seed tài khoản quản trị viên an toàn. | 24/06/2026 | 24/06/2026 | [OpenAPI Specification](https://swagger.io/specification/) |
| Thứ 5 | Tạo migration đầu tiên cho PostgreSQL và kiểm tra tính tương thích với Amazon RDS. | 25/06/2026 | 25/06/2026 | [Alembic Documentation](https://alembic.sqlalchemy.org/en/latest/), [Amazon RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html) |
| Thứ 6 | Thiết lập IAM policy và parameter placeholder cho secrets kết nối database trên AWS. | 26/06/2026 | 26/06/2026 | [AWS IAM User Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html), [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html) |
| Thứ 7 | Kiểm thử đăng nhập nhiều vai trò và xử lý các lỗi 401, 403, validation. | 27/06/2026 | 27/06/2026 | [FastAPI Testing](https://fastapi.tiangolo.com/tutorial/testing/), [Postman API Testing](https://learning.postman.com/docs/tests-and-scripts/write-scripts/test-scripts/) |

### Kết quả đạt được

- Backend nền tảng đã ổn định, hỗ trợ phân quyền và sẵn sàng mở rộng nghiệp vụ tuyển dụng.
- Thiết kế dữ liệu phù hợp để triển khai lên Amazon RDS mà không phụ thuộc môi trường local.



