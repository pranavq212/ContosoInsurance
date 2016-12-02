# Contoso Insurance - Azure App Services Code Sample

## What is Contoso Insurance?
Contoso Insurance is a sample that demonstrates the advantages of using the Azure App Service for building Modern Applications.  It demonstrates using the following Azure App Services features.

- App Service authentication/authorization
- Continuous integration and deployment
- Mobile app server SDK
- Mobile offline sync client SDK
- Mobile file sync SDK
- Logic Apps
  - Invoking Azure Functions via web hooks
  - Sending Email
- Azure Functions
  - Web hook triggers
  - Queue triggers
- Azure Cognitive Services - Computer Vision API
- ARM Templates
- Notification Hubs
  - Push Notifications to mobile devices

The sample also demonstrates how to use other technologies including:

- ASP.NET MVC Web Site with Knockout
- ASP.NET MVC Web API
- Xamarin Forms Mobile Application
  - iOS
  - Android 
- Azure Application Insights
- HockeyApp
- Azure PaaS SQL Databases
- Entity Framework
- Azure Storage Accounts
  - Queues
  - Blobs
- Extension methods
- Custom Attributes

## Documentation ##


## How To: Integrate Hockey App with the Xamarin App for deployment and logging ##

### Integrate Hockey App with the Xamarin App to iOS ###
1. Open the [Hockeyapp](https://www.hockeyapp.net/ "Hockeyapp") site, if you have not already created a Hockey App developer account, please sign up.

    ![](Images/Deployment/HockeyApp-SignUp.png)

2. Log in to Hockey App using the developer user that you registered above, and go to the [Hockey App dashboard](https://rink.hockeyapp.net/manage/dashboard "Hockey App dashboard").

3. Click the **New App** button.

    ![](Images/Deployment/HockeyApp-NewApp.png)

4. Click the create the App **manually** instead link.

    ![](Images/Deployment/HockeyApp-ManuallyCreate.png)

5. Enter your app information and click the **Save** button.

   ![](Images/Deployment/HockeyApp-CreatDetail.png)

6. Copy the **App Id**, you will use it later.
   ![](Images/Deployment/HockeyApp-CopyAppId.png)

7. Use Visual Studio 2015 to open the **ContosoInsurance-Mobile.sln** Visual Studio Solution.

8. Build the iOS project, and upload your iOS **.ipa** file to the iOS Hockey App that you created above.

   > **Note:** Be sure that tester's iOS UDID has been included in your Apple provision file before build.

    ![](Images/Deployment/HockeyApp-AddNewAppFile.png)

9. Enter the release notes for the build, then click **Next Step**

   ![](Images/Deployment/HockeyApp-AddNewAppStep1.png)

10.  Configure the **Status** according to the screen shot below, then click **Next Step**.

    ![](Images/Deployment/HockeyApp-AddNewAppStep2.png)

11.  Configure **Notify** according to the screen shot below, then click **Send**.

   ![](Images/Deployment/HockeyApp-AddNewAppStep3.png)

12.  The confirmation screen will look like this after you have uploaded the file and configured the App successfully.

    ![](Images/Deployment/HockeyApp-AddNewAppFileSuccessfully.png)

13.  Click the **Invite User** button to invite a test user to test the App.

    ![](Images/Deployment/HockeyApp-InviteUser.png)

14.  Enter the tester's email address and click **Save**.

    ![](Images/Deployment/HockeyApp-InviteUserTest.png)

### Integrate Hockey App with the Xamarin App to Android ###
1. Log in to Hockey App using the developer user that you registered above, and go to the [Hockey App dashboard](https://rink.hockeyapp.net/manage/dashboard "Hockey App dashboard").
2. Click the **New App** button.

    ![](Images/Deployment/HockeyApp-NewApp.png)

3. Click the create the App **manually** instead link.

    ![](Images/Deployment/HockeyApp-ManuallyCreate.png)

4. Enter your app information and click the **Save** button.

   ![](Images/Deployment/HockeyApp-CreatDetailAndroid.png)

5. Copy the **App Id**, you will use it later.

   ![](Images/Deployment/HockeyApp-CopyAppIdAndroid.png)

6. Use Visual Studio 2015 to open the **ContosoInsurance-Mobile.sln** Visual Studio Solution.

7. Build the Android project, and upload the Android **.apk** file to the Android Hockey App that you created above.

    ![](Images/Deployment/HockeyApp-AddNewAppFileAndroid.png)

8. Enter the release notes for the build, then click **Next Step**

   ![](Images/Deployment/HockeyApp-AddNewAppStep1.png)

9. Configure the **Status** according to the screen shot below, then click **Next Step**.

    ![](Images/Deployment/HockeyApp-AddNewAppStep2.png)

10. Configure **Notify** according to the screen shot below, then click **Send**.

   ![](Images/Deployment/HockeyApp-AddNewAppStep3.png)

11. The confirmation screen will look like this after you have uploaded the file and configured the App successfully.

    ![](Images/Deployment/HockeyApp-AddNewAppFileSuccessfullyAndroid.png)

12. Click the **Invite User** button to invite a test user to test the App.

    ![](Images/Deployment/HockeyApp-InviteUser.png)

13.  Enter the tester's email address and click **Save**.

    ![](Images/Deployment/HockeyApp-InviteUserTest.png)

### Download the iOS Hockey App to an iOS device and test it ###
1. Open the [Hockey App dashboard](https://rink.hockeyapp.net/manage/dashboard "Hockey App dashboard"), and log into Hockey App using the tester user you sent the email to.
2. Open the **ContosoInsurance.iOS** Hockey App, and Click **Download**.

    ![](Images/Deployment/HockeyApp-DownloadOS.png)

3. **Install** the app with iTunes.

   > **Note:** Be sure that your device UDID has been included in your Apple provision file.

4. Open the **Settings** page and enter the iOS App Id that you copied above.

	![](Images/Deployment/HockeyApp-PastAppId.png)

5. Touch the **Save** button, and **restart** the app. 
	
   > **Note:** You must restart the App to enable the new Hockey App Id after saving the configuration value.

6. Test.

### Download the Android Hockey App to an Android device and test it ###
1. Open the [Hockey App dashboard](https://rink.hockeyapp.net/manage/dashboard "Hockey App dashboard"), and log into Hockey App using the tester user you sent the email to.
2. Open the **ContosoInsurance.Droid** Hockey App, and Click **Download**.

    ![](Images/Deployment/HockeyApp-DownloadAndroid.png)

3. Copy the .apk file to your Android device and install it.

4. Open the **Settings** page and enter the Android App Id that you copied above.

	![](Images/Deployment/HockeyApp-PastAppIdAndroid.png)

5. Touch the **Save** button, and **restart** the app. 
	
   > **Note:** You must restart the App to enable the new Hockey App Id after saving the configuration value.

6. Test.

### Explore Hockey App Crashes/Events ###
1. Open the [Hockey App dashboard](https://rink.hockeyapp.net/manage/dashboard "Hockey App dashboard"), and log into Hockey App using the developer user that you created above.
2. Open the Hockey App you wish to explore and the click **Crashes/Events** tab to see the logs.

    ![](Images/Deployment/HockeyApp-events.png)

3. You can explore HockeyApp data in Application Insights!  To do this follow the steps in this [link](https://azure.microsoft.com/en-us/documentation/articles/app-insights-hockeyapp-bridge-app/ "Exploring HockeyApp data in Application Insights") to configure the Hockey App Bridge to Application Insights.

    ![](Images/Deployment/HockeyApp-Insight.png)

## How To: Install the web application for local execution and debugging ##

1. Use Visual Studio 2015 to open the **src/Cloud/ContosoInsurance-Cloud.sln** Visual Studio Solution file.
2. Right click the **ContosoInsurance.Web** project and select **Set as StartUp Project**.  
3. Press **F5**.
4. Observe the web browser open and load the Contoso Insurance claims search page.

## How To: View the custom events and metrics in Application Insights to monitor and debug the application

The sample logs status information and exceptions to Application Insights for every step in the process.  This starts moment they are received from the mobile app and continues until the very end when a claim is manually approved or rejected by the claims adjuster.

To view the custom events and metrics in Application Insights follow these steps.

1. Open https://portal.azure.com in a web browser and log in.
2. Click the **Application Insights** link in the left menu.
3. Click the **contosoinsurance** Application Insights application that was created when you deployed all the components.
4. Click **Search**.

    ![](Images/Deployment/App-Insights-Search.png)

5. Observe all of the Custom Events.

    ![](Images/Deployment/App-Insights-Search-Results.png)

6. Click a Custom Event in the list to see the metrics logged for the event.

    >**Note:**  You can refer to the Application Insights Logging Matrix in the [Azure Components document](/Azure Components.docx) to see all of the Custom Metrics logged for each Custom Event.  In the example below you can see this custom event was written by the HandleNewClaim Azure Function when it invoked the ClaimAutoApprover Azure Function.

    ![](Images/Deployment/App-Insights-Custom-Event.png)

**Track an individual claim**

Each claim has a CorrelationId associated with it.  You can see this in the screenshot above.  The CorrelationId is used to track the claims from the moment they are received from the mobile app until the end of the process.  You can track the flow of a single claim through the Azure components and the web application by using the CorrelationId.  Here's how to do it:

1. Copy the CorrelationId from a Custom Event.
2. Click **Search**.

        ![](Images/Deployment/App-Insights-Search.png)

3. Paste the CorrelationId into the **Search textbox** and observe all the Custom Events associated with the CorrelationId.

        >**Note:**  This is an excellent way to debug errors in the system and is also especially helpful to determine how long a given step takes to execute.  This sample typically processes claims from the point where they are submitted in the mobile app to the point where they are ready for manual approval in 15 seconds when running the sample on the most basic App Services service level!

        ![](Images/Deployment/App-Insights-Search-Results-CorrelationId.png) 

**Track an individual claim with Application Insights Analytics**

In addition to viewing all the Custom Events associated with a CorrelationId in the Application Insights Search interface, you can use Application Insights Analytics to track an individual claim.

Here is the query to run in Application Insights Analytics to track an individual claim's CorrelationId.

```
customEvents
    | where customDimensions.CorrelationId =~ "<YOUR CORRELATION ID>"
    | project timestamp, customDimensions.LogType, name, customMeasurements, customMeasurements.Host, customDimensions.Description, customDimensions.FunctionName, customDimensions.Status, customDimensions.Version
| order by timestamp asc
```
As you can see below, this claim took 22 seconds to process.

![](Images/Deployment/Application-Insights-Analytics.png)

## How To: Wipe all claims ##

As you use the demo, many claims will accumulate in the databases and in the blob storage container.  To wipe the claims and reset the demo, perform the the following steps:

1. Open the Web App in a web browser and log in.

   ![](Images/Deployment/azure-web-app.png)

2. Click the **username** at the top right of the page:

   ![](Images/Deployment/admin-user-info.png)

3. Click **Wipe Claims**.

   ![](Images/Deployment/admin-wipe-claims.png)

## How To: Test Notifications on the Android simulator/device ##

> **Note:** Make sure [Google Play Service](https://play.google.com/store/apps/details?id=com.google.android.gms&hl=en "Google Play Service") has been installed on your Android simulator/device before testing notifications.

1. Run the **ContosoInsurance.Droid** project on the Android simulator.
2. Step-by-Step, submit a claim successfully.

	![](Images/Deployment/Android-submit-a-claim.png)

3. Go to the Contoso Insurance web site.
4. Search the claim that you just submitted above and go to the claim detail page.
5. **Approve** or **Reject** the claim.

	![](Images/Deployment/approve-a-claim.png)	

6. The Android simulator will display the notification on the status bar.

	![](Images/Deployment/android-display-notification.png)	

## How To: Test Notifications on iOS devices ##

> **Note:** You must use a physical iOS device test notifications because the iOS simulator does not support push notifications.

1. Run the **ContosoInsurance.iOS** app on an iOS device.
2. Step-by-Step, submit a claim successfully.

	![](Images/Deployment/ios-submit-a-claim.png)

3. Go to the Contoso Insurance web site.
4. Search the claim that you just submitted above and go to the claim detail page.
5. **Approve** or **Reject** the claim.

	![](Images/Deployment/approve-a-claim.png)	

6. The iOS device will display the notification.

	![](Images/Deployment/ios-display-notification.png)	

## How To: Take an new Picture on the Android simulator ##

If you want to print out the demo images for license plates, insurance cards, and driver's licenses and use the simulator to take a picture of them, here's how to do it.

>**Note:** Here, we use the **5" KitKat(4.4) XXHDPI Phone (Android 4.4 - API19)** simulator to demonstrate these steps.


>**Note:** You must configure your simulator to use a web cam attached to your computer to take a picture.  See these [instructions](https://developer.android.com/studio/run/managing-avds.html) to learn how to do this.

1. Open the ContosoInsurance App in the Android simulator.

2. Click the **Camera** button.

	![](Images/Deployment/Android-camerabuttonClick.png)

3. Click the **More** button on the bottom bar.

	![](Images/Deployment/Android-galleryClickMenu.png)

4. Click the **Capture picture** button.

	![](Images/Deployment/Android-galleryClickCapturePicture.png)

5. Take a new picture.

6. Select the new picture you just took.

	>**Note:** In this example there was no web cam attached to the Android Simulator, that's why you see the checkerboard image.  When you have a web cam attached to your simulator you will see the image of what the web cam is looking at.

	![](Images/Deployment/Android-gallerySelectPicture.png)
 
## Contributors
| Roles                                    | Author(s)                                |
| ---------------------------------------- | ---------------------------------------- |
| Project Lead / Architect / Documentation | Todd Baginski (Microsoft MVP, Canviz Consulting) @tbag |
| Mobile Apps                              | Cloris Sun (Canviz Consulting)           |
| Web Apps                                 | Albert Xie (Canviz Consulting)           |
| Azure Components, Services, Deployment   | Tyler Lu (Canviz Consulting) @TylerLu    |
| Testing                                  | Ring Li (Canviz Consulting)              |
| Testing                                  | Melody She (Canviz Consulting)           |
| UX Design                                | Justin So (Canviz Consulting)            |
| PM                                       | Johnny Chu (Canviz Consulting) @johnathanchu |
| PM                                       | Arthur Zheng (Canviz Consulting)         |
| Sponsor / Support                        | Donna Malayeri (Microsoft) @lindydonna   |
| Sponsor / Support                        | Cory Fowler (Microsoft) @SyntaxC4-MSFT   |
| Sponsor / Support                        | Jeremy Thake (Microsoft) @jthake         |
| Sponsor / Support                        | Jeff Hollan (Microsoft) @jeffhollan      |
| Sponsor / Support                        | Yochay Kiriaty (Microsoft) @yochay       |
| Sponsor / Support                        | Fabio Kavalcante (Microsoft)             |
| Sponsor / Support                        | Chris Gillum (Microsoft) @cgillum        |

## Version history

| Version | Date          | Comments        |
| ------- | ------------- | --------------- |
| 1.0     | Sept 26, 2016 | Initial release |

## Disclaimer
**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**
