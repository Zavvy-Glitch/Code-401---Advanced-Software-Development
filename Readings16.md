# AWS: Cloud Servers

## EC2
  - What is EC2?
    - To put it simply, an EC2 is a virtual machine that represents a physical server for you to deploy your applications. Instead of purchasing your own hardware and connecting it to a network, Amazon gives you nearly unlimited virtual machines to run your applications while they take care of the hardware. 
  - How does it work?
    - EC2 setup involves creating an Amazon Machine Image (AMI), which includes an operating system, apps, and configurations. That AMI is loaded to the Amazon Simple Storage Service (S3), and it's registered with EC2, at which point users can launch virtual machines as needed
    - How to Create EC2 Instance:
      - How to Create EC2 Instance in AWS: Step by Step Tutorial
        - Login and access to AWS services.
        - Choose AMI.
        - Choose EC2 Instance Types.
        - Configure Instance.
        - Add Storage.
        - Tag Instance.
        - Configure Security Groups.
        - Review Instances.

## Elastic Beanstalk
[Docs for EB](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/GettingStarted.html)
  - What is EB?
    - Elastic Beanstalk is a platform within AWS that is used for deploying and scaling web applications. In simple terms this platform as a service (PaaS) takes your application code and deploys it while provisioning the supporting architecture and compute resources required for your code to run.

  - What are some benefits of EB?
    - Elastic Beanstalk's main benefits include timesaving server configuration, powerful customization, and a cost-effective price point. Elastic Beanstalk automates the setup, configuration, and provisioning of other AWS services like EC2, RDS, and Elastic Load Balancing to create a web service.

  - When should you use EB?
    - AWS Elastic Beanstalk makes it even easier for developers to quickly deploy and manage applications in the AWS Cloud. Developers simply upload their application, and Elastic Beanstalk automatically handles the deployment details of capacity provisioning, load balancing, auto-scaling, and application health monitoring. 
