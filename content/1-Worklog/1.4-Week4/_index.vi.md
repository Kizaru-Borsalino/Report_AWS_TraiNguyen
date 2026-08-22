---
title: "Tuần 4 - Hồ sơ doanh nghiệp và tin tuyển dụng"
date: 2026-07-06
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu

- Xây dựng đầy đủ nghiệp vụ doanh nghiệp: hồ sơ công ty, tạo tin tuyển dụng và danh sách tin.
- Chuẩn hóa các trường master data dùng chung cho công việc và hồ sơ.
- Chuẩn bị container backend để sẵn sàng triển khai lên ECS.

### Công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Thiết kế company profile với tên công ty, website, quy mô, lĩnh vực, địa chỉ và phúc lợi. | 06/07/2026 | 06/07/2026 | [Schema.org Organization](https://schema.org/Organization) |
| Thứ 3 | Xây API tạo và cập nhật tin tuyển dụng với vị trí, kỹ năng, mức lương, hình thức làm việc và cấp bậc. | 07/07/2026 | 07/07/2026 | [REST API Design Best Practices](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design), [Pydantic Models](https://docs.pydantic.dev/latest/concepts/models/) |
| Thứ 4 | Hoàn thiện danh sách tin tuyển dụng của doanh nghiệp và trạng thái bản nháp, chờ duyệt, đã duyệt. | 08/07/2026 | 08/07/2026 | [State Machine Design Pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/state-machine) |
| Thứ 5 | Tạo bảng master data cho kỹ năng, vị trí, địa điểm, loại hình, hình thức làm việc và cấp bậc. | 09/07/2026 | 09/07/2026 | [PostgreSQL Documentation](https://www.postgresql.org/docs/current/index.html), [Database normalization](https://www.ibm.com/think/topics/database-normalization) |
| Thứ 6 | Đóng gói backend bằng Docker và cấu hình image cho Amazon ECR. | 10/07/2026 | 10/07/2026 | [Dockerfile reference](https://docs.docker.com/reference/dockerfile/), [Amazon ECR User Guide](https://docs.aws.amazon.com/AmazonECR/latest/userguide/what-is-ecr.html) |
| Thứ 7 | Kiểm thử nghiệp vụ tạo hồ sơ công ty và đăng tin theo role doanh nghiệp. | 11/07/2026 | 11/07/2026 | [Playwright Docs](https://playwright.dev/docs/intro), [Testing Library Guiding Principles](https://testing-library.com/docs/guiding-principles/) |

### Kết quả đạt được

- Doanh nghiệp có thể quản lý thông tin và tạo tin tuyển dụng với dữ liệu chuẩn hóa.
- Backend đã sẵn sàng cho bước triển khai container trên AWS.



