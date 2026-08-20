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
| Thứ 2 | Thiết kế company profile với tên công ty, website, quy mô, lĩnh vực, địa chỉ và phúc lợi. | 06/07/2026 | 06/07/2026 | Company profile specification |
| Thứ 3 | Xây API tạo và cập nhật tin tuyển dụng với vị trí, kỹ năng, mức lương, hình thức làm việc và cấp bậc. | 07/07/2026 | 07/07/2026 | Job post API contract |
| Thứ 4 | Hoàn thiện danh sách tin tuyển dụng của doanh nghiệp và trạng thái bản nháp, chờ duyệt, đã duyệt. | 08/07/2026 | 08/07/2026 | Job lifecycle design |
| Thứ 5 | Tạo bảng master data cho kỹ năng, vị trí, địa điểm, loại hình, hình thức làm việc và cấp bậc. | 09/07/2026 | 09/07/2026 | Master data schema |
| Thứ 6 | Đóng gói backend bằng Docker và cấu hình image cho Amazon ECR. | 10/07/2026 | 10/07/2026 | Dockerfile, Amazon ECR docs |
| Thứ 7 | Kiểm thử nghiệp vụ tạo hồ sơ công ty và đăng tin theo role doanh nghiệp. | 11/07/2026 | 11/07/2026 | Company flow test plan |

### Kết quả đạt được

- Doanh nghiệp có thể quản lý thông tin và tạo tin tuyển dụng với dữ liệu chuẩn hóa.
- Backend đã sẵn sàng cho bước triển khai container trên AWS.
