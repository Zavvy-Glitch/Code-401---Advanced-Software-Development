# AWS: Events (SNS & SQS)

## SNS (Simple Notification Service)
  What is SNS?
  - a distributed publish-subscribe service
  - a fast, flexible, fully managed push notification service
  - lets you send individual messages or bulk messages to large numbers of recipients
  - simple and cost effective ability to send push notifications to mobile users / email / or other distributed services

## SQS (Simple Queue Service)
  What is SQS?
  - a distributed queuing service
  - a fully managed service that enables you to decouple and scale:
    - microservices
    - distributed systems
    - serverless applications
  - it allows receivers to poll to S!S to receive messages rather than have messages pushed directly
  - it allows messages to be stored for a short duration (max: 14 d ays)
  - it allows messages to be separated. Messages can't be received by multiple receivers at the same time.

### Use Cases:
  ### SNS:
   - if you need the ability to publish and consume batches of messages
   - if you need the same message to be processed down multiple avenues
   - if you need multiple subscribers

  ### SQS:
   - if you need a simple queue without additional requirements
   - if you need to decouple two applications and allow parallel asynchronous processing
   - if you only need one single subscriber

### Key Differences

|-----| SQS | SNS |
|-----|-----|-----|
|Entity Type: | Queue (similar to JMS, MSMQ). | Topic-Subscriber (Pub/Sub system). |
| Message consumption: | Pull Mechanism — Consumers poll messages from SQS. | Push Mechanism — SNS pushes messages to consumers. |
| Persistence: | Messages are persisted for some duration is no consumer available. The retention period value is from 1 minute to 14 days. The default is 4 days. | No persistence. Whichever consumer is present at the time of message arrival, get the message and the message is deleted. If no consumers available then the message is lost. In SQS the message delivery is guaranteed but in SNS it is not. |
| Consumer Type: | All the consumers are supposed to be identical and hence process the messages in exact same way. | All the consumers are (supposed to be) processing the messages in different ways. |
