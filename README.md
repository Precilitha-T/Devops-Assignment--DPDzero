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

![Image](https://github.com/user-attachments/assets/2ceff77a-2127-4912-837b-94d18f5aec52)
![Image](https://github.com/user-attachments/assets/bee9666b-b8db-42c0-ac7b-dbf200148eca)
![Image](https://github.com/user-attachments/assets/cfdf5448-9e49-492a-b920-c6bdce455e47)
![Image](https://github.com/user-attachments/assets/eef68e1f-64cf-4bce-a870-20a0f8cf80b2)
![Image](https://github.com/user-attachments/assets/7572b9b8-9d7f-46a2-b203-c958ceb388d9)
![Image](https://github.com/user-attachments/assets/6eae4a3f-3cb7-4bb6-9dc6-118522270629)
![Image](https://github.com/user-attachments/assets/cb37b278-22a0-449d-b121-7d7c70f1bea6)
![Image](https://github.com/user-attachments/assets/ccc8f2c1-5cd3-45b0-a4a0-56fb2d75f6f4)

![Image](https://github.com/user-attachments/assets/41a3dc34-2a8c-4a1f-b606-98a7dcd3d994)
