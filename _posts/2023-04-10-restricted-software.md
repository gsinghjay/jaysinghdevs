---
title: "Restricted Software"
date: 2023-04-10
tags: macOS jamf mdm restrictions "restricted software" "Keyboard Assistant Setup"
---

[![Restricted Software](/jaysinghdevs/images/restricted_software.png)](https://gsinghjay.github.io/jaysinghdevs/images/restricted_software.png)

### Restricted Software

In our higher education environment, there are three essential drivers that need to be kept up to date to ensure seamless audio and tablet functionality. This page provides an overview of these drivers and their respective policies.

1. Disable Keyboard Setup Assistant
2. Disable Safari
3. Restrict Upgrade to Ventura


---


[![Driver Policies](/jaysinghdevs/images/policies_cat_drivers.png)](https://gsinghjay.github.io/jaysinghdevs/images/policies_cat_drivers.png)

### Zoom
#### Zoom Audio Driver
[![Driver Policies](/jaysinghdevs/images/policies_cat_drivers_zoom.png)](https://gsinghjay.github.io/jaysinghdevs/images/policies_cat_drivers_zoom.png)

Script for Zoom Audio Driver:

```bash
#!/bin/sh
cp -R /Applications/zoom.us.app/Contents/PlugIns/ZoomAudioDevice.driver /Library/Audio/Plug-Ins/HAL/
sudo killall coreaudiod
```

This is mandatory for audio to be shared while screen sharing. If professors are having trouble sharing their sound over Zoom, the Zoom application itself must be updated as the audio driver lives within the contents of the application.

[Configuration Profile](/jaysinghdevs/mobileconfig/Zoom Permissions.mobileconfig)

[Source from Jamf Nation](https://community.jamf.com/t5/jamf-pro/zoom-app-asks-for-admin-credentials-when-trying-to-share-computer/m-p/142244/highlight/true#M131317)
