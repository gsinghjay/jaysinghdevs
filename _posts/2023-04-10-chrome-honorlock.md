---
title: "Chrome Honorlock Extension"
date: 2023-04-10
tags: macOS jamf mdm chrome honorlock
---

## Note: This solution is temporary. View resources below on how to handle this better.

### Honorlock

Honorlock is a Google Chrome extension used in our organization for online exam proctoring, helping maintain academic integrity. This page provides an overview of our current Honorlock management approach and resources for better implementation.

#### What is it?

Honorlock can be compared to LockDown Browser by Respondus. It helps ensure that students are following academic guidelines during online examinations. Currently, we use a workaround to manage permissions for the extension, involving a plist file created using [PPPC Utility](https://github.com/jamf/PPPC-Utility). This allows SpeechRecognition and ScreenCapture for standard users.

- https://honorlock.com/
- https://app.honorlock.com/install/extension

[![Configuration Profile Page for Honorlock](/jaysinghdevs/images/policies_cat_browsers_honorlock.png)](https://gsinghjay.github.io/jaysinghdevs/images/policies_cat_browsers_honorlock.png)

[Configuration Profile](/jaysinghdevs/mobileconfig/Chrome Honorlock.mobileconfig)

#### Resources To Better Handle This

- [Force Install Chrome Extensions](https://community.jamf.com/t5/jamf-pro/force-install-chrome-extensions/m-p/264801#M243294): A Jamf Nation discussion on how to force install Chrome extensions, including the Honorlock extension.
- [JSON Schema for Jamf Pro Applications and Settings MDM Payload](https://github.com/Jamf-Custom-Profile-Schemas/JSON-Schema-for-Jamf-Pro-Applications-and-Settings-MDM-Payload/tree/master/Google/Chrome): Custom JSON schema for managing Google Chrome settings and extensions through Jamf Pro.
- [Chrome Browser Management with Google and Jamf](https://www.jamf.com/blog/chrome-browser-management-with-google-and-jamf-jnuc2022/): A blog post about managing Chrome browser settings and extensions using Jamf and Google Workspace.
- [Install the Honorlock Extension](https://honorlock.kb.help/install-the-honorlock-extension/): A step-by-step guide on how to install the Honorlock extension for various platforms.
