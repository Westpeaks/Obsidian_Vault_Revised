
- This suite of micro services is what handles massaging and queuing in AWS. 

## Tightly Coupled vs. Loosely Coupled Architecture

- In tightly coupled architecture models, components work in a series and are dependent on one another. If a service fails in the chain, the systems fails as a result. 
- Loosely couple systems part of this issue. If a component within the system fails, the other components can operate independently. 

## EventBridge

- EventBridge is a serverless service that helps connect different parts of an application using events, helping to build scalable, event-driven systems. With EventBridge, you route events from sources like custom apps, AWS services, and third-party software to other applications.

### Amazon SQS

- Amazon SQS is a message queuing service that facilitates reliable communication between software components. It can send, store, and receive messages at any scale, making sure messages are not lost and that other services don't need to be available for processing. In Amazon SQS, an application places messages into a queue, and a user or service retrieves the message, processes it, and then removes it from the queue.

## Amazon SNS 

Amazon SNS is a publish-subscribe service that publishers use to send messages to subscribers through SNS topics. In Amazon SNS, subscribers can include web servers, email addresses, Lambda functions, and various other endpoints.

## Links:

[[Amazon Elastic Load Balancing]]

[[Amazon EC2]]

2025111855