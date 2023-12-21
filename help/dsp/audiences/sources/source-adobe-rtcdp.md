---
title: “用于将DSP集成与配合使用的工作流 [!DNL Adobe] [!DNL Real-time CDP]"
description: “了解如何使DSP能够摄取 [!DNL Adobe] [!DNL Real-time CDP] 第一方客户细分。”
feature: DSP Audiences
source-git-commit: fb42e4aacaf0ea22890e0b4a46719725c99fffdc
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# 用于将DSP集成与配合使用的工作流 [!DNL Adobe Real-Time CDP]

1. [允许DSP将客户数据区段转换为 [!DNL LiveRamp RampIDs]](source-universal-id.md) 在竞标环境中可辨认的资产。<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [创建受众源](source-create.md) 将受众导入您的DSP帐户或广告商帐户。

1. 在Experience PlatformDSP中，使用 [!UICONTROL Source Key] 在DSP源设置中生成的属性。

   有关激活DSP目标连接、选择区段和访问控制权限的说明，请参阅&quot;[Adobe Advertising Cloud DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)“

如需其他支持，请联系您的Adobe客户团队或 `adcloud-support@adobe.com`.


>[!MORELIKETHIS]
>
>* [从通用ID合作伙伴激活经过身份验证的区段](source-universal-id.md)
>* [创建受众源以激活第一方受众](source-create.md)
>* [受众源设置](source-settings.md)
>* [Adobe Advertising DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [目标目录概述](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [用于将DSP集成与配合使用的工作流 [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
