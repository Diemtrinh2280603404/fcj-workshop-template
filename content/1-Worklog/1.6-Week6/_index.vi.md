---
title: "Worklog Tuần 6"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---
### Mục tiêu tuần 6:

* Tập trung nghiên cứu sâu về các công cụ bảo mật tự động nhằm tối ưu hóa khả năng giám sát và phản ứng với các rủi ro tiềm ẩn.
* Hoàn thiện kỹ năng thiết lập quyền hạn chi tiết trong IAM, bao gồm việc phân biệt vai trò (roles) và người dùng (users) để áp dụng nguyên tắc đặc quyền tối thiểu trong môi trường đám mây.

### Các công việc cần triển khai trong tuần này:

| Thứ | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --------- | ------------ | --------------- | ------------------- |
| 2   | - Tìm hiểu nền tảng bảo mật AWS:<br>&nbsp;&nbsp;+ Mô hình trách nhiệm chung (Shared Responsibility Model)<br>&nbsp;&nbsp;+ Tầm quan trọng của bảo vệ dữ liệu trên đám mây | 24/05/2026 | 25/05/2026 | [Tài liệu AWS: Mô hình trách nhiệm chung](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/shared-responsibility.html) |
| 3   | - Nghiên cứu quản trị tuân thủ trên AWS:<br>&nbsp;&nbsp;+ Các quy định tiêu chuẩn quốc tế<br>&nbsp;&nbsp;+ 5 chức năng cốt lõi: Identify, Protect, Detect, Respond, Recover | 25/05/2026 | 27/05/2026 | [Tài liệu AWS: Chương trình tuân thủ trên đám mây](https://aws.amazon.com/vi/compliance/) |
| 4   | - Đánh giá công cụ bảo mật tự động:<br>&nbsp;&nbsp;+ Security Hub<br>&nbsp;&nbsp;+ Trusted Advisor<br>&nbsp;&nbsp;+ Amazon GuardDuty | 27/05/2026 | 28/05/2026 | [Tài liệu AWS: Amazon GuardDuty](https://aws.amazon.com/vi/guardduty/) |
| 5   | - Quản lý định danh và truy cập (IAM):<br>&nbsp;&nbsp;+ Nguyên tắc đặc quyền tối thiểu (Least Privilege)<br>&nbsp;&nbsp;+ Bảo mật tài khoản root và MFA<br>&nbsp;&nbsp;+ Quản lý bí mật với Secrets Manager | 28/05/2026 | 29/05/2026 | [Tài liệu AWS: Quản lý nhận dạng và truy cập (IAM)](https://docs.amazonaws.cn/iam/) |
| 6   | - Chuyên sâu IAM:<br>&nbsp;&nbsp;+ Phân biệt IAM User và IAM Role<br>&nbsp;&nbsp;+ Thiết lập chính sách quyền truy cập (Policy)<br>&nbsp;&nbsp;+ Gắn quyền hạn cho tài nguyên EC2/Lambda | 29/05/2026 | 31/05/2026 | [Tài liệu AWS Builder](https://builder.aws.com/content/3C3mJwaTB5NWzcBfEugE7AUx59H/iam-identity-and-access-management) |

### Thành tích tuần 6:

* Nắm vững mô hình trách nhiệm chung của AWS:
  * AWS chịu trách nhiệm bảo mật hạ tầng vật lý, hypervisor và dịch vụ nền tảng
  * Khách hàng chịu trách nhiệm bảo mật dữ liệu, ứng dụng, cấu hình OS và phân quyền truy cập

* Hiểu rõ khung quản trị tuân thủ và 5 chức năng cốt lõi:
  * Identify (Xác định) – nhận diện tài sản và rủi ro
  * Protect (Bảo vệ) – triển khai biện pháp kiểm soát
  * Detect (Phát hiện) – giám sát bất thường liên tục
  * Respond (Phản hồi) – xử lý sự cố kịp thời
  * Recover (Khôi phục) – phục hồi hệ thống sau sự cố

* Đánh giá và sử dụng thành thạo các công cụ bảo mật tự động:
  * Security Hub – tổng hợp và ưu tiên hóa các phát hiện bảo mật từ nhiều dịch vụ
  * Trusted Advisor – kiểm tra cấu hình theo best practices (bảo mật, chi phí, hiệu năng)
  * GuardDuty – phát hiện mối đe dọa thông minh bằng ML, phân tích CloudTrail, VPC Flow Logs, DNS logs

* Thiết lập IAM đúng theo nguyên tắc đặc quyền tối thiểu:
  * Bảo mật tài khoản root: kích hoạt MFA, không dùng root cho tác vụ thường ngày
  * Tạo IAM User với quyền hạn giới hạn theo từng chức năng
  * Quản lý bí mật bằng AWS Secrets Manager và Parameter Store

* Phân biệt rõ IAM User và IAM Role, thiết lập chính sách truy cập chi tiết:
  * IAM User – danh tính cố định cho người dùng hoặc ứng dụng
  * IAM Role – danh tính tạm thời, gắn cho EC2/Lambda/dịch vụ AWS để truy cập tài nguyên
  * Inline Policy vs Managed Policy – phạm vi áp dụng và khả năng tái sử dụng
