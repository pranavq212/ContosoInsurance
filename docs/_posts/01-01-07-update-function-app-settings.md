---
title: Update the Function App Settings
description: 
category: SETUP
---

# Update the Contoso_ClaimAutoApproverUrl App Setting in the Function App

1. In the list of components in the Resource Group the ARM template created (pictured above), click the **ContosoInsuranceClaimAutoApprover Logic App**.

   ![](/img/deployment/azure-claim-auto-approver.png)

2. Scroll to the bottom of the blade on the right side of the screen.
3. In the **All triggers** section, click the **manual** link.
   1. In the manual blade, mouse over the **Callback url** and select **Click to copy**.

   ![](/img/deployment/get-claim-auto-approver-url.png)

4. In the list of components in the Resource Group the ARM template created (pictured above), click the **Function App**.

   ![](/img/deployment/azure-function-app.png)

5. Click the **Function app settings** link

   ![](/img/deployment/function-app-settings-link.png)

6. Click the **Configure app settings** button

   ![](/img/deployment/function-app-settings.png)

7. Paste the Callback Url you copied from the ContosoInsuranceClaimAutoApprover Logic App into the **Contoso_ClaimAutoApproverUrl** App Setting.

   ![Update appsettings of the Function App](/img/deployment/update-appsettings-of-the-function-app.png)

   >**Note:**  If you deploy the Function App again with the ARM template then you will have to manually set  the **Contoso_ClaimAutoApproverUrl** App Setting again.
