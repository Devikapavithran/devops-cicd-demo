🚀 DevOps CI/CD Pipeline for Containerized Web Application
📌 Overview

This project demonstrates the implementation of a complete DevOps CI/CD pipeline to automate the build, containerization, and deployment of a Flask-based web application on AWS.

The pipeline integrates GitHub webhooks, Jenkins automation, Docker containerization, and Nginx routing to simulate a production-style deployment workflow. The system ensures consistent builds, automated release validation, and reliable application deployment.

⚙️ Architecture

Developer → GitHub Repository → Webhook Trigger → Jenkins Pipeline → Build & Test → Docker Image Build → AWS EC2 Deployment → Nginx Routing → Running Application

🛠 Tech Stack

AWS EC2 – Cloud deployment environment

Jenkins – CI/CD pipeline automation

Git & GitHub Webhooks – Version control and automated triggers

Docker – Application containerization and image management

Nginx – Reverse proxy and request routing

Linux (Ubuntu) – Server operating system

Bash – Deployment and automation scripts

systemd – Background service management

Flask – Python web application framework

🔑 Key Features

✔ End-to-end CI/CD pipeline for automated application delivery
✔ GitHub webhook-based pipeline trigger for continuous integration
✔ Docker-based containerized deployment for consistent environments
✔ Automated build and release validation through Jenkins pipelines
✔ Nginx reverse proxy configuration for routing and request handling
✔ systemd service management for reliable application execution

📂 CI/CD Workflow

1️⃣ Developer pushes application code to GitHub
2️⃣ GitHub webhook triggers the Jenkins pipeline automatically
3️⃣ Jenkins pulls the latest code from the repository
4️⃣ Application is built and validated through pipeline stages
5️⃣ Docker image is created and stored locally
6️⃣ Container is deployed on AWS EC2
7️⃣ Nginx routes incoming traffic to the Flask container
8️⃣ Health checks and logs help monitor application performance

📊 Benefits of This Pipeline

Faster and reliable application deployments

Automated build and validation workflow

Consistent runtime environments through Docker containers

Reduced manual deployment effort

Improved system monitoring and troubleshooting capability

🧠 Learning Outcomes

This project demonstrates practical understanding of:

CI/CD pipeline orchestration using Jenkins

Containerized application deployment using Docker

Cloud infrastructure deployment on AWS EC2

Reverse proxy configuration using Nginx

Service management using systemd in Linux environments

Automation of software delivery workflows

👩‍💻 Author

Devika S
B.Tech Computer Science (Data Science)
Lovely Professional University

GitHub: https://github.com/Devikapavithran
