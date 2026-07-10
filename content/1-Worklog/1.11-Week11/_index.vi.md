---
title: "Worklog Tuần 11"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---
### Mục tiêu tuần 11:

* Thiết kế API cốt lõi cho hệ thống FlashLearn.
* Xây dựng cơ sở dữ liệu và giao diện quản trị nội dung.
* Triển khai luồng phê duyệt nội dung tự động.
* Tối ưu hóa quản lý tài nguyên lưu trữ với S3 Presigned URL.
* Hoàn thiện tài liệu kỹ thuật và sơ đồ quan hệ thực thể (ERD).

### Các công việc cần triển khai trong tuần này:

| Thứ | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --------- | ------------ | --------------- | ------------------- |
| 2   | - Thiết kế API RESTful cho Flashcard và Quiz:<br>&nbsp;&nbsp;+ POST /flashcards (Create), GET, PUT, DELETE<br>&nbsp;&nbsp;+ Xác thực dữ liệu đầu vào (tối đa ký tự, định dạng câu hỏi)<br>&nbsp;&nbsp;+ Tích hợp JWT token qua API Gateway Authorizer | 28/06/2026 | 29/06/2026 | [Xây dựng API RESTful với API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/getting-started.html) |
| 3   | - Xây dựng cơ sở dữ liệu và giao diện admin:<br>&nbsp;&nbsp;+ Tạo bảng flashcards với cột status (pending/approved/rejected)<br>&nbsp;&nbsp;+ Tạo bảng quiz_results<br>&nbsp;&nbsp;+ Giao diện admin quản trị nội dung (xem, duyệt, từ chối) | 29/06/2026 | 30/06/2026 | |
| 4   | - Triển khai luồng phê duyệt nội dung tự động:<br>&nbsp;&nbsp;+ Khi admin duyệt → Lambda cập nhật chỉ mục tìm kiếm<br>&nbsp;&nbsp;+ EventBridge gửi thông báo đến người tạo nội dung<br>&nbsp;&nbsp;+ Lưu lịch sử phê duyệt vào bảng audit_logs | 01/07/2026 | 02/07/2026 | |
| 5   | - Tạo S3 Presigned URL cho upload/download:<br>&nbsp;&nbsp;+ Presigned URL có thời hạn để upload trực tiếp lên S3<br>&nbsp;&nbsp;+ CloudFront phân phối ảnh/âm thanh với URL ký số<br>&nbsp;&nbsp;+ Giảm tải băng thông server | 02/07/2026 | 03/07/2026 | [CloudJourney AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| 6   | - Hoàn thiện tài liệu kỹ thuật và ERD:<br>&nbsp;&nbsp;+ ERD đầy đủ: Users, Flashcards, Decks, Quiz, QuizResults, Battle, Progress, AuditLogs<br>&nbsp;&nbsp;+ Tài liệu API với endpoint, request/response schema và mã lỗi | 03/07/2026 | 05/07/2026 | [Hướng dẫn thiết kế sơ đồ quan hệ thực thể](https://lucid.co/diagram/erd/tutorial) |

### Thành tích tuần 11:

* Thiết kế và hoàn thiện API RESTful cốt lõi cho hệ thống FlashLearn:
  * API Flashcard: POST /flashcards (Create), GET /flashcards/{id}, PUT, DELETE với xác thực dữ liệu đầu vào
  * API Quiz: thiết lập cấu trúc câu hỏi, định dạng đáp án và giới hạn ký tự
  * Tích hợp xác thực JWT token qua API Gateway Authorizer

* Xây dựng thành công cơ sở dữ liệu và giao diện quản trị nội dung:
  * Tạo bảng `flashcards` với cột `status` (pending/approved/rejected) và `quiz_results`
  * Giao diện admin cho phép xem, duyệt, từ chối và chỉnh sửa nội dung flashcard
  * Phân quyền admin qua IAM Role riêng biệt

* Triển khai luồng phê duyệt nội dung tự động:
  * Khi admin duyệt nội dung → Lambda trigger tự động cập nhật chỉ mục tìm kiếm
  * Gửi thông báo EventBridge đến người tạo nội dung khi trạng thái thay đổi
  * Lưu lịch sử phê duyệt vào bảng audit_logs

* Tối ưu hóa quản lý tài nguyên lưu trữ với S3 Presigned URL:
  * Tạo Presigned URL có thời hạn cho phép người dùng upload trực tiếp lên S3 (bỏ qua server)
  * CloudFront phân phối ảnh/âm thanh từ S3 với URL ký số, bảo vệ tài nguyên khỏi truy cập trái phép
  * Giảm tải băng thông server, cải thiện tốc độ upload

* Hoàn thiện tài liệu kỹ thuật và ERD hệ thống:
  * ERD đầy đủ gồm các thực thể: Users, Flashcards, Decks, Quiz, QuizResults, Battle, Progress, AuditLogs
  * Xác định quan hệ 1-N và N-N, khoá chính, khoá ngoại cho từng bảng
  * Tài liệu API đầy đủ với mô tả endpoint, request/response schema và mã lỗi
