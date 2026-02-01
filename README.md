# 🚀 AWS Infrastructure Automation with Terraform

This repository contains **Infrastructure as Code (IaC)** for deploying a cloud environment on **AWS** using **Terraform**, managed through **Google Cloud Shell**.



## 🎯 Project Overview
The goal of this project was to implement a professional DevOps workflow for provisioning cloud resources. By using Terraform, I successfully automated the deployment of a compute instance and storage, ensuring the environment is repeatable and version-controlled.

## 🛠️ Tech Stack
* **IaC Tool:** Terraform (HCL)
* **Cloud Provider:** AWS (Region: ap-south-1 Mumbai)
* **Environment:** Google Cloud Shell
* **Version Control:** Git & GitHub

## 🏗️ Resources Managed
* **EC2 Instance:** Ubuntu 24.04 LTS for compute workloads.
* **S3 Bucket:** Scalable object storage for project data.
* **VPC Networking:** Custom subnet engineering to resolve regional connectivity issues.

## 🔄 How to Use
1. **Initialize:** `terraform init`
2. **Plan:** `terraform plan`
3. **Apply:** `terraform apply`
4. **Destroy:** `terraform destroy`



## ✅ Key Learning Outcomes
* **Multi-Cloud Management:** Operating AWS resources via GCP-hosted tools.
* **Security & IAM:** Managing GitHub Personal Access Tokens (PAT) and repository permissions.
* **Git Hygiene:** Implementing `.gitignore` to prevent pushing large binary provider files (>600MB) to version control.

---
**Engineer:** Shivsurya  
**Mentor:** Ashutosh Bhakre Sir
