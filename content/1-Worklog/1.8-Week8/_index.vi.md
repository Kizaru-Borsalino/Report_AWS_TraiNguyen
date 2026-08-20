---
title: "Tuần 8 - Danh sách ứng viên, lịch sử và độ ổn định dữ liệu"
date: 2026-08-03
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu

- Sửa các lỗi dữ liệu khiến công ty không thấy ứng viên hoặc ứng viên không thấy lịch sử đúng.
- Tối ưu thao tác CV, rút đơn và ứng tuyển lại.
- Đảm bảo dữ liệu ứng tuyển luôn phản ánh đúng trên RDS.

### Công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Sửa truy vấn danh sách ứng viên theo từng job để công ty thấy đúng người đã ứng tuyển. | 03/08/2026 | 03/08/2026 | Applicant query review |
| Thứ 3 | Bổ sung nút xem chi tiết hồ sơ và tải CV ngay trên card ứng viên. | 04/08/2026 | 04/08/2026 | Applicant card UX |
| Thứ 4 | Cho phép xóa CV trùng, rút đơn và ứng tuyển lại mà không làm hỏng lịch sử dữ liệu. | 05/08/2026 | 05/08/2026 | Resume/application consistency notes |
| Thứ 5 | Chuẩn hóa trạng thái ứng tuyển về tiếng Việt và đồng bộ hiển thị giữa company với candidate. | 06/08/2026 | 06/08/2026 | Status mapping table |
| Thứ 6 | Rà soát transaction và refresh dữ liệu để các thay đổi trạng thái phản ánh ngay sau khi lưu. | 07/08/2026 | 07/08/2026 | RDS transaction checklist |
| Thứ 7 | Kiểm thử regression toàn bộ luồng company-admin-student trên môi trường AWS staging. | 08/08/2026 | 08/08/2026 | Regression test suite |

### Kết quả đạt được

- Danh sách ứng viên và lịch sử ứng tuyển đã hoạt động ổn định hơn, giảm lỗi dữ liệu chéo vai trò.
- RDS giữ trạng thái nghiệp vụ nhất quán sau nhiều lần cập nhật.
