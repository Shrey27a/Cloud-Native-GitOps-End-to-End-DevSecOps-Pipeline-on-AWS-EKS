# Cloud-Native GitOps: End-to-End DevSecOps Pipeline on AWS EKS

This project demonstrates a **production-grade DevSecOps pipeline** for a cloud-native Tetris application. It highlights how security is integrated across every phase of the CI/CD lifecycle using a **GitOps-driven approach** with ArgoCD on AWS EKS.


---

## Architecture

The application is deployed using a modern and automated workflow:

* **CI/CD Engine:** Jenkins automates build, test, and security validation.

<img width="624" height="274" alt="image" src="https://github.com/user-attachments/assets/6f132be6-8127-4424-a4a2-f8bbfeb28fa2" />

* **DevSecOps Layer:**

  * Trivy → Container image vulnerability scanning
  * OWASP Dependency-Check → Library vulnerability detection
  * SonarQube → Code quality & static analysis
    
    <img width="1555" height="718" alt="image" src="https://github.com/user-attachments/assets/89ce2770-9405-49e6-b939-c137641f584d" />

* **GitOps Delivery:** ArgoCD ensures cluster state matches GitHub (Single Source of Truth).
  

  <img width="1915" height="663" alt="image" src="https://github.com/user-attachments/assets/800b39c5-b6f6-4875-88e7-229ba91f9a34" />




  <img width="1705" height="640" alt="image" src="https://github.com/user-attachments/assets/639ebde7-bbe4-49c1-9fa1-4866471d1123" />


  

* **Cloud Infrastructure:** Hosted on AWS EKS with Application Load Balancer (ALB) for high availability.



  <img width="1575" height="283" alt="image" src="https://github.com/user-attachments/assets/4bef1959-be53-47ca-9b0d-9bca7ca51dd9" />





  <img width="1919" height="965" alt="image" src="https://github.com/user-attachments/assets/8b3904fb-2bc3-4704-b526-8a80202c8d81" />


---

## Key Features

* **Continuous Security:** Automated scanning for containers and dependencies in every pipeline stage.
* **Code Quality:** Static analysis using SonarQube to maintain clean and secure code.
* **GitOps Workflow:** Automated deployment triggered via Git-based manifest updates.
* **Container Orchestration:** Scalable deployment using AWS EKS managed Node Groups.
* **Infrastructure as Code:** Kubernetes manifests managed through Git versioning.

---

## Project Structure

* **Tetris-V2:** React-based Tetris application source code
* **Jenkinsfile:** CI/CD pipeline definition
* **Kubernetes Manifests:** `deployment-service.yml` for EKS deployment

---

## DevSecOps Pipeline

### 1. Continuous Integration (CI - Jenkins)

* Checkout latest code from GitHub
* Perform static analysis using SonarQube
* Run dependency scan using OWASP Dependency-Check

---

### 2. Containerization & Security

* Build Docker image for production
* Scan image using Trivy
* Push image securely to Docker Hub

---

### 3. Continuous Delivery (CD - GitOps)

* Update Kubernetes manifests with latest image
* ArgoCD syncs cluster with Git repository
* Deploy application on AWS EKS

---



## Deployment

The application is deployed on **AWS EKS** and exposed via a Load Balancer, ensuring high availability and scalability.

---

## 🤝 Connect with Me

* LinkedIn: https://www.linkedin.com/in/shreya-sharma-a514092a2/
* GitHub: https://github.com/Shrey27a

---
