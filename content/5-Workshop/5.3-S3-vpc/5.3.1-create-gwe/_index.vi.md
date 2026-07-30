---
title : "Tạo private bucket cho CV"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.3.1. </b> "
---

## Các bước thực hiện

1. Mở Amazon S3 Console.
2. Chọn **Create bucket**.
3. Chọn region `ap-southeast-1`.
4. Đặt tên bucket theo dự án, ví dụ `internship-portal-cv-bucket`.
5. Bật **Block all public access**.
6. Bật encryption bằng SSE-S3 hoặc SSE-KMS.
7. Tạo bucket.

## Lý do cấu hình private

CV chứa dữ liệu cá nhân của sinh viên, vì vậy file không được public trực tiếp. Backend sẽ đóng vai trò kiểm soát quyền truy cập và chỉ tạo presigned URL tạm thời cho người dùng hợp lệ.

## Kết quả

Bucket S3 đã sẵn sàng để backend upload CV và quản lý file theo object key.
