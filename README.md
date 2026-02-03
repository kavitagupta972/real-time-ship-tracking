Real-Time Ship Tracking Platform


A production-grade, real-time, event-driven ship tracking platform using Kafka, Spring Boot, Redis, WebSockets, and React (useRef) to deliver low-latency live map updates at scale.

🌍 Live Architecture Overview
Ship Simulator → Kafka → Spring Boot Consumer → Redis (Latest State)
                                     ↓
                                WebSocket
                                     ↓
                         React (useRef + Map)
🧠 Key Highlights

⚡ Real-time streaming using Kafka + WebSockets

🧠 Redis snapshot caching for fast dashboard load

🗺️ Live map rendering with high-frequency marker updates

🚀 React useRef optimization to prevent unnecessary re-renders

📈 Horizontally scalable architecture

🏗️ System Diagram (Mermaid)
flowchart LR
  A[Ship Simulator] --> B[Kafka Topic]
  B --> C[Spring Boot Consumer]
  C --> D[Redis Cache]
  C --> E[WebSocket Gateway]
  E --> F[React Dashboard]
📁 Project Structure
ship-tracking-platform/
├── backend/
│   ├── docker-compose.yml
│   └── ship-service/
├── frontend/
│   └── src/
│       ├── hooks/
│       └── ShipMap.jsx
├── simulator/
│   └── ship-producer.js
└── README.md
🚀 Quick Start (5 Minutes)
1️⃣ Clone Repo
git clone <repo url>
cd real-time-ship-tracking
2️⃣ Start Kafka + Redis
cd backend
docker-compose up -d
3️⃣ Run Backend
cd ship-service
mvn spring-boot:run
4️⃣ Start Ship Simulator
cd simulator
npm install kafkajs
node ship-producer.js
5️⃣ Start Frontend
