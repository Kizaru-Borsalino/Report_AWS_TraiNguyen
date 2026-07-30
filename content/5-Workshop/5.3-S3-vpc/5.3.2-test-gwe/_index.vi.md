---
title : "Kiểm thử upload CV"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.3.2. </b> "
---

## Luồng kiểm thử

1. Đăng nhập frontend bằng tài khoản student.
2. Vào trang hồ sơ sinh viên.
3. Chọn file CV hợp lệ.
4. Gửi request upload tới backend.
5. Backend lưu file lên S3.
6. Kiểm tra trong S3 bucket có object mới.
7. Đăng nhập bằng tài khoản company.
8. Mở danh sách ứng viên và xem CV thông qua presigned URL.

## Tiêu chí thành công

- CV không thể truy cập bằng public URL trực tiếp.
- Backend lưu đúng object key vào database.
- Presigned URL chỉ được tạo khi user có quyền.
- URL hết hạn sau thời gian cấu hình, ví dụ 300 giây.

## Kết luận

S3 giúp tách file storage khỏi backend server, giảm tải cho EC2 và phù hợp với yêu cầu lưu trữ file trong ứng dụng cloud.
