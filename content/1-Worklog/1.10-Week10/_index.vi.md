---
title: "Worklog Tuần 10"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---
### Mục tiêu tuần 10:

* Tối ưu hóa hiệu năng hệ thống FlashLearn thông qua caching, xử lý ảnh tự động và kiểm thử API toàn diện.
* Phát triển tính năng gợi ý học tập thông minh dựa trên lịch sử của người dùng.
* Thiết lập hệ thống giám sát và theo dõi hiệu năng ứng dụng trên AWS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --------- | ------------ | --------------- | ------------------- |
| 2   | - Họp nhóm lên kế hoạch tối ưu hóa hiệu năng:<br>&nbsp;&nbsp;+ Tối ưu truy vấn trên RDS PostgreSQL (thêm Index)<br>&nbsp;&nbsp;+ Thiết lập cơ chế caching CloudFront với TTL phù hợp | 21/06/2026 | 22/06/2026 | |
| 3   | - Thực hành tối ưu hóa xử lý ảnh với Lambda:<br>&nbsp;&nbsp;+ Lambda auto-trigger khi ảnh upload lên S3<br>&nbsp;&nbsp;+ Resize ảnh về kích thước chuẩn (thumbnail, medium, large)<br>&nbsp;&nbsp;+ Nén định dạng WebP để giảm dung lượng lưu trữ | 22/06/2026 | 23/06/2026 | [CloudJourney AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| 4   | - Kiểm thử API toàn diện với Postman:<br>&nbsp;&nbsp;+ Kiểm tra các phương thức CRUD qua API Gateway<br>&nbsp;&nbsp;+ Xác nhận cấu hình CORS cho frontend<br>&nbsp;&nbsp;+ Kiểm tra phân quyền IAM Authorization | 23/06/2026 | 24/06/2026 | |
| 5   | - Họp nhóm phát triển tính năng gợi ý học tập thông minh:<br>&nbsp;&nbsp;+ Thuật toán dựa trên lịch sử học (tần suất, tỷ lệ đúng/sai)<br>&nbsp;&nbsp;+ Thiết kế luồng: Lambda đọc Progress table → tính toán → trả kết quả | 24/06/2026 | 26/06/2026 | |
| 6   | - Thiết lập hệ thống giám sát trên AWS:<br>&nbsp;&nbsp;+ CloudWatch Dashboard theo dõi CPU, Memory, Network EC2 (ARM64)<br>&nbsp;&nbsp;+ CloudWatch Alarms cảnh báo khi RDS CPU > 80%<br>&nbsp;&nbsp;+ AWS X-Ray trace API nội bộ, xác định bottleneck | 26/06/2026 | 28/06/2026 | [CloudJourney AWS Study Group](https://cloudjourney.awsstudygroup.com/) |

### Thành tích tuần 10:

* Tối ưu hóa thành công hiệu năng truy vấn RDS PostgreSQL và caching CloudFront:
  * Thêm Index cho các cột truy vấn thường xuyên (user_id, deck_id, created_at)
  * Cấu hình CloudFront Cache Policy với TTL phù hợp cho từng loại nội dung tĩnh
  * Giảm thời gian phản hồi trung bình của các truy vấn phức tạp

* Triển khai thành công pipeline xử lý ảnh tự động với Lambda:
  * Lambda trigger tự động khi ảnh được upload lên S3
  * Resize ảnh về kích thước chuẩn (thumbnail, medium, large) và nén định dạng WebP
  * Lưu các phiên bản ảnh vào S3 prefix riêng biệt, giảm đáng kể dung lượng lưu trữ

* Hoàn thành kiểm thử API toàn diện với Postman:
  * Kiểm tra đầy đủ các phương thức CRUD (GET, POST, PUT, DELETE) qua API Gateway
  * Xác nhận cấu hình CORS hoạt động đúng cho frontend
  * Kiểm tra phân quyền IAM đảm bảo chỉ các role được phép mới có thể gọi API

* Phát triển và hoàn thiện tính năng gợi ý học tập thông minh:
  * Xây dựng thuật toán gợi ý dựa trên lịch sử học (tần suất ôn tập, tỷ lệ đúng/sai, thời gian học)
  * Thiết kế luồng dữ liệu: Lambda đọc Progress table → tính toán → trả về danh sách từ ưu tiên

* Thiết lập hệ thống giám sát toàn diện trên AWS:
  * CloudWatch Dashboard theo dõi CPU, Memory, Network của EC2 (ARM64)
  * CloudWatch Alarms cảnh báo khi RDS CPU > 80% hoặc kết nối vượt ngưỡng
  * AWS X-Ray trace các cuộc gọi API nội bộ, xác định bottleneck trong luồng xử lý
