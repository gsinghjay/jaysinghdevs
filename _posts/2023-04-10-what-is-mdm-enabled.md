---
title: "Why You Only Need One MDM-Enabled User"
date: 2023-04-10
tags: macOS jamf mdm mdm-enabled local adminstrator
---

### What is an MDM-Enabled User?

An MDM-enabled user is an account on a macOS device that has been granted additional privileges by the Mobile Device Management (MDM) server. These privileges allow the MDM server to manage user-level settings and configurations on the device.

However, having multiple MDM-enabled users on a single device can create management and security challenges. This is why it's generally recommended to have only one MDM-enabled user account. Here are some reasons behind this recommendation:

It's important to note that best practices for macOS device management often recommend avoiding MDM-enabled user accounts altogether. Instead, it is advised to use standard local accounts in combination with an MDM solution like Jamf Pro

### Why are multiple MDM-Enabled users bad?

1. Security risks: MDM-enabled local accounts grant the MDM server extensive rights and privileges on the device. This creates a potential security risk, as an attacker who gains control of the MDM server could exploit these privileges to compromise the device.
2. User experience impact: The MDM server's elevated privileges can lead to unexpected behavior and potentially negatively impact the user experience. Users may find that their settings and preferences are overridden or restricted, causing frustration and confusion.
3. Limited benefits: Although MDM-enabled local accounts provide some management capabilities, they do not offer the full range of features and functionality that a properly managed device with a standard local account can provide.
4. Configuration challenges: Configuring MDM-enabled local accounts can be complex and time-consuming. Administrators must be familiar with the intricacies of User Approved MDM and be prepared to handle issues that may arise during setup and ongoing management.
5. Inefficient management: MDM-enabled local accounts can lead to inefficient device management, as administrators must manage both the MDM server and local account settings separately. This can result in increased administrative overhead and greater potential for configuration errors.

### How does Jamf Pro Handle the creation of an MDM-Enabled user?

Sources:
- https://community.jamf.com/t5/jamf-pro/admin-account-best-practice/m-p/278364
- https://community.jamf.com/t5/tech-thoughts/mdm-capable-mdm-enabled-or-mdm-managed-users-why-to-not-use-user/ba-p/276926
- https://learn.jamf.com/bundle/jamf-pro-documentation-current/page/MDM-Enabled_Local_User_Accounts.html
