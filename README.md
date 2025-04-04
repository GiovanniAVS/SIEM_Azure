# SIEM_Azure
## Making a SIEM implementation on Microsoft Azure

### Introduction:

This tutorial is focused on setting up a threat intelligence feed using the Microsoft Azure with Sentinel.

1) **Create Azure Virtual Machine (VM):**

Set up a new Azure VM to host MISP (Malware Information Sharing Platform).

In the Virtual machines page, select Create and then Azure virtual machine. The Create a virtual machine page opens.
![image](https://github.com/user-attachments/assets/4dd0698a-304f-424a-b5ed-e92b7c3157ce)

Create now a new name for your VM, a Group  and choose Windows Server 2022 Datacenter: Azure Edition - x64 Gen 2 for the Image. Leave the other defaults. Just pay attention to the region, if you select a distante region you may experience some lag.
![image](https://github.com/user-attachments/assets/72ba2078-f77e-432d-8471-7219dde779f5)

Under Administrator account, provide a username, such as azureuser and a password. The password must be at least 12 characters long and meet the defined complexity requirements.
![image](https://github.com/user-attachments/assets/da4de4e5-016a-4ad1-a00e-bef2dfacff84)

After a while you VM will be created
![image](https://github.com/user-attachments/assets/315bb54d-f79a-4337-94b4-afe0a4af72b1)




Install Docker:

Access the Ubuntu VM.
Install Docker to facilitate the MISP setup.
Use terminal commands to install Docker.
Clone MISP Docker Image:

Clone the MISP Docker image from GitHub to the VM.
Navigate to the cloned directory.
Configure MISP:

Set up the MISP instance using Docker.
Configure necessary settings for MISP, including default threat feeds.
Enable Threat Feeds:

Activate default threat feeds in MISP to start pulling in threat indicators.
Set Up Microsoft Sentinel:

Install the MISP data connector in Microsoft Sentinel to ingest threat intelligence.
Register a new application in Azure for API access.
Configure API Permissions:

Set up necessary permissions for the registered application to interact with MISP.
Set Environmental Variables:

Configure environmental variables in the Azure function app to connect MISP with Sentinel.
Modify Python Script:

Adjust the Python script to ensure compatibility with the single-tenant setup.
Deploy Function App:

Deploy the function app in Azure to facilitate the data transfer from MISP to Sentinel.
Test the Integration:

Run tests to ensure that the script successfully pulls threat indicators from MISP into Microsoft Sentinel.
Create Custom Alerts:

Discuss how the ingested threat intelligence indicators can be used to create custom alerts in Sentinel.
