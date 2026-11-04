# Dockerized Python Flask Web Application

## Project Overview

This project demonstrates how to build and deploy a simple Python Flask web application inside a Docker container.

The application provides a home page and a health-check endpoint. Docker is used to package the application and its dependencies into a portable container.

## Technologies Used

- Python 3.12
- Flask
- Docker
- Linux / WSL Ubuntu
- Git & GitHub

## Project Structure

```text
docker-flask-app/
│
├── app.py
├── requirements.txt
├── Dockerfile
├── .dockerignore
└── README.md
```

## Application Features

- Simple Flask web application
- Docker image creation
- Containerized application deployment
- Port mapping
- Health-check endpoint
- Docker container management

## Prerequisites

Make sure you have installed:

- Docker
- Git
- WSL Ubuntu (optional)
- Web browser

Check Docker installation:

```bash
docker --version
```

## Step 1: Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/docker-flask-app.git

cd docker-flask-app
```

Replace `YOUR_USERNAME` with your GitHub username.

## Step 2: Build Docker Image

```bash
docker build -t flask-docker-app:v1 .
```

Verify the image:

```bash
docker images
```

## Step 3: Run Docker Container

```bash
docker run -d -p 5000:5000 --name flask-container flask-docker-app:v1
```

## Step 4: Access Application

Open your browser:

**Home Page:**

http://localhost:5000

## Step 5: Docker Management Commands

Check running containers:

```bash
docker ps
```

View all containers:

```bash
docker ps -a
```

View container logs:

```bash
docker logs flask-container
```

Stop container:

```bash
docker stop flask-container
```

Start container:

```bash
docker start flask-container
```

Remove container:

```bash
docker rm -f flask-container
```

Remove Docker image:

```bash
docker rmi Flask-Docker-App
```

## Docker Port Mapping

```text
Host Machine          Docker Container
     |                       |
     |                       |
Port 5000  ------------>  Port 5000
     |                       |
     |                       |
     +------ Flask App ------+
```

## Learning Outcomes

Through this project, I learned:

- How to create a Python Flask application.
- How to write a Dockerfile.
- How to build custom Docker images.
- How to run applications inside containers.
- How Docker port mapping works.
- How to inspect and manage Docker containers.
- How to publish a project using GitHub.

## Future Improvements

- Implement Docker Compose.
- Add Nginx as a reverse proxy.
- Configure Jenkins CI/CD pipeline.
- Push Docker images to Docker Hub.
- Deploy the application on AWS EC2.

## Author

**Rushikesh Tayare**

GitHub: https://github.com/RushikeshTayare

## License

This project is licensed under the MIT License.
