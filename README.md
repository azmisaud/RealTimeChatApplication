# Real-Time Chat Application

A real-time chat application built with Spring Boot and WebSocket technology, providing instant messaging capabilities with a modern, responsive user interface.

> **Learning Journey**: This project was created as part of my Spring Boot learning journey. Special thanks to [EmbarkX | Learn Programming](https://www.youtube.com/@EmbarkX) for their excellent tutorials and guidance in Spring Boot development.

## Features

- Real-time messaging using WebSocket
- Clean and responsive user interface
- Support for multiple concurrent users
- Simple and intuitive chat interface
- Bootstrap-based modern design
- Mobile-responsive layout

## Tech Stack

- **Backend:**
  - Spring Boot 3.4.5
  - Spring WebSocket
  - Java 21
  - Maven

- **Frontend:**
  - HTML5
  - CSS3
  - JavaScript
  - Bootstrap 5.3.6
  - SockJS
  - STOMP.js

## Prerequisites

- Java 21 or higher
- Maven 3.9.9 or higher
- Modern web browser

## Getting Started

### Installation

1. Clone the repository:
   ```bash
   git clone [your-repository-url]
   cd chatapp
   ```

2. Build the project:
   ```bash
   ./mvnw clean install
   ```

3. Run the application:
   ```bash
   ./mvnw spring-boot:run
   ```

The application will start on `http://localhost:8080`

### Usage

1. Open your web browser and navigate to `http://localhost:8080/chat`
2. Enter your name in the "Your name" field
3. Start sending messages in the chat interface
4. Messages will be broadcasted to all connected users in real-time

## Project Structure

```
src/
├── main/
│   ├── java/
│   │   └── com/
│   │       └── chat/
│   │           └── app/
│   │               ├── config/
│   │               │   └── WebSocketConfig.java
│   │               ├── controller/
│   │               │   └── ChatController.java
│   │               ├── model/
│   │               │   └── ChatMessage.java
│   │               └── AppApplication.java
│   └── resources/
│       ├── templates/
│       │   └── chat.html
│       └── application.properties
```

## WebSocket Configuration

The application uses STOMP (Simple Text Oriented Messaging Protocol) over WebSocket for real-time communication:

- WebSocket endpoint: `/chat`
- Message broker prefix: `/topic`
- Application destination prefix: `/app`
