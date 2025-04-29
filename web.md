# Deploy a Web Application Using Azure App Service

## Overview

In this lab, you will install Azure extensions, sign in to Azure through Visual Studio Code, create and configure an Azure App Service, and deploy a web application.

---

## Tasks to be Completed

1. Install Azure Extensions In Vs-Code
2. Sign in to Azure from Vs-code
3. Create and Configure a Web App
4. Deploy an Application using Visual Studio Code

---

# Task 1: Install Azure Extensions in VS Code

1. Open **Visual Studio Code** and navigate to the **Extensions(1)** view.

    ![Open Extensions](1.png)

2. Search(2) for **Azure Resources(3)** extension and install it.

    ![Search Azure Resources](2.png)

3. After installing Azure Resources, search for and install the **Azure App Service(4) & Azure Resources** extension.

    ![Install Azure App Service](3.png)

---

# Task 2: Sign in to Azure

1. Click on the **Azure(5)** icon in the Activity Bar to open the **Azure Resources** panel.

    ![Open Azure Panel](4.png)

2. Click **Sign in to Azure(6)**.

    ![Sign In Button](5.png)

3. A window will open. Click **Allow(7)** to proceed.

    ![Browser Sign In](6.png)

4. Enter your **Email Address(8)** and click **Next**.

    ![Enter Email](7.png)

5. Click **Send Notification(9)** to complete the sign-in.

    ![Enter Password](8.png)

6. Approve the **sign-in request(10)** from your device.

    ![Approve Sign In](9.png)

7. Select your appropriate **Tenant(12)** if required.

    ![Allow Permissions](10.png)

8. Then click on **Allow(13)** to login.

    ![Select Tenant](11.png)

---

# Task 3: Create and Configure a Web App

1. In the **Azure** panel, click on **App Services(15)**.

    ![Open App Services](12.png)

2. Click **+ Create New Web App(16)**.

    ![Create New Web App](13.png)

3. Select a **Region(17)**.

    ![Select Resource Group](14.png)

4. Provide a **Unique App Name(18)**.

    ![Enter App Name](15.png)

5. Choose the **Runtime Stack(19)** — select **Java 17(20)** (or another as needed).

    ![Select Runtime Stack](16.png)

6. Select the **Web Server Stac(21)k** — choose **Java SE**.

    ![Select Web Server Stack](17.png)

7. Select the **Pricing Tier** — choose **Free (F1)(22)**.

    ![Select Pricing Tier](18.png)

8. Web App deployment will begin automatically.

    ![Deployment Progress](19.png)

9. Monitor the status of the deployment and verify the settings(23).

    ![Deployment Status](20.png)

---

# Task 4: Deploy an Application to Web App

1. Create a local folder to store your application code.

    ![Create Local Folder](22.png)

2. After deployment, right-click on the created Web App in **App Services** and select **Deploy to Web App(26)**.

    ![Deploy to Web App](23.png)

3. Select your **Application Folder(27)** for deployment.

    ![Select Application Folder](24.png)

4. Enter the **Port Range(27)** you wish to use and press **Enter**.

    ![Enter Port Range](25.png)

5. Confirm by clicking **Deploy(28)** in the popup window.

    ![Confirm Deployment](26.png)

6. Upon successful deployment, VS Code will display a notification. Click **Browse Website(29)**.

    ![Deployment Notification](27.png)

7. Your web application will open in a **browser window(30)**.

    ![Web App Opened](28.png)

---

# End of Lab

---
