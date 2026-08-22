---
title: "Tuần 6 - Giao diện vai trò và dữ liệu tham chiếu"
date: 2026-07-20
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu

- Tái cấu trúc giao diện theo từng vai trò và từng trang nghiệp vụ riêng.
- Đồng bộ master data ở cả backend lẫn frontend để tránh nhập text tự do.
- Đưa frontend production build lên Amazon S3 và CloudFront.

### Công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Tách dashboard doanh nghiệp thành hồ sơ công ty, tạo tin, danh sách ứng viên và danh sách tin tuyển dụng. | 20/07/2026 | 20/07/2026 | [Ant Design Layout](https://ant.design/components/layout), [Information architecture](https://www.nngroup.com/articles/ia-study-guide/) |
| Thứ 3 | Tách dashboard ứng viên thành hồ sơ, CV, ứng tuyển và lịch sử ứng tuyển. | 21/07/2026 | 21/07/2026 | [Ant Design Menu](https://ant.design/components/menu), [Dashboard design patterns](https://www.nngroup.com/articles/dashboards/) |
| Thứ 4 | Xây API và giao diện quản lý master data cho admin. | 22/07/2026 | 22/07/2026 | [Ant Design Table](https://ant.design/components/table), [Ant Design Form](https://ant.design/components/form) |
| Thứ 5 | Chuyển các trường như kỹ năng, địa điểm, vị trí và cấp bậc sang dạng lựa chọn chuẩn hóa. | 23/07/2026 | 23/07/2026 | [Database normalization](https://www.ibm.com/think/topics/database-normalization), [Ant Design Select](https://ant.design/components/select) |
| Thứ 6 | Build frontend bằng Vite và publish asset lên S3, cấu hình CloudFront cache behavior. | 24/07/2026 | 24/07/2026 | [Hosting a static website using Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html), [CloudFront Developer Guide](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html) |
| Thứ 7 | Kiểm thử guest có thể xem danh sách việc làm công khai nhưng chưa thấy AI Matching. | 25/07/2026 | 25/07/2026 | [Playwright Docs](https://playwright.dev/docs/intro), [Amazon CloudFront use cases](https://aws.amazon.com/cloudfront/use-cases/) |

### Kết quả đạt được

- Giao diện JobGo đã rõ ràng hơn theo từng role và thuận tiện cho demo nghiệp vụ.
- Frontend đã có đường triển khai production trên S3 và CloudFront.



