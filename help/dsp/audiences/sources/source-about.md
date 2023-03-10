---
title: 关于从受众源激活经过身份验证的区段
description: 了解如何从客户数据平台引入第一方区段。
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: f6308ac9af8019987f4a2e501cba6b019cb032b6
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 关于从受众源激活经过身份验证的区段

<!-- Doesn't specifically explain what you can do in our UI -->
*测试版功能*

DSP可以摄取由构建在客户数据平台(CDP)中的经过身份验证的信号组成的第一方区段。 您可以将摄取的区段用作投放的目标。

## [!DNL Adobe Real-Time Customer Data Profile]

DSP与集成 [此 [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)，它是Adobe Experience Platform的一部分。

In [!DNL Real-time CDP]， *目标* 连接外部数据平台，实现无缝数据激活。 例如，您可以使用目标在DSP支持的各种数字格式中为定位广告激活已知的客户关系（如哈希电子邮件地址）。

有关目标的更多信息，请参阅Experience Platform [目标指南](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html)，包括产品概述，说明 [创建目标工作区](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) 和 [创建目标连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)、和 [将数据激活到目标](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

### 将DSP集成与配合使用的工作流 [!DNL Real-time CDP] {#workflow-sources}

<!-- Make sure that titles make the distinctions clear -- everything can't be "Activate XXX." -->

1. [允许DSP将客户数据区段转换为 [!DNL LiveRamp RampIDs]](source-durable-id.md) 在竞价环境中可识别的其他资源。<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [创建受众源](source-create.md) 将受众导入您的DSP帐户或广告商帐户。

1. [配置 [!DNL Real-Time CDP] Experience Platform中的目标连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).

要获得其他支持，请联系您的Adobe客户团队或 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [从持久ID合作伙伴激活经过身份验证的区段](source-durable-id.md)
>* [创建受众源以激活第一方受众](source-create.md)
>* [受众源设置](source-settings.md)
>* [AdobeAdvertising DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [目标目录概述](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)

