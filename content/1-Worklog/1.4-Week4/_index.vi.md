---
title: "Worklog Tuần 4"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---
### Mục tiêu tuần 4:

* Phân tích và tổng hợp tài liệu về các giải pháp di chuyển cơ sở dữ liệu trên nền tảng AWS.
* Tìm hiểu chi tiết và hệ thống hóa kiến thức về các dịch vụ hạ tầng mạng, bảo mật và phân phối nội dung của AWS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --------- | ------------ | --------------- | ------------------- |
| 2   | - Xác định mục tiêu và phân tích rào cản di chuyển cơ sở dữ liệu:<br>&nbsp;&nbsp;+ Tương thích schema giữa các engine khác nhau<br>&nbsp;&nbsp;+ Giảm thiểu downtime trong quá trình migration | 10/05/2026 | 14/05/2026 | [AWS Database Migration Service](https://aws.amazon.com/dms/) |
| 3   | - Tìm hiểu bộ công cụ AWS Migration:<br>&nbsp;&nbsp;+ DMS, SCT<br>&nbsp;&nbsp;+ Snow Family, DataSync<br>&nbsp;&nbsp;+ Các kịch bản áp dụng thực tế | 14/05/2026 | 15/05/2026 | [AWS Database Migration Service](https://aws.amazon.com/dms/) |
| 4   | - Quy trình di chuyển dữ liệu 4 giai đoạn:<br>&nbsp;&nbsp;+ Assessment – đánh giá nguồn dữ liệu và rủi ro<br>&nbsp;&nbsp;+ Preparation – chuẩn bị môi trường đích<br>&nbsp;&nbsp;+ Execution – thực thi full load + CDC<br>&nbsp;&nbsp;+ Validation & Optimization – kiểm chứng và tối ưu | 15/05/2026 | 16/05/2026 | [Database Migration Strategies](https://aws.amazon.com/products/databases/) |
| 5   | - Nghiên cứu cấu trúc mạng AWS VPC:<br>&nbsp;&nbsp;+ Subnet, Route Table, Internet/NAT Gateway<br>&nbsp;&nbsp;+ Security Group và Network ACL<br>&nbsp;&nbsp;+ PrivateLink, VPN Site-to-Site, Direct Connect | 16/05/2026 | 17/05/2026 | [Amazon VPC Connectivity Options](https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/introduction.html) |
| 6   | - Tổng hợp chức năng Route 53 và CloudFront:<br>&nbsp;&nbsp;+ Route 53: DNS routing, Weighted, Latency-based, Failover<br>&nbsp;&nbsp;+ CloudFront: CDN, Edge Location, tích hợp WAF + Shield | 17/05/2026 | 17/05/2026 | [Amazon Route 53](https://aws.amazon.com/route53/) / [Amazon CloudFront](https://aws.amazon.com/cloudfront/) |

### Thành tích tuần 4:

* Xác định được các rào cản phổ biến trong di chuyển cơ sở dữ liệu và lựa chọn chiến lược phù hợp:
  * Tương thích schema giữa các database engine khác nhau
  * Giảm thiểu downtime trong quá trình migration
  * Đảm bảo hiệu năng và tính toàn vẹn dữ liệu sau khi chuyển đổi

* Nắm rõ luồng hoạt động của bộ công cụ AWS Migration:
  * DMS: replication instance → source/target endpoints → migration tasks (full load + CDC)
  * SCT: phân tích và chuyển đổi schema tự động giữa các engine khác nhau
  * Snow Family: Snowcone (TB), Snowball Edge (PB), Snowmobile (Exabyte)
  * DataSync: đồng bộ file storage liên tục giữa on-premises và AWS

* Nắm vững quy trình di chuyển dữ liệu gồm 4 giai đoạn:
  * Assessment – đánh giá nguồn dữ liệu và rủi ro
  * Preparation – chuẩn bị môi trường đích và công cụ
  * Execution – thực thi full load và Change Data Capture (CDC)
  * Validation & Optimization – kiểm chứng tính đúng đắn và tối ưu hiệu năng

* Hiểu kiến trúc mạng VPC và các thành phần bảo mật:
  * Subnet (Public/Private), Route Table, Internet Gateway, NAT Gateway
  * Security Group (stateful) vs Network ACL (stateless)
  * Kết nối riêng tư: PrivateLink (nội bộ AWS), VPN Site-to-Site (qua internet), Direct Connect (đường truyền vật lý)

* Phân biệt chức năng và trường hợp sử dụng của Route 53 và CloudFront:
  * Route 53: DNS routing với các policy – Simple, Weighted, Latency-based, Failover, Geolocation
  * CloudFront: CDN cache tại Edge Location, tích hợp WAF và Shield để bảo vệ ứng dụng khỏi DDoS
