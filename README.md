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

### Reset for permanent mount
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/daaa9b09-f879-4c7d-b350-f0565c26fcca" />





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

Created a Terraform configuration file (main.tf) defining an Azure Resource Group using the AzureRM provider.
terraform {
  required_providers {
    azurerm = {
      source  = "hashicorp/azurerm"
      version = "~>4.0"
    }
  }
}

provider "azurerm" {
  features {}
}

resource "azurerm_resource_group" "lab" {
  name     = "june-fifth-terraform-demo-rg"
  location = "East US"
}

resource "azurerm_virtual_network" "lab_vnet" {
  name                = "terraform-demo-vnet"
  address_space       = ["10.0.0.0/16"]
  location            = azurerm_resource_group.lab.location
  resource_group_name = azurerm_resource_group.lab.name
}

resource "azurerm_subnet" "lab_subnet" {
  name                 = "terraform-demo-subnet"
  resource_group_name  = azurerm_resource_group.lab.name
  virtual_network_name = azurerm_virtual_network.lab_vnet.name
  address_prefixes     = ["10.0.1.0/24"]
}

### Terraform Initialization

Initialized the Terraform working directory with terraform init, which downloaded the Azure provider and prepared the environment for deployment.

### Terraform Plan

Executed terraform plan to preview infrastructure changes before deployment and verify the expected resources would be created.

### Terraform Apply

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/ae0ec1d8-360c-4d7c-bc9f-9c4b0015407b" />

### Vnet Created
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/5b524d2c-81e4-4ead-b660-8111a2a8747d" />

### Subnet Deployed
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/bcde1d37-626b-4052-9a8c-445fc73f4d51" />
###Tetraform plan matches: "No changes. Your infrastructure matches the configuration."
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/71601759-2771-4f90-80eb-8f9a54bfa426" />


## Key Takeaways

This project demonstrates Infrastructure as Code (IaC) using Terraform to automate Azure resource deployment instead of manually creating resources through the Azure Portal.

## Author

Nick Stach
