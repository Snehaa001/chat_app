# Project Title
Chat Application – A simple real-time chat application using WebSocket technology.

# Project Description
This application is a real-time chat platform that enables multiple clients to connect, exchange messages, and experience instant communication. The backend server uses Node.js and WebSocket, while the client interface is built with HTML and JavaScript. The application supports multiple concurrent users through WebSocket's event-driven, asynchronous communication model.

# Features
1. Real-time messaging between clients.
2. WebSocket-based full-duplex communication.
3. Supports multiple concurrent connections.
4. Deployed on Vercel for easy access.

# 1. How to Run the Server and Client Applications
# Running Locally
1. Clone the repository:

bash
git clone https://github.com/Sneha001/chat_app.git
cd chat_app

2. Install dependencies:

bash
npm install

3. Start the server:

bash
node server.js
By default, the server will run on http://localhost:3000.

4. Open the client.html file in your browser:

Use any modern browser (e.g., Chrome, Edge).
Connect to the WebSocket server to start chatting.

# Deployed Version
Access the deployed application directly using the link: https://chat-app-gf25-r1dpvkrzi-snehaa001s-projects.vercel.app/

# 2. Application Architecture

# Backend (Node.js WebSocket Server)
The server is built using Node.js with the ws library for WebSocket communication.
It maintains a list of active client connections and broadcasts messages to all connected clients.

# Client (HTML + JavaScript)
The client connects to the WebSocket server using the WebSocket API.
Sends and receives messages in real time.
Displays messages dynamically on the webpage.

# Concurrency Handling
The WebSocket server uses event-driven architecture to handle multiple clients simultaneously.
Each client connection is managed using ws's connection event.
Broadcasts messages to all active clients without blocking the main thread.

# 3. Assumptions and Design Choices

# Assumptions
1. The application assumes all users can send and receive messages in a shared chatroom.
2. A basic implementation focusing on functionality over UI design.

# Design Choices

1. WebSocket Technology:
Chosen for its efficiency in handling real-time communication over HTTP.
Full-duplex communication enables instant message transfer.

2. Broadcast Model:
The server broadcasts messages to all clients for simplicity.
No private messaging or room-based segregation implemented.

3. Deployment:
Deployed on Vercel for free and easy hosting.
The vercel.json file configures server-side handling.

# 4. Accessing the Chat Application

# Deployed Version
Open the application using the following URL: Chat App on Vercel

# Testing Locally
1. Start the server (node server.js) and ensure it runs on http://localhost:3000.
2. Open the client.html file in your browser and ensure the WebSocket URL points to ws://localhost:3000.

# 5. Troubleshooting

1. Blank Screen: Ensure the server is running, and the WebSocket URL is correct.
2. Deployment Issues: Verify that the vercel.json file is correctly configured.
3. WebSocket Not Connecting: Use browser developer tools to check for network issues.
