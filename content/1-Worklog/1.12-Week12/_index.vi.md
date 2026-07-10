---
title: "Worklog Tuần 12"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.12 </b> "
---
### Mục tiêu tuần 12:

* Hoàn thiện tính năng tương tác cộng đồng cho hệ thống FlashLearn.
* Xây dựng logic tính điểm và xếp hạng người dùng.
* Triển khai hệ thống bình luận phân cấp.
* Lưu vết hoạt động người dùng vào cơ sở dữ liệu.
* Hoàn tất tài liệu kỹ thuật và bàn giao dự án.

### Các công việc cần triển khai trong tuần này:

| Thứ | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --------- | ------------ | --------------- | ------------------- |
| 2   | - Họp nhóm thiết kế API tương tác cộng đồng:<br>&nbsp;&nbsp;+ API bình chọn Flashcard (upvote/downvote)<br>&nbsp;&nbsp;+ API xếp hạng Quiz theo thời gian và tỷ lệ đúng | 05/07/2026 | 06/07/2026 | |
| 3   | - Triển khai logic tính điểm và xếp hạng:<br>&nbsp;&nbsp;+ Cộng điểm: upvote, hoàn thành Quiz, tạo Flashcard được duyệt<br>&nbsp;&nbsp;+ Trừ điểm: downvote, vi phạm nội quy<br>&nbsp;&nbsp;+ Leaderboard phân loại theo tuần/tháng/toàn thời gian | 06/07/2026 | 07/07/2026 | |
| 4   | - Thiết kế hệ thống bình luận phân cấp:<br>&nbsp;&nbsp;+ Cấu trúc dữ liệu hỗ trợ reply lồng nhau (parent_id)<br>&nbsp;&nbsp;+ Cập nhật tự động bộ đếm comment_count<br>&nbsp;&nbsp;+ Kiểm duyệt nội dung bình luận qua Lambda | 07/07/2026 | 08/07/2026 | |
| 5   | - Hoàn thiện tính năng bổ sung:<br>&nbsp;&nbsp;+ Tính năng "Yêu thích" (Favorite) Flashcard/Quiz<br>&nbsp;&nbsp;+ Lưu vết hoạt động người dùng vào bảng user_activities<br>&nbsp;&nbsp;+ Dữ liệu hoạt động phục vụ gợi ý học tập thông minh | 08/07/2026 | 09/07/2026 | |
| 6   | - Họp nhóm hoàn tất tài liệu và bàn giao dự án:<br>&nbsp;&nbsp;+ Tài liệu API với Swagger/OpenAPI spec cho toàn bộ endpoints<br>&nbsp;&nbsp;+ ERD tổng hợp toàn hệ thống (10+ bảng)<br>&nbsp;&nbsp;+ Hồ sơ bàn giao: kiến trúc, hướng dẫn triển khai, tài khoản | 09/07/2026 | 10/07/2026 | |

### Thành tích tuần 12:

* Hoàn thiện API tương tác cộng đồng cho FlashLearn:
  * API bình chọn Flashcard: POST /flashcards/{id}/vote (upvote/downvote)
  * API xếp hạng Quiz: tính điểm theo thời gian hoàn thành và tỷ lệ câu đúng
  * Leaderboard cập nhật theo thời gian thực qua DynamoDB

* Triển khai thành công logic tính điểm và xếp hạng:
  * Cộng điểm khi upvote, hoàn thành Quiz, tạo Flashcard được duyệt
  * Trừ điểm khi nhận downvote hoặc vi phạm nội quy
  * Bảng xếp hạng (Leaderboard) phân loại theo tuần/tháng/toàn thời gian

* Xây dựng hệ thống bình luận phân cấp hoàn chỉnh:
  * Cấu trúc dữ liệu hỗ trợ bình luận và reply lồng nhau (parent_id)
  * Tự động cập nhật bộ đếm comment_count trên mỗi Flashcard/Quiz
  * Kiểm duyệt nội dung bình luận qua Lambda trước khi hiển thị

* Hoàn thiện tính năng Favorite và lưu vết hoạt động người dùng:
  * Người dùng có thể lưu Flashcard/Quiz yêu thích vào thư mục cá nhân
  * Bảng `user_activities` ghi lại toàn bộ hành động: xem, học, bình chọn, bình luận
  * Dữ liệu hoạt động phục vụ tính năng gợi ý học tập thông minh

* Hoàn tất tài liệu kỹ thuật và bàn giao dự án thành công:
  * Tài liệu API đầy đủ với Swagger/OpenAPI spec cho toàn bộ endpoints
  * ERD tổng hợp toàn hệ thống với đầy đủ 10+ bảng và quan hệ
  * Hồ sơ bàn giao bao gồm: kiến trúc hệ thống, hướng dẫn triển khai, tài khoản và quyền truy cập
