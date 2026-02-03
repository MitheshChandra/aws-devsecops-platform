# aws-devsecops-platform
I built a production-ready DevSecOps platform on AWS that automates the entire software lifecycle. It uses a multi-account strategy for security, Terraform for infrastructure, and ArgoCD for zero-touch Kubernetes deployments.


☁️ CloudPay Enterprise DevSecOps Platform
StatusLicense

A production-grade cloud architecture implementing GitOps, Infrastructure as Code, and Shift-Left Security on AWS. This project demonstrates how to build a scalable, secure, and compliant Kubernetes platform from scratch using AWS Control Tower and EKS.

🏗 Architecture & Request Flow
This system uses a tiered architecture for maximum security and scalability.

The Request Journey (Traffic Flow):

User: Initiates HTTPS request.
DNS: Route53 resolves domain to Load Balancer.
Edge: AWS WAF filters malicious traffic.
Ingress: AWS ALB forwards traffic to EKS Worker Nodes.
Cluster: Nginx Ingress Controller routes to specific Microservices.
Data: Private subnets host RDS databases, inaccessible from the public internet.
Key Components:

Control Plane: AWS Control Tower (Multi-Account Strategy).
Orchestration: Amazon EKS (Elastic Kubernetes Service).
Delivery: ArgoCD (Pull-based GitOps).
🛠 Tech Stack
Category	Tools
Cloud	AWS (EKS, VPC, IAM, Route53, RDS)
IaC	Terraform, Terragrunt
CI/CD	GitLab CI, ArgoCD
Security	Gitleaks, Trivy, SonarCloud, AWS WAF
Observability	Prometheus, Grafana, Loki
📋 Prerequisites
Before deploying, ensure you have:

AWS CLI v2 configured with SSO.
Terraform v1.5+.
Kubectl & Helm installed.
A registered domain name in Route53.

