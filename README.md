# What are WebSockets?
WebSockets are a communication protocol that enables bidirectional, full-duplex communication between clients (such as web browsers) and servers over a single, persistant TCP connection. They facilitate real-time data exchange and are commonly used in applications that require instant updates and low-latency communication.

```mermaid
sequenceDiagram
    participant Client
    participant Server

    Client ->> Server: WebSocket Handshake (HTTP)
    Server -->> Client: Upgrade Required
    Client -->> Server: WebSocket Connection
    Client -->> Server: Bidirectional Data Transfer
    Server -->> Client: Bidirectional Data Transfer
```
1. **WebSocket Handshake (HTTP):** The WebSocket connection begins with a handshake between the client and server, initiated through an HTTP request. This handshake involves negotiating the WebSocket protocol upgrade.
2. **WebSocket Connection:** Once the handshake is completed and the connection is established, the protocol switches to a WebSocket connection. This connection remains open for the duration of the session.
3. **Bidirectional Data Transfer:** With the WebSocket connection established, both the client and server can send messages to each other at any time, without waiting for a request from the other party. This bidirectional communication allows for real-time data exchange.

### For more detailed information about the websocket protocol and standard, please see the below resources

- [RFC 6455 The WebSocket Protocol IETF](https://datatracker.ietf.org/doc/html/rfc6455)
- [WebSockets Living Standard](https://websockets.spec.whatwg.org/)



# What are WebSockets used for?
WebSockets are employed in various applications requiring real-time communication and low-latency data transfer. Below are some common use cases:

```mermaid
sequenceDiagram
    participant ClientX
    participant Server
    participant ClientY

    ClientX -->> Server: ClientX sends chat message, streams video/audio, moves player
    Server -->> ClientY: Server sends update to any other clients listening for changes
    ClientY -->> Server: ClientY sends chat message, streams video/audio, moves player
    Server -->> ClientX: Server sends update to any other clients listening for changes
```
1. **Real-time Chat Applications:** WebSockets are ideal for chat applications where users need to exchange messages instantly. With WebSockets, messages can be sent and received in real-time, providing a seamless chatting experience.
2. **Live Data Streaming:** WebSockets are utilized to stream live data (e.g., stock prices, weather updates) to clients in real-time. This enables users to receive continuous updates without the need to refresh the page.
3. **Multiplayer Online Games:** WebSockets find extensive usage in multiplayer online games to facilitate real-time communication between players and the game server. This allows players to interact with each other and see updates instantly as they occur in the game world.



# What are some popular WS libraries?

**Socket.IO** (JavaScript/Node.js):
Socket.IO is a JavaScript library for real-time web applications. It enables bidirectional communication between web clients and servers and offers features like multiplexing, broadcasting, and automatic reconnection.
- Website: [Socket.IO](https://socket.io/)
- GitHub: [socketio/socket.io](https://github.com/socketio/socket.io)

**WebSocket-Node** (JavaScript/Node.js):
WebSocket-Node is a WebSocket implementation for Node.js. It provides a simple API for working with WebSocket connections in server-side Node.js applications.
- GitHub: [websocket/websocket-node](https://github.com/websocket/websocket-node)

**ws** (JavaScript/Node.js):
ws is a lightweight WebSocket library for Node.js. It is simple, fast, and easy to use, making it a popular choice for WebSocket communication in Node.js applications.
- GitHub: [websockets/ws](https://github.com/websockets/ws)

