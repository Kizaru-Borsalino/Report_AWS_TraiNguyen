---
title: "Chia sẻ và góp ý"
date: 2026-08-16
weight: 7
chapter: false
pre: " <b> 7. </b> "
---

## Sharing

Điều em học được nhiều nhất từ dự án JobGo là cách kết nối giữa tư duy sản phẩm và tư duy kỹ thuật. Trước đây em thường nhìn bài toán theo hướng “cần thêm tính năng gì”, nhưng sau quá trình làm dự án, em học được cách đặt câu hỏi ngược lại: “người dùng thật sự cần gì, dữ liệu phải đi như thế nào, trạng thái nào cần được lưu, và vai trò nào được phép thao tác ở từng bước”. Cách suy nghĩ đó giúp em nhìn dự án rõ hơn và giúp code sau này ít bị vá lỗi chồng chéo.

Về mặt kỹ thuật, JobGo cho em cơ hội kết hợp nhiều mảng trong một sản phẩm thống nhất: frontend với React, backend với FastAPI, thiết kế database, quản lý file CV, chuẩn hóa master data, và mô phỏng triển khai trên AWS. Phần giá trị nhất là em không chỉ làm CRUD đơn thuần mà còn phải giải quyết bài toán đồng bộ dữ liệu giữa nhiều role và nhiều màn hình khác nhau. Điều này khiến em hiểu sâu hơn về state management, business flow và cấu trúc API phục vụ nhiều nhóm người dùng.

Theo góc nhìn cá nhân, điểm mạnh lớn nhất của dự án là đã hình thành được một luồng nghiệp vụ tương đối đầy đủ cho hệ thống tuyển dụng: guest xem việc làm công khai, ứng viên tạo hồ sơ và ứng tuyển, doanh nghiệp đăng tin và xem ứng viên, admin quản lý dữ liệu và phê duyệt. Ngoài ra, AI Matching Engine là điểm nổi bật giúp dự án có định hướng khác biệt hơn so với một website tuyển dụng cơ bản.

Tuy nhiên, dự án cũng cho thấy một số điểm yếu nội tại. Khi nghiệp vụ mở rộng nhanh, giao diện và dữ liệu rất dễ bị rời rạc nếu không có thiết kế ngay từ đầu. Một số phần như khả năng quan sát hệ thống, CI/CD, rollback release, kiểm thử tự động và tối ưu thuật toán matching vẫn còn ở mức định hướng nhiều hơn là hoàn thiện thực chiến. Điều đó giúp em hiểu rằng làm ra sản phẩm chạy được mới chỉ là bước đầu, còn để sản phẩm thực sự bền và có thể mở rộng thì cần thêm nhiều lớp đầu tư khác.

## Feedback

Nếu đánh giá dự án một cách khách quan, JobGo đã đạt được nền tảng chức năng khá tốt nhưng vẫn còn nhiều khoảng trống cần cải thiện. Phần matching hiện tại hợp lý cho giai đoạn đầu vì dựa trên rule-based scoring và dữ liệu chuẩn hóa, nhưng về lâu dài sẽ cần mở rộng để xử lý tốt hơn các trường hợp hồ sơ và job có độ phong phú cao hơn. Chẳng hạn, khi ứng viên có kỹ năng tương đương nhưng khác cách gọi tên, hoặc khi job description có nhiều tiêu chí ẩn mà không nằm trọn trong master data, thuật toán hiện tại sẽ chưa đủ linh hoạt.

Phần thứ hai cần cải thiện là trải nghiệm quản trị và vận hành. Hệ thống đã có các luồng cho admin, doanh nghiệp và ứng viên, nhưng để đưa vào môi trường production thực tế thì vẫn cần đầu tư thêm vào kiểm thử tự động, audit log, monitoring chi tiết hơn, phân quyền chặt hơn, và quy trình triển khai có thể lặp lại. Đây là những phần ít thấy trên giao diện nhưng lại quyết định trực tiếp chất lượng vận hành lâu dài.

Trong tương lai, em muốn sửa đổi dự án theo ba hướng chính. Thứ nhất là nâng cấp AI Matching từ rule-based sang hướng semantic hơn, có thể kết hợp embedding hoặc mô hình đánh giá ngữ nghĩa khi dữ liệu đủ lớn. Thứ hai là bổ sung pipeline CI/CD và bộ test cho các luồng chính để giảm lỗi hồi quy. Thứ ba là tối ưu lại trải nghiệm người dùng ở các trang có nhiều dữ liệu như danh sách ứng viên, lịch sử ứng tuyển và báo cáo quản trị để sản phẩm không chỉ đúng nghiệp vụ mà còn dễ sử dụng hơn trong thực tế.
