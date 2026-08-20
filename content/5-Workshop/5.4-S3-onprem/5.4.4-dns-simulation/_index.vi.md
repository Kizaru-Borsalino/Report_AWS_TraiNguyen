---
title: "Triển khai AI Matching và kiểm thử end-to-end"
date: 2026-08-10
weight: 4
chapter: false
pre: " <b> 5.4.4. </b> "
---

## Nguyên tắc chấm điểm matching

AI Matching của JobGo không dùng mô hình generative phức tạp ở giai đoạn đầu. Điểm phù hợp được tính theo công thức có trọng số trên dữ liệu đã chuẩn hóa:

- Kỹ năng
- Vị trí ứng tuyển
- Cấp bậc
- Địa điểm
- Loại hình công việc
- Hình thức làm việc

Ví dụ:

```text
AI Match = Skill 40% + Position 20% + Level 15% + Location 10% + Job Type 10% + Work Mode 5%
```

## Cách hệ thống cập nhật điểm

- Khi ứng viên cập nhật hồ sơ, backend tính lại matching với các job đang mở.
- Khi ứng viên xem chi tiết việc làm, giao diện gọi API để lấy breakdown theo từng tiêu chí.
- Khi doanh nghiệp mở danh sách ứng viên, backend sắp xếp theo điểm matching giảm dần để ưu tiên hồ sơ phù hợp hơn.

## Kết quả cần hiển thị

```text
AI Match: 96% - Phù hợp cao
Kỹ năng: 90%
Vị trí: 100%
Cấp bậc: 90%
Địa điểm: 100%
Loại hình: 100%
Hình thức làm việc: 100%
Phù hợp: Python, FastAPI, AWS
Còn thiếu: Docker, Redis
```

## Kiểm thử end-to-end

1. Guest vào trang chủ vẫn xem được việc làm nhưng không thấy AI matching.
2. Ứng viên đăng nhập, tạo hồ sơ và kiểm tra điểm matching thay đổi ngay sau khi lưu.
3. Ứng viên ứng tuyển vào job đã chọn và kiểm tra lịch sử ứng tuyển.
4. Doanh nghiệp mở đúng job để xem danh sách ứng viên theo thứ tự matching giảm dần.
5. Admin duyệt tin tuyển dụng và quản lý master data làm đầu vào chuẩn cho matching engine.
