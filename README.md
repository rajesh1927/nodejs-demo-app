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

Pipeline:

1. Checkout source code
2. Setup Node.js
3. Install dependencies
4. Run tests
5. Build Docker image
6. Login to Docker Hub
7. Push Docker image to Docker Hub

## Project Structure

nodejs-demo-app/
├── .github/
│   └── workflows/
│       └── main.yml
├── app.js
├── app.test.js
├── package.json
├── package-lock.json
├── Dockerfile
├── .dockerignore
└── README.md
