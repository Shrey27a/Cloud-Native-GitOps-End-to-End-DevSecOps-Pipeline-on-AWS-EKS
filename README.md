🚀 Cloud-Native GitOps: End-to-End DevSecOps Pipeline on AWS EKS

This project showcases a production-grade DevSecOps pipeline built for a cloud-native Tetris application. It demonstrates how security can be seamlessly integrated across every phase of the CI/CD lifecycle using a GitOps-driven approach with ArgoCD on AWS EKS.
![Architecture](./assets/architecture.png)

🏗️ Architecture Overview

A fully automated and scalable workflow designed with modern DevOps + DevSecOps practices:

⚙️ CI/CD Engine: Jenkins orchestrates build, testing, and security validation.

🔐 DevSecOps Layer:

Trivy → Container image vulnerability scanning

OWASP Dependency-Check → Library vulnerability detection

SonarQube → Code quality & static analysis

🔄 GitOps Delivery: ArgoCD maintains cluster state as per Git (Single Source of Truth).

☁️ Cloud Infrastructure: Deployed on AWS EKS with Application Load Balancer for high availability.

✨ Key Features

🛡️ Continuous Security
Automated scanning for containers & dependencies at every pipeline stage.

💎 Code Quality Assurance
Static code analysis using SonarQube for maintainable and secure code.

🔄 GitOps Workflow
Deployment triggered automatically via Git-based manifest updates.

🎡 Container Orchestration
Scalable workloads managed through AWS EKS Node Groups.

⚙️ Infrastructure as Code (IaC)
Kubernetes manifests version-controlled via Git.

📂 Project Structure
├── Tetris-V2/                 # React-based Tetris application
├── Jenkinsfile               # CI/CD pipeline definition
├── k8s/
│   └── deployment-service.yml # Kubernetes deployment & service config
🛠️ DevSecOps Pipeline Stages
1️⃣ Continuous Integration (CI - Jenkins)

📥 Checkout: Pull latest code from GitHub

🔍 Static Analysis: SonarQube code quality checks

🧪 Dependency Scan: OWASP Dependency-Check for vulnerabilities

2️⃣ Containerization & Security

🐳 Docker Build: Lightweight production-ready image

🔐 Image Scan: Trivy ensures zero critical vulnerabilities

📦 Registry Push: Secure image push to Docker Hub

3️⃣ Continuous Delivery (CD - GitOps + ArgoCD)

📝 Manifest Update: Auto-update image tag in Git repo

🔄 ArgoCD Sync: Detects changes & syncs cluster state

🚀 EKS Deployment: App deployed behind Load Balancer

📸 Architecture Diagram

(Add your pipeline image here for better visualization)


🤝 Connect with Me

💼 LinkedIn: https://www.linkedin.com/in/shreya-sharma-a514092a2/

💻 GitHub: https://github.com/Shrey27a
