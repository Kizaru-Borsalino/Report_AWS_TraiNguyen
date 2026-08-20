---
title: "Deploy backend lên ECS Fargate"
date: 2026-08-09
weight: 2
chapter: false
pre: " <b> 5.4.2. </b> "
---

1. Build backend image và push lên ECR.
2. Cập nhật task definition sử dụng image mới.
3. Gắn service với Application Load Balancer.
4. Kiểm tra health endpoint và migration database.
