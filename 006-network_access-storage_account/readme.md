# 006 - Network Access to Storage Accounts

## Overview
In this lab, you'll create a storage account with **private endpoint access**, limiting connectivity to a virtual network (VNet). You'll also deploy a VM within the same VNet and access the storage account securely using a connection string.

**Estimated Time**: 60 minutes

## Learning Objectives
- Understand private endpoint usage in Azure Storage
- Create a secure storage account accessible only through private IP
- Connect to storage securely via an Azure VM
- Validate connectivity using Azure Storage Explorer

## Task Summary
1. Sign in to Azure Portal
2. Create a Virtual Network with a custom subnet
3. Create a Storage Account with a private endpoint
4. Deploy a Virtual Machine in the same VNet
5. Access the storage account from the VM using Storage Explorer
6. Run lab validation
7. Clean up resources

## Resources
- Azure Portal: [https://portal.azure.com](https://portal.azure.com)
- [Azure Private Endpoint Overview](https://learn.microsoft.com/en-us/azure/private-link/private-endpoint-overview)
- [Microsoft Azure Storage Explorer](https://azure.microsoft.com/en-us/products/storage/storage-explorer/)
