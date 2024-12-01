---
title : "Overall"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
---
# Deploying Event-Driven Architecture

### Overall
**Event-driven architecture (EDA)** is a modern architecture pattern built from small, decoupled services that publish, consume, or route events.

Unlike traditional request-driven models, EDA promotes loose coupling between producer and consumer services. This makes it easier to scale, update, and independently deploy separate components of a system.

![ConnectPrivate](/images/architect.png) 

### Content
 1. [Introduction ](1-Introduce/)
 2. [Preparation](2-Prerequiste/)
 3. [Create SQS queue](3-sqs/)
 4. [Create SNS topic](4-sns/)
 5. [Create Lambda function](5-lambda/)
 6. [Create an event notification in S3](6-createnotis3/)
 7. [Trigger Lambda function in SQS](7-triggerlambda/)
 8. [Check result](8-checkresult/)
 9. [Clean up](9-cleanup/)
