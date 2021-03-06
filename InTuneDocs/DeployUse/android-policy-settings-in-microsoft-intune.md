---
# required metadata

title: Android and Samsung KNOX configuration policy settings | Microsoft Intune
description:
keywords:
author: robstackmsft
manager: jeffgilb
ms.date: 04/28/2016
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 71cc39cf-e726-40fd-8d08-78776e099a4b

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: heenamac
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Android and Samsung KNOX policy settings in Microsoft Intune

## General configuration policy

Use the Microsoft Intune **Android general configuration policy** to configure settings for:

-   **Mobile device security settings** – Choose from a list of predefined settings that let you control a range of features and functionality on the device.

-   **Kiosk mode** (for Samsung KNOX devices only) - Lock a device to only allow certain features to work. For example, you can allow a device to only run one managed app that you specify, or you can disable the volume buttons on a device. These settings might be used for a demonstration model of a device, or a device that is dedicated to performing only one function, such as a point of sale device.

-   **Compliant and noncompliant apps** - Specify a list of apps that are compliant, or not compliant in your company. On Android and iOS devices, the **Noncompliant Apps Report** can be used to view the compliance of apps you specified in the list against the apps that users have installed (but cannot actually block the installation of the app).

> [!TIP]
> You can configure terms and conditions for users to ensure that they acknowledge that apps on their device, including personal apps will be evaluated, and noncompliant apps will either be blocked, or reported as noncompliant. Users must accept these terms and conditions before they can enroll their device and use the company portal to get apps. For more information about using terms and conditions, see [Terms and condition policy settings in Microsoft Intune](terms-and-condition-policy-settings-in-microsoft-intune.md).

If the setting you are looking for does not appear in this topic, you might be able to create it using an Android custom policy that lets you use OMA-URI settings to control the device. For more information, see **Custom policy settings** later in this topic.

### Password settings

|Setting name|Details|Android 4.0+|Samsung KNOX|
|----------------|-|----------------|----------------|
|**Require a password to unlock mobile devices**|Require a password on supported devices.|Yes|Yes|
|**Minimum password length**|The minimum length for the password.|Yes|Yes|
|**Number of repeated sign-in failures to allow before the device is wiped**|Wipes the device if this number of login attempts fail.|Yes|Yes|
|**Minutes of inactivity before screen turns off**|Specify the number of minutes before the device automatically locks.|Yes|Yes|
|**Password expiration (days)**|The number of days before a password must be changed.|Yes|Yes|
|**Remember password history**|Remember this many previously used passwords.|Yes|Yes|
|**Remember password history** – **Prevent reuse of previous passwords**|Prevents re-using previously used passwords.|Yes|Yes|
|**Password quality**|Select the password complexity level required and also whether biometric devices can be used.|Yes|Yes|
|**Allow fingerprint unlock**|Allow the use of a fingerprint to unlock the device.|No|Yes|
|**Allow Smart Lock and other trust agents**<br>(Android 5 and later)|Let’s you control the Smart Lock feature on compatible Android devices. This phone capability, sometimes known as trust agents lets you disable or bypass the device lock screen password if the device is in a trusted location such as when it is connected to a specific Bluetooth device, or when it is near to an NFC tag. You can use this setting to prevent end users from configuring Smart Lock.|Yes|No|

### Encryption settings

|Setting name|Details|Android 4.0+|Samsung KNOX|
|----------------|----------------|----------------|
|**Require encryption on mobile device**|Requires that files on the mobile device are encrypted.|Yes|Yes|
|**Require encryption on storage cards**|Specifies whether the device storage card must be encrypted.|No|Yes|

### System settings

|Setting name|Details|Android 4.0+|Samsung KNOX|
|----------------|----------------|----------------|
|**Allow screen capture**|Let's the user capture the screen contents as an image.|No|Yes|
|**Allow diagnostic data submission**|Allows the device to submit diagnostic information to Google.|No|Yes|
|**Allow factory reset**|Allow the user to perform a factory reset on the device.|No|Yes|

### Cloud settings – documents and data

|Setting name|Details|Android 4.0+|Samsung KNOX|
|----------------|----------------------------|----------------|
|**Allow Google backup**|Allows use of Google backup.|No|Yes|

### Cloud settings – accounts and synchronization

|Setting name|Details|Android 4.0+|Samsung KNOX|
|----------------|----------------|----------------|
|**Allow Google account auto sync**|Allows Google account settings to be automatically synchronized.|No|Yes|

### Application settings - browser

