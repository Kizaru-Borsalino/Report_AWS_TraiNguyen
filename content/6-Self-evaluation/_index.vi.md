---
title: "Tự đánh giá"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

## Kết quả đạt được

Trong quá trình thực hiện dự án **Cloud-based Student Internship Portal on AWS**, em đã hiểu rõ hơn cách xây dựng một ứng dụng web hoàn chỉnh gồm frontend, backend, database, storage và deployment trên cloud.

Các kỹ năng đã cải thiện:

- Phân tích yêu cầu và chia chức năng theo từng nhóm người dùng.
- Thiết kế REST API bằng FastAPI.
- Thiết kế database quan hệ bằng SQLAlchemy và Alembic.
- Xây dựng authentication bằng JWT và phân quyền theo role.
- Tích hợp Amazon S3 để lưu file CV theo hướng private.
- Cấu hình Amazon RDS PostgreSQL cho môi trường production.
- Deploy backend lên EC2 và frontend lên S3/CloudFront.
- Theo dõi log cơ bản bằng CloudWatch.

## Khó khăn

- Cần xử lý đúng phân quyền giữa student, company và admin.
- Cần đảm bảo CV không bị public nhưng vẫn cho phép người có quyền xem được.
- Cần cấu hình CORS chính xác khi frontend và backend chạy ở hai domain khác nhau.
- Cần chuyển đổi từ SQLite local sang PostgreSQL production mà không làm sai schema.

## Bài học rút ra

Dự án giúp em thấy rõ sự khác biệt giữa chạy ứng dụng local và triển khai trên cloud. Ngoài việc viết code, một hệ thống thực tế còn cần cấu hình network, quyền truy cập, biến môi trường, lưu trữ file, database migration và monitoring.
