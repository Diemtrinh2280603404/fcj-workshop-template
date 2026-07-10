---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---
### Mục tiêu tuần 5:

* Nắm vững các giải pháp lưu trữ đa dạng trên AWS và quy trình quản lý vòng đời dữ liệu.
* Thành thạo việc ứng dụng các dịch vụ AI/ML, công cụ phân tích dữ liệu và tích hợp hệ thống trong các bài tập thực hành cụ thể.

### Các công việc cần triển khai trong tuần này:

| Thứ | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --------- | ------------ | --------------- | ------------------- |
| 2   | - Nghiên cứu các phương thức lưu trữ AWS:<br>&nbsp;&nbsp;+ Object Storage: S3<br>&nbsp;&nbsp;+ Block Storage: EBS<br>&nbsp;&nbsp;+ File Storage: EFS<br>&nbsp;&nbsp;+ In-memory: ElastiCache<br>- Tìm hiểu quy trình quản lý vòng đời và sao lưu dữ liệu | 17/05/2026 | 20/05/2026 | [Tài liệu S3](https://docs.aws.amazon.com/s3/) / [Tài liệu EBS](https://docs.aws.amazon.com/ebs/) / [Tài liệu EFS](https://docs.aws.amazon.com/efs/) |
| 3   | - Tìm hiểu hệ sinh thái AI/ML trên AWS:<br>&nbsp;&nbsp;+ Dịch vụ AI tích hợp sẵn<br>&nbsp;&nbsp;+ Machine Learning với SageMaker<br>&nbsp;&nbsp;+ Hỗ trợ lập trình với CodeWhisperer<br>- Nghiên cứu quy trình triển khai ML chuẩn trên AWS | 20/05/2026 | 22/05/2026 | [Tài liệu SageMaker](https://docs.aws.amazon.com/sagemaker/) / [Dịch vụ AI của AWS](https://aws.amazon.com/ai/services/) |
| 4   | - Khám phá các dịch vụ phân tích dữ liệu:<br>&nbsp;&nbsp;+ Serverless query: Athena<br>&nbsp;&nbsp;+ Xử lý luồng: Kinesis<br>&nbsp;&nbsp;+ ETL: Glue<br>&nbsp;&nbsp;+ Kho dữ liệu: Redshift<br>&nbsp;&nbsp;+ Trực quan hóa: QuickSight | 22/05/2026 | 23/05/2026 | [Tài liệu Athena](https://docs.aws.amazon.com/athena/) / [Tài liệu Kinesis](https://docs.aws.amazon.com/kinesis/) / [Tài liệu Redshift](https://docs.aws.amazon.com/redshift/) |
| 5   | - Tìm hiểu các dịch vụ tích hợp và kết nối ứng dụng:<br>&nbsp;&nbsp;+ EventBridge: định tuyến sự kiện<br>&nbsp;&nbsp;+ SQS: hàng đợi tin nhắn<br>&nbsp;&nbsp;+ SNS: pub/sub notification<br>- Tìm hiểu thêm Connect, SES và công cụ DevOps | 23/05/2026 | 24/05/2026 | [Tài liệu EventBridge](https://docs.aws.amazon.com/eventbridge/) / [Tài liệu SQS](https://docs.aws.amazon.com/sqs/) / [Tài liệu SNS](https://docs.aws.amazon.com/sns/) |
| 6   | - Thực hành tổng hợp:<br>&nbsp;&nbsp;+ Cấu hình S3 Lifecycle Policy<br>&nbsp;&nbsp;+ Tạo model ML với SageMaker<br>&nbsp;&nbsp;+ Xây dựng data pipeline: Kinesis → Glue → Redshift<br>&nbsp;&nbsp;+ Triển khai hệ thống event-driven với EventBridge | 24/05/2026 | 24/05/2026 | [Hướng dẫn thực hành AWS](https://aws.amazon.com/vi/getting-started/hands-on/) |

### Thành tích tuần 5:

* Phân biệt rõ bốn loại lưu trữ trên AWS và trường hợp sử dụng phù hợp:
  * Object Storage (S3) – lưu trữ file tĩnh, backup, data lake
  * Block Storage (EBS) – ổ đĩa gắn trực tiếp vào EC2, phù hợp database
  * File Storage (EFS) – chia sẻ file giữa nhiều instance cùng lúc
  * In-memory (ElastiCache) – cache dữ liệu, giảm độ trễ truy vấn

* Cấu hình thành công S3 Lifecycle Policy để tự động chuyển dữ liệu giữa các storage class (Standard → IA → Glacier) và thiết lập backup định kỳ.

* Nắm được hệ sinh thái AI/ML trên AWS và quy trình triển khai ML chuẩn:
  * SageMaker – xây dựng, huấn luyện và triển khai model ML
  * CodeWhisperer – hỗ trợ viết code bằng AI trong IDE
  * Quy trình: chuẩn bị dữ liệu → huấn luyện → đánh giá → triển khai endpoint

* Thực hành tạo model ML với SageMaker thành công:
  * Chuẩn bị dataset và upload lên S3
  * Khởi tạo training job và theo dõi tiến trình
  * Deploy model lên endpoint và thực hiện inference

* Nắm vững các dịch vụ phân tích dữ liệu và vai trò từng dịch vụ:
  * Athena – truy vấn SQL trực tiếp trên S3 (serverless, trả phí theo dữ liệu quét)
  * Kinesis – xử lý luồng dữ liệu thời gian thực
  * Glue – ETL serverless, chuẩn bị và chuyển đổi dữ liệu
  * Redshift – kho dữ liệu (data warehouse) quy mô lớn cho phân tích
  * QuickSight – trực quan hóa và tạo dashboard báo cáo

* Xây dựng thành công data pipeline kết nối Kinesis → Glue → Redshift và triển khai hệ thống event-driven sử dụng EventBridge:
  * SQS – hàng đợi tin nhắn, đảm bảo xử lý tuần tự và không mất dữ liệu
  * SNS – pub/sub notification, gửi thông báo đến nhiều subscriber
  * EventBridge – định tuyến sự kiện tự động giữa các dịch vụ AWS
