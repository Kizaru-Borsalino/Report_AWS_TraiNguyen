---
title: "Luồng nghiệp vụ và kiểm thử"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

## Luồng demo chính

1. Doanh nghiệp đăng ký hoặc đăng nhập.
2. Doanh nghiệp tạo hồ sơ công ty.
3. Doanh nghiệp đăng một vị trí thực tập.
4. Admin đăng nhập và duyệt bài đăng.
5. Sinh viên đăng ký hoặc đăng nhập.
6. Sinh viên tạo hồ sơ, upload CV.
7. Sinh viên xem danh sách internship đã được duyệt và nộp đơn.
8. Doanh nghiệp xem danh sách ứng viên.
9. Doanh nghiệp mở CV bằng presigned URL.
10. Doanh nghiệp cập nhật trạng thái hồ sơ.
11. Sinh viên nhận thông báo trạng thái ứng tuyển.

## Các trường hợp kiểm thử

Backend có test tự động cho các luồng quan trọng:

- Company tạo bài đăng.
- Admin duyệt bài đăng.
- Student upload CV và apply.
- Company cập nhật trạng thái ứng tuyển.
- Tạo notification khi trạng thái thay đổi.
- Chặn apply trùng.
- Chặn apply khi deadline hết hạn.
- Chặn tài khoản bị khóa.
- Kiểm tra phân quyền admin/company/student.
- Validate GPA, số lượng tuyển và kích thước file CV.
- Kiểm tra analytics cho kỹ năng, vị trí, lương và địa điểm.
- Kiểm tra forum: đăng bài, duyệt bài, comment, like, save và moderation.

## Kết quả

Sau quá trình phát triển và kiểm thử, dự án đáp ứng được luồng nghiệp vụ chính của một hệ thống quản lý thực tập. Ứng dụng có thể chạy local bằng SQLite để demo nhanh và có cấu hình production để triển khai lên AWS với RDS PostgreSQL, S3, EC2 và CloudWatch.
