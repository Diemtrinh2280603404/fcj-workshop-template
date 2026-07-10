---
title: "Proposal"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# FlashLearn – Interactive English Learning App on AWS

## 1. Project Overview

FlashLearn is a comprehensive web application supporting interactive English learning (flashcards, quizzes, community). Rather than deploying with a traditional monolithic model, the project focuses on building a modern cloud infrastructure architecture on Amazon Web Services (AWS) in the Asia Pacific (Singapore) region. The architecture strictly follows enterprise standards for distributed systems, multi-layer security, and automation integration.

---

## 2. Objectives

- **High Availability:** Ensure 24/7 system uptime by spreading infrastructure across 2 Availability Zones (Multi-AZ).
- **Deep Security:** Protect the application at the network edge using a Web Application Firewall (WAF) and fully isolate both the compute layer (EC2) and the database (RDS) within Private Subnets.
- **Performance Optimization:** Deliver static content at high speed via a global CDN and offload the server by separating background tasks.
- **Core Feature Extension:** Apply Artificial Intelligence (AI) to support accurate English pronunciation.

---

## 3. Problem Statement

**Problem:** E-learning systems typically store media directly on the server and place the server in a public network zone, creating major security risks (vulnerability to DDoS attacks, data leaks) and bandwidth bottlenecks when many learners access the system simultaneously.

**Solution:** Move S3 and CloudFront to the front line to handle static content. Hide all business logic (EC2) and data (RDS) in the Private layer. All Backend Internet communication must go through a NAT Gateway and be securely distributed via an Application Load Balancer.

---

## 4. Solution Architecture

The system is fully designed inside a VPC (10.0.0.0/16) spanning 2 Availability Zones to ensure fault tolerance.

![FlashLearn Solution Architecture](/images/2-Proposal/architecture.png)

**Component details & processing flow:**

- **Edge Security & Routing (Edge Layer):** User requests first pass through Amazon Route 53 (DNS management) combined with AWS WAF to filter malicious traffic.
- **Content Delivery:** Amazon CloudFront acts as the CDN, retrieving and caching static content from Amazon S3 (flashcard images, /wwwroot directory).
- **Networking & Load Balancing (Public Subnets):** Public networks (10.0.1.0/24 and 10.0.2.0/24) host the Application Load Balancer (ALB) to receive dynamic API traffic from the Internet Gateway, along with NAT Gateways to allow internal servers to access the Internet for updates.
- **Business Logic & Data (Private Subnets):**
  - EC2 instances (t4g.micro ARM64) handle Backend logic, securely placed in Private Subnets (10.0.3.0/24 and 10.0.4.0/24), receiving traffic only from the ALB.
  - AWS RDS PostgreSQL stores business data with Synchronous Replication across 2 AZs, ensuring zero data loss if one data center encounters an issue.
- **Automation & Integrated AI (Serverless):**
  - EC2 makes internal API calls to Amazon Polly to provide Text-to-Speech functionality.
  - Amazon EventBridge acts as a Cron Scheduler, automatically triggering AWS Lambda to process background tasks.
  - AWS Lambda sends periodic notification emails via Amazon SES.

---

## 5. Deployment Timeline

| Week | Content |
|------|---------|
| Week 1 | Build VPC, divide Public/Private Subnets, set up Route 53, WAF and Internet Gateway |
| Week 2 | Launch ARM64 EC2 instances in Private Subnet, set up ALB and NAT Gateway |
| Week 3 | Initialize RDS PostgreSQL Multi-AZ, create S3 bucket and configure CloudFront OAC |
| Week 4 | Deploy EventBridge → Lambda → SES pipeline, integrate Amazon Polly into Backend |
| Week 5 | Load testing, WAF flow testing, finalize system and export architecture report |

---

## 6. Budget Estimate

Deployed in the Singapore region (ap-southeast-1) on On-Demand pricing:

| Service | Estimated Cost |
|---------|---------------|
| NAT Gateway (x2) | ~$65.70 / month |
| Application Load Balancer | ~$16.42 / month |
| Amazon RDS PostgreSQL (Multi-AZ) | ~$46.40 / month |
| Amazon EC2 (t4g.micro x2) | ~$12.26 / month |
| S3, CloudFront, Route 53, WAF | ~$10.00 / month |
| Polly, Lambda, EventBridge, SES | ~$2.00 / month |
| **Total** | **~$152.78 / month** |

---

## 7. Risk Assessment

| Risk | Severity | Mitigation |
|------|----------|------------|
| NAT Gateway cost overrun | High | Use 1 NAT Gateway or move EC2 to Public Subnet during Dev/Test phase |
| ALB to EC2 connectivity loss | Medium | Review Security Groups: EC2 only accepts Inbound from the ALB's Security Group |
| CloudFront static/dynamic routing error | Medium | Configure Behavior clearly: `/api/*` bypasses cache to ALB, `/wwwroot/*` fetches from S3 |
