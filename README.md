# gcp-cloud
A practical repository for learning, implementing, and managing Google Cloud Platform (GCP) services using the Google Cloud CLI, Terraform, and automation practices.

📌 Overview

This repository contains hands-on examples, configurations, scripts, and infrastructure-as-code resources for commonly used GCP services.

☁️ Covered Areas
Compute — Compute Engine, Cloud Run
Storage — Cloud Storage
Networking — VPC, subnets, firewall rules, load balancing
IAM — Users, service accounts, roles, and permissions
Databases — Cloud SQL and Firestore
Containers — Google Kubernetes Engine (GKE)
Serverless — Cloud Functions and Cloud Run
Infrastructure as Code — Terraform
Monitoring — Cloud Monitoring and Cloud Logging
CI/CD — Cloud Build and GitHub Actions
📂 Repository Structure
gcp_cloud/
├── compute/
├── storage/
├── networking/
├── iam/
├── database/
├── kubernetes/
├── serverless/
├── terraform/
├── scripts/
├── docs/
└── README.md
🛠️ Prerequisites

Install and configure:

Google Cloud CLI
Terraform
Git
An active GCP project

Authenticate with GCP:

gcloud auth login
gcloud config set project PROJECT_ID

Verify the configuration:

gcloud config list
🚀 Getting Started

Clone the repository:

git clone <repository-url>
cd gcp_cloud

Enable required APIs for your project:

gcloud services enable compute.googleapis.com \
    storage.googleapis.com \
    cloudbuild.googleapis.com

For Terraform projects:

cd terraform
terraform init
terraform plan
terraform apply
🔐 Security Best Practices
Follow the principle of least privilege.
Avoid committing service-account keys or credentials.
Store secrets in Secret Manager.
Use IAM roles carefully.
Enable audit logging and monitoring.
Keep Terraform state secured.
Use separate GCP projects/environments where appropriate.

Never commit credentials, private keys, .tfstate files, or other sensitive information to Git.

📊 Architecture

Typical workloads in this repository follow a structure similar to:

Users
  │
  ▼
Load Balancer
  │
  ▼
Cloud Run / GKE
  │
  ├── Cloud SQL
  ├── Cloud Storage
  └── Secret Manager
        │
        ▼
Cloud Monitoring & Logging
🧪 Learning Goals

This repository is intended to provide practical experience with:

Deploying applications on GCP.
Designing secure cloud infrastructure.
Managing IAM and networking.
Automating infrastructure with Terraform.
Building containerized workloads.
Implementing CI/CD pipelines.
Monitoring and troubleshooting cloud resources.
🧹 Cleanup

Remove resources when they are no longer required:

terraform destroy

For manually created resources, verify and delete them from the appropriate GCP project to avoid unnecessary costs.

📚 Documentation

Detailed documentation and examples are available under the docs/ directory.

Recommended topics:

Architecture
IAM and security
Networking
Terraform
Deployment
Monitoring
Troubleshooting
🤝 Contributing

Contributions are welcome.

Fork the repository.
Create a feature branch.
Make your changes.
Test the changes.
Create a pull request.
