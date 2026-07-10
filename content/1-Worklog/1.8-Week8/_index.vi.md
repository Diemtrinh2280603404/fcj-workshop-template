---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---
### Mục tiêu tuần 8:

* Hiểu các khái niệm Cơ sở hạ tầng dưới dạng mã (IaC).
* Tìm hiểu các nguyên tắc cơ bản về AWS CDK và Terraform.
* Bắt đầu với kiến thức cơ bản về NodeJS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --------- | ------------ | --------------- | ------------------- |
| 2   | - Duy trì ôn luyện thi<br>- Khám phá các tư tưởng cốt lõi của IaC:<br>&nbsp;&nbsp;+ Lợi ích so với cấu hình thủ công<br>&nbsp;&nbsp;+ Declarative vs Imperative approach | 07/06/2026 | 08/06/2026 | [Tìm hiểu về Hạ tầng dạng mã](https://aws.amazon.com/what-is/infrastructure-as-code/) |
| 3   | - Tiếp cận AWS CDK:<br>&nbsp;&nbsp;+ Cấu trúc: App → Stack → Construct (L1, L2, L3)<br>&nbsp;&nbsp;+ Hỗ trợ ngôn ngữ: TypeScript, Python, Java, C#<br>&nbsp;&nbsp;+ Synthesize CDK thành CloudFormation template | 08/06/2026 | 09/06/2026 | [Tài liệu AWS CDK](https://docs.aws.amazon.com/cdk/v2/guide/home.html) |
| 4   | - Tìm hiểu về Terraform:<br>&nbsp;&nbsp;+ Cấu trúc file: main.tf, variables.tf, outputs.tf<br>&nbsp;&nbsp;+ Quy trình: init → plan → apply → destroy<br>&nbsp;&nbsp;+ So sánh Terraform với AWS CDK | 09/06/2026 | 10/06/2026 | [Tài liệu Terraform](https://developer.hashicorp.com/terraform/docs) |
| 5   | - Nhập môn NodeJS:<br>&nbsp;&nbsp;+ Cài đặt Node.js và npm<br>&nbsp;&nbsp;+ Event Loop và mô hình non-blocking I/O<br>&nbsp;&nbsp;+ Các mô-đun cơ bản: fs, path, http, events | 10/06/2026 | 12/06/2026 | [Tài liệu Node.js](https://nodejs.org/docs/latest/api/) |
| 6   | - Thực hành kết hợp IaC và NodeJS:<br>&nbsp;&nbsp;+ Triển khai hạ tầng AWS (S3, Lambda) bằng CDK hoặc Terraform<br>&nbsp;&nbsp;+ Viết Lambda function bằng NodeJS xử lý sự kiện từ S3 | 12/06/2026 | 14/06/2026 | [Trung tâm tài nguyên AWS](https://aws.amazon.com/getting-started/) |

### Thành tích tuần 8:

* Nắm vững các khái niệm cốt lõi của Infrastructure as Code (IaC):
  * Lợi ích so với cấu hình thủ công: tái sử dụng, kiểm soát phiên bản, nhất quán môi trường
  * Hai hướng tiếp cận: Declarative (Terraform) và Imperative (AWS CDK)
  * Vòng đời IaC: viết → kiểm tra → triển khai → cập nhật → hủy

* Nắm được nền tảng và mô hình cấu trúc của AWS CDK:
  * App → Stack → Construct (L1, L2, L3)
  * Hỗ trợ nhiều ngôn ngữ lập trình: TypeScript, Python, Java, C#
  * Tổng hợp (synthesize) CDK app thành CloudFormation template

* Hiểu rõ cú pháp và quy trình làm việc của Terraform:
  * Cấu trúc file: `main.tf`, `variables.tf`, `outputs.tf`, `providers.tf`
  * Quy trình: `terraform init` → `plan` → `apply` → `destroy`
  * So sánh với CDK: Terraform dùng HCL (ngôn ngữ riêng), CDK dùng ngôn ngữ lập trình quen thuộc

* Cài đặt và làm quen thành công với môi trường NodeJS:
  * Cài đặt Node.js và npm, quản lý package với `package.json`
  * Hiểu Event Loop và mô hình non-blocking I/O của Node.js
  * Sử dụng các mô-đun cơ bản: `fs`, `path`, `http`, `events`

* Hoàn thành bài tập thực hành kết hợp IaC và NodeJS:
  * Triển khai thành công hạ tầng AWS (S3 bucket, Lambda function) bằng CDK hoặc Terraform
  * Viết Lambda function bằng NodeJS xử lý sự kiện từ S3
