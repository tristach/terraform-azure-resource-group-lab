# Terraform-azure-resource-group-lab

## Overview

This project demonstrates Infrastructure as Code (IaC) using Terraform and Microsoft Azure.

The goal of the lab is to automate Azure resource deployment rather than creating resources manually through the Azure Portal.

## Skills Demonstrated

- Terraform
- Infrastructure as Code (IaC)
- Microsoft Azure
- Azure Resource Groups
- Azure Cloud Shell
- Azure CLI
- GitHub Documentation

## Environment

- Microsoft Azure
- Azure Cloud Shell
- Terraform
- GitHub

## Project Steps

### Lessons Learned

Azure Cloud Shell sessions may not preserve working directories created in temporary locations. Persistent storage and source control (GitHub) should be used to retain Infrastructure-as-Code files between sessions.

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/af8c2f17-3bc8-4b6b-881e-27a44cb93dc7" />

### 1. Create Terraform Configuration

Created a Terraform configuration file (`main.tf`) defining:

- Azure provider
- Resource group
- Japan East region

```terraform
resource "azurerm_resource_group" "demo" {
  name     = "terraform-demo-rg"
  location = "Japan East"
}
```

#### Screenshot

![Terraform Configuration](upload-image-here)

### 2. Initialize Terraform

Executed:

```bash
terraform init

## Terraform Configuration

The following Terraform configuration creates an Azure Resource Group in Japan East.

```terraform
resource "azurerm_resource_group" "demo" {
  name     = "terraform-demo-rg"
  location = "Japan East"
}
```

## Screenshots

### Terraform Configuration

(Add Screenshot Here)

### Terraform Initialization

(Add Screenshot Here)

### Terraform Plan

(Add Screenshot Here)

### Terraform Apply

(Add Screenshot Here)

## Key Takeaways

This project demonstrates Infrastructure as Code (IaC) using Terraform to automate Azure resource deployment instead of manually creating resources through the Azure Portal.

## Author

Nick Stach
