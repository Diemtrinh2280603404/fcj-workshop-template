---
title: "Worklog Tuần 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---
### Mục tiêu tuần 2:

* Nắm vững quản trị người dùng IAM và triển khai lưu trữ trên Amazon S3.
* Thành thạo vận hành máy chủ ảo Amazon EC2 và thiết lập cơ sở dữ liệu Amazon RDS.
* Làm quen với nền tảng điện toán không máy chủ AWS Lambda.

### Các công việc cần triển khai trong tuần này:

| Thứ | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --------- | ------------ | --------------- | ------------------- |
| 2   | - Tìm hiểu hệ sinh thái dịch vụ AWS:<br>&nbsp;&nbsp;+ Compute<br>&nbsp;&nbsp;+ Storage<br>&nbsp;&nbsp;+ Networking<br>&nbsp;&nbsp;+ Database | 27/04/2026 | 27/04/2026 | [AWS Cloud Products Overview](https://aws.amazon.com/vi/products/) |
| 3   | - Nghiên cứu danh mục giải pháp AWS Cloud Practitioner Essentials | 27/04/2026 | 29/04/2026 | [AWS Cloud Practitioner Essentials](https://skillbuilder.aws/search?searchText=aws-cloud-practitioner-essentials&showRedirectNotFoundBanner=true) |
| 4   | - Đăng ký gói Free Tier<br>- Thiết lập môi trường AWS CLI<br>- Thực hành:<br>&nbsp;&nbsp;+ Tạo AWS account<br>&nbsp;&nbsp;+ Cài AWS CLI & cấu hình<br>&nbsp;&nbsp;+ Thực hiện các lệnh cơ bản | 29/04/2026 | 30/04/2026 | [AWS Free Tier & AWS CLI](https://aws.amazon.com/vi/free/) |
| 5   | - Tìm hiểu lý thuyết Amazon EC2:<br>&nbsp;&nbsp;+ Các loại Instance (General Purpose, Compute, Memory)<br>&nbsp;&nbsp;+ AMI (Amazon Machine Image)<br>&nbsp;&nbsp;+ Lưu trữ EBS<br>&nbsp;&nbsp;+ Kết nối SSH / Elastic IP | 30/04/2026 | 02/05/2026 | [Amazon EC2 User Guide](https://docs.aws.amazon.com/ec2/) |
| 6   | - Thực hành triển khai EC2 và EBS:<br>&nbsp;&nbsp;+ Khởi tạo EC2 instance<br>&nbsp;&nbsp;+ Kết nối SSH<br>&nbsp;&nbsp;+ Gắn và mount ổ đĩa EBS | 02/05/2026 | 03/05/2026 | [Thực hành triển khai EC2 và EBS](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html) |

### Thành tích tuần 2:

* Nắm được toàn cảnh các nhóm dịch vụ AWS và vai trò của từng nhóm trong kiến trúc hạ tầng:
  * Compute (EC2, Lambda, ECS)
  * Storage (S3, EBS, EFS)
  * Networking (VPC, Route 53, CloudFront)
  * Database (RDS, DynamoDB, ElastiCache)

* Hoàn thành nghiên cứu danh mục giải pháp AWS Cloud Practitioner Essentials, nắm được các dịch vụ cốt lõi và trường hợp sử dụng thực tế.

* Đăng ký gói Free Tier và thiết lập thành công môi trường AWS CLI; thực hiện thành thạo các lệnh cơ bản để tương tác với các dịch vụ AWS từ dòng lệnh.

* Hiểu rõ các thành phần của Amazon EC2, bao gồm:
  * Các loại Instance (General Purpose, Compute Optimized, Memory Optimized)
  * Quy trình tạo và sử dụng AMI
  * Cấu hình lưu trữ EBS (gp2, gp3, io1)
  * Các phương thức kết nối từ xa (SSH Key Pair, EC2 Instance Connect)

* Triển khai thực tế thành công:
  * Khởi tạo EC2 instance từ AMI
  * Thiết lập kết nối SSH từ máy cục bộ
  * Gắn thêm và mount ổ đĩa EBS vào instance đang chạy
