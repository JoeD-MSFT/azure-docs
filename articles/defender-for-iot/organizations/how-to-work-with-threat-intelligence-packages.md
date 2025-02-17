---
title: Update threat intelligence data
description: The threat intelligence data package is provided with each new Defender for IoT version, or if needed between releases.
ms.date: 11/16/2022
ms.topic: how-to
---
# Threat intelligence research and packages

## Overview

Security teams at Microsoft carry out proprietary ICS threat intelligence and vulnerability research. These teams include MSTIC (Microsoft Threat Intelligence Center), DART (Microsoft Detection and Response Team), DCU (Digital Crimes Unit), and Section 52 (IoT/OT/ICS domain experts that track ICS-specific zero-days, reverse-engineering malware, campaigns, and adversaries)

The teams provide security detection, analytics, and response to Microsoft's:

- Cloud infrastructure and services.
- Traditional products and devices.
- Internal corporate resources.

Security teams gain the benefit of:

- Protection from known and relevant threats.
- Insights that help you triage and prioritize.
- An understanding of the full context of threats before they're affected.
- More relevant, accurate, and actionable data.

This intelligence provides contextual information to enrich Microsoft platform analytics and supports the company's managed services for incident response and breach investigation. Threat intelligence packages contain signatures (including malware signatures), CVEs, and other security content.

## When are packages delivered

Threat intelligence packages are provided approximately once a month, or if needed more frequently. Announcements about new packages are available from: https://techcommunity.microsoft.com/t5/azure-defender-for-iot/bd-p/AzureDefenderIoT.

You can also see the most current package delivered from the **Threat intelligence update** section of the **Updates** page on Defender for IoT in the Azure portal.

## Update threat intelligence packages to your sensors

Three options are available for updating threat intelligence packages to your sensors:

- Automatically push packages to sensors as they're delivered by Defender for IoT.
- Manually push threat intelligence package to sensors as required.
- Download a package and then upload it to a sensor or multiple sensors.

Users with Defender for IoT Security Reader permissions can automatically and manually push packages to sensors.

### Automatically push threat intelligence updates to sensors

Threat intelligence packages can be automatically updated to *cloud connected* sensors as they're released by Defender for IoT. Ensure automatic package update by onboarding your cloud connected sensor with the **Automatic Threat Intelligence Updates** option enabled. For more information, see [Onboard a sensor](tutorial-onboarding.md#onboard-and-activate-the-virtual-sensor).

### Manually push threat intelligence updates to sensors

Your *cloud connected* sensors can be automatically updated with threat intelligence packages. However, if you would like to take a more conservative approach, you can push packages from Defender for IoT to sensors only when you feel it's required. This gives you the ability to control when a package is installed, without the need to download and then upload it to your sensors.

**To manually push packages:**

1. Go to the Microsoft Defender for IoT **Sites and Sensors** page.
1. Select the ellipsis (...) for a sensor and then select **Push Threat Intelligence update**. The **Threat Intelligence update status** field displays the update progress.

#### Change the threat intelligence update mode

You can change the sensor threat intelligence update mode after initial onboarding.

**To change the update mode:**

1. Select the ellipsis (...) for a sensor and then select **Edit**.
1. Enable or disable the **Automatic Threat Intelligence Updates** toggle.

### Download packages and upload to sensors

Packages can be downloaded the Azure portal and manually uploaded to individual sensors. If the on-premises management console manages your sensors, you can download threat intelligence packages to the management console and push them to multiple sensors simultaneously.

:::image type="content" source="media/how-to-work-with-threat-intelligence-packages/download-screen.png" alt-text="Screenshot of how to download updates in the Azure portal." lightbox="media/how-to-work-with-threat-intelligence-packages/download-screen.png":::

This option is available for both *cloud connected* and *locally managed* sensors.

[!INCLUDE [root-of-trust](includes/root-of-trust.md)]

**To upload to a single sensor:**

1. In Defender for IoT on the Azure portal, go to the **Get started** > **Updates** tab.

1. In the **Sensor threat intelligence update** box, select **Download file** to download the latest threat intelligence package.

1. Sign in to the sensor console, and then select **System settings** > **Threat intelligence**.

1. In the **Threat intelligence** pane, select **Upload file**. For example:

    :::image type="content" source="media/how-to-work-with-threat-intelligence-packages/update-threat-intelligence-single-sensor.png" alt-text="Screenshot of where you can upload Threat Intelligence package to a single sensor." lightbox="media/how-to-work-with-threat-intelligence-packages/update-threat-intelligence-single-sensor.png":::

1. Browse to and select the package you'd downloaded from the Azure portal and upload it to the sensor.

**To upload to multiple sensors simultaneously:**

1. In Defender for IoT on the Azure portal, go to the **Get started** > **Updates** tab.

1. In the **Sensor threat intelligence update** box, select **Download file** to download the latest threat intelligence package.

1. Sign in to the management console and select **System settings**.

1. In the **Sensor Engine Configuration** area, select the sensors that you want to receive the updated packages. For example:

    :::image type="content" source="media/how-to-work-with-threat-intelligence-packages/update-threat-intelligence-multiple-sensors.png" alt-text="Screenshot of where you can select which sensors you want to make changes to." lightbox="media/how-to-work-with-threat-intelligence-packages/update-threat-intelligence-multiple-sensors.png":::

1. In the **Sensor Threat Intelligence Data** section, select the plus sign (**+**).

1. In the **Upload File** dialog, select **BROWSE FILE...** to browse to and select the update package. For example:

    :::image type="content" source="media/how-to-work-with-threat-intelligence-packages/upload-threat-intelligence-to-management-console.png" alt-text="Screenshot of where you can upload a Threat Intelligence package to multiple sensors." lightbox="media/how-to-work-with-threat-intelligence-packages/upload-threat-intelligence-to-management-console.png":::

1. Select **CLOSE** and then **SAVE CHANGES** to push the threat intelligence update to all selected sensors.

    :::image type="content" source="media/how-to-work-with-threat-intelligence-packages/save-changes-management-console.png" alt-text="Screenshot of where you can save changes made to selected sensors on the management console." lightbox="media/how-to-work-with-threat-intelligence-packages/save-changes-management-console.png":::

## Review package update status on the sensor

The package update status and version information are displayed in the sensor **System Settings**, **Threat Intelligence** section.  

## Review package information for cloud connected sensors

Review the following information about threat intelligence packages for your cloud connected sensors:

- Package version installed
- Threat intelligence update mode
- Threat intelligence update status

**To review threat intelligence information**:

1. Go to the Microsoft Defender for IoT **Sites and Sensors** page.

1. Review the **Threat Intelligence version** installed on each sensor. Version naming is based on the day the package was built by Defender for IoT.

1. Review the **Threat Intelligence mode** . *Automatic* indicates that newly available  packages will be automatically installed on sensors as they're released by Defender for IoT.

    *Manual* indicates that you can push newly available packages directly to sensors as needed.

1. Review the **Threat Intelligence update status**. The following statuses may be displayed:

    - Failed
    - In Progress
    - Update Available
    - Ok

If cloud connected threat intelligence updates fail, review  connection  information in the **Sensor status** and **Last connected UTC** columns in the **Sites and Sensors** page.

## Next steps

For more information, see:

- [Onboard a sensor](tutorial-onboarding.md#onboard-and-activate-the-virtual-sensor)

- [Manage sensors from the management console](how-to-manage-sensors-from-the-on-premises-management-console.md)
