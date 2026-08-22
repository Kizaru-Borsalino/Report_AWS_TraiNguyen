---
title: "Tuần 9 - Chuẩn bị dữ liệu cho AI Matching"
date: 2026-08-10
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu

- Bổ sung các trường còn thiếu trong hồ sơ ứng viên để phục vụ matching.
- Tái cấu trúc master data, đặc biệt là cấp bậc và loại hình công việc.
- Đảm bảo frontend và backend dùng chung cùng một mô hình dữ liệu chuẩn hóa.

### Công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Đổi master data Danh mục thành Cấp bậc với các giá trị như Intern, Fresher, Junior, Middle, Senior. | 10/08/2026 | 10/08/2026 | [Database normalization](https://www.ibm.com/think/topics/database-normalization), [Master data management overview](https://www.ibm.com/think/topics/master-data-management) |
| Thứ 3 | Bổ sung kỹ năng, vị trí ứng tuyển, địa điểm, hình thức, loại hình và cấp bậc vào hồ sơ ứng viên. | 11/08/2026 | 11/08/2026 | [Amazon Bedrock overview](https://aws.amazon.com/bedrock/), [Feature engineering](https://developers.google.com/machine-learning/data-prep/transform/feature-engineering) |
| Thứ 4 | Cập nhật form công ty để dùng lại cùng bộ master data với phía ứng viên. | 12/08/2026 | 12/08/2026 | [OpenAPI Specification](https://swagger.io/specification/), [Pydantic Models](https://docs.pydantic.dev/latest/concepts/models/) |
| Thứ 5 | Viết rule kiểm tra dữ liệu đầu vào để không còn giá trị tự do gây lệch khi chấm điểm. | 13/08/2026 | 13/08/2026 | [Pydantic Validation](https://docs.pydantic.dev/latest/concepts/validators/), [OWASP Input Validation Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Input_Validation_Cheat_Sheet.html) |
| Thứ 6 | Rà soát cấu trúc API response cho jobs và profiles để sẵn sàng gắn kết quả matching. | 14/08/2026 | 14/08/2026 | [REST API Design Best Practices](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design), [JSON:API Recommendations](https://jsonapi.org/recommendations/) |
| Thứ 7 | Kiểm thử cập nhật hồ sơ ứng viên làm thay đổi dữ liệu đầu vào cho matching ngay trên AWS. | 15/08/2026 | 15/08/2026 | [Amazon Bedrock overview](https://aws.amazon.com/bedrock/), [AWS Well-Architected Reliability Pillar](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/welcome.html) |

### Kết quả đạt được

- Dữ liệu đầu vào cho AI Matching đã được chuẩn hóa và đủ chiều để tính độ phù hợp.
- Nền tảng master data của JobGo rõ ràng hơn cho cả trải nghiệm người dùng và xử lý hệ thống.



