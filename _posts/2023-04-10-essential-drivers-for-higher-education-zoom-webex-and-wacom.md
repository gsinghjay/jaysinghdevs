---
title: "Essential Drivers for Higher Education: Zoom, Webex, and Wacom"
date: 2023-04-10
tags: 
- macOS
- Zoom
- Webex
- Wacom
- Drivers
- Higher Education
- Jamf
categories: 
- macOS
- Drivers
- Jamf
---

### Essential Drivers for Higher Education: Zoom, Webex, and Wacom

In higher education settings, maintaining up-to-date drivers for Zoom, Webex, and Wacom is crucial for seamless audio and tablet functionality. This article outlines these essential drivers and their respective policies.

1. Zoom
  * Zoom Audio Driver
2. Webex
  * Cisco Webex Meetings Audio Driver
3. Wacom
  * Wacom Driver

---


[![Driver Policies](/images/policies_cat_drivers.png)](https://jaysingh.dev/images/policies_cat_drivers.png)

### Zoom
#### Zoom Audio Driver
[![Driver Policies](/images/policies_cat_drivers_zoom.png)](https://jaysingh.dev/images/policies_cat_drivers_zoom.png)

The Zoom Audio Driver is crucial for sharing audio while screen sharing. If educators experience issues sharing sound through Zoom, updating the Zoom application itself may resolve the problem, as the audio driver resides within the app's contents.

[Configuration Profile](/mobileconfig/Zoom Permissions.mobileconfig)

[Source from Jamf Nation](https://community.jamf.com/t5/jamf-pro/zoom-app-asks-for-admin-credentials-when-trying-to-share-computer/m-p/142244/highlight/true#M131317)


---


## Webex
#### Cisco Webex Meetings Audio Driver
[![Driver Policies](/images/policies_cat_drivers_webex.png)](https://jaysingh.dev/images/policies_cat_webex.png)

The [Cisco Webex Audio Driver Package](https://help.webex.com/en-us/article/WBX9000031110/Cisco-Webex-Audio-Driver-Package-Download-for-Mac) is necessary for sharing audio during screen sharing on Webex. If educators have trouble sharing sound over Webex, updating this package may help. As of the time of this post, there is no way to automatically update this driver.

[Configuration Profile (Webex)](/mobileconfig/Webex Permissions.mobileconfig)\
[Configuration Profile (Meetings)](/mobileconfig/Webex Meetings Permissions.mobileconfig)


---


### Wacom
#### Wacom Driver
[![Driver Policies](/images/policies_cat_drivers_wacom.png)](https://www.jaysingh.dev/images/policies_cat_drivers_wacom.png)

[Configuration Profile](/mobileconfig/Wacom Tablet.mobileconfig)

The Wacom Driver is deployed to all studio arts classes, open labs, and the library. It is also available as a self-service option for other devices.

[Source from Jamf Nation](https://community.jamf.com/t5/jamf-pro/monterey-m1-and-pppc-you-re-killing-us-wacom/m-p/264566)
