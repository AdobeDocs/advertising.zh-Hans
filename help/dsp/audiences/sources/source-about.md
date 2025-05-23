---
title: 关于第一方受众源
description: 了解如何将第一方区段中的其他用户标识符转换为通用ID以实现无痕定位。
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 3a641db6b145e67e6e1f1daca271dd524973e075
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# 关于第一方受众源

*Beta功能*

DSP可以摄取由您在客户数据平台(CDP)中构建的经过哈希处理的电子邮件ID组成的第一方区段，并将它们转换为由通用ID组成的区段。 每个生成的ID都基于人员，广告频率上限应用于ID级别<!-- Move that info. to somewhere else? -->。

区段详细信息包括每种通用ID类型的大小，以及Cookie或设备ID跟踪的每个设备类型的大小。

## 通用ID类型 {#universal-id-types}

<!--  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

您可以将第一方区段转换为具有以下通用ID合作伙伴的已验证（确定性）ID的区段。

* [[!DNL LiveRamp] [!DNL RampIDs]](https://liveramp.com/identity-resolution)：

   * 用于重新定位已登录的用户。

     [!DNL RampIDs]适用于北美洲、澳大利亚和新西兰的用户。

     费用包括交付的每个展示广告展示0.15美元，以及交付的每个视频广告展示0.25美元。

   * 用于使用[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)的测量。

* [[!DNL Unified ID 2.0 (UID2.0)] ID](https://unifiedid.com)：

   * 用于重新定位已登录的用户。

     [!DNL UID2 IDs]不适用于欧洲经济区和其他一些国家/地区的用户。 查看[禁止的国家/地区列表](/help/policies/universal-id-policy.md#prohibited-countries-uid2)。

     费用包括交付的每个展示广告展示0.15美元，以及交付的每个视频广告展示0.25美元。

<!-- Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. <!-- Contact your Adobe Account Team for instructions. -->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## 第一方区段支持的客户数据平台

DSP已建立到以下CDP的连接器，以快速摄取您的第一方区段。

DSP还可以使用批处理、流式传输或基于API的数据共享连接到任何其他CDP。 要与新的CDP集成，请联系您的Adobe客户团队。

### [!DNL Adobe Real-Time CDP]

DSP是[the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=zh-Hans)的集成&#x200B;*目标*，它是Adobe Experience Platform的一部分。

在[!DNL Real-Time CDP]中，目标是与外部数据平台的连接，可无缝激活数据。 您可以使用目标在DSP中为定向广告激活经过哈希处理的电子邮件地址。 有关目标的更多信息，请参阅Experience Platform[目标指南](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html?lang=zh-Hans)，包括产品概述、有关[创建目标工作区](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html?lang=zh-Hans)和[创建目标连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=zh-Hans)以及[将数据激活到目标](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html?lang=zh-Hans)的说明。

要使DSP能够摄取您的[!DNL Adobe] [!DNL Real-time CDP]第一方区段并将经过哈希处理的电子邮件地址转换为通用ID，请参阅“[将用户ID从 [!DNL Adobe Real-Time CDP] 转换为通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)”。

### [!DNL ActionIQ]

您可以与DSP共享您组织从[!DNL ActionIQ]客户数据平台的第一方数据，以将经过哈希处理的电子邮件地址转换为通用ID，以便在DSP中进行目标广告。 此集成需要自定义。 有关更多信息，请与您的Adobe客户团队联系。

### [!DNL Amperity]

您可以与DSP共享您组织从[!DNL Amperity]客户数据平台的第一方数据，以将经过哈希处理的电子邮件地址转换为通用ID，以便在DSP中进行目标广告。 有关详细信息，请参阅[将用户ID从 [!DNL Amperity] 转换为通用ID](/help/dsp/audiences/sources/source-amperity.md)。

### [!DNL Optimizely]

您可以与DSP共享您组织从[!DNL Optimizely]客户数据平台的第一方数据，以将经过哈希处理的电子邮件地址转换为通用ID，以便在DSP中进行目标广告。 有关详细信息，请参阅[将用户ID从 [!DNL Optimizely] 转换为通用ID](/help/dsp/audiences/sources/source-optimizely.md)。

### [!DNL Tealium]

您可以使用[!DNL Amazon Web Services]从[!DNL Tealium]客户数据平台共享您组织的第一方数据。 有关在DSP中将经过哈希处理的电子邮件地址转换为通用ID的详细信息，请参阅[将用户ID从 [!DNL Tealium] 转换为通用ID](/help/dsp/audiences/sources/source-tealium.md)。

>[!MORELIKETHIS]
>
>* [管理受众源以激活通用ID受众](source-manage.md)
>* [支持激活通用ID](/help/dsp/audiences/universal-ids.md)
>* [将用户ID从 [!DNL Adobe Real-Time CDP] 转换为通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [将用户ID从 [!DNL Amperity] 转换为通用ID](/help/dsp/audiences/sources/source-amperity.md)
>* [将用户ID从 [!DNL Optimizely] 转换为通用ID](/help/dsp/audiences/sources/source-optimizely.md)
>* [将用户ID从 [!DNL Tealium] 转换为通用ID](/help/dsp/audiences/sources/source-tealium.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
