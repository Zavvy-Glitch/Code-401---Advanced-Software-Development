# AWS

  - Describe “The Cloud”
    -  A cloud is a type of a server, which is remote (usually in Data Centers), meaning you access it via the internet. You are renting the server space, rather than owning the server. A local (regular) server is one that you do buy and own physically, as well as have on site with you.
    
  - What is a container (as it relates to computers and servers)?
    - Containers are packages of software that contain all of the necessary elements to run in any environment. In this way, containers virtualize the operating system and run anywhere, from a private data center to the public cloud or even on a developer's personal laptop.
    
  - What is auto-scaling?
    - It monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost.
    
  - What is bandwidth?
    - Bandwidth is measured as the amount of data that can be transferred from one point to another within a network in a specific amount of time.
    
  - How do cloud providers compute service costs?
    - When calculating the prices charged by cloud vendors, you must realize that the vendor will also decide how much they have to spend to maintain the network. So, the vendor will estimate the costs for the hardware, network set-ups, labor and maintenance. For instance, every virtual server will demand some specific kind of hardware which the provider has to purchase. The infrastructure maintenance related to costs for security tools like firewalls, patch panels, routing, uplinks, load balancers, LAN switching etc which are needed to make sure that the architecture runs smoothly. Labor costs refer to expenses needed to monitor, manage and maintain the infrastructure and staff so that they can guarantee 24x7 up-time.

| Terminology | Definitions |
| ----------- | ----------- |
| Server Instances | A server instance is a collection of SQL Server databases which are run by a solitary SQL Server service or instance. The details of each server instance can be viewed on the service console which can be web-based or command-line based. |
| Containers | Containers are packages of software that contain all of the necessary elements to run in any environment. In this way, containers virtualize the operating system and run anywhere, from a private data center to the public cloud or even on a developer's personal laptop. |
| Cloud Services | Cloud based services provide information technology (IT) as a service over the Internet or dedicated network, with delivery on demand, and payment based on usage. Cloud based services range from full applications and development platforms, to servers, storage, and virtual desktops. |
| AWS | AWS is a comprehensive, easy to use computing platform offered Amazon. The platform is developed with a combination of infrastructure as a service (IaaS), platform as a service (PaaS) and packaged software as a service (SaaS) offerings. |
|EC2/Beanstalk vs Heroku | [Document Source: Beanstalk VS Heroku](https://codeburst.io/heroku-v-s-aws-elastic-beanstalk-1cc6f12ca3c7) |

## Lambda Basics

  - AWS Lambda is a serverless computing service provided by Amazon Web Services (AWS). Users of AWS Lambda create functions, self-contained applications written in one of the supported languages and runtimes, and upload them to AWS Lambda, which executes those functions in an efficient and flexible manner.

  - The concept of “serverless” computing refers to not needing to maintain your own servers to run these functions. AWS Lambda is a fully managed service that takes care of all the infrastructure for you. And so “serverless” doesn’t mean that there are no servers involved: it just means that the servers, the operating systems, the network layer and the rest of the infrastructure have already been taken care of, so that you can focus on writing application code.
        
        - Why is AWS Lambda an essential part of the Serverless architecture?   
              - a computing service;
              - a database service; and
              - an HTTP gateway service.
        
        - What are the most common use cases for AWS Lambda?
              - individual tasks run for a short time
              - each task is generally self-contained
              - there is a large difference between the lowest and highest level in the workload of the application
