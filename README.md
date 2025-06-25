# 🚀 DevOps Internship Assignment – Docker + NGINX Reverse Proxy

This project sets up two backend services (Golang and Python Flask) and an NGINX reverse proxy using Docker Compose.

---

## 📦 Services Overview

| URL Path         | Service        | Port Inside Container |
|------------------|----------------|------------------------|
| `/service1/hello`| Golang Service | 8001                   |
| `/service2/hello`| Python Flask   | 8002                   |

All traffic is routed through NGINX at:
http://localhost:8080

---

## 🐳 Tech Stack

- Docker
- Docker Compose
- Golang (service 1)
- Python Flask (service 2)
- NGINX (as reverse proxy)

---

## 📁 Folder Structure

Assignment/
├── docker-compose.yml
├── nginx/
│ ├── nginx.conf
│ └── Dockerfile
├── service_1/
│ ├── main.go
│ └── Dockerfile
├── service_2/
│ ├── app.py
│ ├── requirements.txt
│ └── Dockerfile
---

## ⚙️ Setup Instructions

### 🐙 Step 1: Clone the Repo
```bash
git clone https://github.com/yourusername/devops-nginx-assignment.git
cd devops-nginx-assignment
🛠 Step 2: Run the App
bash
docker-compose up --build
This will:

Build the Golang and Python images

Build and run the NGINX reverse proxy

Expose all services via port 8080

✅ Features
NGINX routing:

/service1 → Go app

/service2 → Python app

Bridge networking only (no host mode)

Logs each request with timestamp and path

Health checks (optional: if implemented)

🔍 Test Endpoints
http://localhost:8080/service1/hello

http://localhost:8080/service2/hello

**Results**:

![Screenshot (303)](https://github.com/user-attachments/assets/078e3444-8dbb-4ec4-bd9f-761ccf0a6ba5)



![Screenshot (305)](https://github.com/user-attachments/assets/7a2c2728-ba1d-418c-ab12-ef7343e0e7e0)


![Screenshot (308)](https://github.com/user-attachments/assets/77488710-0661-4e71-b21c-d4487067b6e5)


![Screenshot (309)](https://github.com/user-attachments/assets/5a9022b0-4d58-4cd8-a170-22081935f2aa)


![Screenshot (310)](https://github.com/user-attachments/assets/59bb24f7-3e4d-4582-a911-40a933c2b6cb)


![Screenshot (311)](https://github.com/user-attachments/assets/ef1d4995-5021-4e0c-8c9f-8fcf2d6928b7)