|Setting name|Details|Android 4.0+|Samsung KNOX|
|----------------|----------------|----------------|
|**Allow web browser**|Specifies whether the device web browser can be used.|No|Yes|
|**Allow autofill**|Allow the Autofill function of the web browser to be used.|No|Yes|
|**Allow pop-up blocker**|Allows the use of the pop-up blocker in the web browser.|No|Yes|
|**Allow cookies**|Allow the device web browser to use cookies.|No|Yes|
|**Allow active scripting**|Allow the device web browser to use active scripting.|No|Yes|

### Application settings - apps

|Setting name|Details|Android 4.0+|Samsung KNOX|
|----------------|----------------|----------------|
|**Allow Google Play store**|Allow the user to access the Google Play store on the device.|No|Yes|

### Device capabilities settings - hardware

|Setting name|Details|Android 4.0+|Samsung KNOX|
|----------------|----------------|----------------|
|**Allow camera**|Allows the use of the device camera.|Yes|Yes|
|**Allow removable storage**|Allows the device to use removable storage, like an SD card.|No|Yes|
|**Allow Wi-Fi**|Allows the use of the Wi-Fi capabilities of the device.|No|Yes|
|**Allow Wi-Fi tethering**|Allows the use of Wi-Fi tethering on the device.|No|Yes|
|**Allow geolocation**|Allows the device to utilize location information.|No|Yes|
|**Allow NFC**|Allows operations that use near field communication if the device supports it.|No|Yes|
|**Allow Bluetooth**|Allows the use of Bluetooth on the device.|No|Yes|
|**Allow power off**|Allows the user to power off the device.<br /><br />If this setting is disabled, the setting **Number of repeated sign in failures to allow before the device is wiped** for Samsung KNOX devices does not function.|No|Yes|

### Device capabilities settings - cellular

|Setting name|Details|Android 4.0+|Samsung KNOX|
|----------------|----------------|----------------|
|**Allow voice roaming**|Allow voice roaming when the device is on a cellular network.|No|Yes|
|**Allow data roaming**|Allow data roaming when the device is on a cellular network.|No|Yes|
|**Allow SMS/MMS messaging**|Allow the use of SMS and MMS messaging on the device.|No|Yes|

### Device capabilities settings - features

|Setting name|Details|Android 4.0+|Samsung KNOX|
|----------------|----------------|----------------|
|**Allow voice assistant**|Allows the use of voice assistant software on the device.|No|Yes|
|**Allow voice dialing**|Enables or disables the voice dialing feature on the device.|No|Yes|
|**Allow copy and paste**|Allow copy and paste functions on the device.|No|Yes|
|**Allow clipboard share between applications**|Use the clipboard to copy and paste between apps.|No|Yes|
|**Allow YouTube**|Allow the use of YouTube on the device.|No|Yes|

### Settings for compliant and noncompliant apps
In the **Compliant &amp; Noncompliant Apps** list, specify a list of compliant or noncompliant apps using the following information:

> [!NOTE]
> A single policy can only contain a list of compliant, or a list of noncompliant apps. You cannot specify both in the same policy.

|Setting name|Details|
|----------------|--------------------|
|**Report noncompliance when users install the listed apps**|Lists the apps that are not managed by Intune which you do not want users to install and run. If users install one of these apps, it will be listed in the noncompliant apps report.|
|**Do not report noncompliance when users install the listed apps**|Lists the apps that you want to allow in your company. To remain compliant, users must not install any apps that are not listed. Apps that are managed by Intune are automatically allowed.|
|**Add**|Adds an app to the selected list. Specify a name of your choice, optionally the app publisher, and the URL to the app in the app store.<br /><br />For help, see How to specify URLs to app stores later in this topic.|
|**Import Apps**|Imports a list of apps you have specified in a comma-separated values file. Use the format, application name, publisher, app URL in the file.|
|**Edit**|Let’s you edit the name, publisher and URL of the selected app.|
|**Delete**|Deletes the selected app from the list.|

### Kiosk mode settings
Specify the following settings for **Samsung KNOX devices**:

|Setting name|Details|
|----------------|--------------------|
|**Select a managed app that will be allowed to run when the device is in kiosk mode**|Choose **Browse**, then select the managed app that will be allowed to run when the device is in kiosk mode (apps specified as a link to the store are not currently supported). No other apps will be allowed to run on the device.|
|**Allow volume buttons**|Enables or disables the use of the volume buttons on the device.|
|**Allow screen sleep wake button**|Enables or disables the screen sleep wake button on the device.|

### Reference information for compliant and noncompliant apps

#### Monitor compliant and noncompliant apps
Use the **Noncompliant Apps Report** to view the compliance of allowed and blocked apps.

