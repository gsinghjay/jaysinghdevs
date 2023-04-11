---
title: "A Step-by-Step Guide on VPP Integration and App Deployment with Jamf Pro"
date: 2023-04-10
categories:
  - Jamf
  - VPP
tags:
  - Apple School Manager
  - Apple Business Manager
  - Volume Purchase Program
  - Jamf Pro
  - App Deployment
---
In this guide, we'll walk you through the process of integrating VPP with Jamf Pro and deploying an app to a group using Apple School Manager (ASM) and Jamf Pro. By following these steps, you'll be able to efficiently distribute apps to your organization's devices using VPP.

### Step 1: Acquire the App through ASM

1. Log in to your Apple School Manager account.
2. Navigate to the 'Apps and Books' section.

[![Apps and Books](/images/vpp-sbs/01apple-school-apps-and-books.png)](https://www.jaysingh.dev/images/vpp-sbs/01apple-school-apps-and-books.png)

3. Search for the desired app and select it.

[![Search for App](/images/vpp-sbs/02apple-school-apps-to-do.png)](https://www.jaysingh.dev/images/vpp-sbs/02apple-school-apps-to-do.png)

4. Specify the quantity and click 'Get' to acquire the app.

[![Specific Quality](/images/vpp-sbs/03apple-school-get-licenses.png)](https://www.jaysingh.dev/images/vpp-sbs/03apple-school-get-licenses.png)

5. Verify that the licenses have been purchased.

[![Succesful Purchasing](/images/vpp-sbs/04-apple-school-licenses-sucessful.png)](https://www.jaysingh.dev/images/vpp-sbs/04-apple-school-licenses-sucessful.png)

### Step 2: Add the App to Jamf Pro

#### For Mobile Devices:

1. In Jamf Pro, navigate to 'Devices' > 'Mobile Device Apps' > 'Volume Content'.
2. Click 'New'.
3. Search for the app you want to add and click 'Next'.
4. Configure the app settings as needed and click 'Save'.

#### For Computers:

1. In Jamf Pro, navigate to 'Computers' > 'Mac Apps'.
2. Click 'New'.
3. Select 'Mac App Store'.
4. Search for the app you want to add and click 'Next'.
5. Configure the app settings as needed and click 'Save'.

After completing these steps, the app will be added to Jamf Pro and will be available for deployment to your organization's devices and computers.

### Step 3: Deploy the App to a Group

#### For Mobile Devices:

1. In Jamf Pro, navigate to 'Devices' > 'Apps' > 'Volume Content'.
2. Locate the app you want to deploy and click its name.
3. In the 'General' tab, scroll down to the 'App Assignment' section.
4. Select the 'User-Based VPP' or 'Device-Based VPP' assignment method.
5. Click the 'Add' button in the 'Scope' tab.
6. Select the group you want to deploy the app to and click 'Add'.
7. Click 'Save'.

#### For Computers:

1. In Jamf Pro, navigate to 'Computers' > 'Mac App Store Apps'.
2. Click 'New'.
3. Search for the app you want to deploy and click 'Next'.
4. Configure the app settings as needed and click 'Save'.
5. Click the 'Scope' tab and click the 'Add' button.

[![Scope](/images/vpp-sbs/08-scope.png)](https://www.jaysingh.dev/images/vpp-sbs/08-scope.png)


6. Select the group you want to deploy the app to and click 'Add'.
7. Click 'Save'.
8. Click the 'Managed Distribution'.
9. Go to 'Device Assignments' and check the box 'Assign Content Purchased in Volume' and click save.

[![Select VPP Account](/images/vpp-sbs/09-assign-content-purchased-in-volume.png)](https://www.jaysingh.dev/images/vpp-sbs/09-assign-content-purchased-in-volume.png)

By following these steps, you can successfully integrate VPP with Jamf Pro and deploy apps to your organization's devices and computers using Apple School Manager and Jamf Pro.

[![Updated VPP](/images/vpp-sbs/10-updated-vpp.png)](https://www.jaysingh.dev/images/vpp-sbs/10-updated-vpp.png)[![Updated ASM](/images/vpp-sbs/11-updated-asm.png)](https://www.jaysingh.dev/images/vpp-sbs/11-updated-asm.png)




[Source from Jamf Pro Documentation](https://docs.jamf.com/10.26.0/jamf-pro/administrator-guide/Integrating_with_Volume_Purchasing.html)
