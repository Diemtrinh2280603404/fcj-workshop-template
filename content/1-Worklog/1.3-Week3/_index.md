---
title: "Week 3 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---
### Week 3 Objectives:

* Master EC2 architecture, load balancing mechanisms and automatic resource scaling strategies.
* Gain a clear understanding of modern data storage service models and database migration solutions to AWS.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study EC2 architecture:<br>&nbsp;&nbsp;+ Classify Instance types by workload<br>&nbsp;&nbsp;+ Components: AMI, VPC, Security Group, EBS<br>&nbsp;&nbsp;+ Remote access: SSH, EC2 Connect, Session Manager | 05/03/2026 | 05/06/2026 | [Amazon EC2 Documentation](https://docs.aws.amazon.com/ec2/) |
| 3   | - Explore Elastic Load Balancing (ELB) and Auto Scaling:<br>&nbsp;&nbsp;+ Application Load Balancer (ALB)<br>&nbsp;&nbsp;+ Auto Scaling Group and Scaling Policy | 05/06/2026 | 05/08/2026 | [Elastic Load Balancing](https://aws.amazon.com/vi/elasticloadbalancing/) / [Auto Scaling](https://aws.amazon.com/vi/autoscaling/) |
| 4   | - Discover Container and Serverless on AWS:<br>&nbsp;&nbsp;+ Container: ECS, EKS<br>&nbsp;&nbsp;+ Serverless: AWS Lambda, Fargate | 05/08/2026 | 05/09/2026 | [Amazon ECS](https://aws.amazon.com/ecs/) / [AWS Lambda](https://aws.amazon.com/lambda/) |
| 5   | - Explore AWS database catalog:<br>&nbsp;&nbsp;+ SQL: RDS (MySQL, PostgreSQL), Aurora<br>&nbsp;&nbsp;+ NoSQL: DynamoDB<br>&nbsp;&nbsp;+ In-memory: MemoryDB | 05/09/2026 | 05/10/2026 | [Amazon RDS](https://aws.amazon.com/rds/) / [Amazon DynamoDB](https://aws.amazon.com/dynamodb/) |
| 6   | - Data migration strategy (6Rs):<br>&nbsp;&nbsp;+ Tools: DMS, SCT, Snow Family, DataSync<br>&nbsp;&nbsp;+ Select the appropriate solution per scenario | 05/10/2026 | 05/10/2026 | [AWS Database Migration Service](https://aws.amazon.com/dms/) / [AWS Snow Family](https://aws.amazon.com/snowball/) |

### Week 3 Achievements:

* Classified EC2 architecture in detail by workload and understood all key setup components:
  * AMI, VPC, Security Group, EBS
  * Remote access methods: SSH Key Pair, EC2 Instance Connect, Session Manager

* Understood load balancing and automatic resource scaling mechanisms:
  * Application Load Balancer (ALB) – path/host-based routing
  * Scaling Policies: Target Tracking, Step Scaling, Scheduled Scaling
  * Combined ELB with Auto Scaling Group to ensure high availability

* Clearly distinguished Container and Serverless models on AWS:
  * ECS (EC2 launch type) vs EKS (Kubernetes)
  * Fargate – serverless containers, no server management required
  * AWS Lambda – event-driven, billed per invocation and execution duration

* Correctly classified and selected database services based on requirements:
  * SQL: RDS (MySQL, PostgreSQL), Aurora (high performance)
  * NoSQL: DynamoDB (key-value, document, low latency)
  * In-memory: MemoryDB (Redis-compatible, durable)

* Mastered the 6 migration strategies (6Rs) and the role of each tool:
  * AWS DMS – online database migration
  * AWS SCT – automatic schema conversion between different engines
  * Snow Family – offline large-scale data migration (TB to PB)
  * DataSync – continuous and automated file storage synchronization
