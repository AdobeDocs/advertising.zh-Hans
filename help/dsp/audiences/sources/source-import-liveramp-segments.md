---
title: 从 [!DNL LiveRamp]手动导入经过身份验证的区段
description: 了解如何通过 [!DNL LiveRamp]激活经过身份验证的受众。
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# 从[!DNL LiveRamp]手动导入经过身份验证的区段

*Beta功能*

您可以使用[!DNL LiveRamp] [!DNL Connect]仪表板手动将经过身份验证的[!DNL LiveRamp]区段发送到DSP。 您可以使用导入的区段进行投放定位。 对于第一方区段，费用为投放的每个显示广告展示0.15美元，投放的每个视频广告展示0.25美元。

每个导入作业的区段映射和上传可能最多需要7天。

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. 在[!DNL Connect]仪表板中完成以下步骤：

   1. 激活目标磁贴&#x200B;**[!DNL AAC API 1P Onboarding]**。

   1. 仅将[!DNL Identifier Settings]设置为&#x200B;**[!DNL Ramp ID]**。

      ![标识符设置](/help/dsp/assets/liveramp-tile-settings.png)

   1. （可选）如果您仍希望接收基于Cookie的标识符，请创建第二个[!DNL AAC API 1P Onboarding]目标磁贴，并选中“[!DNL Cookies]”、“[!DNL IDFA]”和“[!DNL AAID]”。

   1. 验证您的受众库（在从[!UICONTROL Audiences] > [!UICONTROL All Audiences]创建或编辑受众时或在版面设置内可用）中是否导入了整个区段计数。

>[!MORELIKETHIS]
>
>* [关于第一方受众源](source-about.md)
>* [管理受众源以激活通用ID受众](source-manage.md)
>* [Adobe Advertising DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
