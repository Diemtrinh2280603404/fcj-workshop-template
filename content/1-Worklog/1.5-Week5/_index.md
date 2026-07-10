---
title: "Week 5 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---
### Week 5 Objectives:

* Master diverse AWS storage solutions and data lifecycle management workflows.
* Proficiently apply AI/ML services, data analytics tools, and system integration in hands-on practice exercises.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study AWS storage options:<br>&nbsp;&nbsp;+ Object Storage: S3<br>&nbsp;&nbsp;+ Block Storage: EBS<br>&nbsp;&nbsp;+ File Storage: EFS<br>&nbsp;&nbsp;+ In-memory: ElastiCache<br>- Study data lifecycle and backup management workflows | 05/17/2026 | 05/20/2026 | [S3 Documentation](https://docs.aws.amazon.com/s3/) / [EBS Documentation](https://docs.aws.amazon.com/ebs/) / [EFS Documentation](https://docs.aws.amazon.com/efs/) |
| 3   | - Explore the AWS AI/ML ecosystem:<br>&nbsp;&nbsp;+ Built-in AI services<br>&nbsp;&nbsp;+ Machine Learning with SageMaker<br>&nbsp;&nbsp;+ Code assistance with CodeWhisperer<br>- Research the standard ML deployment workflow on AWS | 05/20/2026 | 05/22/2026 | [SageMaker Documentation](https://docs.aws.amazon.com/sagemaker/) / [AWS AI Services](https://aws.amazon.com/ai/services/) |
| 4   | - Discover data analytics services:<br>&nbsp;&nbsp;+ Serverless query: Athena<br>&nbsp;&nbsp;+ Stream processing: Kinesis<br>&nbsp;&nbsp;+ ETL: Glue<br>&nbsp;&nbsp;+ Data warehousing: Redshift<br>&nbsp;&nbsp;+ Visualization: QuickSight | 05/22/2026 | 05/23/2026 | [Athena Documentation](https://docs.aws.amazon.com/athena/) / [Kinesis Documentation](https://docs.aws.amazon.com/kinesis/) / [Redshift Documentation](https://docs.aws.amazon.com/redshift/) |
| 5   | - Study application integration services:<br>&nbsp;&nbsp;+ EventBridge: event routing<br>&nbsp;&nbsp;+ SQS: message queue<br>&nbsp;&nbsp;+ SNS: pub/sub notification<br>- Explore Connect, SES and DevOps tools | 05/23/2026 | 05/24/2026 | [EventBridge Documentation](https://docs.aws.amazon.com/eventbridge/) / [SQS Documentation](https://docs.aws.amazon.com/sqs/) / [SNS Documentation](https://docs.aws.amazon.com/sns/) |
| 6   | - Comprehensive hands-on practice:<br>&nbsp;&nbsp;+ Configure S3 Lifecycle Policy<br>&nbsp;&nbsp;+ Build ML model with SageMaker<br>&nbsp;&nbsp;+ Build data pipeline: Kinesis → Glue → Redshift<br>&nbsp;&nbsp;+ Deploy event-driven system with EventBridge | 05/24/2026 | 05/24/2026 | [AWS Hands-on Guide](https://aws.amazon.com/vi/getting-started/hands-on/) |

### Week 5 Achievements:

* Clearly distinguished the four AWS storage types and their appropriate use cases:
  * Object Storage (S3) – static file storage, backup, data lake
  * Block Storage (EBS) – disk directly attached to EC2, suitable for databases
  * File Storage (EFS) – shared file system across multiple instances simultaneously
  * In-memory (ElastiCache) – data caching, reducing query latency

* Successfully configured S3 Lifecycle Policy to automatically transition data between storage classes (Standard → IA → Glacier) and set up scheduled backups.

* Understood the AWS AI/ML ecosystem and the standard ML deployment workflow:
  * SageMaker – build, train and deploy ML models
  * CodeWhisperer – AI-powered code assistance within the IDE
  * Workflow: data preparation → training → evaluation → endpoint deployment

* Successfully completed hands-on ML model creation with SageMaker:
  * Prepared dataset and uploaded to S3
  * Launched a training job and monitored progress
  * Deployed the model to an endpoint and performed inference

* Mastered data analytics services and the role of each:
  * Athena – serverless SQL queries directly on S3 (pay per data scanned)
  * Kinesis – real-time data stream processing
  * Glue – serverless ETL for data preparation and transformation
  * Redshift – large-scale data warehouse for analytics
  * QuickSight – data visualization and dashboard reporting

* Successfully built a data pipeline connecting Kinesis → Glue → Redshift and deployed an event-driven system using EventBridge:
  * SQS – message queue ensuring sequential processing and no data loss
  * SNS – pub/sub notifications delivered to multiple subscribers
  * EventBridge – automatic event routing between AWS services
