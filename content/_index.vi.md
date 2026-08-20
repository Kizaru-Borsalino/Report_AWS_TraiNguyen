---
title: "Báo cáo thực tập"
date: 2026-06-15
weight: 1
chapter: false
---

# Báo cáo thực tập

### Thông tin sinh viên:

&emsp; **Họ và tên:** Nguyễn Quang Trãi

&emsp; **Số điện thoại:** 0869905028

&emsp; **Email:** trai271020004@gmail.com

&emsp; **Trường:** Đại học Công nghệ Thông tin

&emsp; **Ngành:** Hệ thống thông tin

&emsp; **Lớp:** AWS082025

&emsp; **Công ty thực tập:** Công ty TNHH Amazon Web Services Việt Nam

&emsp; **Vị trí thực tập:** Fullstack Developer Intern

&emsp; **Thời gian thực tập:** Từ ngày 15/06/2026 đến ngày 05/09/2026

![Ảnh đại diện của bạn](/images/avatar.jpg)

### Giới thiệu dự án

Trong kỳ thực tập, em tham gia xây dựng **JobGo** - một nền tảng tuyển dụng và tìm việc làm tập trung trên cloud, hỗ trợ ba nhóm người dùng chính: **ứng viên**, **doanh nghiệp** và **quản trị viên**. Hệ thống cho phép ứng viên tạo hồ sơ, quản lý CV, nhận gợi ý công việc phù hợp bằng **AI Matching**; doanh nghiệp có thể tạo tin tuyển dụng, xem danh sách ứng viên và cập nhật trạng thái; còn quản trị viên chịu trách nhiệm duyệt nội dung, quản lý danh mục dữ liệu và vận hành hệ thống.

Kiến trúc triển khai của JobGo được định hướng cho môi trường AWS production:

- **Frontend** được build bằng React và phân phối qua **Amazon S3 + Amazon CloudFront**.
- **Backend FastAPI** được container hóa và chạy trên **Amazon ECS Fargate** sau **Application Load Balancer**.
- **Dữ liệu quan hệ** được lưu trên **Amazon RDS for PostgreSQL**.
- **CV của ứng viên** được lưu trong **Amazon S3 private bucket** và truy cập bằng **presigned URL**.
- **Giám sát vận hành** sử dụng **Amazon CloudWatch Logs** và các cảnh báo cơ bản.

### Nội dung báo cáo

1. [Worklog](1-Worklog/)
2. [Proposal](2-Proposal/)
3. [Blogs Posted](3-Project/)
4. [Events Participated](4-EventParticipated/)
5. [Workshop](5-Workshop/)
6. [Tự đánh giá](6-Self-evaluation/)
7. [Chia sẻ, đóng góp ý kiến](7-Feedback/)
8. [Tài liệu tham khảo](8-References/)
