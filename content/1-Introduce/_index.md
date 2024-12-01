---
title : "Introduction"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
### Amazon S3
**Amazon Simple Storage Service (Amazon S3)** is an object storage service offering industry-leading scalability, data availability, security, and performance. It is designed for large-capacity, low-cost storage provision across multiple geographical regions. Amazon S3 provides developers and IT teams with secure, durable and highly scalable object storage.

### Amazon SNS
**Amazon Simple Notification Service (Amazon SNS)** is a web service that coordinates and manages the delivery or sending of messages to subscribing endpoints or clients.

### Amazon SQS
**Amazon Simple Queue Service (Amazon SQS)** offers a secure, durable, and available hosted queue that lets you send, store, and receive messages between software components at any volume, without losing messages or requiring other services to be available.

### AWS Lambda
**AWS Lambda** is a compute service that runs your code in response to events and automatically manages the compute resources, making it the fastest way to turn an idea into a modern, production, serverless applications.

### Benefits of This Architecture:
- Scalability: The use of serverless components ensures automatic scaling to handle varying workloads.
- Decoupling: SNS and SQS enable loose coupling between components, improving the system's flexibility and maintainability.
- Reliability: SQS provides reliable message delivery and retry mechanisms, ensuring no messages are lost.
- Cost-Effectiveness: Serverless services like S3 and Lambda are billed based on usage, minimizing costs for low workloads.