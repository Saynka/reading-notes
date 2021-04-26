# AWS: S3 and Lambda

## Refrences

- https://aws.amazon.com/s3/
- https://www.serverless.com/aws-lambda
- https://aws.amazon.com/lambda/
- https://cyberhoot.com/cybrary/content-delivery-network-cdn/

## Review, Research, and Discussion

1. What’s the difference between a FIFO and a standard queue?

- FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing. FIFO queues provide additional features that help prevent unintentional duplicates from being sent by message producers or from being received by message consumers.

2. How can the server be assured a message was properly received?

- sync and async sender and receiver

3. What classic design pattern is best represented by event driven programming?

- command design pattern

4. How do you test an event driven system?

- you would test the logs to make sure they were called

## Vocabulary

- Server Instances - is a collection of SQL Server databases which are run by a solitary SQL Server service or instance. The details of each server instance can be viewed on the service console which can be web-based or command-line based.

- Containers - A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another.

- Cloud Services - Cloud computing is the on-demand availability of computer system resources, especially data storage and computing power, without direct active management by the user. The term is generally used to describe data centers available to many users over the Internet.

- Cloud Architecture - Cloud computing architecture refers to the components and subcomponents required for cloud computing. These components typically consist of a front end platform, back end platforms, a cloud based delivery, and a network. Combined, these components make up cloud computing architecture.

- AWS - Amazon Web Services is a subsidiary of Amazon providing on-demand cloud computing platforms and APIs to individuals, companies, and governments, on a metered pay-as-you-go basis

- EC2/Beanstalk vs Heroku - "its the same picture" it looks like the the main differnce is money and learning curve. they essentially do the same thing
