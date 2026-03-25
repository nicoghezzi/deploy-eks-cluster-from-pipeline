# 🚀 Secure CI/CD Integration: Jenkins → AWS → EKS

![CI/CD: Jenkins](https://img.shields.io/badge/CI%2FCD-Jenkins-%23D24939?style=for-the-badge&logo=jenkins&logoColor=white)
![Cloud: AWS](https://img.shields.io/badge/Cloud-AWS-%23FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Kubernetes: EKS](https://img.shields.io/badge/Kubernetes-EKS-%23326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![CLI: kubectl](https://img.shields.io/badge/CLI-kubectl-%23326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Security: Credentials](https://img.shields.io/badge/Security-Credentials-green?style=for-the-badge&logo=shield&logoColor=white)

A hands-on CI/CD integration project focused on securely connecting Jenkins with AWS and Amazon EKS to automate Kubernetes deployments.

---

## 📌 Overview

This project demonstrates how to build a secure, end-to-end CI/CD workflow:

- Configured Jenkins to authenticate with AWS securely  
- Built pipelines to deploy Dockerized applications to EKS  
- Enabled Jenkins to interact with Kubernetes using `kubectl`  
- Implemented credential management best practices  

---

## ⚙️ Core Workflow

### 1. AWS Access Validation
- Verified AWS CLI configuration locally  
- Ensured correct IAM permissions before pipeline integration  

### 2. Jenkins Pipeline Setup
- Defined multi-stage pipeline using Jenkinsfile  
- Automated build, packaging, and deployment steps  

### 3. Secure Credential Management
- Stored AWS credentials using Jenkins Credentials Plugin  
- Injected secrets securely into pipeline runtime  
- Avoided hardcoding sensitive information  

### 4. Kubernetes Deployment
- Used `kubectl` within Jenkins pipeline  
- Deployed and updated workloads on Amazon EKS  
- Validated application status post-deployment  

---

## 🧰 Tech Stack

- Jenkins (CI/CD)  
- AWS (Cloud)  
- Amazon EKS (Kubernetes)  
- kubectl (Kubernetes CLI)  
- AWS CLI  
- Jenkins Credentials Plugin  

---

## ⚠️ Challenges & Fixes

- **Protecting sensitive data** → Removed hardcoded credentials, used Jenkins secure storage  
- **AWS & Jenkins integration issues** → Validated IAM roles and CLI configuration  
- **Kubernetes access errors** → Ensured correct kubeconfig and cluster access  

---

## 💡 Key Learnings

- Secure handling of credentials is critical in CI/CD pipelines  
- Jenkins pipelines should externalize secrets using credential managers  
- Kubernetes deployments can be fully automated using CLI tools inside pipelines  
- IAM, kubeconfig, and pipeline environments must align for successful deployments  

---

## ✅ Outcome

- ✔ Secure Jenkins-to-AWS integration established  
- ✔ Automated Kubernetes deployments via pipeline  
- ✔ Credentials managed without exposing secrets  
- ✔ Reliable CI/CD workflow for EKS deployments  

---

## 🧪 Takeaway

This project highlights how to securely integrate CI/CD pipelines with cloud-native infrastructure, enabling reliable and repeatable deployments to Amazon EKS while following best practices for credential management and automation.
