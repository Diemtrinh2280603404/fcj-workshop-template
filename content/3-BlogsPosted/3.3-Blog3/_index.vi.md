---
title: "Blog 3"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# XÂY DỰNG DATA LAKE VỚI AMAZON S3 VÀ AMAZON ATHENA

Data Lake là một kiến trúc lưu trữ tập trung cho phép chứa dữ liệu thô ở mọi định dạng – có cấu trúc, bán cấu trúc hoặc phi cấu trúc – cho đến khi cần sử dụng. Trên AWS, kiến trúc này có thể được triển khai hiệu quả với Amazon S3 làm tầng lưu trữ, AWS Glue để quản lý Metadata và Amazon Athena để truy vấn dữ liệu bằng SQL mà không cần quản lý bất kỳ hạ tầng nào.

<div style="display:flex; justify-content:center;">
  <img src="/images/blogs/blog3.png" alt="Blog 3" style="width:80%; margin:8px 0;">
</div>

### Những điểm chính cần biết

- Amazon S3 là nền tảng lưu trữ của Data Lake: S3 cung cấp khả năng lưu trữ với chi phí thấp, độ bền cao và khả năng mở rộng gần như không giới hạn, phù hợp để chứa dữ liệu thô từ nhiều nguồn khác nhau như ứng dụng, thiết bị IoT, log hệ thống hoặc dữ liệu streaming.
- AWS Glue quản lý Metadata thông qua Data Catalog: Glue Crawler tự động quét dữ liệu trong S3, nhận diện Schema và đăng ký thông tin vào Glue Data Catalog, giúp các dịch vụ như Athena có thể hiểu và truy vấn dữ liệu một cách chính xác.
- Amazon Athena cho phép truy vấn SQL trực tiếp trên S3: Athena là dịch vụ truy vấn Serverless, sử dụng Presto Engine để thực thi câu lệnh SQL trên dữ liệu lưu trữ trong S3 mà không cần tải dữ liệu vào cơ sở dữ liệu riêng biệt, chỉ tính phí theo lượng dữ liệu được quét.
- Phân vùng dữ liệu giúp tối ưu hiệu suất và chi phí: Tổ chức dữ liệu theo cấu trúc phân vùng (ví dụ: theo năm, tháng, ngày) trong S3 giúp Athena chỉ quét đúng phần dữ liệu cần thiết, từ đó giảm thời gian truy vấn và chi phí đáng kể.
- Định dạng dữ liệu tối ưu hóa tốc độ truy vấn: Sử dụng các định dạng lưu trữ dạng cột như Parquet hoặc ORC thay vì CSV hoặc JSON giúp cải thiện đáng kể hiệu suất đọc và giảm lượng dữ liệu cần quét khi truy vấn.
- Kiến trúc hoàn toàn Serverless và tích hợp linh hoạt: Toàn bộ luồng xử lý từ thu thập, lưu trữ đến truy vấn đều không cần quản lý máy chủ, đồng thời dễ dàng tích hợp với Amazon QuickSight để trực quan hóa dữ liệu hoặc Amazon SageMaker cho các bài toán Machine Learning.

Kiến trúc Data Lake trên AWS với S3, Glue và Athena đặc biệt phù hợp với các tổ chức cần xây dựng nền tảng phân tích dữ liệu với chi phí tối ưu, khả năng mở rộng cao và không muốn đầu tư vào hạ tầng phức tạp. Đây cũng là nền tảng lý tưởng để phát triển các ứng dụng phân tích nâng cao, Business Intelligence hoặc các mô hình Machine Learning trong tương lai.

[Xem bài đăng trên AWS Study Group](https://web.facebook.com/share/p/1Bn86KFzSx/)

---

### Nguồn tham khảo

- [Amazon Athena – AWS Documentation](https://docs.aws.amazon.com/athena/latest/ug/what-is.html)
- [AWS Glue – AWS Documentation](https://docs.aws.amazon.com/glue/latest/dg/what-is-glue.html)
- [Data Lakes and Analytics on AWS](https://aws.amazon.com/big-data/datalakes-and-analytics/)
