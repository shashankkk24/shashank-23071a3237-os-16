# Chat Server Implementation

This repository contains two different implementations of a simple chat server: one using TCP (Transmission Control Protocol) and another using Unix Domain Sockets. Both implementations allow communication between a server and a client, where the server listens for messages from the client and responds to them.

## Features:
- **TCP-based Chat Server**: Implements a basic server that uses TCP sockets to establish communication over a network.
- **Unix Domain Socket Chat Server**: Implements a server that uses Unix Domain Sockets for communication, typically for local machine communication.

---

## 1. **TCP Chat Server**

### Overview:
This is a simple chat server that utilizes TCP sockets to enable communication between the server and client over a network. The server listens for incoming client connections, and once a client connects, it allows bidirectional communication by reading and writing messages.

### Functionality:
- **Socket Creation**: The server creates a socket using the `AF_INET` address family and the `SOCK_STREAM` type for reliable TCP communication.
- **Binding**: The server binds the socket to a specific IP address and port (`PORT 12345`) to listen for incoming connections.
- **Listening**: The server listens for client requests.
- **Client Connection**: The server accepts a client connection and enters a loop to communicate by reading messages from the client and allowing the server user to type responses.
- **Communication**: The server reads messages sent by the client and writes responses back to the client.
- **Graceful Termination**: The server closes the connection after the communication ends.

### Instructions:
1. **Compile**:  
   ```bash
   gcc tcp_chat_server.c -o tcp_chat_server
