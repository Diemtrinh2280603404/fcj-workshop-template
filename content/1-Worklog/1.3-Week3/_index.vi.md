---
title: "Worklog Tuần 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---
### Mục tiêu tuần 3:

* Nắm vững kiến trúc EC2, cơ chế cân bằng tải và chiến lược mở rộng tài nguyên tự động.
* Hiểu rõ các mô hình dịch vụ lưu trữ dữ liệu hiện đại và giải pháp di chuyển cơ sở dữ liệu lên AWS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --------- | ------------ | --------------- | ------------------- |
| 2   | - Nghiên cứu kiến trúc EC2:<br>&nbsp;&nbsp;+ Phân loại Instance theo workload<br>&nbsp;&nbsp;+ Thành phần: AMI, VPC, Security Group, EBS<br>&nbsp;&nbsp;+ Cơ chế truy cập: SSH, EC2 Connect, Session Manager | 03/05/2026 | 06/05/2026 | [Amazon EC2 Documentation](https://docs.aws.amazon.com/ec2/) |
| 3   | - Tìm hiểu cân bằng tải (ELB) và tự động mở rộng (Auto Scaling):<br>&nbsp;&nbsp;+ Application Load Balancer (ALB)<br>&nbsp;&nbsp;+ Auto Scaling Group và Scaling Policy | 06/05/2026 | 08/05/2026 | [Elastic Load Balancing](https://aws.amazon.com/vi/elasticloadbalancing/) / [Auto Scaling](https://aws.amazon.com/vi/autoscaling/) |
| 4   | - Khám phá Container và Serverless trên AWS:<br>&nbsp;&nbsp;+ Container: ECS, EKS<br>&nbsp;&nbsp;+ Serverless: AWS Lambda, Fargate | 08/05/2026 | 09/05/2026 | [Amazon ECS](https://aws.amazon.com/ecs/) / [AWS Lambda](https://aws.amazon.com/lambda/) |
| 5   | - Tìm hiểu các loại cơ sở dữ liệu AWS:<br>&nbsp;&nbsp;+ SQL: RDS (MySQL, PostgreSQL), Aurora<br>&nbsp;&nbsp;+ NoSQL: DynamoDB<br>&nbsp;&nbsp;+ In-memory: MemoryDB | 09/05/2026 | 10/05/2026 | [Amazon RDS](https://aws.amazon.com/rds/) / [Amazon DynamoDB](https://aws.amazon.com/dynamodb/) |
| 6   | - Chiến lược di chuyển dữ liệu (6R):<br>&nbsp;&nbsp;+ Công cụ: DMS, SCT, Snow Family, DataSync<br>&nbsp;&nbsp;+ Lựa chọn giải pháp phù hợp theo từng kịch bản | 10/05/2026 | 10/05/2026 | [AWS Database Migration Service](https://aws.amazon.com/dms/) / [AWS Snow Family](https://aws.amazon.com/snowball/) |

### Thành tích tuần 3:

* Phân loại chi tiết kiến trúc EC2 theo workload và nắm rõ các thành phần thiết lập:
  * AMI, VPC, Security Group, EBS
  * Các phương thức truy cập từ xa: SSH Key Pair, EC2 Instance Connect, Session Manager

* Nắm được nguyên lý cân bằng tải và tự động mở rộng tài nguyên:
  * Application Load Balancer (ALB) – định tuyến theo path/host
  * Scaling Policy: Target Tracking, Step Scaling, Scheduled Scaling
  * Kết hợp ELB với Auto Scaling Group để đảm bảo tính sẵn sàng cao

* Phân biệt rõ các mô hình Container và Serverless trên AWS:
  * ECS (EC2 launch type) vs EKS (Kubernetes)
  * Fargate – serverless container, không quản lý máy chủ
  * AWS Lambda – event-driven, tính phí theo số lần gọi và thời gian thực thi

* Phân loại và lựa chọn đúng dịch vụ cơ sở dữ liệu theo yêu cầu:
  * SQL: RDS (MySQL, PostgreSQL), Aurora (hiệu năng cao)
  * NoSQL: DynamoDB (key-value, document, độ trễ thấp)
  * In-memory: MemoryDB (Redis-compatible, bền vững)

* Nắm được 6 chiến lược di chuyển (6R) và vai trò của từng công cụ:
  * AWS DMS – di chuyển database trực tuyến (online migration)
  * AWS SCT – chuyển đổi schema tự động giữa các engine khác nhau
  * Snow Family – di chuyển dữ liệu offline quy mô lớn (TB đến PB)
  * DataSync – đồng bộ file storage liên tục và tự động
