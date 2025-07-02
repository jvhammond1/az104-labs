# 007 - Create a Storage Account using Terraform

## Overview
This lab demonstrates how to use Terraform to deploy a Storage Account in Azure. You'll write infrastructure-as-code (IaC) using `main.tf`, upload it to Azure Cloud Shell, and run it to provision a storage account.

**Estimated Time**: 30 minutes

## Learning Objectives
- Understand Terraform's role in Infrastructure as Code (IaC)
- Write and upload a Terraform configuration file
- Use Azure Cloud Shell to apply Terraform
- Validate deployment through Azure Portal

## Task Summary
1. Sign in to Azure Portal
2. Create a `main.tf` file using Terraform syntax
3. Upload the file and run `terraform init` and `terraform apply`
4. Validate that the storage account has been created
5. Clean up all deployed resources

## Prerequisites
- Visual Studio Code (or any text editor)
- Azure subscription and Cloud Shell access

## Resources
- [Terraform by HashiCorp](https://www.terraform.io)
- [Azure Provider Documentation](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs)
- [Azure Portal](https://portal.azure.com)
