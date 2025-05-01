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
    
    ![Open Extensions](1.png)

2. **Search(2)** for **Azure Functions(3)** extension and install it.
   
    ![Search Azure Functions](2.png)

3. Check if Python is Installed on Your System
Before proceeding, ensure Python is already installed. You can verify this by opening a terminal or command prompt and typing:
   ```bash
   python --version
   ```
    ![Check Python Version](3.png)

4. Install the Azure Functions Core Tools. You can do this by running the following command in your terminal:
   ```bash
   npm install -g azure-functions-core-tools@4 --unsafe-perm true
   ```
    This command installs the Azure Functions Core Tools globally on your machine, allowing you to create and manage Azure Functions from the command line.
     
     ![Install Azure Functions Core Tools](4.png)

5. After installing the Azure Functions Core Tools, you can verify the installation by running the following command in your terminal:
   ```bash
   func --version
   ```

    This command should return the version of the Azure Functions Core Tools you just installed.
    
     ![Verify Azure Functions Core Tools](5.png)

---
## Task 2: Sign in to Azure from Visual Studio Code
1. Click on the **Azure(1)** icon in the Activity Bar.
    
    ![Open Azure Panel](6.png)

2. Click **Sign in to Azure(2)**.
   
    ![Sign In Button](7.png)

3. A window will open. Click **Allow(3)** to proceed.
   
    ![Browser Sign In](8.png)

4. Enter your **Email Address(4)** and click **Next(5)**.
   
    ![Enter Email](9.png)

5. Click **Send Notification(6)** to complete the sign-in.
   
    ![Enter Password](10.png)

6. Approve the **sign-in request(7)** from your device.
   
    ![Approve Sign In](11.png)

7. Select your appropriate **Tenant(8)** and select your **subscription(9)**.
   
    ![Allow Permissions](12.png)

8. Then click on **Allow(10)** to login.
   
    ![Select Tenant](13.png)  

---
## Task 3: Create and Configure a Function App

1. In the **Visual Studio Code** click the following keyboard shortcut **Ctrl + Shift + P** to open the command palette(1).
   
    ![Open Command Palette](14.png)

2. Type **Azure Functions: Create New Project(2)** and select it.
   
    ![Create New Project](15.png)

3. Select a location for your project and click **Select Folder(3)**.
   
    ![Select Folder](16.png)

4. Select **Python(4)** as the language for your function app.
   
    ![Select Python](17.png)

5. Select the **Python interpreter version** you want to use for your function app.

6. Select the **Blob Trigger(5)** template for your function app.
   
    ![Select Blob Trigger](18.png)

7. Enter a **name for your function app(6)** and click **Enter**.
   
    ![Enter Function Name](19.png)

8. Enter the **name of the Container(7)** you want to use for your function app and click **Enter**.
   
    ![Enter Container Name](20.png)

9. Select the **Create a new local.settings.json file** option.
   
10. Select the **Subscription(8)** in which you have hosted the storage account.
    
    ![Select Subscription](21.png)

11. Select the **Use Azure Storage for remote storage(9)** option.
    
    ![Select Azure Storage](22.png)

12. Select the **Storage Account(10)** you want to use for your function app(11).
    
    ![Select Storage Account](23.png)

13. Select The option **Open in current window(12)**.
    
    ![Open in Current Window](24.png)

14. It will start the process of creating the function app. Once it is done, you will see a new folder with the name of your function app in the **Explorer** view.
    
    ![Function App Created](25.png)

15. Now open the **local.settings.json** file and add the Storage Account connection string to the **AzureWebJobsStorage(13)** key.
    
    ![Add Storage Account Connection String](26.png)

    Hint: You can find the connection string in the **Azure Portal** by navigating to your Storage Account, selecting **Access keys(14)**, and copying the connection string from there.

    ![Access Keys](27.png)

16. Now open the terminal in Visual Studio Code and click Fn + F5 to run the function app locally.
    
    ![Run Function App Locally](28.png)

