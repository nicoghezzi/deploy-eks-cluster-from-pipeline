# 🚀 Secure CI/CD Integration: Jenkins → AWS → EKS

![CI/CD: Jenkins](https://img.shields.io/badge/CI%2FCD-Jenkins-%23D24939?style=for-the-badge&logo=jenkins&logoColor=white)
![Cloud: AWS](https://img.shields.io/badge/Cloud-AWS-%23FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Kubernetes: EKS](https://img.shields.io/badge/Kubernetes-EKS-%23326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![CLI: kubectl](https://img.shields.io/badge/CLI-kubectl-%23326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Security: Credentials](https://img.shields.io/badge/Security-Credentials-green?style=for-the-badge&logo=shield&logoColor=white)

A hands-on CI/CD integration project focused on securely connecting Jenkins with AWS and Amazon EKS to automate Kubernetes deployments.

---

# 🚀 Secure CI/CD Integration: Jenkins → AWS → EKS

A hands-on CI/CD project integrating Jenkins with AWS and Amazon EKS to automate Kubernetes deployments while managing cloud credentials securely.

## 🏗️ Architecture & Tech Stack

**Workflow:** Jenkins → AWS CLI → Amazon EKS → Kubernetes workloads

- **CI/CD:** Jenkins Pipeline (`Jenkinsfile`)
- **Cloud:** AWS, Amazon EKS
- **Deployment:** Kubernetes, `kubectl`
- **Security:** Jenkins Credentials Plugin, AWS IAM
- **Automation:** Pipeline stages for build, packaging, and deployment

## ⚙️ Implementation

1. **AWS Access Validation:** Verified AWS CLI configuration and IAM permissions before integrating Jenkins.
2. **Pipeline Automation:** Defined pipeline stages in `Jenkinsfile` to automate application build, packaging, and deployment.
3. **Credential Management:** Used the Jenkins Credentials Plugin to inject AWS credentials at runtime instead of hardcoding sensitive values.
4. **EKS Deployment:** Configured Kubernetes access through AWS CLI and kubeconfig, deployed workloads using `kubectl`, and validated deployment status.

## 🧠 Engineering Decisions & Trade-offs

| Decision | Rationale | Trade-off |
|---|---|---|
| **Jenkins Pipeline** | Provides a customizable, code-defined workflow that integrates with existing enterprise tooling. | Requires maintenance of Jenkins agents, plugins, credentials, and build environments. |
| **Jenkins Credentials Plugin** | Keeps AWS credentials outside application code and injects them when needed. | Credentials still require rotation, access controls, and careful handling within pipeline execution. AWS IAM role assumption through OIDC can reduce reliance on long-lived credentials. |
| **AWS CLI and kubectl** | Uses standard tools to authenticate with AWS, configure EKS access, and deploy Kubernetes resources. | Adds dependencies to Jenkins agents and requires correct IAM permissions, kubeconfig, and Kubernetes authorization. |
| **Direct Kubernetes deployment from Jenkins** | Keeps the deployment workflow straightforward and easy to troubleshoot. | Couples deployment execution to Jenkins availability; GitOps tools such as ArgoCD could provide continuous reconciliation and drift detection. |

## 🛠️ Challenges & Solutions

- **Credential exposure risk:** Removed hardcoded credentials and moved sensitive values into Jenkins credential storage.
- **AWS integration issues:** Validated AWS CLI configuration and IAM permissions.
- **Kubernetes access errors:** Verified kubeconfig, cluster connectivity, and access authorization.
- **Pipeline reliability:** Aligned Jenkins execution environments, AWS authentication, and Kubernetes deployment requirements.

## ✅ Results & Key Learnings

- Established Jenkins-to-AWS integration.
- Automated Kubernetes workload deployment to Amazon EKS.
- Improved credential handling by externalizing secrets from application code.
- Developed practical experience troubleshooting IAM permissions, kubeconfig, and pipeline execution environments.

**Key takeaway:** Reliable CI/CD depends on more than pipeline syntax. It requires aligning identity, permissions, execution environments, and deployment configuration.

## 🚀 Author
Nicolas Ghezzi LinkedIn: https://www.linkedin.com/in/nghezzi/
