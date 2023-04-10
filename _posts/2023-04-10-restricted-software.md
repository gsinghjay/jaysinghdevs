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

[![Restricted Software](/jaysinghdevs/images/restricted_software.png)](https://gsinghjay.github.io/jaysinghdevs/images/restricted_software.png)


---


### Restricting Keyboard Setup Assistant
#### Reasoning

In our academic labs and the library, peripherials especially keyboards tend to grow legs and walk away. Either that or they get extremely dirty to the point where the lab manager or librarians will order third-party keyboards to replace existing ones. Since these are all third-party, the Keyboard Setup Assistant launches every single time an end-user logs in or uses their own keyboard (think Accessibility). 

[Source from Jamf Nation](https://community.jamf.com/t5/jamf-pro/disabling-suppressing-keyboard-setup-assistant-in-sierra/m-p/202741/highlight/true#M191463)

While the provided script doesn't work, the last solution in the post works, but with one missing detail. Make sure to check "Kill Process" as shown below.

[![Restricted Software - Keyboard Setup Assistant](/jaysinghdevs/images/restricted_software_kbsa.png)](https://gsinghjay.github.io/jaysinghdevs/images/restricted_software_kbsa.png)
