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

Results:

![Screenshot (307)](https://github.com/user-attachments/assets/1e15d3cd-c2c1-4371-bff2-723e391c3d10)
