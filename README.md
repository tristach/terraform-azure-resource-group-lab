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

### Reset for permanent mount.

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/fe035bec-985c-411f-bd30-daba1f8c9499" />

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/90557bc4-a717-4f6a-9ebc-8ae33025796b" />

-Created a new storage account on azure cloud shell.
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/920a37d5-c0a1-4093-b82e-5fe69fac1bff" />
-New RG
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/1de00841-13bf-4e26-8048-a02235707dcc" />
-Success
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
