# SIEM_Azure
Making a SIEM implementation on Microsoft Azure
Step-by-Step Summary:
Introduction:

Overview of the tutorial's focus on setting up a threat intelligence feed.
Mention of the presenter’s Patreon for additional support and content.
Create Azure Virtual Machine (VM):

Set up a new Azure VM to host MISP (Malware Information Sharing Platform).
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
