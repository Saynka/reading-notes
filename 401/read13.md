# Message Queues

## Refrences

- https://socket.io/get-started/chat/
- https://socket.io/docs/v3/rooms/index.html
- https://socket.io/docs/v3/rooms/index.html

## Review, Research, and Discussion

1. What does it mean that web sockets are bidirectional? Why is this useful?

- An important consequence is that you may efficiently push data from the server to the client. ... It must be handled both client-side and server-side. Of course that implies that both software be updated (old browsers and old servers can't handle websockets).

2. Does socket.io use HTTP? Why?

- socket.io server will attach to an HTTP server so it can serve its own client code through /socket.io/socket.io.js .

3. What happens when a client emits an event?

- The main idea behind Socket.IO is that you can send and receive any events you want, with any data you want. Any objects that can be encoded as JSON will do, and binary data is supported too.

4. What happens when a server emits an event?

- Sets a modifier for a subsequent event emission that the event data will only be broadcast to every sockets but the sender.

5. What happens if a client “misses” an event?

- When a client connects, it provides a startAfter query parameter that is used to initialize an IObserver against the ReplaySubject, and this observer then sends each event in the observed sequence to the client. Each event has a sequence number, and the client can tell, based on the event sequence number, if any event is missing in the sequence. (Which would be a serious problem in this application.)

6. How can we mitigate this?

- Also, the first time a client connects to the server it always receives the entire sequence just fine. It's the subsequent connections that exhibit the regular skipping problem. So it seems like it's a server-side problem, and not a client problem at all.

## Vocabulary

- Socket - a software structure within a network node of a computer network that serves as an endpoint for sending and receiving data across the network. The structure and properties of a socket are defined by an application programming interface for the networking architecture.

- Web Socket - protocol enables interaction between a web browser (or other client application) and a web server with lower overhead

- Socket.io - is a JavaScript library for realtime web applications. It enables realtime, bi-directional communication between web clients and servers.

- Client - is a computer or a program that, as part of its operation, relies on sending a request to another program or a computer hardware or software that accesses a service made available by a server (which may or may not be located on another computer).

- Server - is a piece of computer hardware or software that provides functionality for other programs or devices, called "clients". This architecture is called the client–server model.

- OSI Model - is a conceptual model that characterises and standardises the communication functions of a telecommunication or computing system without regard to its underlying internal structure and technology.

- TCP Model - The Internet protocol suite is the conceptual model and set of communications protocols used in the Internet and similar computer networks. It is commonly known as TCP/IP because the foundational protocols in the suite are the Transmission Control Protocol and the Internet

- TCP - is one of the main protocols of the Internet protocol suite. It originated in the initial network implementation in which it complemented the Internet Protocol. Therefore, the entire suite is commonly referred to as TCP/IP.

- UDP - is a communications protocol that is primarily used for establishing low-latency and loss-tolerating connections between applications on the internet. It speeds up transmissions by enabling the transfer of data before an agreement is provided by the receiving party.

- Packets - is a formatted unit of data carried by a packet-switched network. A packet consists of control information and user data; the latter is also known as the payload. Control information provides data for delivering the payload
