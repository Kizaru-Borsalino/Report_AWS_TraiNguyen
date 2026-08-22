---
title: "Tài liệu tham khảo"
date: 2026-08-17
weight: 8
chapter: false
pre: " <b> 8. </b> "
---

Phần này tổng hợp các tài liệu được sử dụng trong quá trình phân tích, phát triển và định hướng triển khai dự án JobGo. Các tài liệu không chỉ phục vụ việc viết báo cáo mà còn hỗ trợ trực tiếp cho thiết kế kiến trúc, xây dựng API, xử lý giao diện, lưu trữ file và chuẩn hóa dữ liệu nghiệp vụ.

| Nhóm tài liệu | Tên tài liệu | Liên kết | Mục đích sử dụng |
| --- | --- | --- | --- |
| AWS | AWS Well-Architected Framework | https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html | Định hướng cách đánh giá kiến trúc hệ thống theo các trụ cột như bảo mật, độ tin cậy, hiệu năng và tối ưu chi phí. |
| AWS | Amazon S3 User Guide | https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html | Nghiên cứu cách lưu trữ static assets của frontend, lưu CV trong private bucket và quản lý truy cập file. |
| AWS | Amazon CloudFront Developer Guide | https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html | Tìm hiểu cách phân phối frontend qua CDN, cấu hình cache, HTTPS và hỗ trợ routing cho SPA. |
| AWS | Amazon ECS Developer Guide | https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html | Tham khảo mô hình container orchestration để mô tả hướng triển khai backend FastAPI trên ECS Fargate. |
| AWS | Amazon RDS for PostgreSQL Documentation | https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html | Xây dựng định hướng lưu trữ dữ liệu quan hệ của người dùng, hồ sơ, công việc và ứng tuyển trên PostgreSQL. |
| AWS | Amazon CloudWatch Documentation | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html | Phục vụ phần logging, alarm, giám sát ứng dụng và định hướng vận hành production. |
| AWS | IAM Best Practices | https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html | Tham khảo nguyên tắc phân quyền tối thiểu, quản lý bí mật và bảo vệ tài nguyên AWS. |
| Backend | FastAPI Documentation | https://fastapi.tiangolo.com/ | Sử dụng để thiết kế API, validation request/response và cấu trúc backend service. |
| Backend | SQLAlchemy Documentation | https://docs.sqlalchemy.org/ | Tham khảo cách ánh xạ dữ liệu, xây dựng model và làm việc với PostgreSQL ở tầng ORM. |
| Backend | Pydantic Documentation | https://docs.pydantic.dev/ | Hỗ trợ định nghĩa schema, kiểm tra dữ liệu đầu vào và chuẩn hóa dữ liệu trao đổi qua API. |
| Backend | Uvicorn Documentation | https://www.uvicorn.org/ | Tham khảo cách chạy và phục vụ ứng dụng ASGI cho môi trường phát triển và mô phỏng production. |
| Frontend | React Documentation | https://react.dev/ | Phục vụ việc tổ chức giao diện nhiều vai trò, quản lý state và xây dựng các trang nghiệp vụ. |
| Frontend | Vite Guide | https://vite.dev/guide/ | Tham khảo quy trình build frontend, cấu hình môi trường và xuất bản static assets. |
| Frontend | Ant Design Documentation | https://ant.design/docs/react/introduce | Dùng để chọn component, icon và chuẩn hóa cách xây dựng giao diện cho hệ thống JobGo. |
| Frontend | Ant Design Icons | https://ant.design/components/icon | Tham khảo bộ icon miễn phí để tạo giao diện trực quan hơn cho các vai trò và hành động chính. |
| Tài liệu kỹ thuật | Hugo Documentation | https://gohugo.io/documentation/ | Sử dụng để cấu trúc website báo cáo thực tập, tổ chức nội dung song ngữ và build GitHub Pages. |
| Tài liệu kỹ thuật | GitHub Pages Documentation | https://docs.github.com/en/pages | Tham khảo cách publish website báo cáo, quản lý branch triển khai và kiểm tra kết quả build. |
| Nghiệp vụ / báo cáo | FCAJ Project Rules | https://hcm-rules.awsfcaj.com/3-project/ | Bám theo yêu cầu chính thức về cấu trúc báo cáo, worklog, workshop, blog và nội dung cần có. |
| Nghiệp vụ / báo cáo | Workshop Sample | https://workshop-sample.awsfcaj.com/5-workshop/ | Dùng để tham khảo cấu trúc workshop chuẩn, sau đó điều chỉnh lại nội dung cho phù hợp với JobGo. |
| Source code | Project_AWS_Trai_JobGo | https://github.com/Kizaru-Borsalino/Project_AWS_Trai_JobGo | Mã nguồn project thực tiễn được sử dụng trong báo cáo.|
| Video demo | VideoDemo_Jobgo | https://drive.google.com/drive/folders/1XVq1LOzE-sm1OYaa7ji7e_abpZ6v5QGi?usp=sharing
drive.google.com | Video demo quá trình vận hành và các chức năng chính của project.|
