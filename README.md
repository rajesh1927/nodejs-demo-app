# Node.js CI/CD Pipeline

**DevOps Internship – Task 1**

This project demonstrates a CI/CD pipeline built with:

- GitHub
- GitHub Actions
- Node.js
- Docker
- Docker Hub

---

## CI/CD Workflow

The pipeline is triggered whenever code is pushed to the `main` branch.

1. Code is pushed to the GitHub repository.
2. GitHub Actions automatically starts the workflow.
3. The Node.js application is built and tested.
4. A Docker image is created.
5. GitHub Actions logs in to Docker Hub using GitHub Secrets.
6. The Docker image is pushed to Docker Hub.
7. The workflow completes successfully.

---

## Project Structure

```text
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
```

---

## GitHub Secrets

The following repository secrets are used by the workflow:

| Secret               | Purpose                     |
| -------------------- | --------------------------- |
| `DOCKERHUB_USERNAME` | Docker Hub account username |
| `DOCKERHUB_TOKEN`    | Docker Hub access token     |

The Docker Hub access token is stored securely as a GitHub Secret and is not included in the source code.

---

## Run the Application Locally

Install the dependencies:

```bash
npm install
```

Run the application:

```bash
node app.js
```

---

## Docker

Build the Docker image:

```bash
docker build -t nodejs-demo-app .
```

Run the Docker container:

```bash
docker run -p 3000:3000 nodejs-demo-app
```

The application can then be accessed locally at <http://localhost:3000>.

---

## GitHub Actions

The CI/CD workflow is located at:

```text
.github/workflows/main.yml
```

Every push to the `main` branch triggers the automated workflow.

---

## Docker Hub

The Docker image is published to the project's Docker Hub repository through GitHub Actions.

---

## Result

The GitHub Actions workflow completed successfully, confirming that the CI/CD pipeline is working.
