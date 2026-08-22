---
title: "Tuần 3 - Hồ sơ ứng viên và lưu trữ CV trên S3"
date: 2026-06-29
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu

- Hoàn thiện hồ sơ ứng viên và danh sách CV theo mô hình lưu trữ tệp an toàn.
- Tích hợp Amazon S3 private bucket cho upload và download CV.
- Đảm bảo doanh nghiệp chỉ xem CV thông qua luồng được cấp quyền.

### Công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Thiết kế student profile với trường học, chuyên ngành, kỹ năng, vị trí mong muốn và liên kết xã hội. | 29/06/2026 | 29/06/2026 | [Pydantic Models](https://docs.pydantic.dev/latest/concepts/models/), [Schema.org Person](https://schema.org/Person) |
| Thứ 3 | Xây API cập nhật hồ sơ ứng viên và validate dữ liệu đầu vào theo master data. | 30/06/2026 | 30/06/2026 | [REST API Design Best Practices](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design) |
| Thứ 4 | Tích hợp upload CV lên S3 private bucket và lưu object key trong PostgreSQL. | 01/07/2026 | 01/07/2026 | [Uploading objects to Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/upload-objects.html) |
| Thứ 5 | Triển khai presigned URL để tải CV đúng quyền và đúng thời hạn truy cập. | 02/07/2026 | 02/07/2026 | [Download and upload objects with presigned URLs](https://docs.aws.amazon.com/AmazonS3/latest/userguide/using-presigned-url.html) |
| Thứ 6 | Kiểm thử luồng thêm nhiều CV, chọn CV mặc định và xóa CV chưa được sử dụng. | 03/07/2026 | 03/07/2026 | [Amazon S3 object naming guidelines](https://docs.aws.amazon.com/AmazonS3/latest/userguide/object-keys.html), [FastAPI Testing](https://fastapi.tiangolo.com/tutorial/testing/) |
| Thứ 7 | Bổ sung log tải tệp và lỗi truy cập để theo dõi trên CloudWatch Logs. | 04/07/2026 | 04/07/2026 | [CloudWatch Logs User Guide](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html) |

### Kết quả đạt được

- Ứng viên đã có thể quản lý hồ sơ và CV theo mô hình lưu trữ production-ready trên AWS.
- Luồng truy cập CV an toàn hơn vì file không công khai trực tiếp.



