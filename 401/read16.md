# AWS: Cloud Servers

## refences

- https://www.youtube.com/watch?v=yIVXjl4SwVo
- https://www.youtube.com/watch?v=l0DfHUWMjsU
- https://aws.amazon.com/ec2/?ec2-whats-new.sort-by=item.additionalFields.postDateTime&ec2-whats-new.sort-order=desc
- https://www.youtube.com/watch?v=lZMkgOMYYIg
- https://www.youtube.com/watch?v=SrwxAScdyT0

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

- Server - is a piece of computer hardware or software that provides functionality for other programs or devices, called "clients".
- Pub/Sub - In software architecture, publish–subscribe is a messaging pattern where senders of messages, called publishers, do not program the messages to be sent directly to specific receivers, called subscribers,
- WRRC - Web Request Response Cycle, that is the cycle of sending request objects to an API and receiving a payload in the response object
