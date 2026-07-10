---
title: "Blog 3"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

# BUILDING A DATA LAKE WITH AMAZON S3 AND AMAZON ATHENA

A Data Lake is a centralized storage architecture that can hold raw data in any format — structured, semi-structured or unstructured — until it is needed. On AWS, this architecture can be effectively implemented with Amazon S3 as the storage layer, AWS Glue to manage Metadata, and Amazon Athena to query data using SQL without managing any infrastructure.

<div style="display:flex; justify-content:center;">
  <img src="/images/blogs/blog3.png" alt="Blog 3" style="width:80%; margin:8px 0;">
</div>

### Key points to know

- Amazon S3 is the foundation of the Data Lake: S3 provides low-cost, highly durable and nearly unlimited scalable storage, suitable for holding raw data from various sources such as applications, IoT devices, system logs or streaming data.
- AWS Glue manages Metadata through the Data Catalog: Glue Crawlers automatically scan data in S3, detect schemas and register the information into the Glue Data Catalog, allowing services like Athena to understand and query data accurately.
- Amazon Athena enables direct SQL queries on S3: Athena is a Serverless query service that uses the Presto Engine to execute SQL statements on data stored in S3 without loading data into a separate database, charging only for the amount of data scanned.
- Data partitioning optimizes performance and cost: Organizing data with a partition structure (e.g., by year, month, day) in S3 allows Athena to scan only the necessary data, significantly reducing query time and cost.
- Optimized data formats improve query speed: Using columnar storage formats such as Parquet or ORC instead of CSV or JSON significantly improves read performance and reduces the amount of data scanned during queries.
- Fully Serverless architecture with flexible integration: The entire pipeline from collection, storage to querying requires no server management, and easily integrates with Amazon QuickSight for data visualization or Amazon SageMaker for Machine Learning workloads.

The Data Lake architecture on AWS with S3, Glue and Athena is particularly well-suited for organizations that need to build a data analytics platform with optimized costs, high scalability and no desire to invest in complex infrastructure. It also serves as an ideal foundation for developing advanced analytics applications, Business Intelligence or Machine Learning models in the future.

[View post on AWS Study Group](https://web.facebook.com/share/p/1Bn86KFzSx/)

---

### References

- [Amazon Athena – AWS Documentation](https://docs.aws.amazon.com/athena/latest/ug/what-is.html)
- [AWS Glue – AWS Documentation](https://docs.aws.amazon.com/glue/latest/dg/what-is-glue.html)
- [Data Lakes and Analytics on AWS](https://aws.amazon.com/big-data/datalakes-and-analytics/)
