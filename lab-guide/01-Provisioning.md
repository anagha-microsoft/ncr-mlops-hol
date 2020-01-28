# Module 1 - Provisioning

## About
This module covers provisioning of resources for the lab.  Please follow the steps carefully, and sequentially to ensure you dont run into issues.
<br><br>Dedicate 20-30 minutes to complete this module if new to Azure.  Otherwise, you can complete modules in parallel and complete is 15 minutes
## 1.0. Provision a resource group
1. Logon to the Azure portal (portal.azure.com), and sign-in to your Azure subscription<br>
2. Create a resource group as shown in the screenshots below<br>
![rg-1](../images/0001-create-rg-1.png)
<br>
<hr>
<br>

## 2.0. Provision an Azure Machine Learning Service instance
1.  Navigate into the resource group from #1.0.2 above<br>
2.  Click on "+ Add" and type "Azure Machine Learning"<br>
3.  Follow the steps below to provision the service<br>
Ensure you pick the same region as your resource group <br><br>

![aml-1](../images/0001-create-aml-1.png)
<br>
<hr>

![aml-2](../images/0001-create-aml-2.png)
<br>
<hr>

Click create<br>
![aml-3](../images/0001-create-aml-3.png)
<br>
<hr>

Enter the details and click n "create"<br>
![aml-4](../images/0001-create-aml-4.png)
<br>
<hr>

You should see this...<br>
![aml-5](../images/0001-create-aml-5.png)
<br>
<hr>
<br>

## 3.0. Provision a Storage Account (blob storage)
Note: We are using blob storage in this lab for simplicity.<br>
We are also not using the AML dataset abstraction for the same reason.  <br>
For an actual project, consult your Microsoft CSA for guidance.<br><br>

1.  Navigate into the resource group from #1.0.2 above<br>
2.  Click on "+ Add" and type "Storage Account"<br>
3.  Follow the steps below to provision the service<br>
Note - Storage account names are globally unique so you will not be able to use the exact same name as mine.  Consider a suffix that you can easily remember and add it to the name.<br>
Ensure you pick the same region as your resource group <br><br>

![storage-1](../images/0001-create-storage-1.png)
<br>
<hr>

![storage-2](../images/0001-create-storage-2.png)
<br>
<hr>

![storage-3](../images/0001-create-storage-3.png)
<br>
<hr>
<br>

![storage-4](../images/0001-create-storage-4.png)
<br>
<hr>

![storage-5](../images/0001-create-storage-5.png)
<br>
<hr>
<br>

## 5.0. Provision an Azure Devops Repository
Go to dev.azure.com <br>

1.  Create a new project<br>
2.  Enter details as depicted below<br><br>

![devops-1](../images/0001-create-azure-devops-1.png)
<br>
<hr>
<br>

![devops-2](../images/0001-create-azure-devops-2.png)
<br>
<hr>
<br>

![devops-3](../images/0001-create-azure-devops-3.png)
<br>
<hr>
<br>

## Recap
Its a wrap for this module.  In this module you learned to (1) connect to the Azure portal, (2) create a resource group, (3) create an AML workspace, (4) create a blob storage account, (5) provision an Azure DevOps repo, (6) create a new project in the DevOps repo

## Next steps
Move to the next module -> download notebooks and datasets
