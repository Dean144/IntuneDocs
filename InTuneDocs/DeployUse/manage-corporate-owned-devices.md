---
# required metadata

title: Manage corporate-owned devices | Microsoft Intune
description:
keywords:
author: NathBarn
manager: jeffgilb
ms.date: 04/28/2016
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 2b60bbff-25e6-489b-9621-c71b4275fa06

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: dagerrit
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Enroll corporate-owned devices with Microsoft Intune
Organization or corporate-owned devices (COD) can be brought into management by Intune in a variety of ways depending upon the device, how it was purchased, and the needs of the organization.

## Corporate-owned iOS devices
These enrollment methods are good for "Choose your own device" (CYOD) scenarios where the organization purchases the devices for users, but wants to retain management of the device. If your organization has purchased iOS devices, you can pre-configure enrollment so that the device is managed from the first time its user turns it on. Intune supports enrollment via [Apple's Device Enrollment Program (DEP)](ios-device-enrollment-program-in-microsoft-intune.md) or using the Apple Configurator tool running on a Mac computer for [direct](ios-direct-enrollment-in-microsoft-intune.md) or [Setup Assistant](ios-setup-assistant-enrollment-in-microsoft-intune.md) enrollment.

[Enroll corporate-owned iOS devices](enroll-corporate-owned-ios-devices-in-microsoft-intune.md)

## Device enrollment manager
Organizations can use Intune to manage large numbers of mobile devices with a single user account called a device enrollment manager account. After creating a device enrollment manager account, that account can be used by a manager to enroll more than the standard five devices allowed by default to normal users. Enrolling devices with a device enrollment manager only works for devices that aren't used by a specific user. These devices are good for point-of-sale or utility apps, for example, but bad for users who need access to email or company resources.

[Enroll corporate-owned devices with the device enrollment manager](enroll-corporate-owned-devices-with-the-device-enrollment-manager-in-microsoft-intune.md)

## International mobile equipment identity (IMEI)
Unique international mobile equipment identity (IMEI) numbers are a common device property for many mobile device manufacturers. Intune administrators can import IMEI numbers for devices the company owns. When the device becomes managed by Intune, it can be tagged as a corporate-owned device and targeted with appropriate policy.

[Specify corporate-owned devices with international mobile equipment identity (IMEI) numbers](specify-corporate-owned-devices-with-international-mobile-equipment-identity-imei-numbers.md)
