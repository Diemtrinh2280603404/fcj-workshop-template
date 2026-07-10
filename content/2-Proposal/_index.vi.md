---
title: "Bản đề xuất"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# FlashLearn – Ứng Dụng Học Tiếng Anh Tương Tác Trên AWS

## 1. Tổng quan dự án

Dự án FlashLearn là một ứng dụng web toàn diện hỗ trợ học tiếng Anh tương tác (flashcard, quiz, cộng đồng). Thay vì triển khai theo mô hình nguyên khối truyền thống, dự án tập trung xây dựng một kiến trúc hạ tầng đám mây hiện đại trên Amazon Web Services (AWS) tại khu vực Asia Pacific (Singapore). Kiến trúc tuân thủ nghiêm ngặt các tiêu chuẩn doanh nghiệp về tính phân tán, bảo mật đa lớp và tích hợp tự động hóa.

---

## 2. Mục tiêu

- **Tính sẵn sàng cao (High Availability):** Đảm bảo hệ thống hoạt động liên tục 24/7 bằng cách trải rộng hạ tầng (Multi-AZ) trên 2 Availability Zones.
- **Bảo mật hệ thống chuyên sâu (Deep Security):** Bảo vệ ứng dụng từ biên mạng bằng tường lửa web (WAF) và cô lập hoàn toàn cả máy chủ xử lý (EC2) lẫn cơ sở dữ liệu (RDS) bên trong các mạng riêng tư (Private Subnets).
- **Tối ưu hóa hiệu năng:** Phân phối nội dung tĩnh với tốc độ cao qua mạng lưới CDN toàn cầu và giảm tải cho máy chủ bằng cách tách biệt các tác vụ nền.
- **Mở rộng tính năng cốt lõi:** Ứng dụng trí tuệ nhân tạo (AI) để hỗ trợ phát âm tiếng Anh chuẩn xác.

---

## 3. Vấn đề cần giải quyết

**Vấn đề:** Các hệ thống e-learning thường lưu trữ media trực tiếp trên server và đặt server ở vùng mạng công cộng, gây ra rủi ro bảo mật lớn (dễ bị tấn công DDoS, rò rỉ dữ liệu) và tình trạng thắt nút cổ chai băng thông khi nhiều học viên truy cập cùng lúc.

**Giải pháp:** Đưa S3 và CloudFront ra tuyến đầu để xử lý nội dung tĩnh. Giấu toàn bộ logic nghiệp vụ (EC2) và dữ liệu (RDS) vào lớp Private. Mọi giao tiếp với Internet của Backend phải đi qua NAT Gateway và được phân phối an toàn qua Application Load Balancer.

---

## 4. Kiến trúc giải pháp

Hệ thống được thiết kế hoàn chỉnh bên trong một VPC (10.0.0.0/16) trải dài trên 2 Availability Zone để đảm bảo tính chịu lỗi.

![Kiến trúc giải pháp FlashLearn](/images/2-Proposal/architecture.png)

**Chi tiết các thành phần & luồng xử lý:**

- **Bảo mật & Định tuyến biên (Edge Layer):** Yêu cầu từ người dùng đi qua Amazon Route 53 (quản lý DNS) kết hợp AWS WAF để sàng lọc các luồng truy cập độc hại.
- **Phân phối nội dung (Content Delivery):** Amazon CloudFront đóng vai trò CDN, truy xuất và cache các nội dung tĩnh từ Amazon S3 (ảnh flashcard, thư mục /wwwroot).
- **Mạng & Cân bằng tải (Public Subnets):** Mạng công cộng (10.0.1.0/24 và 10.0.2.0/24) chứa Application Load Balancer (ALB) tiếp nhận traffic API động từ Internet Gateway, và NAT Gateways hỗ trợ các máy chủ bên trong đi ra Internet.
- **Xử lý nghiệp vụ & Dữ liệu (Private Subnets):**
  - Máy chủ EC2 (t4g.micro ARM64) xử lý logic Backend, đặt trong Private Subnets (10.0.3.0/24 và 10.0.4.0/24), chỉ nhận traffic từ ALB.
  - AWS RDS PostgreSQL lưu trữ dữ liệu nghiệp vụ với cơ chế Synchronous Replication giữa 2 AZ, đảm bảo không mất dữ liệu khi một AZ gặp sự cố.
- **Tự động hóa & AI tích hợp (Serverless):**
  - EC2 gọi API nội bộ tới Amazon Polly để cung cấp tính năng Text-to-Speech.
  - Amazon EventBridge hoạt động như Cron Scheduler, tự động kích hoạt AWS Lambda xử lý các tác vụ nền.
  - AWS Lambda gửi email thông báo định kỳ qua Amazon SES.

---

## 5. Lộ trình triển khai

| Tuần | Nội dung |
|------|----------|
| Tuần 1 | Xây dựng VPC, chia Public/Private Subnets, thiết lập Route 53, WAF và Internet Gateway |
| Tuần 2 | Khởi chạy EC2 ARM64 trong Private Subnet, thiết lập ALB và NAT Gateway |
| Tuần 3 | Khởi tạo RDS PostgreSQL Multi-AZ, tạo S3 bucket và cấu hình CloudFront OAC |
| Tuần 4 | Triển khai luồng EventBridge → Lambda → SES, tích hợp Amazon Polly vào Backend |
| Tuần 5 | Kiểm thử chịu tải, kiểm thử WAF, hoàn thiện hệ thống và xuất báo cáo kiến trúc |

---

## 6. Ngân sách dự kiến

Triển khai tại khu vực Singapore (ap-southeast-1) theo hình thức On-Demand:

| Dịch vụ | Chi phí ước tính |
|---------|-----------------|
| NAT Gateway (x2) | ~$65.70 / tháng |
| Application Load Balancer | ~$16.42 / tháng |
| Amazon RDS PostgreSQL (Multi-AZ) | ~$46.40 / tháng |
| Amazon EC2 (t4g.micro x2) | ~$12.26 / tháng |
| S3, CloudFront, Route 53, WAF | ~$10.00 / tháng |
| Polly, Lambda, EventBridge, SES | ~$2.00 / tháng |
| **Tổng** | **~$152.78 / tháng** |

---

## 7. Rủi ro & Khắc phục

| Rủi ro | Mức độ | Giải pháp |
|--------|--------|-----------|
| Quá tải chi phí NAT Gateway | Cao | Dùng 1 NAT Gateway hoặc đưa EC2 ra Public Subnet trong giai đoạn Dev/Test |
| Mất kết nối từ ALB đến EC2 | Trung bình | Rà soát Security Group: EC2 chỉ nhận Inbound từ Security Group của ALB |
| Lỗi phân giải luồng tĩnh/động ở CloudFront | Trung bình | Cấu hình Behavior rõ ràng: `/api/*` bypass cache về ALB, `/wwwroot/*` truy xuất S3 |
