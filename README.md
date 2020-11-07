# AzSwarm/Cloud-Init
Cloud-Init files to setup a Docker Swarm cluster in Microsoft Azure

## Requirements 
In order to use the cloud-init files you will need to do the following:

* Create an Azure Resource Group
* Create an Azure Key Vault
* Create an Azure User-assigned Managed Identity
* Setup the Azure Key Vault Access Policy and give "Secret Permissions" to the User-assigned Identity

The Key Vault is used to store the Docker Swarm Join token for the managers and workers using the User-Assigned Managed Identity, in order to do this it is necessary to assign **Secret Permissions** inside the Access Policy to the created identity. Please check this Microsoft document for an example [Link](https://docs.microsoft.com/en-us/azure/key-vault/general/assign-access-policy-portal)

## Deploy Docker Swarm Manager.

In order to deploy a Docker Swarm Manager please select the **cloud-init-manager.yml** file for your distribution and replace the following values:

| Key                       |  
|---------------------------|
| subscriptionId            |   
| resourceGroupName         |   
| userAssignedIdentityName  |   
| keyVaultName              | 

After replacing the values you can create a new VM using Azure CLI and include the **cloud-init-manager.yml**. Please check this Microsoft document for an example [Link](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/using-cloud-init#deploying-a-cloud-init-enabled-virtual-machine).

## Adding a Docker Swarm Manager.

Pending

## Adding a Docker Swarm Worker.

Pending


