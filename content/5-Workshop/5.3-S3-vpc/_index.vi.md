---
title : "Cấu hình S3 lưu trữ CV"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

Amazon S3 được dùng để lưu file CV của sinh viên. Vì CV là dữ liệu cá nhân, bucket cần được cấu hình private.

## 1. Tạo bucket

Thiết lập đề xuất:

```text
Bucket purpose: CV uploads
Region: ap-southeast-1
Block public access: On
Encryption: SSE-S3 hoặc SSE-KMS
Versioning: Optional
```

## 2. Cấp quyền cho backend

Backend trên EC2 chỉ cần quyền tối thiểu để upload và đọc file CV:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "s3:PutObject",
        "s3:GetObject"
      ],
      "Resource": "arn:aws:s3:::<your-cv-bucket>/*"
    }
  ]
}
```

## 3. Cấu hình backend

```env
AWS_REGION=ap-southeast-1
S3_BUCKET_NAME=<your-cv-bucket>
S3_PRESIGNED_URL_EXPIRE_SECONDS=300
```

## 4. Kiểm thử

1. Đăng nhập bằng tài khoản student.
2. Cập nhật hồ sơ cá nhân.
3. Upload CV.
4. Kiểm tra object đã xuất hiện trong S3 bucket.
5. Đăng nhập company và mở CV của ứng viên thông qua API backend.

Kết quả mong đợi là CV không public trực tiếp nhưng vẫn xem được qua presigned URL khi người dùng có quyền hợp lệ.