17. You should see the following output in the terminal, indicating that the function app is running locally and waiting for a blob to be uploaded.
   
    ![Function App Running Locally](29.png)

18. Now you have successfully created and configured a function app that will trigger when a new file is uploaded to the specified blob storage container. 

### Great work! Let’s move on to the next step to see it in action. ##

## Task 4: Deploy a Function App using Visual Studio Code

1. In the **Azure** panel, click on **WorkSpace** and select your **local project(1)** where function app is hosted from the list.
   
    ![Select Workspace](30.png)

2. Right-Click on the **local project** and select **Deploy to Azure(2)** from the context menu.
    
    ![Deploy to Azure](31.png)

3. Select the **Subscription(3)** in which you want to deploy the function app.
    
    ![Select Subscription](32.png)

4. Create a new **Function App(4)** in the selected subscription.
    
    ![Create New Function App](33.png)

5. Enter a name for your function app and click **Enter(5)**.
    
    ![Enter Function App Name](34.png)

6. Select the **Location(6)** where you want to deploy the function app.
    
    ![Select Location](35.png)

7. Select the **Runtime Stack(7)** for your function app.
    
    ![Select Runtime Stack](36.png)

8. Select the **Instance Memory Type(8)** for your function app(2048).
    
    ![Select Instance Memory Type](37.png)

9. Enter the **100 in Maximum Number of Instances(9)** and click **Enter**.
    
    ![Enter Maximum Number of Instances](38.png)

10. Now the deployment process will start. You can monitor the progress in the **Output** panel.
    
    ![Deployment Progress](39.png)

11. It will show an popup message indicating that ** Are you sure you want to deploy the function app**. Click **Deploy(10)** to proceed.
    
    ![Deployment Confirmation](40.png)

12. Confirm Successful Deployment
Once the deployment is complete, you’ll see a confirmation message indicating that your Function App has been successfully deployed.
   
    ![Deployment Confirmation Success](41.png)

### **Deployment complete!** Your Azure Function App is now live and ready to respond to blob storage events.
---

## Task 5: Monitor the Function App

1. You can now navigate to the **Azure Portal** and check the **function app(1)** you just deployed.
   
    ![Function App in Azure Portal](42.png)

2. You should see the function app listed there, along with its status and other details(2).
    
    ![Function App Details](43.png)

3. Navigate to the **Settings(3)** and select the **Environment Variables(4)** option from the left menu.
    
    ![Environment Variables](44.png)

4. Now you can add the **AzureWebJobsStorage** connection string to the **Environment Variables** section.
    
    ![Add Environment Variables](45.png)

5. Now go to the **Overview** section of the function app and navigate to the **Functions(5)** section.
    
    ![Functions Section](46.png)

6. Click on the **Function** you just deployed to view its details(6).
    
    ![Function Details](47.png)
    
7. You can monitor the **logs** to see the events triggered by the blob uploads.
        
     ![Function Logs](48.png)

8. Now you can upload a file to the blob storage container you specified earlier and check the logs to see if the function app is triggered and logs the event.
    
    ![Upload File to Blob Storage](49.png)

## Congratulations! You have successfully deployed a Function App using Visual Studio Code and monitored its performance. ##
## Summary ##
In this lab, you learned how to install the necessary Azure extensions in Visual Studio Code, sign in to Azure, create and configure a Function App, deploy it, and monitor its performance. You also learned how to troubleshoot any issues that arise during the deployment process. This knowledge will help you in your future projects involving Azure Functions and cloud computing.
## Additional Resources ##
- [Azure Functions Documentation](https://docs.microsoft.com/en-us/azure/azure-functions/)
- [Azure Functions Core Tools Documentation](https://docs.microsoft.com/en-us/azure/azure-functions/functions-run-local)
- [Azure Storage Documentation](https://docs.microsoft.com/en-us/azure/storage/)
    

   
