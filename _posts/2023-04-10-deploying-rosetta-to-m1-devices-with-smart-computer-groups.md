---
title: "Deploying Rosetta to M1 Devices with Smart Computer Groups"
date: 2023-04-10
tags: macOS jamf mdm m1 rosetta silicon DEPNotify
---

### Rosetta and Smart Computer Groups

Not all apps are universal and at the time of this post, Jamf has not released patch management for Intel and Apple Silicon based devices separately. In this environment, a majority of our devices are Intel based. If a universal package is not available, we default to using the Intel version of the package we're trying to deploy or update. Because of this, we install Rosetta depending on whether if the computer is Apple Silicon based or not through Smart Computer Groups.

#### What is it?

In a nutshell, Rosetta 2 allows Intel applications to run on Apple Silicon based devices.

[Source](https://www.howtogeek.com/822889/what-is-rosetta-2-on-mac/): What Is Rosetta 2 on Mac?

[![Configuration Profile Page for Honorlock](/jaysinghdevs/images/policies_cat_browsers_honorlock.png)](https://gsinghjay.github.io/jaysinghdevs/images/policies_cat_browsers_honorlock.png)

[Configuration Profile](/jaysinghdevs/mobileconfig/Chrome Honorlock.mobileconfig)

#### Resources To Better Handle This

- [Force Install Chrome Extensions](https://community.jamf.com/t5/jamf-pro/force-install-chrome-extensions/m-p/264801#M243294): A Jamf Nation discussion on how to force install Chrome extensions, including the Honorlock extension.
- [JSON Schema for Jamf Pro Applications and Settings MDM Payload](https://github.com/Jamf-Custom-Profile-Schemas/JSON-Schema-for-Jamf-Pro-Applications-and-Settings-MDM-Payload/tree/master/Google/Chrome): Custom JSON schema for managing Google Chrome settings and extensions through Jamf Pro.
- [Chrome Browser Management with Google and Jamf](https://www.jamf.com/blog/chrome-browser-management-with-google-and-jamf-jnuc2022/): A blog post about managing Chrome browser settings and extensions using Jamf and Google Workspace.
- [Install the Honorlock Extension](https://honorlock.kb.help/install-the-honorlock-extension/): A step-by-step guide on how to install the Honorlock extension for various platforms.
