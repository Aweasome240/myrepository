
# Deploy a Function App using Visual Studio Code Which updates the logs when a new file is uploaded in the blob storage. #

## Overview

In this lab, you will install Azure extensions, sign in to Azure through Visual Studio Code, create and configure an Azure Function App, and deploy a function app that updates the logs when a new file is uploaded in the blob storage. You will also learn how to monitor the function app and troubleshoot any issues that arise.

---
### Tasks to be Completed
1. Install the necessary Azure extensions in Visual Studio Code, Python, and Azure Functions Core Tools.
2. Sign in to Azure from Visual Studio Code.
3. Create and configure a Function App.
4. Deploy a Function App using Visual Studio Code.
5. Monitor the Function App.

---
## Task 1: Install the necessary Azure extensions in Visual Studio Code, Python, and Azure Functions Core Tools.
1. Open **Visual Studio Code** and navigate to the **Extensions(1)** view.
    
    ![Open Extensions]()

2. Search(2) for **Azure Functions(3)** extension and install it.
   
    ![Search Azure Functions]()

3. Check if Python is Installed on Your System
Before proceeding, ensure Python is already installed. You can verify this by opening a terminal or command prompt and typing:
   ```bash
   python --version
   ```
    ![Check Python Version]()
4. Install the Azure Functions Core Tools. You can do this by running the following command in your terminal:
   ```bash
   npm install -g azure-functions-core-tools@4 --unsafe-perm true
   ```
    This command installs the Azure Functions Core Tools globally on your machine, allowing you to create and manage Azure Functions from the command line.
     
     ![Install Azure Functions Core Tools]()

5. After installing the Azure Functions Core Tools, you can verify the installation by running the following command in your terminal:
   ```bash
   func --version
   ```

    This command should return the version of the Azure Functions Core Tools you just installed.
    
     ![Verify Azure Functions Core Tools]()

---
## Task 2: Sign in to Azure from Visual Studio Code
1. Click on the **Azure(5)** icon in the Activity Bar to open the **Azure Functions** panel.
    
    ![Open Azure Panel]()

2. Click **Sign in to Azure(6)**.
   
    ![Sign In Button]()

3. A window will open. Click **Allow(7)** to proceed.
   
    ![Browser Sign In]()

4. Enter your **Email Address(8)** and click **Next**.
   
    ![Enter Email]()

5. Click **Send Notification(9)** to complete the sign-in.
   
    ![Enter Password]()

6. Approve the **sign-in request(10)** from your device.
   
    ![Approve Sign In]()

7. Select your appropriate **Tenant(12)** if required.
   
    ![Allow Permissions]()

8. Then click on **Allow(13)** to login.
   
    ![Select Tenant]()  

---
## Task 3: Create and Configure a Function App

1. In the **Vsual Studio Code** click the following keyboard shortcut **Ctrl + Shift + P** to open the command palette.
   
    ![Open Command Palette]()

2. Type **Azure Functions: Create New Project** and select it.
   
    ![Create New Project]()

3. Select a location for your project and click **Select Folder**.
   
    ![Select Folder]()

4. Select **Python** as the language for your function app.
   
    ![Select Python]()

5. Select the **Python interpreter version** you want to use for your function app.
   
    ![Select Python Interpreter]()

6. Select the **Blob Trigger** template for your function app.
   
    ![Select Blob Trigger]()

7. Enter a name for your function app and click **Enter**.
   
    ![Enter Function Name]()

8. Enter the **name of the Container** you want to use for your function app and click **Enter**.
   
    ![Enter Container Name]()

9. Select the **Create a new local.settings.json file** option.
   
    ![Select Local Settings]()

10. Select the **Subscription** in which you have hosted the storage account.
    
    ![Select Subscription]()

11. Select the **Use Azure Storage for remote storage** option.
    
    ![Select Azure Storage]()

12. Select the **Storage Account** you want to use for your function app.
    
    ![Select Storage Account]()

13. Select The option **Open in current window**.
    
    ![Open in Current Window]()

14. It will start the process of creating the function app. Once it is done, you will see a new folder with the name of your function app in the **Explorer** view.
    
    ![Function App Created]()

