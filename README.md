# 🚀 Student Profile App – DevOps Project

## 📌 Project Overview

This project demonstrates a complete **CI/CD pipeline using Jenkins, Docker, and GitHub Webhooks**.
It is a simple **Flask-based Student Profile Application** that is automatically built and deployed whenever code is pushed to GitHub.

---

## 🛠️ Tech Stack

* **Frontend / Backend:** Flask (Python)
* **Version Control:** Git & GitHub
* **CI/CD Tool:** Jenkins
* **Containerization:** Docker
* **Automation:** GitHub Webhooks + ngrok

---

## ⚙️ Features

* Automatic code integration using Jenkins
* Docker image build on every commit
* Auto deployment using Docker container
* Real-time CI/CD pipeline execution
* Webhook-based trigger (no manual build)

---

## 🔄 CI/CD Pipeline Flow

1. Developer pushes code to GitHub
2. GitHub webhook triggers Jenkins
3. Jenkins pulls latest code
4. Docker image is built
5. Old container is stopped and removed
6. New container is deployed automatically

---

## 📂 Project Structure

```
student-profile-app/
│── app.py
│── Dockerfile
│── requirements.txt
│── package.json
│── README.md
│── .gitignore
```

---

## 🐳 Docker Commands Used

```bash
docker build -t student-app .
docker run -d -p 5001:5001 --name student-container student-app
```

---

## 🔗 Jenkins Pipeline Stages

* Clone Repository
* Build Docker Image
* Stop Old Container
* Run New Container

---

## 🌐 Webhook Integration

GitHub webhook is configured using **ngrok** to expose local Jenkins server.

---

## ▶️ How to Run Locally

1. Clone repository

```bash
git clone https://github.com/abhinayanand7/student-profile-app.git
```

2. Build Docker image

```bash
docker build -t student-app .
```

3. Run container

```bash
docker run -d -p 5001:5001 student-app
```

4. Open in browser

```
http://localhost:5001
```

---

## 📈 Outcome

* Learned real-world DevOps workflow
* Implemented CI/CD pipeline
* Automated deployment process
* Integrated multiple tools (GitHub, Jenkins, Docker)

---

## 🔮 Future Enhancements

* Deploy on AWS / Cloud
* Add Kubernetes for orchestration
* Integrate DockerHub for image storage
* Add monitoring tools (Prometheus, Grafana)

---


