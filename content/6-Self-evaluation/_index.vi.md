---
title: "Tự đánh giá"
date: 2026-08-15
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

## Kết quả đạt được

Trong suốt quá trình thực hiện dự án JobGo, em đã đạt được tiến bộ rõ rệt ở cả ba mặt: phân tích nghiệp vụ, phát triển fullstack và tư duy triển khai hệ thống trên AWS. Ở giai đoạn đầu, em chủ yếu tiếp cận bài toán dưới góc nhìn tính năng đơn lẻ như đăng ký, đăng nhập, tạo hồ sơ hay đăng tin tuyển dụng. Tuy nhiên sau khi đi sâu hơn vào dự án, em đã hiểu rằng một sản phẩm thực tế cần được nhìn như một hệ thống hoàn chỉnh, bao gồm dữ liệu, luồng nghiệp vụ, quyền truy cập, lưu trữ file, khả năng theo dõi vận hành và định hướng triển khai production.

Về mặt kỹ thuật, em đã có cơ hội làm việc đồng thời với frontend React, backend FastAPI và cơ sở dữ liệu PostgreSQL. Em hiểu rõ hơn cách thiết kế API phục vụ nhiều vai trò khác nhau như guest, ứng viên, doanh nghiệp và quản trị viên. Em cũng học được cách tách master data thành những danh mục chuẩn hóa để tránh nhập liệu tự do, từ đó giúp cho hệ thống nhất quán hơn và tạo nền tảng tốt cho AI Matching Engine hoạt động chính xác hơn.

Một kết quả đáng chú ý khác là em đã xây dựng được tư duy triển khai cloud thay vì chỉ dừng ở môi trường local. Dù trong báo cáo có những phần mô tả theo hướng production giả lập, quá trình nghiên cứu đã giúp em hiểu rõ vai trò của các dịch vụ như Amazon S3, CloudFront, ECS Fargate, RDS PostgreSQL và CloudWatch trong một kiến trúc web hiện đại. Đây là điểm tiến bộ lớn nhất của em so với thời điểm mới bắt đầu kỳ thực tập.

## Khó khăn

Khó khăn lớn nhất trong quá trình thực hiện JobGo là phải xử lý đồng thời cả chiều sâu nghiệp vụ lẫn chiều sâu kỹ thuật. Nghiệp vụ tuyển dụng không chỉ đơn giản là đăng job và ứng tuyển, mà còn kéo theo rất nhiều bài toán liên quan như quản lý CV, cập nhật trạng thái ứng tuyển, duyệt tin tuyển dụng, quản lý master data, và đặc biệt là làm cho các luồng giữa ứng viên và doanh nghiệp không bị rời rạc. Nhiều lỗi ban đầu không nằm ở một chức năng riêng lẻ, mà xuất phát từ việc dữ liệu và trạng thái giữa các màn hình chưa được đồng bộ chặt chẽ.

Khó khăn thứ hai là thiết kế dữ liệu sao cho phù hợp với yêu cầu AI Matching. Nếu hồ sơ ứng viên và tin tuyển dụng cho phép nhập text tự do quá nhiều, hệ thống sẽ rất khó so sánh và tính mức độ phù hợp một cách nhất quán. Vì vậy em phải quay lại chuẩn hóa các trường như kỹ năng, vị trí, địa điểm, loại hình, hình thức làm việc, cấp bậc thành master data dùng chung. Đây là công việc mất thời gian nhưng rất quan trọng để hệ thống hoạt động ổn định hơn.

Ngoài ra, phần tài liệu song ngữ và cấu trúc báo cáo cũng là một thử thách riêng. Việc vừa viết nội dung kỹ thuật, vừa đảm bảo bố cục đúng yêu cầu, vừa giữ tính nhất quán giữa tiếng Việt và tiếng Anh đòi hỏi nhiều thời gian rà soát. Em nhận ra rằng viết báo cáo kỹ thuật tốt không hề đơn giản hơn viết code, vì nó yêu cầu khả năng hệ thống hóa và diễn đạt lại toàn bộ quá trình làm việc một cách rõ ràng.

## Bài học rút ra

Bài học đầu tiên em rút ra là phải bắt đầu từ nghiệp vụ trước khi đi quá nhanh vào kỹ thuật. Nếu không hiểu rõ actor, use case, dữ liệu đầu vào và đầu ra của từng màn hình, việc code sẽ dễ dẫn đến chắp vá, sửa đi sửa lại nhiều lần. Khi đã có một nền tảng phân tích tốt, việc thiết kế database, API và giao diện sẽ mạch lạc hơn rất nhiều.

Bài học thứ hai là dữ liệu chuẩn hóa quan trọng không kém logic xử lý. Trước đây em thường tập trung vào phần giao diện và API trước, nhưng sau dự án này em hiểu rằng master data, trạng thái nghiệp vụ, naming convention và quy tắc validate mới là phần quyết định một hệ thống có bền hay không. Đặc biệt với những tính năng như AI Matching, chất lượng dữ liệu đầu vào gần như quyết định trực tiếp chất lượng của kết quả đầu ra.

Bài học cuối cùng là tư duy production cần được hình thành ngay từ khi bắt đầu phát triển. Dù sản phẩm có thể chạy được ở local, nhưng nếu không nghĩ trước về bảo mật, logging, phân quyền, file storage, chi phí hạ tầng và khả năng mở rộng, hệ thống sẽ rất khó chuyển lên môi trường thực tế. Sau kỳ thực tập này, em tự tin hơn nhiều trong việc nhìn một ứng dụng web không chỉ như một bài tập lập trình, mà như một sản phẩm có vòng đời triển khai và vận hành thực sự.
