# Module 1: Core Architectural Components

## Key Services
- **Regions**: Geographic locations with data centers (e.g., East US, West Europe)
- **Availability Zones**: Physically separate datacenters within a region
- **Resource Groups**: Logical containers for Azure resources
- **Subscriptions**: Billing boundaries with access control

## Important Concepts
1. **Region Pairs**: Most regions paired for disaster recovery (e.g., East US ↔ West US)
2. **Service Availability**: Not all services available in all regions
3. **Resource Group Rules**:
   - Resources can exist in only one RG
   - RGs can't be nested

## CLI Commands
```bash
# List all regions
az account list-locations --query "[].{Name:name, DisplayName:displayName}" -o table

# Create resource group
az group create --name MyRG --location eastus
