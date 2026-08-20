---
title: "Tuần 5 - Ứng tuyển, trạng thái hồ sơ và phê duyệt"
date: 2026-07-13
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu

- Kết nối trọn vẹn luồng ứng tuyển giữa ứng viên, doanh nghiệp và admin.
- Quản lý trạng thái đơn ứng tuyển và thông báo thay đổi.
- Đưa backend chạy thử trên Amazon ECS Fargate môi trường staging.

### Công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Xây API ứng tuyển với resume_id, thư giới thiệu và kiểm tra trùng đơn. | 13/07/2026 | 13/07/2026 | Application API contract |
| Thứ 3 | Triển khai lịch sử trạng thái đơn và khả năng rút đơn, ứng tuyển lại khi phù hợp. | 14/07/2026 | 14/07/2026 | Application status model |
| Thứ 4 | Tạo trang admin để duyệt tin tuyển dụng trước khi hiển thị công khai. | 15/07/2026 | 15/07/2026 | Admin moderation checklist |
| Thứ 5 | Sinh thông báo khi đơn ứng tuyển được tạo, thay đổi trạng thái hoặc khi tin tuyển dụng được duyệt. | 16/07/2026 | 16/07/2026 | Notification flow design |
| Thứ 6 | Tạo task definition, service và ALB target group cho backend staging trên ECS Fargate. | 17/07/2026 | 17/07/2026 | ECS Fargate deployment notes |
| Thứ 7 | Chạy smoke test end-to-end trên môi trường staging bằng dữ liệu mẫu. | 18/07/2026 | 18/07/2026 | Staging smoke test checklist |

### Kết quả đạt được

- Luồng ứng tuyển cơ bản đã hoàn chỉnh và có thể trình diễn trên môi trường staging AWS.
- Admin đã kiểm soát được chất lượng bài đăng trước khi công khai ra trang việc làm.
