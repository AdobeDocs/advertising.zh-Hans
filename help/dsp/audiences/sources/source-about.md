---
title: 关于从受众源激活经过身份验证的区段
description: 了解如何从客户数据平台引入第一方区段。
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: f01cfbf22628cec0510f4a860ad927b333d5946a
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# 关于从受众源激活经过身份验证的区段

DSP可以摄取第一方区段，这些区段由在客户数据平台(CDP)中构建的经过哈希处理的电子邮件ID或通用ID组成。 您可以将摄取的区段用作投放的目标。

以下CDP已建立连接器，但DSP也可以使用批处理、流式传输或基于API的数据共享连接到任何CDP。 要与新的CDP集成，请联系您的Adobe客户团队。

## [!DNL Adobe Real-Time Customer Data Platform]

DSP已与 [该 [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=zh-Hans)，它是Adobe Experience Platform的一部分。

在 [!DNL Real-Time CDP]， *目标* 是到外部数据平台的连接，可无缝激活数据。 例如，您可以使用目标为各种DSP支持的数字格式的目标广告激活已知的客户关系（如哈希电子邮件地址）。 有关目标的更多信息，请参阅Experience Platform [目标指南](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html)，包括产品概述，说明 [创建目标工作区](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) 和 [创建目标连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)、和 [将数据激活到目标](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

有关更多信息，请参阅&quot;[用于将DSP集成与配合使用的工作流 [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)“

## [!DNL ActionIQ]

您可以从以下位置共享您组织的第一方数据 [!DNL Action IQ] 使用DSP的客户数据平台。 然后，您可以使用将DSP投放定位到区段 [!DNL RampIDs] 或 [!DNL Unified IDs 2.0].

此集成需要自定义。 有关更多信息，请与您的Adobe客户团队联系。

## [!DNL Tealium]

您可以从以下位置共享您组织的第一方数据 [!DNL Tealium] 客户数据平台使用 [!DNL Amazon Web Services]. 然后，您可以使用将DSP投放定位到区段 [!DNL RampIDs]. 有关更多信息，请参阅&quot;[用于将DSP集成与配合使用的工作流 [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)“

>[!MORELIKETHIS]
>
>* [用于将DSP集成与配合使用的工作流 [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [用于将DSP集成与配合使用的工作流 [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [创建受众源以激活第一方受众](source-create.md)
>* [受众源设置](source-settings.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)

<!--
>* [Workflow for Using the DSP Integration with [!DNL ActionIQ]](/help/dsp/audiences/sources/source-actioniq.md)
-->
