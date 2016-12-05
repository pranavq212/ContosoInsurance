---
title: Configure Authentication For Web Apps
description:
category: SETUP
---

{% include header.md %}

1. Configure the API App to use Microsoft Authentication

   ![]({{site.baseurl}}/img/deployment/azure-api-app.png)

   >**Note:** Step 1 in the article below tells you to copy the Url for your web app.  To copy the URL for your web app click the API **App Service** in the list of components in the Resource Group the ARM template created (pictured above).  Then, mouse over the **URL** and select **Click to copy**.
   >
   >![]({{site.baseurl}}/img/deployment/Copy-Web-Api-URL.png)
   {: .blockquote .alert-info }

   Follow the steps in this article: [How to configure your App Service application to use Microsoft Account login](https://azure.microsoft.com/en-us/documentation/articles/app-service-mobile-how-to-configure-microsoft-authentication/)
   ​	
   ![]({{site.baseurl}}/img/deployment/auth-api-app.png)

   > **Note:**
   >  
   > Ensure that the Action to take when a request is not authenticated is set to **Allow request (no action)**.  This is shown in the screenshot above.
   {: .blockquote .alert-warning }

   > **Note:**
   > 
   > Ensure that **wl.offline_access**, **wl.signin** and **wl.emails** are selected.  This is shown in the screenshot above.
   {: .blockquote .alert-warning }	

2. Configure the Web App to use AAD Authentication.

   ![]({{site.baseurl}}/img/deployment/azure-web-app.png)

   If the Express configuration does not work, follow the steps in the **Manually configure Azure Active Directory with advanced settings** section in this article: [How to configure your App Service application to use Azure Active Directory login](https://azure.microsoft.com/en-us/documentation/articles/app-service-mobile-how-to-configure-active-directory-authentication/)

   ![]({{site.baseurl}}/img/deployment/auth-web-app.png)

   > **Note:**
   > 
   > Ensure that the Action to take when a request is not authenticated is set to **Log in with Azure Active Directory**.  This is shown in the screenshot above.
   {: .blockquote .alert-warning }