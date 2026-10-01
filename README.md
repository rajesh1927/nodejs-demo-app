# Node.js CI/CD Pipeline

## DevOps Internship - Task 1

This project demonstrates a CI/CD pipeline using:

- GitHub
- GitHub Actions
- Node.js
- Docker
- Docker Hub

## CI/CD Workflow

The pipeline is triggered whenever code is pushed to the main branch.

Workflow:

1. Code is pushed to the GitHub repository.
2. GitHub Actions automatically starts the workflow.
3. The Node.js application is built and tested.
4. A Docker image is created.
5. GitHub Actions logs in to DockerHub using GitHub Secrets.
6. The Docker image is pushed to DockerHub.
7. The workflow completes successfully.

## Project Structure

nodejs-demo-app/
├── .github/
│   └── workflows/
│       └── main.yml
├── app.js
├── package.json
├── package-lock.json
├── Dockerfile
├── .dockerignore
└── README.md

GitHub Secrets

The following GitHub repository secrets are used:

DOCKERHUB_USERNAME
DOCKERHUB_TOKEN

The DockerHub access token is stored securely as a GitHub Secret and is not included in the source code


Run the Application Locally
Install the dependencies:

npm install
Run the application:

node app.js
Build Docker Image
docker build -t nodejs-demo-app .
Run Docker Container
docker run -p 3000:3000 nodejs-demo-app
The application can then be accessed locally on port 3000.

GitHub Actions
The CI/CD workflow is located at:

.github/workflows/main.yml
Every push to the repository can trigger the automated workflow.

DockerHub
The Docker image is published to the project's DockerHub repository through GitHub Actions.

Result
The GitHub Actions workflow completed successfully, confirming that the CI/CD pipeline is working.

.
