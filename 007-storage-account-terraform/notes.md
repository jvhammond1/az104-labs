# Notes - Create a Storage Account using Terraform

## What is Terraform?
- Open-source IaC tool developed by HashiCorp
- Declarative language (HCL) to define infrastructure
- Manages state through a `.tfstate` file
- Supports multiple cloud providers (Azure, AWS, GCP)

## Configuration Overview
The `main.tf` file in this lab includes:
1. **Provider Block**
   ```hcl
   terraform {
     required_providers {
       azurerm = {
         source  = "hashicorp/azurerm"
         version = "3.0.0"
       }
     }
   }

   provider "azurerm" {
     features {}
     skip_provider_registration = true
   }
