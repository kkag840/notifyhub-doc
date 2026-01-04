<h1 align="center">
  <a href="https://notifyhub-5bys.onrender.com/login/index.html" target="_blank">
     🔔NotifyHub
  </a>
</h1>

##  NotifyHub – Distributed Messaging Platform

NotifyHub is a **cloud-native, microservices-based messaging platform** designed to support  
**user-to-user communication**, scalable backend services, and real-world cloud deployment practices.

---

## 🤔 Why the Name “NotifyHub”?

The name **NotifyHub** comes from two ideas:

- **Notify** → Deliver messages/events reliably
- **Hub** → A central platform where users and services connect

📌 NotifyHub acts as a **central hub** for:
- User communication
- Message delivery
- Future real-time interactions

Even though the name includes “Notify”, the system is designed as a **Messaging Hub**, not just a notification sender.

---

## 💡 What is NotifyHub Used For?

NotifyHub is used to:
- Enable **user-to-user chat**
- Handle **message delivery and routing**
- Store conversations and message history
- Support **real-time and async messaging**

Example use cases:
- Chat applications
- Internal messaging systems
- Community platforms
- Real-time communication services

---

## 🧩 High-Level Architecture
Client (Web / Mobile)
|
v
API Gateway
|
v
User Service
|
v
Service Registry (Eureka)


---

## ☁️ Cloud Platforms Used
## ☁️ Cloud Platforms Used (Problems & Fixes)

| Platform | Used For | Problem Faced | How It Was Fixed |
|---------|----------|---------------|------------------|
| **[Render](https://render.com)** | Backend Microservices (API Gateway, User Service, Eureka) | Free tier services **sleep after inactivity**, causing cold start delays | Implemented **health check strategy** using `/actuator/health`  endpoint |
| **[Render](https://render.com)** | Frontend (HTML, CSS, JS) deployed as **Static Service** | No major issue, only static hosting required | Used **Render Static Service** for lightweight and fast frontend delivery |
| **[UptimeRobot](https://uptimerobot.com)** | Backend Monitoring & Keep-Alive | Backend services were going to sleep on Render free tier | Configured **HTTP monitors (5-minute interval)** to ping Beckend services |
| **[Neon](https://neon.tech)** | PostgreSQL Database | Needed a **free, reliable cloud database** | Used **Neon Free Tier PostgreSQL** for persistent data storage |
| **[Upstash](https://upstash.com)** | Redis Cache | Required Redis without managing infrastructure | Used **Upstash Free Tier Redis** (serverless & easy integration) |


---
## 🗄️ Databases & Caching

### 🟢 Primary Database – PostgreSQL
Used for:
- User data
- Message persistence
- Conversation history

Why PostgreSQL?
- Reliable relational database
- ACID compliant
- Production-grade

---

### 🔴 Cache – Redis
Used for:
- Session caching
- Fast data access
- Future real-time message state (online/offline users)

Why Redis?
- In-memory storage
- Very fast
- Perfect for messaging systems

---

## 🛠️ Technologies Used

- Java
- Spring Boot
- Spring Cloud
- Spring Cloud Gateway
- Netflix Eureka (Service Discovery)
- Spring Boot Actuator
- PostgreSQL
- Redis

---

## 🧱 Microservices Implemented So Far

### 1️⃣ Service Registry (Eureka Server)
- Central service discovery
- All services register dynamically
- No hard-coded URLs

---

### 2️⃣ API Gateway
- Single entry point for clients
- Routes requests to microservices
- Exposes a custom `/deep-health` endpoint

---

### 3️⃣ User Service
- Manages users
- Foundation for messaging features
- Connects to PostgreSQL & Redis

---

## ✨ Current Features

- Microservices architecture
- Service discovery using Eureka
- API Gateway routing
- Centralized health checks
- No-sleep backend strategy
- PostgreSQL integration
- Redis caching
- Cloud deployment (free tier)

---

## 🚧 Upcoming Services & Features

### 📨 Messaging Service (Core Goal)
- User-to-user chat
- Message persistence
- Conversation threads

### ⚡ Real-Time Messaging
- WebSocket / SSE
- Typing indicators
- Read receipts

### 🔐 Security
- Authentication & Authorization
- JWT-based login

---

## 🎯 Why NotifyHub Matters

NotifyHub demonstrates:
- Real-world microservices design
- Cloud-native deployment
- Scalable messaging architecture
- Cost-efficient backend setup
- Production-like monitoring on free tier

Perfect for:
- Backend developer portfolios
- System design interviews
- Learning distributed systems

---

## 👨‍💻 Author

**Kamal Kag**  
Backend Engineer | Java | Spring Boot | Microservices

---

## 📌 Final Note

NotifyHub is evolving from a **strong architectural foundation** into a  
**full-featured messaging platform**.

The current focus is on:
- Architecture
- Scalability
- Reliability
- Cloud deployment best practices

