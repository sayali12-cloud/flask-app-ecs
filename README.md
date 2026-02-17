# 🚀 Flask Application Deployment using Docker on AWS EC2

> Forked from Vedant Tambe's open-source project and deployed independently on AWS EC2.

This project is a **Python Flask web application** that is fully **containerized using Docker** and deployed on **AWS EC2**.  
It demonstrates a real-world **DevOps workflow** including **Docker image building, container management, and cloud deployment**.

---

## 📌 Project Highlights

- ✅ Flask-based Python web application  
- ✅ Docker containerization  
- ✅ Deployment on AWS EC2  
- ✅ Multi-stage Docker build support  
- ✅ DevOps-ready structure  
- ✅ Ideal for students & DevOps beginners  

---

## 📁 Project Structure

```
app.py               → Main Flask application  
run.py               → Application entry point  
requirements.txt     → Python dependencies  
Dockerfile           → Docker build file  
Dockerfile-multi     → Multi-stage Docker file  
README.md            → Project documentation  
```

---

## 🛠️ Technologies Used

- **Python**
- **Flask**
- **Docker**
- **AWS EC2**
- **Linux (Ubuntu)**

---

# 🐳 Docker + AWS EC2 Deployment Guide

Follow these steps to run this project on an AWS EC2 instance.

---

## 🔧 Step 1: Install Docker on EC2

```bash
sudo apt update
sudo apt install -y docker.io
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker $USER
newgrp docker
```

---

## 📥 Step 2: Clone the GitHub Repository

```bash
git clone <YOUR_GITHUB_REPO_URL>
cd <YOUR_PROJECT_FOLDER>
```

---

## 🧱 Step 3: Build Docker Image

Using the default Dockerfile:

```bash
docker build -t flask-app .
```

Using the multi-stage Dockerfile:

```bash
docker build -f Dockerfile-multi -t flask-app .
```

---

## 🚀 Step 4: Run Docker Container

```bash
docker run -d -p 5000:5000 --name flask-container flask-app
```

🌍 Open in browser:

```
http://<EC2-PUBLIC-IP>:5000
```

---

## ✅ Step 5: Check Running Container

```bash
docker ps
```

---

## 📜 Step 6: View Application Logs

```bash
docker logs -f flask-container
```

---

## 🔄 Step 7: Container Management

```bash
docker stop flask-container
docker start flask-container
docker rm flask-container
```

---

## 🗑️ Step 8: Remove Docker Image (Optional)

```bash
docker rmi flask-app
```

---

## ✅ Final Output

Your Flask application is now **successfully running on AWS EC2 using Docker** ☁️🐳  
This project proves your knowledge of:

- ✔️ Docker Image Creation  
- ✔️ Docker Container Management  
- ✔️ AWS EC2 Deployment  
- ✔️ Basic DevOps Workflow  

---

## 🙌 Author

**Developed by:** Vedant Tambe  
**Role:** DevOps Enthusiast  

---

⭐ If you like this project, don’t forget to give it a **star** on GitHub!
