### Zoom, Webex, and Wacom Drivers

In our higher education environment, there are three essential drivers that need to be kept up to date to ensure seamless audio and tablet functionality. This page provides an overview of these drivers and their respective policies.

1. Zoom
  * Zoom Audio Driver
2. Webex
  * Cisco Webex Meetings Audio Driver
3. Wacom
  * Wacom Driver


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


---


## Webex
#### Cisco Webex Meetings Audio Driver
[![Driver Policies](/jaysinghdevs/images/policies_cat_drivers_webex.png)](https://gsinghjay.github.io/jaysinghdevs/images/policies_cat_webex.png)

[Cisco Webex Audio Driver Package](https://help.webex.com/en-us/article/WBX9000031110/Cisco-Webex-Audio-Driver-Package-Download-for-Mac) is mandatory for audio to be shared while screen sharing. If professors are having trouble sharing their sound over Webex, it's most likely this package needs to be updated. As of the time of this post, there is no way to automatically update this driver.

[Configuration Profile (Webex)](/jaysinghdevs/mobileconfig/Webex Permissions.mobileconfig)\
[Configuration Profile (Meetings)](/jaysinghdevs/mobileconfig/Webex Meetings Permissions.mobileconfig)


---


### Wacom
#### Wacom Driver
[![Driver Policies](/jaysinghdevs/images/policies_cat_drivers_wacom.png)](https://gsinghjay.github.io/jaysinghdevs/images/policies_cat_drivers_wacom.png)

[Configuration Profile](/jaysinghdevs/mobileconfig/Wacom Tablet.mobileconfig)

This is pushed out to all studio arts classes, open labs, and the library. They are a self-service option for other devices.

[Source from Jamf Nation](https://community.jamf.com/t5/jamf-pro/monterey-m1-and-pppc-you-re-killing-us-wacom/m-p/264566)