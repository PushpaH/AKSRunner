
# This project consists of a sample Action pipelines that can be used to apply changes to an Azure Resources by running Azure CLI commands.

## Pre-requirement before running the pipeline

#### Create an Azure service principal and add the values as GitHub Action secrets under AZURE_CREDENTIALS.

#### * Pipeline YAMLs

1. maintenancewindow.yml

The following Azure CLI command is executed by maintenancewindow.yml to create a maintenance window for an Azure Container App Environment. This ensures that all non-critical updates are performed during the specified maintenance period.

az containerapp env maintenance-config add \
  --resource-group \
  --environment  \
  --weekday  \
  --start-hour-utc  \
  --duration 

Example: 
