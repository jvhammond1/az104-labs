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
Data Block for Resource Group

hcl
Copy
Edit
data "azurerm_resource_group" "rg" {
  name = "<resource-group-name>"
}
Storage Account Resource

hcl
Copy
Edit
resource "azurerm_storage_account" "storage" {
  name                     = "mywhizstorageyourname"
  resource_group_name      = data.azurerm_resource_group.rg.name
  location                 = data.azurerm_resource_group.rg.location
  account_tier             = "Standard"
  account_replication_type = "LRS"
}
Terraform Workflow
terraform init – Downloads Azure provider and initializes config

terraform apply – Plans and applies infrastructure changes

yes – Confirms and executes the resource creation

Gotchas
Terraform files must have .tf extension

Avoid hardcoding credentials; use Azure identity or environment

Always verify the output of terraform plan before applying

Resource names must be globally unique (especially storage)

Validation
Go to Azure Portal > Resource Group > Confirm storage account exists

Ensure Terraform reports no errors after apply
