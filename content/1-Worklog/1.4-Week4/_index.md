---
title: "Week 4 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---
### Week 4 Objectives:

* Analyze and compile documentation on database migration solutions on the AWS platform.
* Study in detail and systematize knowledge of AWS networking infrastructure, security, and content delivery services.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Identify objectives and analyze barriers in database migration:<br>&nbsp;&nbsp;+ Schema compatibility between different engines<br>&nbsp;&nbsp;+ Minimize downtime during migration | 05/10/2026 | 05/14/2026 | [AWS Database Migration Service](https://aws.amazon.com/dms/) |
| 3   | - Explore the AWS migration toolset:<br>&nbsp;&nbsp;+ DMS, SCT<br>&nbsp;&nbsp;+ Snow Family, DataSync<br>&nbsp;&nbsp;+ Real-world applicable scenarios | 05/14/2026 | 05/15/2026 | [AWS Database Migration Service](https://aws.amazon.com/dms/) |
| 4   | - 4-stage data migration workflow:<br>&nbsp;&nbsp;+ Assessment – evaluate data source and risks<br>&nbsp;&nbsp;+ Preparation – set up target environment<br>&nbsp;&nbsp;+ Execution – full load + CDC<br>&nbsp;&nbsp;+ Validation & Optimization | 05/15/2026 | 05/16/2026 | [Database Migration Strategies](https://aws.amazon.com/products/databases/) |
| 5   | - Study AWS VPC network architecture:<br>&nbsp;&nbsp;+ Subnet, Route Table, Internet/NAT Gateway<br>&nbsp;&nbsp;+ Security Group and Network ACL<br>&nbsp;&nbsp;+ PrivateLink, VPN Site-to-Site, Direct Connect | 05/16/2026 | 05/17/2026 | [Amazon VPC Connectivity Options](https://docs.aws.amazon.com/whitepapers/latest/aws-vpc-connectivity-options/introduction.html) |
| 6   | - Consolidate Route 53 and CloudFront functionalities:<br>&nbsp;&nbsp;+ Route 53: DNS routing, Weighted, Latency-based, Failover<br>&nbsp;&nbsp;+ CloudFront: CDN, Edge Location, WAF + Shield integration | 05/17/2026 | 05/17/2026 | [Amazon Route 53](https://aws.amazon.com/route53/) / [Amazon CloudFront](https://aws.amazon.com/cloudfront/) |

### Week 4 Achievements:

* Identified common barriers in database migration and selected appropriate strategies:
  * Schema compatibility between different database engines
  * Minimizing downtime during the migration process
  * Ensuring data integrity and performance after migration

* Gained a clear understanding of the AWS Migration toolset workflows:
  * DMS: replication instance → source/target endpoints → migration tasks (full load + CDC)
  * SCT: automatic schema analysis and conversion between different engines
  * Snow Family: Snowcone (TB), Snowball Edge (PB), Snowmobile (Exabyte)
  * DataSync: continuous file storage synchronization between on-premises and AWS

* Mastered the complete 4-stage data migration workflow:
  * Assessment – evaluate the data source and identify risks
  * Preparation – set up the target environment and tools
  * Execution – perform full load and Change Data Capture (CDC)
  * Validation & Optimization – verify data correctness and optimize performance

* Understood VPC network architecture and security components:
  * Subnet (Public/Private), Route Table, Internet Gateway, NAT Gateway
  * Security Group (stateful) vs Network ACL (stateless)
  * Private connectivity options: PrivateLink (within AWS), Site-to-Site VPN (over internet), Direct Connect (dedicated physical line)

* Distinguished the functions and use cases of Route 53 and CloudFront:
  * Route 53: DNS routing with policies – Simple, Weighted, Latency-based, Failover, Geolocation
  * CloudFront: CDN caching at Edge Locations, integrated with WAF and Shield to protect applications against DDoS
