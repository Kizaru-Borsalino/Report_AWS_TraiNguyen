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
| Thứ 2 | Đổi master data Danh mục thành Cấp bậc với các giá trị như Intern, Fresher, Junior, Middle, Senior. | 10/08/2026 | 10/08/2026 | Master data redesign notes |
| Thứ 3 | Bổ sung kỹ năng, vị trí ứng tuyển, địa điểm, hình thức, loại hình và cấp bậc vào hồ sơ ứng viên. | 11/08/2026 | 11/08/2026 | Matching field matrix |
| Thứ 4 | Cập nhật form công ty để dùng lại cùng bộ master data với phía ứng viên. | 12/08/2026 | 12/08/2026 | Shared master data contract |
| Thứ 5 | Viết rule kiểm tra dữ liệu đầu vào để không còn giá trị tự do gây lệch khi chấm điểm. | 13/08/2026 | 13/08/2026 | Validation rules |
| Thứ 6 | Rà soát cấu trúc API response cho jobs và profiles để sẵn sàng gắn kết quả matching. | 14/08/2026 | 14/08/2026 | API response design |
| Thứ 7 | Kiểm thử cập nhật hồ sơ ứng viên làm thay đổi dữ liệu đầu vào cho matching ngay trên AWS. | 15/08/2026 | 15/08/2026 | Matching readiness checklist |

### Kết quả đạt được

- Dữ liệu đầu vào cho AI Matching đã được chuẩn hóa và đủ chiều để tính độ phù hợp.
- Nền tảng master data của JobGo rõ ràng hơn cho cả trải nghiệm người dùng và xử lý hệ thống.
