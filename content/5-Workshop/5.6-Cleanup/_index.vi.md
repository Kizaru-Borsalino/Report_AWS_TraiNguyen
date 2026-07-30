---
title : "Kiểm thử, giám sát và dọn dẹp"
date : 2024-01-01
weight : 6
chapter : false
pre : " <b> 5.6. </b> "
---

## 1. Kiểm thử sau deploy

Luồng kiểm thử cuối:

1. Mở frontend domain.
2. Đăng nhập bằng tài khoản company.
3. Tạo hồ sơ công ty.
4. Tạo bài đăng thực tập.
5. Đăng nhập bằng tài khoản admin.
6. Admin duyệt bài đăng.
7. Đăng nhập bằng tài khoản student.
8. Cập nhật hồ sơ sinh viên.
9. Upload CV lên S3.
10. Apply vào bài internship đã duyệt.
11. Company cập nhật trạng thái ứng tuyển.
12. Student kiểm tra notification.

## 2. CloudWatch Logs

Backend FastAPI ghi log ra stdout/stderr. Khi chạy trên EC2, có thể cài CloudWatch Agent để gửi log về CloudWatch Logs.

Các thông tin cần theo dõi:

- Lỗi 4xx/5xx từ API.
- Lỗi kết nối RDS.
- Lỗi upload hoặc đọc file từ S3.
- Tần suất gọi health check.
- CPU, RAM và disk của EC2.

## 3. Dọn dẹp tài nguyên

Sau khi demo hoặc hoàn thành workshop, cần dọn các tài nguyên không còn sử dụng để tránh phát sinh chi phí:

- Dừng hoặc terminate EC2 instance.
- Xóa RDS demo nếu không cần giữ dữ liệu.
- Xóa object trong S3 bucket CV.
- Xóa S3 bucket frontend demo.
- Xóa CloudWatch log group nếu không cần lưu log.
- Kiểm tra lại billing dashboard.

## 4. Kết luận workshop

Workshop giúp nhóm hiểu cách triển khai một ứng dụng web thực tế lên AWS: backend chạy trên EC2, dữ liệu lưu ở RDS, CV lưu ở S3 private bucket, frontend deploy static hosting và log được theo dõi bằng CloudWatch.
