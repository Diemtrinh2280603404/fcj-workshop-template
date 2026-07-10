---
title: "Week 9 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.9. </b> "
---
### Week 9 Objectives:

* Build the FlashLearn system – a web application supporting English learning through flashcards, quizzes, battles and a learning community.
* Deploy a modern system architecture on AWS (Singapore Region) with a VPC structure across two Availability Zones to ensure high availability.
* Optimize application performance by combining the Serverless model with managed services such as Amazon CloudFront, Lambda and EventBridge.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Team meeting to kick off FlashLearn project:<br>&nbsp;&nbsp;+ Finalize PostgreSQL database Schema design<br>&nbsp;&nbsp;+ Collect and normalize English vocabulary dataset | 06/14/2026 | 06/15/2026 | |
| 3   | - Deploy multi-AZ VPC network architecture:<br>&nbsp;&nbsp;+ VPC with 2 Public Subnets and 2 Private Subnets<br>&nbsp;&nbsp;+ Configure IAM Role for EC2 with least privilege<br>&nbsp;&nbsp;+ Set up layered Security Groups per application tier | 06/15/2026 | 06/16/2026 | [CloudJourney AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| 4   | - Configure ALB and distribute static content:<br>&nbsp;&nbsp;+ ALB routing traffic to EC2 instances by health check<br>&nbsp;&nbsp;+ Upload static assets to S3<br>&nbsp;&nbsp;+ Integrate CloudFront CDN | 06/16/2026 | 06/18/2026 | [CloudJourney AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| 5   | - Team Meeting: Review UI/UX design on Figma:<br>&nbsp;&nbsp;+ Review flashcard, quiz and battle screens<br>&nbsp;&nbsp;+ Optimize user experience flow based on feedback | 06/18/2026 | 06/19/2026 | |
| 6   | - Build automated notification system and pronunciation feature:<br>&nbsp;&nbsp;+ EventBridge rule triggers Lambda to send learning reminders<br>&nbsp;&nbsp;+ Integrate Amazon Polly to convert text to speech for vocabulary | 06/19/2026 | 06/21/2026 | [CloudJourney AWS Study Group](https://cloudjourney.awsstudygroup.com/) |

### Week 9 Achievements:

* Completed the PostgreSQL database Schema design for the FlashLearn system:
  * Defined core tables: Users, Flashcards, Decks, Quiz, Battle, Progress
  * Established foreign key relationships and indexes to optimize query performance
  * Collected and normalized an English vocabulary dataset

* Successfully deployed a high-availability multi-zone VPC architecture on AWS Singapore:
  * VPC with 2 Public Subnets and 2 Private Subnets across 2 Availability Zones
  * Configured IAM Roles for EC2 following the principle of least privilege
  * Set up layered Security Groups for each application tier

* Configured Application Load Balancer and distributed static content:
  * ALB routing traffic to EC2 instances based on health checks
  * Uploaded and configured S3 bucket for static asset storage
  * Integrated CloudFront CDN to deliver content with low latency globally

* Optimized user experience through Team Meeting with Figma:
  * Reviewed and improved UI/UX for flashcard, quiz and battle screens
  * Adjusted user flows based on team feedback

* Successfully built an automated notification system and pronunciation feature:
  * EventBridge rule triggers Lambda on schedule to send learning reminders
  * Integrated Amazon Polly to convert vocabulary text to speech
  * Lambda processes events and stores results in S3
