---
title: "Worklog Tuần 9"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---
### Mục tiêu tuần 9:

* Xây dựng hệ thống FlashLearn – ứng dụng web hỗ trợ học tiếng Anh thông qua flashcard, quiz, battle và cộng đồng học tập.
* Triển khai kiến trúc hệ thống hiện đại trên nền tảng AWS (Khu vực Singapore) với cấu trúc VPC trên hai Availability Zone để đảm bảo tính sẵn sàng cao.
* Tối ưu hóa hiệu năng ứng dụng bằng cách kết hợp mô hình Serverless và các dịch vụ quản lý như Amazon CloudFront, Lambda và EventBridge.

### Các công việc cần triển khai trong tuần này:

| Thứ | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --------- | ------------ | --------------- | ------------------- |
| 2   | - Họp nhóm khởi động dự án FlashLearn:<br>&nbsp;&nbsp;+ Hoàn thiện thiết kế Schema cơ sở dữ liệu PostgreSQL<br>&nbsp;&nbsp;+ Thu thập và chuẩn hóa bộ dữ liệu từ vựng tiếng Anh | 14/06/2026 | 15/06/2026 | |
| 3   | - Triển khai kiến trúc mạng VPC đa AZ:<br>&nbsp;&nbsp;+ VPC với 2 Public Subnet và 2 Private Subnet<br>&nbsp;&nbsp;+ Cấu hình IAM Role cho EC2 với quyền hạn tối thiểu<br>&nbsp;&nbsp;+ Thiết lập Security Group phân tầng | 15/06/2026 | 16/06/2026 | [CloudJourney AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| 4   | - Cấu hình ALB và phân phối nội dung tĩnh:<br>&nbsp;&nbsp;+ ALB định tuyến traffic theo health check<br>&nbsp;&nbsp;+ Upload tài nguyên tĩnh lên S3<br>&nbsp;&nbsp;+ Tích hợp CloudFront CDN | 16/06/2026 | 18/06/2026 | [CloudJourney AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| 5   | - Team Meeting: Review thiết kế UI/UX trên Figma:<br>&nbsp;&nbsp;+ Review màn hình flashcard, quiz và battle<br>&nbsp;&nbsp;+ Tối ưu luồng trải nghiệm người dùng | 18/06/2026 | 19/06/2026 | |
| 6   | - Xây dựng hệ thống thông báo và phát âm:<br>&nbsp;&nbsp;+ EventBridge rule trigger Lambda gửi nhắc nhở học tập<br>&nbsp;&nbsp;+ Tích hợp Amazon Polly chuyển văn bản thành giọng nói | 19/06/2026 | 21/06/2026 | [CloudJourney AWS Study Group](https://cloudjourney.awsstudygroup.com/) |

### Thành tích tuần 9:

* Hoàn thiện thiết kế Schema cơ sở dữ liệu PostgreSQL cho hệ thống FlashLearn:
  * Xác định các bảng chính: Users, Flashcards, Decks, Quiz, Battle, Progress
  * Thiết lập quan hệ khoá ngoại và chỉ mục tối ưu hoá truy vấn
  * Thu thập và chuẩn hoá bộ dữ liệu từ vựng tiếng Anh

* Triển khai thành công kiến trúc mạng VPC đa vùng sẵn sàng cao trên AWS Singapore:
  * VPC với 2 Public Subnet và 2 Private Subnet trên 2 Availability Zone
  * Cấu hình IAM Role cho EC2 với quyền hạn tối thiểu
  * Thiết lập Security Group phân tầng theo từng lớp ứng dụng

* Cấu hình Application Load Balancer và phân phối nội dung tĩnh:
  * ALB định tuyến traffic đến các EC2 instance theo health check
  * Upload và cấu hình S3 bucket để lưu trữ tài nguyên tĩnh
  * Tích hợp CloudFront CDN để phân phối nội dung với độ trễ thấp toàn cầu

* Tối ưu hoá trải nghiệm người dùng qua Team Meeting với Figma:
  * Review và cải thiện UI/UX cho các màn hình flashcard, quiz và battle
  * Điều chỉnh luồng người dùng dựa trên phản hồi từ nhóm

* Xây dựng thành công hệ thống thông báo tự động và tính năng phát âm:
  * EventBridge rule trigger Lambda theo lịch để gửi nhắc nhở học tập
  * Tích hợp Amazon Polly để chuyển văn bản thành giọng nói cho từ vựng
  * Lambda xử lý sự kiện và lưu kết quả vào S3