15. Now open the **local.settings.json** file and add the Storage Account connection string to the **AzureWebJobsStorage** key.
    
    ![Add Storage Account Connection String]()

    Hint: You can find the connection string in the **Azure Portal** by navigating to your Storage Account, selecting **Access keys**, and copying the connection string 
    from there.
    
    ![Access Keys]()

17. Now open the terminal in Visual Studio Code and click Fn + F5 to run the function app locally.
    
    ![Run Function App Locally]()

18. You should see the following output in the terminal, indicating that the function app is running locally and waiting for a blob to be uploaded.
   
    ![Function App Running Locally]()

19. Now you have successfully created and configured a function app that will trigger when a new file is uploaded to the specified blob storage container. 

### Great work! Let’s move on to the next step to see it in action. ##

## Task 4: Deploy a Function App using Visual Studio Code

1. In the **Azure** panel, click on **WorkSpace** and select your local project where function app is hosted from the list.
   
    ![Select Workspace]()

2. Right-Click on the **local project** and select **Deploy to Azure** from the context menu.
    
    ![Deploy to Azure]()

3. Select the **Subscription** in which you want to deploy the function app.
    
    ![Select Subscription]()

4. Create a new **Function App** in the selected subscription.
    
    ![Create New Function App]()

5. Enter a name for your function app and click **Enter**.
    
    ![Enter Function App Name]()

6. Select the **Location** where you want to deploy the function app.
    
    ![Select Location]()

7. Select the **Runtime Stack** for your function app.
    
    ![Select Runtime Stack]()

8. Select the **Instance Memory Type** for your function app(2048).
    
    ![Select Instance Memory Type]()

9. Enter the **100 in Maximum Number of Instances** and click **Enter**.
    
    ![Enter Maximum Number of Instances]()

10. Now the deployment process will start. You can monitor the progress in the **Output** panel.
    
    ![Deployment Progress]()

11. It will show an popup message indicating that ** Are you sure you want to deploy the function app**. Click **Deploy** to proceed.
    
    ![Deployment Confirmation]()

12. Confirm Successful Deployment
Once the deployment is complete, you’ll see a confirmation message indicating that your Function App has been successfully deployed.
   
    ![Deployment Confirmation Success]()

### **Deployment complete!** Your Azure Function App is now live and ready to respond to blob storage events.
---

## Task 5: Monitor the Function App

1. You can now navigate to the **Azure Portal** and check the function app you just deployed.
   
    ![Function App in Azure Portal]()

    
2. You should see the function app listed there, along with its status and other details.
    
    ![Function App Details]()

3. Navigate to the **Function App** and select the **Environment Variables** option from the left menu.
    
    ![Environment Variables]()

4. Now you can add the **AzureWebJobsStorage** connection string to the **Environment Variables** section.
    
    ![Add Environment Variables]()

5. Now go to the **Overview** section of the function app and navigate to the **Functions** section.
    
    ![Functions Section]()

6. Click on the **Function** you just deployed to view its details.
    
    ![Function Details]()
    
7. You can monitor the **logs** to see the events triggered by the blob uploads.
        
     ![Function Logs]()

8. Now you can upload a file to the blob storage container you specified earlier and check the logs to see if the function app is triggered and logs the event.
    
    ![Upload File to Blob Storage]()

## Congratulations! You have successfully deployed a Function App using Visual Studio Code and monitored its performance. ##
## Summary ##
In this lab, you learned how to install the necessary Azure extensions in Visual Studio Code, sign in to Azure, create and configure a Function App, deploy it, and monitor its performance. You also learned how to troubleshoot any issues that arise during the deployment process. This knowledge will help you in your future projects involving Azure Functions and cloud computing.
## Additional Resources ##
- [Azure Functions Documentation](https://docs.microsoft.com/en-us/azure/azure-functions/)
- [Azure Functions Core Tools Documentation](https://docs.microsoft.com/en-us/azure/azure-functions/functions-run-local)
- [Azure Storage Documentation](https://docs.microsoft.com/en-us/azure/storage/)
    

   
