# Wagr - MAM Sample App in Objective-C
> A sample iOS app built in Objective-C that uses the MAM SDK and auth with MSAL

## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Inspiration](#inspiration)

## General info
This is an iOS app that is built with Objective-C. This app gives an example on how to implement MAM and MSAL in your app.

## Technologies
> Note: Please Update to the latest Frameworks: 
* MSAL - version 1.6.3 
* MAM - version 20.2.2 

## Setup
> Note: Don't forget to Set api permission for Microsoft Mobile Application Management ref [More Info](https://learn.microsoft.com/mem/intune/developer/app-sdk-get-started#give-your-app-access-to-the-intune-mobile-app-management-service)
To run this app:s

1. Register Wagr in your Azure portal
2. Open Wagr.xcworkspace
3. Open the AppDelegate change the aadClientIdOveride, aadRedirectUriOverride, and aadAuthorityOveride to your values
4. Build the project to your device/simulator
5. Run the app!

## Features
List of MSAL and MAM features in the source code: 

> Note: Clicking on a link will take you to the folder/files that contains the listed feature. From there, search the name of the function in the right file to find the SDK/API calls

### MSAL
* [Login](./Wagr/Application/Login/) (_#pragma mark MSAL Login_ - LoginViewController.m)
* [Logout](./Wagr/Application/Delegates/) (_unenrollRequestWithStatus_ - MAMEnrollmentDelegate.m)
* [Handle MSAL Responses](./Wagr/Application/Main/) (_application:_ - AppDelegate.m) (Note: This app does not use scenes, so only the AppDelegate needs this method. More info: [Click here and go to step 3](https://github.com/AzureAD/microsoft-authentication-library-for-objc#configuring-msal)

### MAM
* [Login](./Wagr/Application/Login/) (_#pragma mark MAM Login_ - LoginViewController.m)
* [Logout](./Wagr/Application/SettingsTab/) (_#pragma mark Deregister The Account_ - SettingsViewController.m)
* [Create MAM Delegates](./Wagr/Application/Delegates/)
    - Compliance Delegate (MAMComplianceDelegate.m)
    - Enrollment Delegate (MAMEnrollmentDelegate.m)
    - Policy Delegate (MAMPolicyDelegate.m)
* [Set MAM Delegates](./Wagr/Application/Main/) (_#pragma mark - MAM Delegates_ - AppDelegate.m)
* [Save-To and Open-From](./Wagr/Application/DataTab/) (Follow the #pragma mark lines - SaveOpenPolicy.m)
* [MAM Diagnostic Console](./Wagr/Application/SettingsTab/) (_onMAMDiagnosticConsoleBtnPressed_ - SettingsViewController.m)
* [MAM App Config](./Wagr/Application/SettingsTab/) (_mamAppConfig_ - SettingsViewController.m)


## Inspiration
Project inspired by the original [Wagr](https://github.com/msintuneappsdk/Wagr-Sample-Intune-iOS-App). The original Wagr explored the capabilities of the Intune App Wrapping Tool.
