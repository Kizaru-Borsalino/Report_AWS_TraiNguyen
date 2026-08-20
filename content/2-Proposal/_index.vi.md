---
title: "Bản đề xuất"
date: 2026-06-29
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# JobGo 

## Xây dựng nền tảng tuyển dụng và tìm việc tích hợp AI Matching trên AWS

### 1. Tóm tắt dự án

**JobGo** là một nền tảng tuyển dụng trực tuyến giúp ứng viên tìm việc phù hợp nhanh hơn và giúp doanh nghiệp sàng lọc hồ sơ hiệu quả hơn. Hệ thống cung cấp các chức năng cốt lõi như quản lý hồ sơ ứng viên, quản lý hồ sơ doanh nghiệp, đăng tin tuyển dụng, nộp đơn ứng tuyển, theo dõi trạng thái hồ sơ, quản trị danh mục dữ liệu dùng chung và **AI Matching** để đo mức độ phù hợp giữa hồ sơ ứng viên với tin tuyển dụng.

Thay vì triển khai như một bài tập chạy cục bộ, dự án được định hướng ngay từ đầu cho môi trường **AWS production** với các thành phần:

- **Amazon CloudFront + Amazon S3** cho frontend React.
- **Amazon ECS Fargate + Application Load Balancer** cho backend FastAPI.
- **Amazon RDS for PostgreSQL** cho dữ liệu quan hệ.
- **Amazon S3 private bucket** để lưu CV ứng viên.
- **Amazon CloudWatch Logs** để giám sát và theo dõi lỗi.

### 2. Bài toán cần giải quyết

Quá trình tìm việc và tuyển dụng hiện nay thường gặp ba nhóm vấn đề:

1. **Dữ liệu phân tán:** ứng viên phải tìm việc qua nhiều kênh khác nhau, khó theo dõi trạng thái và quản lý CV.
2. **Sàng lọc thủ công:** doanh nghiệp mất nhiều thời gian để đọc hồ sơ và so sánh mức độ phù hợp giữa ứng viên với tin tuyển dụng.
3. **Thiếu quản trị tập trung:** nếu không có cơ chế duyệt bài đăng, chuẩn hóa danh mục dữ liệu và phân quyền rõ ràng, chất lượng nền tảng sẽ giảm nhanh.

JobGo giải quyết các vấn đề đó bằng một hệ thống tập trung, đa vai trò, có master data rõ ràng và tích hợp engine chấm điểm phù hợp.

### 3. Giải pháp đề xuất

#### Luồng chức năng chính

- **Ứng viên**
  - Đăng ký, đăng nhập, cập nhật hồ sơ.
  - Tải nhiều CV và chọn CV để ứng tuyển.
  - Xem danh sách việc làm công khai.
  - Xem điểm **AI Matching** theo từng tin tuyển dụng.
  - Gửi đơn, rút đơn, xem lịch sử và trạng thái ứng tuyển.

- **Doanh nghiệp**
  - Quản lý hồ sơ công ty.
  - Tạo và quản lý nhiều tin tuyển dụng.
  - Xem danh sách ứng viên cho từng job.
  - Xem điểm **AI Matching** của từng ứng viên.
  - Cập nhật trạng thái ứng tuyển và ghi chú phản hồi.

- **Quản trị viên**
  - Duyệt bài đăng trước khi hiển thị công khai.
  - Quản lý master data như kỹ năng, vị trí, địa điểm, loại hình, hình thức làm việc, cấp bậc.
  - Theo dõi tài khoản và hoạt động chung của hệ thống.

#### AI Matching Engine

AI Matching của JobGo được thiết kế như một dịch vụ chấm điểm có trọng số, dựa trên:

- Kỹ năng
- Vị trí
- Cấp bậc
- Địa điểm
- Hình thức làm việc
- Loại hình công việc

Kết quả trả về bao gồm:

- Điểm phù hợp tổng thể theo phần trăm
- Mức đánh giá định tính
- Điểm thành phần theo từng chiều
- Danh sách kỹ năng phù hợp
- Danh sách kỹ năng còn thiếu

### 4. Kiến trúc triển khai trên AWS

```text
User Browser
  -> CloudFront
  -> S3 static frontend
  -> Application Load Balancer
  -> ECS Fargate service (FastAPI backend)
  -> Amazon RDS PostgreSQL
  -> Amazon S3 private bucket (CV files)
  -> CloudWatch Logs / Alarms
```

![Sơ đồ kiến trúc dự án](/images/architecture_final.png)

### 5. Kết quả kỳ vọng

- Có một web tuyển dụng hoạt động theo đúng vai trò nghiệp vụ.
- Có AI Matching giúp ứng viên và doanh nghiệp ra quyết định nhanh hơn.
- Có kiến trúc triển khai thực tế trên AWS, không phụ thuộc chạy local.
- Có tài liệu song ngữ đủ để demo, bàn giao và mở rộng hệ thống sau kỳ thực tập.
