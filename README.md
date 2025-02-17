# DevSecOps-K8s-Three-Tier-App


![image](https://github.com/user-attachments/assets/66ddf5d0-1267-42b1-bad5-4334ea234d97)

# Project Overview
This project integrates DevSecOps principles into a three-tier web application running on Kubernetes (K8s), ensuring security, automation, and scalability.


🔹 Three-Tier Architecture
1️⃣ Frontend → React/Angular/Vue (Static Web App)
2️⃣ Backend → Node.js/Flask/Django (API Services)
3️⃣ Database → PostgreSQL/MySQL/MongoDB (Persistent Storage)

🛠️ Tech Stack
Infrastructure → Kubernetes, Helm, Terraform
Security → Trivy, Falco, OPA/Gatekeeper
CI/CD → GitHub Actions, ArgoCD, Jenkins
Monitoring → Prometheus, Grafana, OpenTelemetry
Networking → Istio (Service Mesh), Nginx Ingress
⚙️ Features
✔ Automated CI/CD Pipeline → Secure & seamless deployment
✔ Container Security Scanning → Scan images with Trivy
✔ Runtime Security Monitoring → Detect anomalies using Falco
✔ Infrastructure as Code (IaC) → Terraform for infrastructure provisioning
✔ Zero Trust Networking → Secure communication with Istio

🚀 Deployment Guide

🔹 Prerequisites
Kubernetes Cluster (Minikube, EKS, GKE, AKS)
Helm, Kubectl installed
Docker & Terraform for infrastructure

🔹 Steps to Deploy

1️⃣ Clone Repository

git clone https://github.com/PournimaTivatane12/DevSecOps-K8s-Three-Tier-App.git
 DevSecOps-K8s-Three-Tier-App

2️⃣ Build & Push Docker Images


docker build -t my-app-frontend ./frontend
docker build -t my-app-backend ./backend
docker push my-app-frontend:latest
docker push my-app-backend:latest

3️⃣ Deploy to Kubernetes


kubectl apply -f k8s/
4️⃣ Verify Deployment

kubectl get pods -n my-app
📊 Monitoring & Security
Run Security Scans

trivy image my-app-backend:latest
Check Kubernetes Runtime Security

falco --rules-file /etc/falco/rules.yaml
View Metrics in Grafana

kubectl port-forward svc/grafana 3000:3000

📜 Contributing
Want to contribute? Follow the contribution guidelines. PRs are welcome!

📄 License
This project is licensed under MIT License. See the LICENSE file for details.

📬 Contact
For questions or discussions, open an Issue or connect via LinkedIn.

