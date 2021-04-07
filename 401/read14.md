# Event Driven Architecture

## Refrences

- https://www.youtube.com/watch?v=mXk0MNjlO7A

## Review, Research, and Discussion

1. What’s the difference between a FIFO and a standard queue?

- FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing. FIFO queues provide additional features that help prevent unintentional duplicates from being sent by message producers or from being received by message consumers.

2. How can the server be assured a message was properly received?

- Every response that is received from a server contains zero or more headers. Headers are the part of Response that is sent by the server. Each header entry is basically a Key-Value pair. Headers are used to send across extra information by the server. This extra information is also referred to as Metadata of the Response.

3. What classic design pattern is best represented by event driven programming?

- a point of sale signal flow from customer to where the event happened

4. How do you test an event driven system?

- There are multiple levels of tests you will typically write for your system. In the most canonical case, you will write unit tests, service tests, and end-to-end tests. In each of these cases, your System Under Test (SUT, what is actually being tested) comprises a different part of your application.

## Vocabulary

- FIFO Queue - delivery and exactly-once processing: The order in which messages are sent and received is strictly preserved and a message is delivered once and remains available until a consumer processes and deletes it.
- Pub/Sub - in software architecture, publish–subscribe is a messaging pattern where senders of messages, called publishers, do not program the messages to be sent directly to specific receivers
