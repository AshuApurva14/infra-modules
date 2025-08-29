# Terraform Infra Modules

This repo contains reusable Terraform modules for common infrastructure components.

## 📦 Modules
- `vpc/` → Create VPC + subnets + routing
- `eks/` → Create Kubernetes cluster
- `s3/` → Create S3 bucket with policies
- `iam/` → User, groups, roles

## 🛠 Usage
Modules are designed to be used from the [`infra-live`](https://github.com/AshuApurva14/infra-live) repo.

Example:
```hcl
module "vpc" {
  source = "github.com/<your-username>/infra-modules/vpc"
  cidr_block = "10.0.0.0/16"
}
