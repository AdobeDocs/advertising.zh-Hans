---
title: 将DSP集成与 [!DNL Adobe] [!DNL Real-time CDP]
description: 了解如何启用DSP以摄取 [!DNL Adobe] [!DNL Real-time CDP] 第一方区段。
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# 转换用户ID [!DNL Adobe Real-Time CDP] 到通用ID

*Beta功能*

将DSP集成用于 [该 [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=zh-Hans)，它是Adobe Experience Platform的一部分，用于将经过哈希处理的电子邮件地址转换为通用ID以进行定向广告。

1. (要将电子邮件地址转换为 [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；广告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))为设置跟踪 [!DNL Analytics] 计量：

   1. （如果您尚未这样做）完成所有 [实施的先决条件 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) 和 [跟踪URL中的AMO ID和EF ID](/help/integrations/analytics/ids.md).

   1. 向通用ID合作伙伴注册，并在您的网页上部署特定于通用ID的代码，以便匹配从桌面和移动Web浏览器（但不包括移动应用程序）上的ID到显示到达次数的转换：

      * **对象 [!DNL RampIDs]：** 您必须在您的网页上部署额外的JavaScript标记，以便匹配从桌面和移动Web浏览器（但不包括移动应用程序）上的ID到显示到达的转换。 请联系您的Adobe客户团队，他们将为您提供注册 [!DNL LiveRamp] [!DNL LaunchPad] 标记自 [!DNL LiveRamp] 身份验证流量解决方案。 注册是免费的，但您必须签署协议。 注册后，您的Adobe客户团队将生成并提供一个唯一标记，供贵组织在网页上实施。

1. [创建受众源](source-manage.md) 将受众导入您的DSP帐户或广告商帐户。 您可以选择将用户标识符转换为 [可用的通用ID格式](source-about.md).

   源设置将包括自动生成的源密钥，您将在下一步中使用它。

1. 在Adobe Experience Platform中，使用配置Advertising DSP目标连接 [!UICONTROL Source Key] 在DSP源设置中生成的属性。

   有关激活DSP目标连接、选择区段和访问控制权限的说明，请参阅&quot;[Adobe Advertising Cloud DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)“

   源电子邮件地址必须使用SHA-256算法进行哈希处理。

1. 验证受众库（从中创建或编辑受众时可用） [!UICONTROL Audiences] > [!UICONTROL All Audiences] ，并将通用ID的数量与原始经过哈希处理的电子邮件地址的数量进行比较。

   区段应在24小时内可在DSP中使用。 DSP收到区段数据后，受众计数应在九(9)小时内可见。 有关可接受的ID转换率以及区段计数发生变化的原因的信息，请参阅[电子邮件ID与通用ID之间的数据差异](#universal-ids-data-variances)“

区段每24小时刷新一次。 但是，默认情况下，区段中的内容会在30天后过期，或者在客户指定的有效期后过期。 在到期之前，通过从Real-Time CDP重新推送区段来刷新区段。 要请求自定义区段过期，请联系您的Adobe客户团队。

## 故障排除

要排查翻译率和用户计数问题，请参阅&quot;[支持激活通用ID](/help/dsp/audiences/universal-ids.md)“

要排除转换过程的问题，请联系您的Adobe客户团队或 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [关于第一方受众源](/help/dsp/audiences/sources/source-about.md)
>* [管理受众源以激活通用ID受众](source-manage.md)
>* [Adobe Advertising DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [目标目录概述](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [支持激活通用ID](/help/dsp/audiences/universal-ids.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
