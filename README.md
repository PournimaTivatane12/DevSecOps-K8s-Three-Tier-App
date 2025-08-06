# 🚀 3-Tier Web Application Deployment on AWS EKS (Production-Grade)

**This architecture represents a production-grade 3-tier web app deployed on AWS EKS using Terraform, Jenkins, ArgoCD, Vault, Prometheus, Grafana, and Let’s Encrypt for HTTPS. It follows GitOps practices, is fully observable, and supports resilient, secure deployments.**

## 🗺️ Architecture Overview
<img width="2793" height="1411" alt="diagram-export-8-6-2025-9_53_38-PM" src="https://github.com/user-attachments/assets/792b66f0-2a5b-43ae-a4f0-56bcb9fb4756" />


**A complete, production-ready 3-tier web application deployment on Amazon EKS, built with:**

✅ Infrastructure as Code
✅ CI/CD Pipelines
✅ GitOps with Canary Deployments
✅ Secrets Management
✅ HTTPS + DNS
✅ Observability + Resilience
✅ Real-World Cloud Hosting

# 📌 Project Highlights

| Capability                     | Tools/Services Used                               |
| ------------------------------ | ------------------------------------------------- |
| **Infrastructure as Code**     | Terraform                                         |
| **Kubernetes Platform**        | Amazon EKS (Elastic Kubernetes Service)           |
| **CI/CD Pipelines**            | Jenkins (CI), ArgoCD (CD), Argo Rollouts (Canary) |
| **GitOps Workflow**            | ArgoCD, GitHub                                    |
| **Monitoring & Observability** | Prometheus, Grafana, OpenTelemetry, Jaeger        |
| **Secrets Management**         | AWS Secrets Manager, HashiCorp Vault              |
| **Security**                   | IAM Roles for Service Accounts, Security Groups   |
| **Resilience Testing**         | LitmusChaos (Chaos Engineering)                   |
| **Autoscaling**                | Kubernetes HPA (Horizontal Pod Autoscaler)        |
| **Ingress & Routing**          | NGINX / ALB Ingress Controller, Route 53          |
| **HTTPS & TLS**                | Let’s Encrypt + Cert-Manager                      |
| **DNS Setup**                  | Custom domain: `yourapp.dev`                      |


# Infrastructure Stack 

Terraform: Automates provisioning of:

VPC (with public/private subnets)

NAT Gateway, Internet Gateway

EKS Cluster

IAM Roles & Policies

Security Groups

# ⚙️ CI/CD Pipeline Flow

GitHub ➜ Jenkins ➜ Docker Image Build ➜ ArgoCD ➜ Canary Deploy via Argo Rollouts ➜ EKS

Code Push triggers Jenkins CI

Jenkins builds and pushes Docker images

ArgoCD watches Git and deploys updated manifests

Argo Rollouts enables controlled, canary deployments

# 🔐 Security & Secrets

Secrets Management via:

AWS Secrets Manager (native AWS secrets)

HashiCorp Vault (external secrets integration)

IAM Roles for Service Accounts (IRSA) for pod access

TLS certificates provisioned via Let’s Encrypt + cert-manager

# 📈 Observability & Monitoring

Prometheus: Metric scraping and alerts

Grafana: Custom dashboards

OpenTelemetry & Jaeger: Tracing

HPA: Autoscaling pods based on CPU metrics

# ☠️ Chaos Engineering
LitmusChaos: Injects controlled faults (e.g., pod delete, resource stress)

Ensures application resilience and recovery

# 🌐 DNS + HTTPS
cert-manager issues free TLS certificates from Let’s Encrypt

Route 53 for domain routing (e.g., https://yourapp.dev)

Users access the app securely via HTTPS

# ✅ Project Checklist

| Feature                             | Status      |
| ----------------------------------- | ----------- |
| Terraform-based Infra               | ✅ Completed |
| Jenkins CI Setup                    | ✅ Completed |
| ArgoCD GitOps                       | ✅ Completed |
| Argo Rollouts + Canary              | ✅ Completed |
| Kubernetes HPA                      | ✅ Completed |
| Vault / Secrets Manager Integration | ✅ Completed |
| cert-manager + Let’s Encrypt        | ✅ Completed |
| Route 53 DNS + HTTPS                | ✅ Completed |
| Prometheus + Grafana Dashboards     | ✅ Completed |
| LitmusChaos Fault Injection         | ✅ Completed |
| Custom Domain with SSL              | ✅ Completed |

# 📹 YouTube Demo

# 📁 Project Structure

.
├── terraform/              # Infra provisioning (VPC, EKS, IAM)
├── manifests/              # Kubernetes YAMLs (frontend, backend, DB)
├── charts/                 # Helm charts (if used)
├── jenkins/                # Jenkinsfile, pipeline configs
├── argocd/                 # ArgoCD app manifests
├── secrets/                # Vault + AWS Secrets Manager templates
├── monitoring/             # Prometheus, Grafana configs
└── README.md

# 🤝 Contributing

Contributions, suggestions, and feedback are welcome. Feel free to fork this repo, submit issues, or raise pull requests!

**📜 Contributing**
Want to contribute? Follow the contribution guidelines. PRs are welcome!

**📄 License**
This project is licensed under MIT License. See the LICENSE file for details.

**📬 Contact**
*For questions or discussions, open an Issue or connect via LinkedIn.*

