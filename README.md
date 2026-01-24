## Project Overview

Completed a hands-on CI/CD integration project using Jenkins with Amazon EKS, with a focus on automating Kubernetes deployments and securely managing cloud credentials.
The work involved configuring AWS credentials within Jenkins and building a Jenkins pipeline to deploy Dockerized applications to an EKS cluster. This setup enabled Jenkins to interact safely with both AWS and Kubernetes as part of an end-to-end CI/CD workflow.

## Technologies and Tools

- Jenkins
Used to define and run CI/CD pipelines that build, package, and deploy applications automatically.

- AWS CLI
Verified AWS access and permissions locally to ensure correct integration with Jenkins pipelines.

- kubectl
Executed Kubernetes commands from Jenkins to deploy, update, and validate workloads running on EKS.

- Jenkins Credentials Plugin
Stored and injected AWS access keys securely into Jenkins pipelines without exposing sensitive data in code.

## Key Takeaways

- Secure CI/CD Credential Handling
Learned how to manage and bind AWS credentials safely within Jenkins jobs using built-in credential management.

- Pipeline as Code
Created a multi-stage Jenkinsfile to automate application builds, containerization, and deployments in a repeatable way.

- Automated Kubernetes Deployments
Integrated kubectl commands into Jenkins pipelines to deploy applications and verify their status on Amazon EKS.

## Issues Encountered and Resolutions

- Protecting Sensitive Information
Prevented hardcoding of AWS credentials by applying best practices for secrets management in Jenkins.

- Jenkins and EKS Integration
Resolved access and permission issues by validating IAM roles, AWS credentials, and Kubernetes configuration files.

## Practical Impact

This project demonstrates how CI/CD pipelines can be securely integrated with cloud-native platforms. By combining Jenkins automation with proper credential management and Kubernetes deployment workflows, it enables reliable, repeatable application delivery to EKS clusters—an essential capability for modern DevOps and cloud engineering environments.