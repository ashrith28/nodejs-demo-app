# 🚀 DevOps Task 1 – CI/CD Pipeline with GitHub Actions
📌 Objective

Automate the build and deployment of a Node.js web application using GitHub Actions and DockerHub.

# ⚙️ Tools & Technologies

GitHub – Code repository & CI/CD workflows

GitHub Actions – CI/CD automation

Node.js – Sample application

Docker – Containerization

DockerHub – Image registry

# 🛠️ Steps Implemented

Created GitHub Repository – Uploaded the sample Node.js app (nodejs-demo-app).

Added GitHub Actions Workflow – Added .github/workflows/main.yml file to automate the pipeline.

Pipeline Workflow:

Runs on every push to the main branch.

Installs dependencies and runs tests.

Builds Docker image of the Node.js app.

Pushes the Docker image to DockerHub.

Secrets Configuration – Stored DOCKER_USERNAME and DOCKER_PASSWORD in GitHub secrets for authentication.

# 🐳 Docker Image

The Docker image is pushed to DockerHub:
👉 dockerhub_username/nodejs-demo-app:latest

# 📂 Project Structure
.
├── nodejs-demo-app/       # Node.js sample app
├── Dockerfile             # Docker build instructions
├── .github/
│   └── workflows/
│       └── main.yml       # CI/CD workflow
└── README.md              # Documentation

# ▶️ How to Run Locally

Clone the repo:
```
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```


Install dependencies and run app:
```
npm install
npm start
```

Build and run Docker container:
```
docker build -t nodejs-demo-app .
docker run -p 3000:3000 nodejs-demo-app
```

# ✅ Learning Outcome

By completing this task, I learned:

How to set up a CI/CD pipeline using GitHub Actions.

Automating test → build → push steps.

Securing credentials with GitHub Secrets.

Pushing Docker images to DockerHub automatically.



# Here are some screenshots of this Task


<img width="1859" height="970" alt="Screenshot from 2025-09-22 18-00-01" src="https://github.com/user-attachments/assets/46f5e2cd-9f67-48ab-a767-abfbd1941a4d" />


<img width="1859" height="970" alt="Screenshot from 2025-09-22 18-00-18" src="https://github.com/user-attachments/assets/2c0e174c-0ced-4d17-a984-f0fc3c32462d" />


<img width="1842" height="415" alt="Screenshot from 2025-09-22 18-01-46" src="https://github.com/user-attachments/assets/ffd446b4-6463-4f79-9ced-6b1ffe24ee9e" />



# Jenkins CI/CD Pipeline – Task 2 

## 📌 Objective
This project demonstrates a simple **Jenkins Pipeline** to automate the process of building and deploying a Dockerized application.

## ⚙️ Tools Used
- **Jenkins** – CI/CD automation tool  
- **Docker** – To containerize and run the application  

## 📂 Project Structure

├── Jenkinsfile # Defines the CI/CD pipeline
├── Dockerfile # Builds the app image
├── app/ # Application source code
└── README.md # Documentation

## 🚀 Pipeline Stages
1. **Checkout** – Clones the repository.  
2. **Build** – Builds a Docker image from the source code.  
3. **Test** – Runs application/unit tests (can be extended).  
4. **Deploy** – Runs the container on port 3000.  

## 🛠️ Setup Instructions
1. Install Jenkins (local or cloud).  
2. Install **Docker** on the Jenkins server.  
3. Create a **Jenkins pipeline job** and connect it to this repository.  
4. Jenkins will detect the `Jenkinsfile` and run the pipeline.

## 📸 Screenshots


<img width="1855" height="774" alt="Screenshot from 2025-09-23 19-44-35" src="https://github.com/user-attachments/assets/c600518b-54d7-4235-b3f0-b8b58ffbaaf3" />


<img width="1855" height="774" alt="Screenshot from 2025-09-23 19-44-48" src="https://github.com/user-attachments/assets/2bd8c054-8006-4ca6-939f-5c7664ed87a7" />


<img width="1855" height="774" alt="Screenshot from 2025-09-23 19-45-28" src="https://github.com/user-attachments/assets/6fae1940-a856-4d1b-a99d-12b055e44e52" />

