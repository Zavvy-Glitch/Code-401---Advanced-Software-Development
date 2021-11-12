# AWS: Events (SNS & SQS)

- Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server
  - API Gateway: Amazon’s API Gateway is a fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale. With a few clicks you can create an API that acts as a “front door” for applications to access data, business logic, or functionality from your back-end services, such as workloads running on Amazon Elastic Compute Cloud (Amazon EC2), code running on AWS Lambda, or any Web application. Amazon API Gateway handles all the tasks involved in accepting and processing up to hundreds of thousands of concurrent API calls, including traffic management, authorization and access control, monitoring, and API version management.
  - Express: Express Gateway is an API Gateway that can sit at the heart of any microservices architecture, regardless of what language or platform you’re using. Express Gateway secures your microservices and exposes them through APIs using Node.js, ExpressJS and Express middleware.
- List the AWS Database offerings and talk about the pros and cons of each
  - [RDS](https://www.googleadservices.com/pagead/aclk?sa=L&ai=DChcSEwj_4t6L7JH0AhUiGK0GHbifBukYABABGgJwdg&ae=2&ohost=www.google.com&cid=CAESQeD2pA3iSSnOiS0Ki4KCiizCbRym-PTi3IoqcnQFquxCCZTmrnzbuidHfF54mHTgPdyS0kiZtcsjlDnudi7zMraW&sig=AOD64_22U8uoHwH9QrA7IwxJoM2JcaXHFw&q=&ved=2ahUKEwjVkdeL7JH0AhVWDzQIHZBfAkEQqyQoAHoECAIQBw&adurl=)
  - [Redshift](https://www.googleadservices.com/pagead/aclk?sa=L&ai=DChcSEwj_4t6L7JH0AhUiGK0GHbifBukYABADGgJwdg&ae=2&ohost=www.google.com&cid=CAESQeD2pA3iSSnOiS0Ki4KCiizCbRym-PTi3IoqcnQFquxCCZTmrnzbuidHfF54mHTgPdyS0kiZtcsjlDnudi7zMraW&sig=AOD64_0OWEmk0-LHNceo4t1r-NxKnx_BqQ&q=&ved=2ahUKEwjVkdeL7JH0AhVWDzQIHZBfAkEQqyQoAXoECAIQCA&adurl=)
  - [DynamoDB](https://www.googleadservices.com/pagead/aclk?sa=L&ai=DChcSEwj_4t6L7JH0AhUiGK0GHbifBukYABACGgJwdg&ae=2&ohost=www.google.com&cid=CAESQeD2pA3iSSnOiS0Ki4KCiizCbRym-PTi3IoqcnQFquxCCZTmrnzbuidHfF54mHTgPdyS0kiZtcsjlDnudi7zMraW&sig=AOD64_2ppwvRxqJrdgs1Gc19yNnS2ow-Hw&q=&ved=2ahUKEwjVkdeL7JH0AhVWDzQIHZBfAkEQqyQoAnoECAIQCQ&adurl=)
- What’s the difference between a FIFO and a standard queue?
  - Standard queues provide at-least-once delivery, which means that each message is delivered at least once. FIFO queues provide exactly-once processing, which means that each message is delivered once and remains available until a consumer processes it and deletes it
- How can the server be assured a message was properly received?
  - Client can be configured to reply with a reciept back to the server.
  
 | Terminology | Definition |
 | ----------- | ---------- |
 | Serverless API | A cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers. A serverless application runs in stateless compute containers that are event-triggered, ephemeral (may last for one invocation), and fully managed by the cloud provider. |
 | Triggers | A trigger is a Lambda resource or a resource in another service that you configure to invoke your function in response to lifecycle events, external requests, or on a schedule. Your function can have multiple triggers. Each trigger acts as a client invoking your function independently. |
 | Dynamo vs Mongo | MongoDB: Agnostic \ DynamoDB: Limited to AWS, schema-less database -> [Full Reading Source: bmcBlogs](https://www.bmc.com/blogs/mongodb-vs-dynamodb/) |
