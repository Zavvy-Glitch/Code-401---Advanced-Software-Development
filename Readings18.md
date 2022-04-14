# AWS: API Gateway / DynamoDB
  
  ## API Gateway
  
  - What is Amazon API Gateway?
    - Amazon API Gateway is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic. It also handles authentication, access control, monitoring, and tracing of API requests.
  - How does API Gateway work?
    - API Gateway sits between the backend services of your API and your API’s users, handling the HTTP requests to your API endpoints and routing them to the correct backends. It provides a set of tools that help you manage your API definitions and the mappings between endpoints and their respective backend services. It can also generate API references from your definitions and make them available to your users as API documentation.

![apiGateway](https://user-images.githubusercontent.com/84699682/163300527-2731ec12-f1c0-40f7-99ed-9b044631f319.jpg)

  ## DynamoDB
  
  - What is DynamoDB?
    - DynamoDB is a hosted NoSQL database offered by Amazon Web Services (AWS)
        - Offers:
            - reliable performance even as it scales;
            - a managed experience, so you won't be SSH-ing into servers to upgrade the crypto libraries;
            - a small, simple API allowing for simple key-value access as well as more advanced query patterns.
    - DynamoDB is a particularly good fit for the following use cases:
        - Applications with large amounts of data and strict latency requirements
        - Serverless applications using AWS Lambda
        - Data Sets with simple, known access patterns

            - Core Building Blocks of DynamoDB
              - Tables: a grouping of data records. For example, you might have a Users table to store data about your users, and an Orders table to store data about your users' orders.
              - Items: a single data record in a table. Each item in a table is uniquely identified by the stated primary key of the table.
              - Attributes: pieces of data attached to a single item. This could be a simple Age attribute that stores the age of a user.
