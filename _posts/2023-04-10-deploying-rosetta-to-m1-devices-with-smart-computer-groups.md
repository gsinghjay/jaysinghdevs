---
title: "Deploying Rosetta to M1 Devices with Smart Computer Groups"
date: 2023-04-10
tags: macOS jamf mdm m1 rosetta silicon DEPNotify
---

### Rosetta and Smart Computer Groups

Not all apps are universal and at the time of this post, Jamf has not released patch management for Intel and Apple Silicon based devices separately. In this environment, a majority of our devices are Intel based. If a universal package is not available, we default to using the Intel version of the package we're trying to deploy or update. Because of this, we install Rosetta depending on whether if the computer is Apple Silicon based or not through Smart Computer Groups.

[![Rosetta Policies](/jaysinghdevs/images/policies_cat_enrollment_installrosetta.png)](https://www.jaysingh.dev/images/policies_cat_enrollment_installrosetta.png)

#### What is it?

In a nutshell, Rosetta 2 allows Intel applications to run on Apple Silicon based devices.

[Source](https://www.howtogeek.com/822889/what-is-rosetta-2-on-mac/): What Is Rosetta 2 on Mac?

---

#### 1. Creating the Smart Computer Group

- Navigate to Computers > Smart Group Groups > New
- Display Name: Apple Silicon
- For Criteria, when you go to Add, you may have to press `Show Advanced Criteria`. There will be one for `Apple Silicon`.
- Set the operator to `is` and the value to `Yes`

[![Rosetta Policies](/jaysinghdevs/images/rosetta2onm1/creating_smartgroup.png)](https://www.jaysingh.dev/images/rosetta2onm1/creating_smartgroup.png)

#### 2. Creating the Script

```bash
#!/bin/bash

# Installs Rosetta as needed on Apple Silicon Macs.

exitcode=0

# Determine OS version
# Save current IFS state

OLDIFS=$IFS

IFS='.' read osvers_major osvers_minor osvers_dot_version <<< "$(/usr/bin/sw_vers -productVersion)"

# restore IFS to previous state

IFS=$OLDIFS

# Check to see if the Mac is reporting itself as running macOS 11

if [[ ${osvers_major} -ge 11 ]]; then

  # Check to see if the Mac needs Rosetta installed by testing the processor

  processor=$(/usr/sbin/sysctl -n machdep.cpu.brand_string | grep -o "Intel")
  
  if [[ -n "$processor" ]]; then
    echo "$processor processor installed. No need to install Rosetta."
  else

    # Check for Rosetta "oahd" process. If not found,
    # perform a non-interactive install of Rosetta.
    
    if /usr/bin/pgrep oahd >/dev/null 2>&1; then
        echo "Rosetta is already installed and running. Nothing to do."
    else
        /usr/sbin/softwareupdate --install-rosetta --agree-to-license
       
        if [[ $? -eq 0 ]]; then
        	echo "Rosetta has been successfully installed."
        else
        	echo "Rosetta installation failed!"
        	exitcode=1
        fi
    fi
  fi
  else
    echo "Mac is running macOS $osvers_major.$osvers_minor.$osvers_dot_version."
    echo "No need to install Rosetta on this version of macOS."
fi

exit $exitcode
```

#### 3. Create the Policy

- Make sure the Trigger is set to `Enrollment Complete` and the Execution Frequency is set to Ongoing

[![Install Rosetta Policy](/jaysinghdevs/images/rosetta2onm1/creating_policy.png)](https://www.jaysingh.dev/images/rosetta2onm1/creating_policy.png)

#### What about DEPNotify?

- Out of all my policies, this is the only one that that is triggered to install during enrollment.
- Through my own testing, it's important not to have more than two policies trigger to install during enrollment as that could cause the Jamf binary to fail during the enrollment process.
- If you're curious about DEPNotify, please refer to this article: <coming soon>. Below is a screenshot of the policies being installed in my depNotify.sh:
  
```bash
  
#########################################################################################
# Policy Variable to Modify
#########################################################################################
# The policy array must be formatted "Progress Bar text,customTrigger". These will be
# run in order as they appear below.
  POLICY_ARRAY=(
    "Installing Adobe Creative Cloud,install-creativecloud"
    "Installing Google Chrome,install-chrome"
    "Installing Webex,install-webex"
    "Installing Zoom,install-zoom"
    "Installing Webex Drivers,install-webex-driver"
    "Installing Zoom Drivers,install-zoom-driver"
    "Installing Custom Dock,set-dock"
    "Preparing for the next login,uninstall-depnotify-installers"
  )
```
  
