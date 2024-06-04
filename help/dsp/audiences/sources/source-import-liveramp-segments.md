---
title: 从手动导入经过身份验证的区段 [!DNL LiveRamp]
description: 了解如何通过激活经过身份验证的受众 [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: f10a0bd487d641bd150d9ecbefe907b2bf25e5a7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# 从手动导入经过身份验证的区段 [!DNL LiveRamp]

*Beta版功能*

您可以手动发送经过身份验证的 [!DNL LiveRamp] 使用将区段发送到DSP [!DNL LiveRamp] [!DNL Connect] 仪表板。 您可以使用导入的区段进行投放定位。 对于第一方区段，费用为投放的每个显示广告展示0.15美元，投放的每个视频广告展示0.25美元。

每个导入作业的区段映射和上传可能最多需要7天。

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. 在中完成以下步骤 [!DNL Connect] 仪表板：

   1. 激活目标拼贴 **[!DNL AAC API 1P Onboarding]**.

   1. 设置 [!DNL Identifier Settings] 到 **[!DNL Ramp ID]** 仅限。

      ![标识符设置](/help/dsp/assets/liveramp-tile-settings.png)

   1. （可选）如果您仍要接收基于Cookie的标识符，请创建第二个 [!DNL AAC API 1P Onboarding] 目标拼贴，带有&quot;[!DNL Cookies]，&quot; &quot;[!DNL IDFA]，”和“[!DNL AAID]已选择“”。

   1. 验证受众库（从中创建或编辑受众时可用） [!UICONTROL Audiences] > [!UICONTROL All Audiences] ，或在版面设置内)导入了整个区段计数。

>[!MORELIKETHIS]
>
>* [关于第一方受众源](source-about.md)
>* [创建受众源以激活通用ID受众](source-create.md)
>* [受众源设置](source-settings.md)
>* [Adobe Advertising DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
