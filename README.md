\# Containerized Cloud REST API Deployment (Docker + AWS EC2)



This project demonstrates how to build, containerize, and deploy a Python Flask REST API on a cloud virtual machine using Docker.



\## Tech Stack

\- Python (Flask)

\- Docker

\- AWS EC2 (Ubuntu)

\- Docker Hub

\- Linux



\## What It Does

\- Exposes a REST API endpoint returning JSON.

\- Provides a /health endpoint for service monitoring.

\- Runs inside a Docker container for portability.

\- Deployed on an AWS EC2 instance and accessible via public IP.



\## Architecture

User -> AWS EC2 -> Docker Container -> Flask API

Docker Hub -> EC2 (image pull)



\## How to Run Locally

docker build -t cloud-api .

docker run -p 5000:5000 cloud-api



\## Cloud Deployment

The Docker image is pushed to Docker Hub and pulled on an AWS EC2 instance.

The container is exposed via port 5000 using security group rules and port mapping.



Public Endpoint:

http://<EC2\_PUBLIC\_IP>:5000

http://<EC2\_PUBLIC\_IP>:5000/health

## Screenshots



\### Architecture

!\[Architecture](screenshots/architecture-docker.png)



\### Live API Output

!\[API Output](screenshots/api-live.png)



\### Health Check

!\[Health](screenshots/health.png)



\### Docker Running on EC2

!\[Docker](screenshots/docker-ps.png)



\### AWS Security Group

!\[Security Group](screenshots/security-group.png)



\### Code Snapshot

!\[Code](screenshots/code.png)



