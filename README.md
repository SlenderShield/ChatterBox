## Chatter Box

### **📌 High-Level Architecture Overview**  

#### **1️⃣ Frontend (React + WebSockets)**
- **User Interface:** Built with **React + Tailwind CSS** for a responsive UI.  
- **State Management:** Context API / Redux for managing chat state.  
- **WebSockets:** **Socket.io / STOMP over WebSockets** for real-time messaging.  
- **Authentication:** JWT-based authentication for secure user sessions.  
- **API Communication:** Uses **REST APIs** (Axios/Fetch) to interact with the backend.  

#### **2️⃣ Backend (Spring Boot + WebSockets + AI APIs)**
- **Spring Boot REST APIs** for authentication, message storage, and user management.  
- **WebSockets (Spring WebSocket + STOMP)** for real-time chat.  
- **AI Model Integration:** API clients for **GPT-3.5, Grok, AWS Bedrock, Claude**, etc.  
- **Database:** PostgreSQL / MongoDB for storing chat history and user data.  
- **Authentication & Security:** JWT / OAuth2-based authentication.  

#### **3️⃣ Database Layer (PostgreSQL / MongoDB)**
- **User Table:** Stores user details & credentials.  
- **Chat Messages Table:** Stores chat history.  
- **AI Query Logs:** Logs AI interactions for future insights.  

#### **4️⃣ AI Model Integration Layer**
- **Spring Boot Service Layer** to handle API requests for different AI models.  
- **Dynamic Model Selection:** Users choose **GPT, Grok, Bedrock, or Claude** at runtime.  
- **AI Model Request Flow:**  
  1. User selects an AI model.  
  2. Request sent to backend via REST API.  
  3. Spring Boot forwards request to the selected AI API.  
  4. Response is sent back to the user.  

#### **5️⃣ Deployment & DevOps**
- **Frontend:** Deployed on **Vercel / Netlify**.  
- **Backend:** Deployed on **AWS EC2 / DigitalOcean / Heroku**.  
- **Database Hosting:** AWS RDS (PostgreSQL) / MongoDB Atlas.  
- **Containerization:** Docker for managing services.  
- **CI/CD:** GitHub Actions / Jenkins for automated deployment.  

### **📌 Architecture Diagram (Conceptual)**  
```
[ React (Frontend) ]  <-->  [ Spring Boot (Backend) ]  <-->  [ AI Models API ]
         |                            |                          |
     WebSockets                 PostgreSQL / MongoDB         GPT, Grok, Bedrock
```
