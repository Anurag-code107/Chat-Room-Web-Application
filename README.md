# Chat Room Application


## **Overview**

This is a real-time fullstack chatroom application built using Spring Boot, WebSocket, and JavaScript. The app allows multiple users to join a public chatroom and communicate with each other instantly. It supports seamless message exchange with features like user notifications for join and leave events. The chatroom utilizes STOMP over WebSocket for real-time communication, ensuring smooth and responsive interactions between users.

---

## Features

- Real-time messaging using WebSocket.
- Users can join the chatroom with a username.
- Notifications for user join and leave events.
- Clear and responsive UI.
- Powered by STOMP over WebSocket for communication.

---

## Technologies Used

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Spring Boot
- **WebSocket Library**: STOMP.js
- **Socket Server**: SockJS

---

## Demo of Application


### Chatroom Login

![image](https://github.com/user-attachments/assets/436d8740-9ba6-4239-bf5f-f084863f89b0)


### Chat Room

![image](https://github.com/user-attachments/assets/4d8f3137-2b74-459d-be9d-c0c8056a9fd7)

![image](https://github.com/user-attachments/assets/87a13203-e3e5-493d-ba15-daa17080c8bf)

![image](https://github.com/user-attachments/assets/761fa975-0183-4e04-8c40-8be9109e2299)

![image](https://github.com/user-attachments/assets/1ecfa18d-100a-4b6f-a6c2-d33db123c479)

![image](https://github.com/user-attachments/assets/f319f01e-7713-4374-87a4-9468fa6d0832)

![image](https://github.com/user-attachments/assets/33f84413-8348-4320-b509-1dd49ce832ce)

---

## Live Demo

You can try the live version of the Chat Room through the link below:  
[Live Demo](https://chat-room-web-application-production.up.railway.app/)

The project is deployed on railway.

---

## Prerequisites

1. **Java Development Kit (JDK)**: Ensure you have JDK 11 or later installed.
2. **Maven**: Make sure Maven is installed for building the Spring Boot application.
3. **Web Browser**: Modern browser like Chrome, Firefox, or Edge.

---

## Getting Started

Follow the steps below to set up and run the chat application locally:

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/chat-application.git
cd chat-application
```

### 2. Backend Setup

1. Open the project in your favorite IDE (e.g., IntelliJ IDEA, Eclipse).
2. Build the project:

   ```bash
   mvn clean install
   ```

3. Run the application:

   ```bash
   mvn spring-boot:run
   ```

   The server will start at: `http://localhost:8282`.

### 3. Frontend Setup

No additional setup is required for the frontend. Once the backend is running, you can access the chat application in your browser:

```plaintext
http://localhost:8282
```

---

## Folder Structure

```
src
├── main
│   ├── java
│   │   └── com
│   │       └── negi
│   │           └── chat
│   │               ├── ChatController.java        # Handles WebSocket messaging
│   │               ├── ChatMessage.java           # Chat message model
│   │               └── MessageType.java           # Enum for message types
│   │           └── config
│   │               ├── WebSocketConfig.java       # WebSocket configuration
│   │               └── WebSocketEventListener.java# Event listener for WebSocket events
│   │           └── ChatserverApplication.java     # Main Spring Boot application class
│   └── resources
│       ├── application.properties                 # Application properties
│       └── static
│           ├── css
│           │   └── main.css                       # Stylesheet for the app
│           └── js
│               └── main.js                        # JavaScript for client-side logic
│       └── templates
│           └── index.html                         # Frontend HTML for the chat interface

```

---

## Key Files

1. **Backend:**
   - `ChatController.java`: Handles WebSocket connections and message broadcasting.
   - `WebSocketConfig.java`: Configures WebSocket endpoints and STOMP protocol.
   - `Message.java`: Represents the chat message structure.

2. **Frontend:**
   - `index.html`: Chatroom UI.
   - `chat.js`: Manages WebSocket connections and frontend logic.

---

## How to Use

1. Open the application in your browser at [http://localhost:8282](http://localhost:8282).
2. Enter your username and click **Join Chat**.
3. Start chatting! Messages sent will appear in the chatroom in real-time.

---

## Example Usage

1. Open the application in two different browser tabs.
2. Enter different usernames in each tab.
3. Send messages and watch them appear in both tabs instantly.

---

## How It Works

1. **User joins the chat**:
   - The user enters their name on the welcome screen (`index.html`).
   - A WebSocket connection is established.
   - Other users are notified of the new user joining.

2. **Sending a message**:
   - Users can send messages via the input box.
   - Messages are broadcast to all connected users.

3. **User leaves the chat**:
   - When a user closes their browser or disconnects, others are notified.

## Troubleshooting

- **WebSocket not connecting?**
  - Ensure the backend is running on the correct port (`8282` by default).
  - Check the WebSocket endpoint in `chat.js` matches your backend configuration.

- **Messages not showing?**
  - Verify the WebSocket subscription path in `chat.js` matches the backend's topic path.
  - Check the backend logs for any errors.

---

## Contributing

Feel free to fork the repository, make your changes, and submit a pull request. Contributions are welcome!

---

## License

This project is licensed under the [**MIT License**](LICENSE).

---

## Support

If you encounter any issues or have any questions, feel free to open an issue in the [GitHub repository issues page](https://github.com/Anurag-code107/RecipeHub-Frontend/issues) or contact us directly at [anuragnegi2704@gmail.com](mailto:anuragnegi2704@gmail.com).



