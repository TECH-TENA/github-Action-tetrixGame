<h1 align="center">TIC-TAC-TOE-GAME</h1>

Title:
[DEVOPS] Build End-to-End CI/CD Pipeline with EKS Deployment and Security Scans

Type:
Story

Priority:
High 🔴

Assignee:
To be assigned

Sprint:
DevOps Sprint 3 – Full Pipeline Integration

Epic:
Platform Infrastructure Automation

📌 Description:
Set up a complete DevOps pipeline for the Node.js application using GitHub Actions and AWS. The pipeline should handle testing, code quality checks, security scanning, Docker containerization, deployment to EKS, and notifications to Slack.

✅ Acceptance Criteria:
 GitHub Actions pipeline is triggered on push to main.

 EC2 instance is configured as a GitHub self-hosted runner.

 Dockerfile is created and builds the app successfully.

 Trivy scans both file system and Docker image for vulnerabilities.

 SonarQube analyzes codebase with results viewable in dashboard.

 Docker image is pushed to AWS ECR repository.

 Terraform provisions an EKS cluster with necessary resources.

 Kubernetes manifests deploy app to EKS (LoadBalancer service).

 Checkov scans Terraform code for misconfigurations.

 Slack receives deployment success/failure notifications.

 Full deployment is documented in README.md with CLI proof/screenshots.

🧱 Task Checklist:
🏗️ Infrastructure
 Spin up EC2 instance (Ubuntu) to serve as GitHub runner.

 Install Docker, AWS CLI, kubectl, and Terraform on EC2.

 Register EC2 as a GitHub self-hosted runner.

⚙️ GitHub Actions Setup
 Create .github/workflows/ci-cd.yml file.

 Add stages: checkout, install, build, test, scan, push, deploy, notify.

🐳 Docker & ECR
 Create Dockerfile for Node.js app.

 Build Docker image during workflow.

 Authenticate and push image to AWS ECR.

🔐 Security & Quality
 Add Trivy file system scan in workflow.

 Add Trivy Docker image scan in workflow.

 Integrate SonarQube static analysis.

 Add Checkov step for Terraform security.

☁️ Terraform & EKS
 Write Terraform to provision EKS cluster (modular).

 Generate kubeconfig for GitHub runner.

 Deploy deployment.yaml and service.yaml to EKS.

📬 Notifications
 Create Slack webhook and store it in GitHub Secrets.

 Add Slack message step in workflow (on success/failure).

📄 Documentation
 Update README.md with instructions for setting up and testing.

 Include screenshots or terminal outputs of key deployment stages.

🔐 Secrets Required in GitHub:
AWS_ACCESS_KEY_ID

AWS_SECRET_ACCESS_KEY

AWS_ACCOUNT_ID

SLACK_WEBHOOK

SONAR_TOKEN

ECR_REPOSITORY_URL

KUBECONFIG or EKS CLUSTER_NAME

📅 Due Date:
TBD (Estimate: 2–3 business days)


