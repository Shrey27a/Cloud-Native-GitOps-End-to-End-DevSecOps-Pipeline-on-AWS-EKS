🚀 Cloud-Native GitOps: End-to-End DevSecOps Pipeline on AWS EKS
This project demonstrates a sophisticated DevSecOps pipeline for a Cloud-Native Tetris application. It showcases the integration of security at every stage of the CI/CD lifecycle, using a GitOps approach with ArgoCD on a production-grade AWS EKS cluster.


![Infrastructure Diagram](assets/Infra.gif)
🏗️ Architecture
The application is deployed using a modern, automated workflow:

CI/CD Engine: Jenkins automates the build, test, and security scanning phases.

Security (DevSecOps): Integrated Trivy for image scanning, OWASP Dependency-Check for library analysis, and SonarQube for code quality.

GitOps Delivery: ArgoCD ensures the EKS cluster state matches the GitHub manifest repository (Single Source of Truth).

Cloud Infrastructure: Hosted on Amazon EKS with an Application Load Balancer (ALB) for high availability.

✨ Key Features
🛡️ Continuous Security: Automated container and dependency scanning in the pipeline.

💎 Code Quality: Static analysis via SonarQube to maintain clean and secure code.

🔄 GitOps Workflow: Automated deployment triggered by manifest updates in GitHub.

🎡 Container Orchestration: Scalable deployment on AWS EKS using managed Node Groups.

⚙️ Infrastructure as Code: Kubernetes manifests and services managed through Git versioning.

📂 Project Structure
Tetris-V2: Source code of the React-based Tetris application.

Jenkinsfile: The pipeline script defining the automated workflow.

deployment-service.yml: Kubernetes manifests for EKS deployment and service configuration.

🛠️ DevSecOps Pipeline Stages
1. Continuous Integration (Jenkins)
Checkout: Pulling the latest code from GitHub.

Static Analysis: Code quality check using SonarQube.

Dependency Scan: Identifying vulnerable libraries with OWASP Dependency-Check.

2. Containerization & Security
Docker Build: Creating a lightweight production image.

Image Scanning: Trivy scan to ensure zero critical vulnerabilities in the Docker image.

Registry Push: Securely pushing the image to Docker Hub.

3. Continuous Delivery (GitOps & ArgoCD)
Manifest Update: Pipeline automatically updates the image tag in the Git repository.

ArgoCD Sync: ArgoCD detects changes and synchronizes the cluster state with the repo.

EKS Deployment: Application goes live on AWS EKS behind a Load Balancer.

🤝 Connect with Me
LinkedIn: Shreya Sharma

GitHub: Shrey27a
