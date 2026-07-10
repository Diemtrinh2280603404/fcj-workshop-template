---
title: "Worklog Tuần 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---



### Mục tiêu tuần 1:

* Thiết lập hoàn thiện tài khoản AWS và tổ chức nhóm làm việc.
* Nhận gói tín dụng $200 và xây dựng chiến lược quản lý chi phí.
* Nắm vững kiến thức nền tảng về mô hình điện toán đám mây.
* Cài đặt và cấu hình thành công AWS CLI.

### Các công việc cần triển khai trong tuần này:

| Thứ | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --------- | ------------ | --------------- | ------------------- |
| 2   | - Làm quen với các thành viên FCAJ<br>- Đọc và lưu ý các nội quy tại đơn vị thực tập<br>- Hoàn tất đăng ký tài khoản AWS<br>- Thành lập nhóm làm việc | 20/04/2026 | 21/04/2026 | [Video hướng dẫn](https://www.youtube.com/watch?v=2QSXYi6Ofmc&t=1s) |
| 3   | - Thực hiện nhiệm vụ để nhận $200 Credit AWS | 21/04/2026 | 22/04/2026 | [Hướng dẫn nhận $200 Credit](https://000001.awsstudygroup.com/3-chi%E1%BA%BFn-l%C6%B0%E1%BB%A3c-nh%E1%BA%ADn-%C4%91%E1%BB%A7-200-credit/) |
| 4   | - Xây dựng chiến lược quản lý ngân sách AWS:<br>&nbsp;&nbsp;+ Thiết lập AWS Budgets và Cost Explorer<br>&nbsp;&nbsp;+ Lập kế hoạch phân bổ $200 credit cho cả kỳ thực tập | 22/04/2026 | 23/04/2026 | [Quản lý Chi phí AWS](https://aws.amazon.com/vi/aws-cost-management/) |
| 5   | - Nghiên cứu kiến thức nền tảng điện toán đám mây:<br>&nbsp;&nbsp;+ Mô hình triển khai: Public, Private, Hybrid Cloud<br>&nbsp;&nbsp;+ Mô hình dịch vụ: IaaS, PaaS, SaaS | 23/04/2026 | 24/04/2026 | [Tổng quan về Điện toán đám mây](https://www.youtube.com/watch?v=HxYZAK1coOI&list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&index=5) |
| 6   | - Thiết lập và cấu hình môi trường AWS CLI:<br>&nbsp;&nbsp;+ Cài đặt AWS CLI<br>&nbsp;&nbsp;+ Cấu hình Access Key, Region, Output Format<br>&nbsp;&nbsp;+ Thực hành các lệnh AWS CLI cơ bản | 24/04/2026 | 26/04/2026 | [Hướng dẫn cài đặt và cấu hình AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html) |

### Thành tích tuần 1:

* Đăng ký thành công tài khoản AWS, kích hoạt gói tín dụng $200 và thành lập nhóm làm việc theo đúng tiến độ.

* Thiết lập AWS Budgets và Cost Explorer, xây dựng chiến lược phân bổ ngân sách $200 để duy trì hoạt động trong suốt kỳ thực tập.

* Phân biệt rõ ba mô hình triển khai điện toán đám mây:
  * Public Cloud
  * Private Cloud
  * Hybrid Cloud

* Nắm vững ba tầng dịch vụ đám mây với ví dụ thực tế trên AWS:
  * IaaS (EC2, VPC, S3)
  * PaaS (Elastic Beanstalk, RDS)
  * SaaS (Amazon WorkMail, Chime)

* Cài đặt và cấu hình AWS CLI thành công, bao gồm:
  * Access Key & Secret Key
  * Region mặc định
  * Output format

* Sử dụng AWS CLI để thực hiện các thao tác cơ bản như:
  * Kiểm tra thông tin tài khoản (`aws sts get-caller-identity`)
  * Liệt kê danh sách region (`aws ec2 describe-regions`)
  * Truy vấn tài nguyên EC2 đang chạy
