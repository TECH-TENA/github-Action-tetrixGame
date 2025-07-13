# 🚀 Full DevOps Pipeline: Node.js App Deployment on AWS EKS

This project demonstrates a complete DevOps workflow for a Node.js application using GitHub Actions, AWS services, Docker, security scanners, and Slack notifications.

---

## 📌 Objective

Build an automated CI/CD pipeline that performs the following:

- Lint, test, and analyze code quality
- Perform security scans on source and Docker image
- Build Docker image and push to AWS ECR
- Provision EKS cluster using Terraform
- Deploy the containerized app to EKS
- Send Slack notifications for deployment status

---

## ✅ Acceptance Criteria

- [ ] GitHub Actions pipeline is triggered on push to `main`
- [ ] EC2 instance is used as GitHub self-hosted runner
- [ ] Dockerfile builds the Node.js app
- [ ] Trivy scans source and Docker image for vulnerabilities
- [ ] SonarQube performs static code analysis
- [ ] Docker image is pushed to AWS ECR
- [ ] Terraform provisions an EKS cluster and node group
- [ ] Kubernetes deployment manifests are applied to EKS
- [ ] Checkov scans Terraform code
- [ ] Mattermost receives success/failure notifications

---

## 🛠️ Tech Stack

| Tool          | Purpose                            |
|---------------|------------------------------------|
| GitHub Actions | CI/CD pipeline orchestration       |
| EC2            | GitHub self-hosted runner          |
| Docker         | App containerization               |
| ECR            | Container registry                 |
| Terraform      | Infrastructure provisioning        |
| EKS            | App deployment on Kubernetes       |
| Trivy          | Security vulnerability scanning    |
| SonarQube      | Code quality analysis              |
| Checkov        | IaC security scanning              |
| Mattermost          | Deployment notifications           |

---

## 🧱 Setup Instructions

### 1. 🖥️ Set Up EC2 Runner
- Launch Ubuntu EC2 instance
- Install Docker, AWS CLI, `kubectl`, Terraform
- Register EC2 as a GitHub runner:
  ```bash
  ./config.sh --url https://github.com/YOUR_ORG/YOUR_REPO --token YOUR_TOKEN
  ./svc.sh install
  ./svc.sh start
