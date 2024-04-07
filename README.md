# Terraform EKS Deployment

## Overview
This repository contains Terraform code to deploy Elastic Kubernetes Service (EKS) on AWS as infrastructure as code (IAC). The Terraform configuration includes provisioning EKS clusters along with necessary resources such as VPC, subnets, security groups, and IAM roles.

## Features
- Automated deployment of Elastic Kubernetes Service (EKS) on AWS using Terraform.
- Configuration of VPC, subnets, security groups, and IAM roles required for EKS deployment.
- Utilization of variables for customizing the deployment based on specific requirements.

## Prerequisites
Before deploying EKS using Terraform, ensure the following prerequisites are met:
1. AWS CLI installed and configured with appropriate IAM credentials.
2. Terraform installed on your local machine.
3. Basic understanding of Terraform and AWS services.

## Terraform Configuration
### Variables
The Terraform configuration utilizes variables to customize the deployment. The following variables can be configured in the `variables.tf` file:
- `region`: AWS region where EKS will be deployed.
- `cluster_name`: Name of the EKS cluster.
- `vpc_cidr_block`: CIDR block for the VPC.
- Add any additional variables as needed.

### VPC Configuration
The Terraform configuration includes the creation of a VPC with the specified CIDR block (`vpc_cidr_block`). It also creates subnets, route tables, internet gateway, and NAT gateway as necessary for EKS deployment.

### EKS Deployment
The Terraform code provisions the EKS cluster with the specified `cluster_name` in the desired AWS region (`region`). It configures necessary IAM roles, security groups, and networking settings required for EKS.

## Usage
To deploy EKS using Terraform:
1. Clone or download this repository to your local machine.
2. Customize the Terraform variables in the `variables.tf` file as per your requirements.
3. Initialize the Terraform configuration:

   ```bash
   terraform init
terraform fmt
terraform validate
terraform plan
terraform apply
