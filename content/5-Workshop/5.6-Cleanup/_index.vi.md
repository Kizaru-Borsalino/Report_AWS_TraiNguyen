---
title: "Dọn dẹp tài nguyên và bàn giao"
date: 2026-08-12
weight: 6
chapter: false
pre: " <b> 5.6. </b> "
---

## Dọn dẹp tài nguyên

1. Xóa CloudFront distribution sau khi đã disable.
2. Xóa nội dung bucket frontend và bucket CV nếu không cần lưu giữ.
3. Scale ECS service về `0` hoặc xóa service, task definition không còn dùng.
4. Xóa image cũ trong ECR.
5. Snapshot RDS trước khi xóa database.
6. Xóa alarm và log group không còn sử dụng để tránh phát sinh chi phí.

## Gói bàn giao

- Sơ đồ kiến trúc JobGo trên AWS.
- Danh sách biến môi trường production.
- Checklist build frontend, push image, update ECS service và invalidation CloudFront.
- Danh sách master data phục vụ AI Matching.
- Tài liệu kiểm thử luồng guest, ứng viên, doanh nghiệp và admin.

## Hướng phát triển tiếp theo

- Tích hợp CI/CD bằng GitHub Actions và AWS CodeDeploy hoặc ECS deployment workflow.
- Gắn domain riêng với [AWS Certificate Manager](https://docs.aws.amazon.com/acm/latest/userguide/acm-overview.html) và [Amazon Route 53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Welcome.html).
- Nâng cấp AI Matching từ rule-based sang mô hình semantic hoặc embedding khi có dữ liệu đủ lớn.
