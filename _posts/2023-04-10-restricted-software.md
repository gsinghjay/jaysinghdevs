---
title: "Restricted Software"
date: 2023-04-10
tags: macOS jamf mdm restrictions KeyboardSetupAssistant.app
---

### Restricted Software

In our higher education environment, there are three essential drivers that need to be kept up to date to ensure seamless audio and tablet functionality. This page provides an overview of these drivers and their respective policies.

1. Disable Keyboard Setup Assistant
2. Disable Safari
3. Restrict Upgrade to Ventura

[![Restricted Software](/images/restricted_software.png)](https://www.jaysingh.dev/images/restricted_software.png)


---


### Restricting Keyboard Setup Assistant
#### Reasoning

In our academic labs and the library, peripherials especially keyboards tend to grow legs and walk away. Either that or they get extremely dirty to the point where the lab manager or librarians will order third-party keyboards to replace existing ones. Since these are all third-party, the Keyboard Setup Assistant launches every single time an end-user logs in or uses their own keyboard (think Accessibility). 

[Source from Jamf Nation](https://community.jamf.com/t5/jamf-pro/disabling-suppressing-keyboard-setup-assistant-in-sierra/m-p/202741/highlight/true#M191463)

While the provided script doesn't work, the last solution in the post works, but with one missing detail. Make sure to check "Kill Process" as shown below.

[![Restricted Software - Keyboard Setup Assistant](/images/restricted_software_kbsa.png)](https://www.jaysingh.dev/images/restricted_software_kbsa.png)


---


### Restricting Safari
#### Reasoning

Restricting Safari or certain Safari features in an organization, school, or enterprise environment might be necessary for a few reasons:

1. Security: Limiting Safari features or disabling the browser altogether can help minimize potential security threats from malicious websites, phishing attempts, and malware.
2. Compliance: Organizations may need to comply with industry-specific regulations or internal policies that require them to restrict or control web browsing activities.
3. Alternative browsers: An organization may choose to restrict Safari if they prefer using another browser with better management capabilities, security features, or compatibility with their specific infrastructure.

[![Restricted Software - Safari](/images/restricted_software_safari.png)](https://jaysingh.dev/images/restricted_software_safari.png)


---


### Restricting Ventura
#### Reasoning

Major operating system updates often have significant bugs at first so it's always ideal to wait one or two versions more rolling things out.

[![Restricted Software - Install macOS Ventura](/images/restricted_software_ventura.png)](https://jaysingh.dev/images/restricted_software_ventura.png)

Since Studio Arts is a huge subject at the college, it's important we remain on 12.6.3 for as long as possible as there are still issues with Adobe products.

[Source from Adobe]([https://community.jamf.com/t5/jamf-pro/disabling-suppressing-keyboard-setup-assistant-in-sierra/m-p/202741/highlight/true#M191463](https://helpx.adobe.com/download-install/kb/macos-ventura-compatibility-common-issues.html))


