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

## 🐳 Tech Stack

- Docker
- Docker Compose
- Golang (service 1)
- Python Flask (service 2)
- NGINX (as reverse proxy)
- 
## Run the App
docker-compose up --build
This will:

Build the Golang and Python images

Build and run the NGINX reverse proxy

Expose all services via port 8080

## Features
NGINX routing:

/service1 → Go app

/service2 → Python app

Bridge networking only (no host mode)

Logs each request with timestamp and path

## Test Endpoints
http://localhost:8080/service1/hello

http://localhost:8080/service2/hello

## Results

## Building & Running Golang Service (Docker)

![Screenshot (307)](https://github.com/user-attachments/assets/40bc8402-b70c-43a0-a616-490e833a394e)


## Building & Running Python Flask Service (Docker)

![Screenshot (305)](https://github.com/user-attachments/assets/5062696b-87ca-406c-9fa1-68c7cee35319)

## Building Docker Compose (Multi-Service Setup)

![Screenshot (308)](https://github.com/user-attachments/assets/21d91d95-ae57-4a66-b8bc-569329d9a963)

![Screenshot (309)](https://github.com/user-attachments/assets/f60cb850-78c0-43eb-b5d1-85adacb0c325)

 ## Testing the Services via NGINX Proxy (localhost:8080)

### Golang Service – `/service1/hello`
![Screenshot (310)](https://github.com/user-attachments/assets/8acb890c-bcdf-4bd1-93bf-502d742ffd85)

###  Python Flask Service – `/service2/hello`
![Screenshot (311)](https://github.com/user-attachments/assets/4f4ab884-1c0b-4897-b8b8-c816c0ee8482)





