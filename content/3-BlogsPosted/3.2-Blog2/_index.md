---
title: "Blog 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

# EVENT-DRIVEN ARCHITECTURE ON AWS: EVENTBRIDGE, SNS AND SQS IN SERVERLESS SYSTEMS

Event-Driven Architecture is a system design pattern in which components communicate with each other through Events rather than direct REST API calls. On AWS, this architecture can be effectively implemented using services such as Amazon API Gateway, AWS Lambda, Amazon EventBridge, Amazon SNS and Amazon SQS, helping reduce dependencies between services, increase scalability and improve system stability when handling asynchronous processing.

<div style="display:flex; justify-content:center;">
  <img src="/images/blogs/blog2.png" alt="Blog 2" style="width:80%; margin:8px 0;">
</div>

### Key points to know

- Producers only emit Events: After processing business logic, AWS Lambda sends Events to Amazon EventBridge instead of calling other services directly, reducing coupling between system components.
- Amazon EventBridge is responsible for routing Events: EventBridge receives, filters and forwards Events according to configured Rules, while also supporting event transmission across multiple AWS Accounts.
- Amazon SNS implements the Publish/Subscribe mechanism: A single Event can be distributed simultaneously to multiple Subscribers such as AWS Lambda, Amazon SQS, HTTP Endpoints or Email without modifying the Producer.
- Amazon SQS ensures asynchronous processing: SQS acts as a Queue, temporarily storing Events, absorbing traffic spikes, supporting Retry and Dead Letter Queue (DLQ) to minimize data loss when Consumers encounter errors.
- Architecture is easy to scale: When adding new functions such as email notifications, Audit Logs, Data Lake or Machine Learning, simply register a new Consumer to receive Events without affecting existing components.
- Cost optimization and scalability: Using Serverless services such as API Gateway, Lambda, EventBridge, SNS and SQS allows the system to automatically scale with traffic and only incurs costs when there are processing requests.

This architecture is particularly well-suited for Microservices systems, asynchronous processing, multi-system integration, or multi-account AWS environments where high scalability, reduced inter-service dependencies and improved fault tolerance are required.

[View post on AWS Study Group](https://www.facebook.com/share/p/19BpYphs7p/)

---

### References

- [Amazon EventBridge – AWS Documentation](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-what-is.html)
- [Amazon SNS – AWS Documentation](https://docs.aws.amazon.com/sns/latest/dg/welcome.html)
- [Amazon SQS – AWS Documentation](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/welcome.html)
