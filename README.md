# DevOps CI/CD Pipeline with Monitoring

## Overview
This project demonstrates a complete DevOps workflow:
- CI/CD using GitHub Actions
- Containerized Node.js application
- Automated deployment to AWS EC2
- Infrastructure monitoring using Prometheus and Grafana

## Architecture


GitHub → GitHub Actions → Docker Hub → AWS EC2 (Docker)
├─ App (Node.js)
├─ Prometheus
├─ Node Exporter
└─ Grafana



## Tools Used
- GitHub & GitHub Actions
- Docker & Docker Hub
- AWS EC2 (Ubuntu)
- Prometheus
- Node Exporter
- Grafana

## CI/CD Process
1. Code pushed to GitHub
2. GitHub Actions builds Docker image
3. Image pushed to Docker Hub
4. EC2 pulls latest image and redeploys container automatically

## Monitoring
- Node Exporter collects host metrics
- Prometheus scrapes metrics
- Grafana visualizes CPU, memory, disk usage

## Evidence
### Grafana Dashboard
![Grafana](screenshots/grafana-dashboard.png)

### Prometheus Targets
![Prometheus](screenshots/prometheus-targets.png)

### GitHub Actions
![CI/CD](screenshots/github-actions-success.png)

## Notes
Infrastructure was intentionally torn down after validation to manage cloud costs.

