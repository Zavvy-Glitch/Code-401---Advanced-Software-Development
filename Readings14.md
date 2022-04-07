# AWS: SNS & SQS
  - What is SNS?
    - Simple Notification Service
    - Publish / Subscriber System
    - Publishing messages to a topic
      - Can be delivered to many subscribers(can be various types)
        - SQS
        - Lambda
        - Email 
  
  - What is SQS?
    - Simple Queue Service
    - Queueing service for message processing
    - System must poll the queue to find new events
    - Typically processed by a single consumer

When should you use SNS?
  - If other systems care about an event

When should you use SQS?
  - If your system cares about an event

## Practical Example
  ### SNS
  - Credit Card Transactions
    - Flow: 
      - Purchase
      - Transaction Processing Web Service
      - Credit Card Authority Service (verification)
      - Transaction SNS Topic
        - Customer Reminder Service -> Customer Email
        - Transaction Analytics Queue <-> Transaction Analytics Service (EC2)
        - Transaction Fraud Detection Service Queue -> Transaction Fraud Detection Service (EC2)
