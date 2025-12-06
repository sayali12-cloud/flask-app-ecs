🚀 Flask Application Deployment Using Docker on AWS EC2

This project is a Python Flask web application that is fully containerized using Docker and can be easily deployed on an AWS EC2 instance.
It demonstrates real-world DevOps practices such as containerization, image building, and server deployment using Docker.

This setup is ideal for:

DevOps learners 👨‍💻

Cloud beginners ☁️

Students preparing for interviews 🎯

📁 What’s Inside This Project?

✅ app.py → Main Flask application code

✅ run.py → Entry point to start the Flask server

✅ requirements.txt → Python dependencies

✅ Dockerfile → Used to build the Docker image

✅ Dockerfile-multi → Multi-stage Docker build file

✅ Deployed & executed using Docker on AWS EC2

🐳 AWS EC2 + Docker Deployment Commands

Follow these exact steps to deploy the project on an EC2 Ubuntu server 👇

🛠️ Step 1: Install Docker on EC2
sudo apt update
sudo apt install -y docker.io
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker $USER
newgrp docker


🔹 Installs Docker and allows you to run it without sudo.

📥 Step 2: Clone Your GitHub Project
git clone <YOUR_GITHUB_REPO_URL>
cd <YOUR_PROJECT_FOLDER>


📂 Downloads your project into the EC2 server.

🧱 Step 3: Build the Docker Image

Using normal Dockerfile:

docker build -t flask-app .


Using multi-stage Dockerfile:

docker build -f Dockerfile-multi -t flask-app .


🐳 Creates a Docker image of your Flask application.

🚀 Step 4: Run the Docker Container
docker run -d -p 80:5000 --name flask-container flask-app


🌍 Access your live app in the browser:

http://<EC2-PUBLIC-IP>

✅ Step 5: Check Running Containers
docker ps


👀 Shows currently running containers.

📜 Step 6: View Container Logs
docker logs -f flask-container


🧾 Useful for debugging and monitoring.

🔄 Step 7: Stop, Start & Remove Containers
docker stop flask-container
docker start flask-container
docker rm flask-container


⚙️ Full container lifecycle control.

🗑️ Step 8: Remove Docker Image (If Needed)
docker rmi flask-app


🧹 Helps keep your server clean.
