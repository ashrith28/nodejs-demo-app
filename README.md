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
