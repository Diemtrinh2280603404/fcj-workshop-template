---
title: "Week 10 Worklog"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.10. </b> "
---
### Week 10 Objectives:

* Optimize FlashLearn system performance through caching, automated image processing and comprehensive API testing.
* Develop a smart learning recommendation feature based on user history.
* Set up a monitoring and performance tracking system for the application on AWS.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Team meeting to plan performance optimization:<br>&nbsp;&nbsp;+ Optimize RDS PostgreSQL queries (add Indexes)<br>&nbsp;&nbsp;+ Configure CloudFront caching with appropriate TTL | 06/21/2026 | 06/22/2026 | |
| 3   | - Hands-on automated image processing with Lambda:<br>&nbsp;&nbsp;+ Lambda auto-triggers on S3 image upload<br>&nbsp;&nbsp;+ Resize images to standard sizes (thumbnail, medium, large)<br>&nbsp;&nbsp;+ Compress to WebP format to reduce storage | 06/22/2026 | 06/23/2026 | [CloudJourney AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| 4   | - Comprehensive API testing with Postman:<br>&nbsp;&nbsp;+ Test all CRUD methods via API Gateway<br>&nbsp;&nbsp;+ Verify CORS configuration for frontend<br>&nbsp;&nbsp;+ Validate IAM Authorization | 06/23/2026 | 06/24/2026 | |
| 5   | - Team meeting to develop smart learning recommendation:<br>&nbsp;&nbsp;+ Algorithm based on study history (frequency, correct/incorrect ratio)<br>&nbsp;&nbsp;+ Data flow: Lambda reads Progress table → compute → return prioritized list | 06/24/2026 | 06/26/2026 | |
| 6   | - Set up monitoring system on AWS:<br>&nbsp;&nbsp;+ CloudWatch Dashboard: CPU, Memory, Network of EC2 (ARM64)<br>&nbsp;&nbsp;+ CloudWatch Alarms when RDS CPU > 80%<br>&nbsp;&nbsp;+ AWS X-Ray to trace internal API calls and identify bottlenecks | 06/26/2026 | 06/28/2026 | [CloudJourney AWS Study Group](https://cloudjourney.awsstudygroup.com/) |

### Week 10 Achievements:

* Successfully optimized RDS PostgreSQL query performance and CloudFront caching:
  * Added indexes on frequently queried columns (user_id, deck_id, created_at)
  * Configured CloudFront Cache Policy with appropriate TTL for each type of static content
  * Reduced average response time for complex queries

* Successfully deployed an automated image processing pipeline with Lambda:
  * Lambda auto-triggers when images are uploaded to S3
  * Resizes images to standard dimensions (thumbnail, medium, large) and compresses to WebP format
  * Stores image versions in separate S3 prefixes, significantly reducing storage consumption

* Completed comprehensive API testing with Postman:
  * Verified all CRUD methods (GET, POST, PUT, DELETE) via API Gateway
  * Confirmed CORS configuration works correctly for the frontend
  * Validated IAM authorization ensuring only permitted roles can invoke APIs

* Developed and finalized the smart learning recommendation feature:
  * Built a recommendation algorithm based on learning history (review frequency, correct/incorrect ratio, study time)
  * Designed data flow: Lambda reads Progress table → computes → returns prioritized vocabulary list

* Established a comprehensive monitoring system on AWS:
  * CloudWatch Dashboard tracking CPU, Memory and Network of EC2 (ARM64)
  * CloudWatch Alarms triggered when RDS CPU > 80% or connections exceed threshold
  * AWS X-Ray tracing internal API calls to identify bottlenecks in the processing flow
