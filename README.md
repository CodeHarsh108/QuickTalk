# 💬 QuickTalk - Real-Time Chat Application

<p align="center">
  <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" />
  <img src="https://img.shields.io/badge/WebSocket-010101?style=for-the-badge&logo=socket.io&logoColor=white" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" />
  <img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white" />
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
</p>

<p align="center">
  <b>⚡ Instant messaging • 🔐 End-to-End Encryption • 📎 File Sharing • 👥 Real-time Presence</b>
</p>

---

## ✨ Features

### 🚀 **Core Messaging**
- Real-time messaging with WebSocket & STOMP
- Instant delivery with read receipts (✓, ✓✓, ✓✓✓)
- Message reactions with emojis
- Reply threads for organized conversations
- Typing indicators & online user tracking

### 📁 **File Sharing**
- Upload images, videos, audio, PDFs, documents
- Inline preview for images & videos
- Download files with progress indicator
- Thumbnail generation for images

### 🔐 **Security & Authentication**
- JWT-based authentication
- Password encryption with BCrypt
- End-to-end encryption ready (AES-256-GCM)
- Role-based access control

### ⚡ **Performance**
- Redis caching for recent messages
- Optimized MongoDB queries with indexing
- Message pagination for smooth scrolling
- Rate limiting to prevent spam

### 🎨 **Modern UI/UX**
- Beautiful gradient design
- Dark theme optimized
- Responsive layout for all devices
- Real-time updates without page refresh

---

## 🛠️ **Tech Stack**

### **Backend**
- **Java 21** with Spring Boot 3.5.7
- **WebSocket** + STOMP for real-time
- **MongoDB** for primary database
- **Redis** for caching & rate limiting
- **JWT** for authentication
- **Apache Tika** for file type detection
- **Thumbnailator** for image thumbnails

### **Frontend**
- **React 18** with Vite
- **TailwindCSS** for styling
- **STOMP.js** + **SockJS** for WebSocket
- **React Hot Toast** for notifications
- **React Icons** for beautiful icons


## 🚀 **Getting Started**

### **Prerequisites**
- Java 21+
- Node.js 18+
- MongoDB
- Redis

### **Backend Setup**

```bash
# Clone the repository
git clone https://github.com/yourusername/quicktalk.git
cd quicktalk/backend

# Configure application.yml
# Update MongoDB and Redis connection settings

# Run the application
./mvnw spring-boot:run
```

### **Frontend Setup**

```bash
cd frontend

# Install dependencies
npm install

# Start development server
npm run dev
```

### **Environment Variables**

```properties
# Backend .env
MONGODB_URI=mongodb://localhost:27017/quicktalk
REDIS_HOST=localhost
REDIS_PORT=6379
JWT_SECRET=your-secret-key
ENCRYPTION_MASTER_KEY=your-master-key
```

---

## 📚 **API Documentation**

### **Authentication Endpoints**

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/v1/auth/register` | Register new user |
| POST | `/api/v1/auth/login` | Login user |
| POST | `/api/v1/auth/refresh` | Refresh JWT token |
| GET | `/api/v1/auth/me` | Get current user |

### **Room Endpoints**

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/v1/rooms` | Create room |
| GET | `/api/v1/rooms/{roomId}` | Join room |
| GET | `/api/v1/rooms/{roomId}/messages` | Get messages |
| GET | `/api/v1/rooms/{roomId}/exists` | Check room exists |

### **WebSocket Topics**

| Topic | Purpose |
|-------|---------|
| `/topic/room/{roomId}` | Chat messages |
| `/topic/room/{roomId}/typing` | Typing indicators |
| `/topic/room/{roomId}/status` | User join/leave |
| `/topic/room/{roomId}/users` | Online users |
| `/topic/room/{roomId}/receipts` | Read receipts |
| `/topic/room/{roomId}/reactions` | Message reactions |
| `/topic/room/{roomId}/replies` | Thread replies |

---

## 🏗️ **Architecture**

```
┌─────────────┐     ┌──────────────┐     ┌─────────────┐
│   React     │◄───►│  WebSocket   │◄───►│ Spring Boot │
│   Frontend  │     │   (STOMP)    │     │   Backend   │
└─────────────┘     └──────────────┘     └─────────────┘
                                                │
                                      ┌─────────┴─────────┐
                                      ▼                   ▼
                                ┌─────────────┐     ┌─────────────┐
                                │   MongoDB   │     │    Redis    │
                                │  Database   │     │    Cache    │
                                └─────────────┘     └─────────────┘
```

---

## 🔒 **Security Features**

- ✅ **JWT Authentication** - Secure token-based auth
- ✅ **Password Encryption** - BCrypt hashing
- ✅ **Rate Limiting** - Prevent abuse with Redis
- ✅ **Input Validation** - All inputs validated
- ✅ **CORS Configuration** - Properly configured
- ✅ **E2EE Ready** - AES-256 encryption (optional)

---

## 📈 **Performance Optimizations**

- **Redis Caching** - Recent messages cached
- **MongoDB Indexing** - Optimized queries
- **Pagination** - Efficient message loading
- **Connection Pooling** - Optimized database connections
- **Message Compression** - Smaller payloads

---

## 🤝 **Contributing**

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



## 🙏 **Acknowledgments**

- Spring Boot team for amazing framework
- MongoDB for excellent database
- Redis for super-fast caching
- React community for awesome tools

---

## 📞 **Contact**

itsharshhh6@gmail.com
Project Link: [https://github.com/CodeHarsh108/QuickTalk](https://github.com/CodeHarsh108/QuickTalk)

---

<p align="center">
  Made with ❤️ and Java
</p>
