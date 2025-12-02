# devops-portfolio-project

Full-stack application with complete CI/CD pipeline, containerization, and infrastructure automation.

## Features
- Dockerized Node.js application
- Automated CI/CD with GitHub Actions
- Infrastructure as Code using Terraform
- Monitoring with Prometheus & Grafana
- Automated testing and deployment

## Architecture
- Application: Node.js + Express
- Containerization: Docker
- CI/CD: GitHub Actions
- Infrastructure: AWS EC2 (Terraform)
- Monitoring: Prometheus + Grafana

## Setup
bash
# Local development
npm install
npm start

# Docker
docker-compose up

# Infrastructure
cd terraform
terraform init
terraform apply

# Monitoring
docker-compose -f docker-compose.monitoring.yml up

## CI/CD Pipeline
- Automated testing on PR
- Docker image build and push
- Automated deployment to AWS

## Monitoring
- Prometheus: http://localhost:9090
- Grafana: http://localhost:3001
- _________________________________________________________________
  Deploy & Test
bash
# Push to GitHub
git add .
git commit -m "Initial DevOps project setup"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/devops-portfolio-project.git
git push -u origin main

# Deploy infrastructure
cd terraform
terraform init
terraform plan
terraform apply

# Test deployment
curl http://YOUR_EC2_IP:3000
