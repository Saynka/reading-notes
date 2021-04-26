# AWS: API, Dynamo and Lambda

## Refrences

- https://www.serverless.com/amazon-api-gateway
- https://aws.amazon.com/api-gateway/
- https://www.dynamodbguide.com/what-is-dynamo-db/
- https://aws.amazon.com/dynamodb/
- https://dynamoosejs.com/getting_started/Introduction/

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

- Serverless Functions - is a programmatic function written by a software developer for a single purpose. It's then hosted and maintained on infrastructure by cloud computing companies. These companies take care of code maintenance and execution so that developers can deploy new code faster and easier.

- Cloud Storage - is a model of computer data storage in which the digital data is stored in logical pools, said to be on "the cloud". The physical storage spans multiple servers, and the physical environment is typically owned and managed by a hosting company.

- CDN - content delivery network, or content distribution network, is a geographically distributed network of proxy servers and their data centers. The goal is to provide high availability and performance by distributing the service spatially relative to end users.
