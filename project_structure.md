## **📌 Project Structure**
### **1️⃣ Frontend (React)**
📂 **chatterbox-frontend/** *(React Project Root)*  
```
├── public/               # Static files (index.html, icons, etc.)
├── src/                  
│   ├── components/       # Reusable UI components (ChatBox, MessageList, etc.)
│   ├── pages/            # Page components (Login, ChatRoom, etc.)
│   ├── services/         # API calls & WebSocket services
│   ├── context/          # State management (AuthContext, ChatContext)
│   ├── hooks/            # Custom hooks (useAuth, useChat, etc.)
│   ├── App.js            # Main app entry point
│   ├── index.js          # Root React entry point
│   ├── websocket.js      # WebSocket client setup
│   ├── api.js            # Axios API client setup
│   ├── styles/           # Global styles (CSS/Tailwind)
│   ├── config.js         # Configuration (API URLs, env variables)
├── .env                  # Environment variables
├── package.json          # Dependencies & scripts
```

### **2️⃣ Backend (Spring Boot)**
📂 **chatterbox-backend/** *(Spring Boot Project Root)*  
```
├── src/main/java/com/chatterbox/
│   ├── config/               # WebSocket & Security Configuration
│   ├── controller/           # REST & WebSocket Controllers
│   ├── model/                # Entity models (User, Message, AIQuery)
│   ├── repository/           # Database repositories (JPA / MongoDB)
│   ├── service/              # Business logic (ChatService, AIService)
│   ├── utils/                # Helper utilities
│   ├── ChatterboxApplication.java  # Main Spring Boot Application
│
├── src/main/resources/
│   ├── application.properties  # Database & App Config
│   ├── static/                 # Static files (if needed)
│
├── pom.xml                     # Maven dependencies
├── Dockerfile                   # Docker configuration
├── README.md                    # Documentation
```

## **📌 Key Components**
### **Frontend**
- `websocket.js`: Handles **real-time communication** via WebSockets.  
- `api.js`: Manages **REST API** calls to the Spring Boot backend.  
- `context/ChatContext.js`: Centralized chat state management.  

### **Backend**
- `ChatController.java`: Handles WebSocket **message exchange**.  
- `AIController.java`: Routes requests to **GPT, Grok, Bedrock, Claude**.  
- `ChatService.java`: Business logic for **message processing & AI integration**.  
- `WebSocketConfig.java`: Configures **STOMP WebSockets in Spring Boot**.  
- `UserRepository.java`: Manages **user authentication & storage**.  
