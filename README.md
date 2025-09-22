# 🚀 Node.js CI/CD Pipeline with GitHub Actions & Docker

This project demonstrates how to automate **code deployment** using a **CI/CD pipeline** with **GitHub Actions**.  
A simple Node.js application is containerized using Docker and deployed to **DockerHub** automatically on every push to the `main` branch.  

---

## 📂 Project Structure

nodejs-cicd-app/

├── app.js # Sample Node.js app
├── package.json # Node.js dependencies
├── Dockerfile # Docker container setup
└── .github/
└── workflows/
└── main.yml # GitHub Actions pipeline

---

## ⚙️ Workflow Overview

The CI/CD pipeline performs the following steps:

1. **Checkout Code** – Pulls latest code from GitHub.  
2. **Setup Node.js** – Installs Node.js environment.  
3. **Install Dependencies** – Runs `npm install`.  
4. **Run Tests** – Executes basic test script.  
5. **Build Docker Image** – Creates Docker image of the app.  
6. **Push to DockerHub** – Uploads image to DockerHub repository.  

---

## 🐳 DockerHub Integration

To enable DockerHub deployment:

1. Create a DockerHub repository (e.g., `your-dockerhub-username/nodejs-cicd-app`).  
2. In GitHub, go to:  
   **Settings → Secrets and variables → Actions**  
   Add the following secrets:
   - `DOCKER_USERNAME` → your DockerHub username  
   - `DOCKER_PASSWORD` → your DockerHub password or access token  

---

## 🚀 Run Locally

Clone the repo and start the app locally:

git clone https://github.com/your-username/nodejs-cicd-app.git

cd nodejs-cicd-app

npm install

npm start

---

## 🐳 Run with Docker 

You can run the app locally using Docker:


docker build -t your-dockerhub-username/nodejs-cicd-app .

docker run -p 3000:3000 your-dockerhub-username/nodejs-cicd-app

