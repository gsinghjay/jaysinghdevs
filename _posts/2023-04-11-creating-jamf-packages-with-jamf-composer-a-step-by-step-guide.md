---
title: "Creating Jamf Packages with Jamf Composer: A Step-by-Step Guide"
date: 2023-04-11
tags: 
- Jamf
- Jamf Pro
- Jamf Composer
- Package Building
- macOS
- Keychain
categories: 
- Jamf
- Package Creation
---
Jamf Composer is a powerful tool that simplifies the process of creating custom packages for macOS devices managed by Jamf Pro. In this article, we'll walk you through the steps to create Jamf packages using Jamf Composer, and we'll also cover signing the package via Keychain.

#### Step 1: Launch Jamf Composer

To begin, open the Jamf Composer application on your macOS device.

#### Step 2: Choose a Package Type

Jamf Composer offers two package types: DMG and PKG. Select the package type that best fits your needs.

#### Step 3: Add Items to the Package

Drag and drop items from Finder to the package in Jamf Composer. You can include files, folders, and applications.

#### Step 4: Configure Package Settings

Click the 'Settings' tab to configure the package's identifier, version number, and other metadata.

#### Step 5: Save the Package

Choose 'File' > 'Save As' to save the package to your desired location.

#### Step 6: Build the Package

Click the 'Build' button in the toolbar or choose 'File' > 'Build' to build the package.

#### Step 7: Sign the Package (Optional)

To sign the package with a Developer ID Installer certificate from your keychain:

1. Open the 'Keychain Access' application on your macOS device.
2. Locate the Developer ID Installer certificate in your keychain.
3. In Jamf Composer, click the 'Settings' tab.
4. In the 'Signing' section, select the 'Sign package' checkbox.
5. Choose your Developer ID Installer certificate from the dropdown menu.

By signing the package, you ensure that it is trusted by macOS and can be installed without security warnings.

#### Step 8: Test the Package

Deploy the package to a test device to ensure that it works as intended.

By following these steps, you can create custom Jamf packages with Jamf Composer and sign them with a Developer ID Installer certificate from your keychain. This process simplifies package creation for macOS devices managed by Jamf Pro, allowing for seamless deployment and management.
