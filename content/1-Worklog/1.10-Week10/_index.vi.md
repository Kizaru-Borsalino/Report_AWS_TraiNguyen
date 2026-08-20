---
title: "Tuần 10 - Xây dựng AI Matching Engine"
date: 2026-08-17
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu

- Triển khai engine chấm điểm mức độ phù hợp giữa hồ sơ ứng viên và tin tuyển dụng.
- Hiển thị AI Matching cho ứng viên ở trang việc làm và cho doanh nghiệp ở danh sách ứng viên.
- Sắp xếp ứng viên theo độ phù hợp để hỗ trợ tuyển dụng nhanh hơn.

### Công việc đã thực hiện

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu |
| --- | --- | --- | --- | --- |
| Thứ 2 | Thiết kế công thức chấm điểm có trọng số cho kỹ năng, vị trí, cấp bậc, địa điểm, loại hình và hình thức làm việc. | 17/08/2026 | 17/08/2026 | Matching formula notes |
| Thứ 3 | Xây service backend trả về overall score, label, matched skills và missing skills. | 18/08/2026 | 18/08/2026 | Matching service contract |
| Thứ 4 | Gắn kết quả matching vào API danh sách việc làm cho ứng viên đã có hồ sơ. | 19/08/2026 | 19/08/2026 | Public jobs API integration |
| Thứ 5 | Hiển thị badge AI Matching nổi bật trong card việc làm và drawer chi tiết tin tuyển dụng. | 20/08/2026 | 20/08/2026 | Frontend matching UI |
| Thứ 6 | Sắp xếp danh sách ứng viên của doanh nghiệp theo điểm matching giảm dần. | 21/08/2026 | 21/08/2026 | Applicant ranking logic |
| Thứ 7 | Kiểm tra việc cập nhật hồ sơ ứng viên sẽ refresh điểm matching ngay mà không cần đăng nhập lại. | 22/08/2026 | 22/08/2026 | Matching refresh test plan |

### Kết quả đạt được

- AI Matching Engine đã trở thành điểm nhấn chức năng chính của JobGo.
- Doanh nghiệp có thể ưu tiên ứng viên phù hợp cao, còn ứng viên nhận được phản hồi định lượng trước khi nộp đơn.
