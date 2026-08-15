# 🛒 RoboShop — AWS DevOps Project

RoboShop is a microservices-based e-commerce application that I used to build and practice an end-to-end **AWS DevOps environment**.

The project covers infrastructure provisioning, configuration management, containerization, CI/CD, Kubernetes deployment, security scanning, monitoring, and troubleshooting.

## 🏗️ Architecture

<img width="1536" height="1024" alt="architecture" src="https://github.com/user-attachments/assets/9930ad4e-97e1-49b8-8865-db153947891e" />

**Architecture & Project Discussion:**
**My Linkedin post:** https://lnkd.in/p/dM6CWCbm

### Deployment Flow

```text
Developer
   ↓
GitHub / GitFlow
   ↓
Jenkins CI/CD
   ↓
Build → Test → SonarQube → Trivy
   ↓
Docker Image
   ↓
Amazon ECR
   ↓
Amazon EKS
   ↓
Kubernetes Services
   ↓
Monitoring & Logging
```

## 🛠️ Tech Stack

| Area            | Tools                                  |
| --------------- | -------------------------------------- |
| Cloud           | AWS                                    |
| Infrastructure  | Terraform                              |
| Configuration   | Ansible                                |
| CI/CD           | Jenkins                                |
| Containers      | Docker                                 |
| Orchestration   | Kubernetes / EKS                       |
| Registry        | Amazon ECR                             |
| Version Control | Git / GitHub                           |
| Security        | SonarQube, Trivy, IAM, Security Groups |
| Monitoring      | Prometheus, Grafana, CloudWatch        |
| Databases       | MongoDB, MySQL, Redis, RabbitMQ        |

## ☁️ AWS Infrastructure

The infrastructure is designed using a multi-tier AWS architecture:

* VPC with public and private subnets
* Internet Gateway and NAT Gateway
* Application Load Balancer
* Amazon EKS for container orchestration
* IAM and Security Groups
* S3 for storage
* Route 53 and CloudFront for application access
* CloudWatch for monitoring and logging

Infrastructure is provisioned using **Terraform** to make the environment repeatable and easier to manage.

## 🔄 CI/CD Pipeline

Jenkins automates the application delivery process:

1. Code is pushed to GitHub.
2. Jenkins is triggered through a webhook.
3. Source code is checked out.
4. Application is built and tested.
5. SonarQube performs code-quality analysis.
6. Trivy scans for vulnerabilities.
7. Docker image is built.
8. Image is pushed to Amazon ECR.
9. Application is deployed to Kubernetes/EKS.
10. Deployment and application health are verified.

## ☸️ Kubernetes

The application is deployed as independent Kubernetes workloads.

I worked with:

* Deployments
* Services
* Namespaces
* Configurations
* Container images
* Application manifests
* Kubernetes troubleshooting

The architecture is designed to support **scaling, self-healing, rolling deployments, and multi-AZ availability**.

## 🏗️ Infrastructure as Code

Terraform is organized into reusable components for:

```text
terraform-aws-vpc
terraform-aws-eks
terraform-roboshop-component
```

This allows AWS infrastructure to be created consistently instead of configuring resources manually.

## ⚙️ Configuration Management

Ansible is used for server configuration and automation.

The project includes reusable Ansible roles and playbooks for installing and configuring required components.

## 📊 Monitoring & Troubleshooting

Monitoring is implemented using:

* Prometheus
* Grafana
* AWS CloudWatch

The focus is not only on monitoring metrics but also on **identifying and troubleshooting real deployment and infrastructure issues**.

Examples of troubleshooting areas include:

* Failed deployments
* Container failures
* Kubernetes pod issues
* CI/CD pipeline failures
* Docker image problems
* AWS networking issues
* Application connectivity issues

## 🔐 DevSecOps

Security checks are integrated into the CI/CD workflow using:

* SonarQube for code quality
* Trivy for vulnerability scanning
* IAM for access control
* Security Groups for network-level protection
* AWS WAF for web protection
* Secrets management for sensitive configuration

## 📁 Repository Structure

```text
Roboshop-Project/
│
├── ansible-roboshop-roles-tf/
├── jenkins-shared-library/
├── kubernetes/
├── roboshop-docker/
├── roboshop-documentation/
├── shell-roboshop-v2/
├── terraform-aws-eks/
├── terraform-aws-vpc/
└── terraform-roboshop-component/
```

## 🎯 Key Takeaways

Through this project, I gained hands-on experience with:

* AWS networking and infrastructure
* Terraform-based infrastructure provisioning
* Ansible automation
* Docker and containerization
* Kubernetes and Amazon EKS
* Jenkins CI/CD
* DevSecOps practices
* Monitoring and troubleshooting
* High-availability architecture
* Cloud cost optimization

The main goal was to understand **how the tools work together as one DevOps system**, rather than learning each tool independently.

## 🔗 Project & LinkedIn

**GitHub:**
https://github.com/Syam-devs/Roboshop-Project

**Architecture & Project Discussion:**
https://lnkd.in/p/dM6CWCbm

**AWS | Kubernetes | Terraform | Jenkins | Docker | Ansible**

