# 🚀 ShopSphere – Production Grade AWS DevOps Platform

## 📌 Project Overview

ShopSphere is a complete production-grade cloud-native DevOps project built on AWS.
The project demonstrates end-to-end CI/CD automation using Jenkins, Docker, AWS ECR, Amazon EKS (Kubernetes), Prometheus, and Grafana.

The application is automatically built, containerized, pushed to AWS ECR, and deployed to Kubernetes using a fully automated Jenkins pipeline.

---

# ☁️ Project Architecture

```text
Developer
   ↓
GitHub Repository
   ↓
Jenkins CI/CD Pipeline
   ↓
Docker Image Build
   ↓
AWS ECR
   ↓
Amazon EKS Kubernetes Cluster
   ↓
Kubernetes Deployments & Pods
   ↓
AWS Load Balancer
   ↓
Prometheus + Grafana Monitoring
```

---

# 🔥 Technologies Used

| Category           | Tools/Services                         |
| ------------------ | -------------------------------------- |
| Cloud Platform     | AWS                                    |
| CI/CD              | Jenkins                                |
| Containerization   | Docker                                 |
| Container Registry | AWS ECR                                |
| Orchestration      | Kubernetes (EKS)                       |
| Monitoring         | Prometheus + Grafana                   |
| Version Control    | Git & GitHub                           |
| Infrastructure     | VPC, NAT Gateway, IAM, Security Groups |

---

# 🚀 Features Implemented

✅ Jenkins CI/CD Automation
✅ Docker Containerization
✅ AWS ECR Integration
✅ Amazon EKS Kubernetes Cluster
✅ Kubernetes Deployments & Services
✅ Self-Healing Pods
✅ Rolling Updates
✅ Kubernetes Scaling
✅ AWS LoadBalancer Integration
✅ Prometheus Monitoring
✅ Grafana Dashboards
✅ Automated Kubernetes Deployment

---

# 📊 Monitoring Stack

The monitoring stack includes:

* Prometheus
* Grafana
* Alertmanager
* Node Exporter
* kube-state-metrics

Grafana dashboards provide:

* CPU utilization
* Memory usage
* Pod metrics
* Cluster health visibility

---

# 🔄 CI/CD Workflow

```text
Code Push
   ↓
GitHub
   ↓
Jenkins Pipeline Trigger
   ↓
Docker Build
   ↓
Push Image to AWS ECR
   ↓
Deploy to Amazon EKS
   ↓
Rolling Update
   ↓
Live Application Updated
```

---

# ☸️ Kubernetes Features Demonstrated

* Deployments
* Services
* LoadBalancer
* Self-Healing
* Scaling
* Rolling Updates
* Zero Downtime Deployment

---

# 🛠️ Challenges Solved During Project

## 🔹 EKS Nodegroup Issue

Resolved Kubernetes worker node creation and pod density limitations.

## 🔹 Jenkins ↔ Kubernetes Authentication

Configured kubeconfig access for Jenkins user to automate deployments.

## 🔹 ECR Authentication

Integrated Jenkins with AWS ECR using IAM role-based authentication.

## 🔹 NAT Gateway & Private Subnet Networking

Configured private subnet internet access using NAT Gateway.

---

# 🚀 Future Enhancements

* Horizontal Pod Autoscaler (HPA)
* ArgoCD GitOps
* Terraform Automation
* SSL/HTTPS with Ingress
* Route53 Domain Integration
* Centralized Logging (ELK/Loki)

---

# 👨‍💻 Author

### Prajwal Ahirrao

Production Grade AWS DevOps Project 🚀

