---
title: "Kiểm thử API, upload CV và quan sát hệ thống"
date: 2026-08-10
weight: 3
chapter: false
pre: " <b> 5.4.3. </b> "
---

## Kiểm thử backend

```bash
curl https://api.jobgo.example.com/health
curl https://api.jobgo.example.com/api/jobs
```

## Kiểm thử nghiệp vụ chính

1. Ứng viên đăng ký tài khoản và tạo hồ sơ.
2. Ứng viên tải CV lên bucket private thông qua backend.
3. Doanh nghiệp tạo tin tuyển dụng với kỹ năng, vị trí, cấp bậc và địa điểm.
4. Trang việc làm hiển thị phần trăm **AI Matching** khi ứng viên đã có hồ sơ.
5. Khi ứng viên bấm ứng tuyển, hệ thống tạo `application`, lưu thư giới thiệu và đồng bộ sang lịch sử ứng tuyển.
6. Doanh nghiệp mở danh sách ứng viên để xem điểm matching, thư giới thiệu, CV và cập nhật trạng thái.

## Quan sát

- Xem log backend trong [CloudWatch Logs](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html).
- Theo dõi lỗi 4xx/5xx tại ALB và ECS service.
- Kiểm tra log upload CV, tạo job, tạo application và cập nhật trạng thái ứng tuyển.
