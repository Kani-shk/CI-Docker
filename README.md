# 🚀 Docker CI/CD with GitHub Actions

This project demonstrates a simple CI/CD pipeline using **Docker** and **GitHub Actions** to automatically build and push Docker images to **Docker Hub** on every push to the `master` branch.

---

## 📦 Tech Stack

- 🐳 Docker
- ⚙️ GitHub Actions
- 🐍 Python / Flask (replaceable with any app)
- ☁️ Docker Hub

---

## 📁 Project Structure


---

## 🔧 GitHub Actions Workflow

The workflow is defined in `.github/workflows/docker-build.yml`. It does the following:

1. Checks out the source code
2. Sets up Docker Buildx
3. Logs in to Docker Hub using secrets
4. Builds the Docker image
5. Pushes the image to Docker Hub

---

## 🔐 Secrets Required

Go to your GitHub repo → **Settings** → **Secrets and variables** → **Actions** → Add the following:

| Secret Name         | Description                     |
|---------------------|---------------------------------|
| `DOCKER_USERNAME`   | Your Docker Hub username        |
| `DOCKER_PASSWORD`   | Docker Hub password or token    |

---

## 🛠️ Usage

### 🔨 Build Locally
```bash
docker build -t yourdockerusername/yourimage:latest .
docker run -p 5000:5000 yourdockerusername/yourimage:latest
