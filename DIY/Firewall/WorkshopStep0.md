[Main Page][Prev]&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;Step 0&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Next Step][Next] >> 

# DIY Firewall Workshop - Cloud Shell Initialization (Step 0)

## Abstract
[Azure Cloud Shell][CloudShell] is an interactive, authenticated, browser-accessible shell for managing Azure resources. It provides the flexibility of choosing the shell experience that best suits the way you work, either Bash or PowerShell. We'll be using the Cloud Shell for the deployment of PowerShell scripts in today's workshop. Using the Cloud Shell provides a unified foundation to interact with Azure with all the PowerShell settings and Azure SDKs loaded, so you can start the shell and immediately begin interacting with Azure.

This initialization step (step 0) of the workshop has you start the Cloud Shell, ensure you're using the PowerShell experience, download the Workshop files, and log in using your Azure credentials.

## Observations
Once you're done with this step, you'll know more about the Azure Cloud Shell and how to get started with it.

## Deployment
1. Connect to the internet
2. Login to https://portal.azure.com
3. Start Cloud Shell (select or create a storage account if prompted)
   
    [![1]][1]
4. Ensure Cloud Shell is set to PowerShell
   
    [![2]][2]
5. In the cloud shell run
   
   ```powershell
   Connect-AzAccount -UseDeviceAuthentication
   ```
   and follow the instructions. Login using your Azure Portal credentials
6. In Cloud Shell run the following to download the workshop files
    ```powershell 
    (IWR aka.ms/1).Content | IEX
    ```
    > **NOTE**
    > A warning about the subscription ID will be shown, we’ll fix this next

7. Open the Cloud Shell editor (red circled icon)
   
    [![3]][3]
8. Navigate to init.txt (red boxed item in file hierarchy in the image above)
9.  In the right-hand pane, update the Subscription ID to your Subscription ID and optionally the RGName to use the resource group name you wish to use inside your subscription.
    > **IMPORTANT**
    >
    > All scripts in this workshop pull critical information from the init.txt file, so it’s important to update this file to reflect the resource group name and subscription you’ll be using for this deployment of the firewall workshop.  
10. Once updated, press CTRL+S to save the init.txt file.
11. Rerun the validation script, ensuring no errors and that the File Variables displayed are as intended.
    ```powershell
    ./Scripts/Validate-Lab.ps1
    ```

[Main Page][Prev]&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;Step 0&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Next Step][Next] >> 





<!--Link References-->
[Prev]: ./README.md
[Next]: ./WorkshopStep1.md
[CloudShell]: https://docs.microsoft.com/azure/cloud-shell/overview

<!--Image References-->
[1]: ./Media/CloudShellLaunch.svg "Launch Cloud Shell Icon" 
[2]: ./Media/CloudShellPowerShell.svg "Set Cloud Shell to PowerShell" 
[3]: ./Media/CloudShellEditor.svg "Open Cloud Shell file editor" 