# GKE Terraform Project

## Overview
This project contains Terraform configurations for deploying resources on Google Kubernetes Engine (GKE).

## Prerequisites
- [Terraform](https://www.terraform.io/downloads.html) installed on your machine.
- Google Cloud account with the necessary permissions to create GKE clusters and other resources.

## Setup
1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd gke-terraform
   ```

2. Configure your Google Cloud credentials:
   ```bash
   gcloud auth login
   gcloud config set project <your-project-id>
   ```

3. Initialize Terraform:
   ```bash
   terraform init
   ```

## Usage
To create the GKE cluster and other resources defined in the Terraform configuration, run:
```bash
terraform apply
```

## Cleanup
To destroy the resources created by Terraform, run:
```bash
terraform destroy
```

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