###### To run the Noncompliant Apps Report

1.  In the [Microsoft Intune administration console](https://manage.microsoft.com), choose **Reports** &gt; **Noncompliant Apps Report**.

2.  Select the device groups that you would like to check, whether you want to check for compliant apps, noncompliant apps, or both, then choose **View Report**.

#### How to specify URLs to app stores
To specify an app URL in the compliant and noncompliant apps list, use the following format:

In the [Apps section of Google Play](https://play.google.com/store/apps), search for the app you want to use.

Open the installation page for the app, and copy the URL to the clipboard. You can now use this as the URL in either the compliant or noncompliant apps list.

**Example:** Search Google Play for Microsoft Office Mobile. The URL you use will be **https://play.google.com/store/apps/details?id=com.microsoft.office.officehub**.

## Custom policy settings
Use the Microsoft Intune **Android custom configuration policy** to deploy OMA-URI (Open Mobile Alliance Uniform Resource Identifier) settings that can be used to control features on Android devices. These are standard settings that many mobile device manufacturers use to control device features.

This capability is intended to allow you to deploy Android settings that are not configurable with Intune policies.

> [!NOTE]
> Currently, Android custom policies only support configuring Wi-Fi settings for Android devices that include a pre-shared key.

### General settings

|Setting name|Details|
    |----------------|--------------------|
    |**Name**|Enter a unique name for the Android custom policy to help you identify it in the Intune console.|
    |**Description**|Provide a description that gives an overview of the Android custom policy and other relevant information that helps you to locate it.|

### OMA-URI settings

   |Setting name|Details|
    |--------|--------------------|
    |**Setting name**|Enter a unique name for the OMA-URI setting to help you identify it in the list of settings.|
    |**Setting description**|Provide a description that gives an overview of the setting and other relevant information to help you locate it.|
    |**Data type**|Select the date type in which you will specify this OMA-URI setting. Choose from  **String, String (XML), Date and time, Integer, Floating point**, or **Boolean**.|
    |**OMA-URI (case sensitive)**|Specify the OMA-URI you want to supply a setting for.|
    |**Value**|Specify the value to associate with the OMA-URI you specified previously.|

### Example: Configure a custom Wi-Fi profile with a pre-shared key
Although Intune supports Wi-Fi profiles for Android devices, this feature does not currently support the inclusion of a pre-shared key in the configuration. In this example, you’ll learn how to create an Android custom policy that creates a Wi-Fi profile with a pre-shared key on the Android device.

#### To create a Wi-Fi profile with a pre-shared key

1.  Ensure that your users are using the latest version of the [Intune Company Portal](https://play.google.com/store/apps/details?id=com.microsoft.windowsintune.companyportal) app for Android.

2.  Create an Android custom policy and add the following settings:

|Setting name|Details|
|----------------|--------------------|
|**Setting name**|Specify a name of your choice for the setting.|
|**Setting description**|Specify a description for the setting.|
|**Data type**|Select **String (XML)**.|
|**OMA-URI**|Enter the following: ./Vendor/MSFT/WiFi/Profile/*&lt;your Wi-Fi profile&gt;*/Settings|

3.  For **Value**, copy and paste the following XML code:

    ```
    <!--
    WEP Wifi Profile
                    <Name of wifi profile> = Name of profile 
                    <SSID of wifi profile> = Plain text of SSID. Does not need to be escaped, could be <name>Your Company's Network</name>
                    <WEP password> = Password to connect to the network
    -->
    <WLANProfile 
    xmlns="http://www.microsoft.com/networking/WLAN/profile/v1">
      <name><Name of wifi profile></name>
      <SSIDConfig>
        <SSID>
          <name><SSID of wifi profile></name>
        </SSID>
      </SSIDConfig>
      <connectionType>ESS</connectionType>
      <MSM>
        <security>
          <authEncryption>
            <authentication>open</authentication>
            <encryption>WEP</encryption>
            <useOneX>false</useOneX>
          </authEncryption>
          <sharedKey>
            <keyType>networkKey</keyType>
            <protected>false</protected>
            <keyMaterial><WEP password></keyMaterial>
          </sharedKey>
          <keyIndex>0</keyIndex>
        </security>
      </MSM>
    </WLANProfile>
    ```

4.  When you are done, save the policy and deploy it to the required Android devices. The new Wi-Fi profile will appear in the list of connections on the device.

### See also
[Manage settings and features on your devices with Microsoft Intune policies](manage-settings-and-features-on-your-devices-with-microsoft-intune-policies.md)

