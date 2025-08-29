# PREREQUISITES

This document lists the files and configurations required to set up and run the DevSecOps Kubernetes Three-Tier Application.
The project combines frontend, backend, and database tiers with DevSecOps practices (security scanning, policy enforcement, and CI/CD).

# 🔑 Core Files

1. Dockerfile (frontend, backend, db)	Containerize each service.
2. docker-compose.yml (optional)	Local testing of all three tiers.
3. namespace.yaml	Creates an isolated namespace for the app.
4. deployment-frontend.yaml	Deploys frontend container to Kubernetes.
5. deployment-backend.yaml	Deploys backend container to Kubernetes.
6. deployment-database.yaml	Deploys database container to Kubernetes.
7. service-frontend.yaml	Exposes frontend within cluster.
8. service-backend.yaml	Exposes backend within cluster.
9. service-database.yaml	Exposes database within cluster.
10. ingress.yaml	Configures external access to frontend.
11. configmap.yaml	Stores non-sensitive application configs.
12. secret.yaml	Stores sensitive credentials (e.g., DB password).
    
# 🔒 DevSecOps Files

1. trivyignore	Ignore specific vulnerabilities when scanning images with Trivy.
2. grype.yaml (if used)	Config for Grype image scanning.
3. opa-policies/	Open Policy Agent or Kyverno security policies (e.g., block root containers, restrict registries).
4. .github/workflows/devsecops-pipeline.yml OR Jenkinsfile	CI/CD pipeline for build, test, and security scans.
   
# 📂 Testing & Monitoring

1. kube-bench-config.yaml	Security benchmark testing for Kubernetes.
2. kube-hunter.yaml	Security penetration testing inside cluster.
3. prometheus.yaml	Config for monitoring application metrics.
4. grafana-dashboards.json	Pre-built Grafana dashboards for visualization.
   
# ✅ Requirements Before Running

**Kubernetes cluster (local with Minikube/Kind, or cloud-managed like EKS/GKE/AKS).**

**kubectl installed and configured.**

**Docker (for building images).**

**Helm (if using charts instead of raw YAMLs).**

**DevSecOps tools: Trivy, OPA/Kyverno, kube-bench, kube-hunter.**

Monitoring tools: Prometheus, Grafana.

🔹 With these files and tools, the three-tier app can be deployed securely with DevSecOps best practices.
