# AWS: API, Dynamo and Lambda

## Refrences

- https://www.youtube.com/watch?v=UesxWuZMZqI
- https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5
- https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SNS.html
- https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SQS.html

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

- Serverless API - Creates a collection of Amazon API Gateway resources and methods that can be invoked through HTTPS endpoints.

- Triggers - you can add up to four triggers (associations) that cause a Lambda function to execute when specific CloudFront events occur. CloudFront triggers can be based on one of four CloudFront events,

- Dynamo vs Mongo - DynamoDB is a fully managed AWS service, MongoDB can be self installed or fully managed with MongoDB Atlas. ... DynamoDB uses tables, items and attributes, MongoDB uses JSON-like documents. DynamoDB supports limited data types and smaller item sizes; MongoDB supports more data types and has fewer size restrictions.

- Dynamoose vs Mongoose - i mean they are the same thing... dynamoose is just infinitly more scaleable due to amazon and also the fact mongoose itself it stored on aws seems silly if your gonna use aws obviouly you would go dynamoose
