---
title: "Honorlock"
date: 2023-04-10
tags: macOS jamf mdm chrome honorlock
---

### Honorlock
#### What is it?
Honorlock is an extension for Google Chrome that can be compared to LockDown Browser by Respondus. While there are better methods to handle permissions for this specific extension (refer to the resources below), the implementation has not been completed. The quick workaround was to create a plist file using [PPPC Utility](https://github.com/jamf/PPPC-Utility) to allow SpeechRecognition and ScreenCapture for Standard Users.
 - https://honorlock.com/
 - https://app.honorlock.com/install/extension
 
[![Driver Policies](/jaysinghdevs/images/policies_cat_browsers_honorlock.png)](https://gsinghjay.github.io/jaysinghdevs/images/policies_cat_browsers_honorlock.png)

[Configuration Profile](/jaysinghdevs/mobileconfig/Chrome Honorlock.mobileconfig)

#### Resources To Better Handle This
- https://community.jamf.com/t5/jamf-pro/force-install-chrome-extensions/m-p/264801#M243294
- https://github.com/Jamf-Custom-Profile-Schemas/JSON-Schema-for-Jamf-Pro-Applications-and-Settings-MDM-Payload/tree/master/Google/Chrome
- https://www.jamf.com/blog/chrome-browser-management-with-google-and-jamf-jnuc2022/
- https://honorlock.kb.help/install-the-honorlock-extension/

