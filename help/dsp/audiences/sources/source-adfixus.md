---
title: 从 [!DNL AdFixus]导入第一方区段
description: 了解如何将包含 [!DNL AdFixus] 通用ID的 [!DNL AdFixus] 第一方区段导入DSP。
feature: DSP Audiences
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 79f0b3872a0d5d3765093ce83cc8f1c284a8255c
workflow-type: tm+mt
source-wordcount: 448
ht-degree: 0%

---

# 从[!DNL AdFixus]导入第一方区段

*仅适用于澳大利亚的广告商*

使用Advertising DSP与[!DNL AdFixus]的集成，导入带有目标广告区段映射的[!DNL AdFixus]通用ID。[!DNL AdFixus] ID仅在澳大利亚可用。 DSP不会将[!DNL AdFixus] ID更改为其他ID类型，也不会将其他ID类型转换为[!DNL AdFixus] ID。 DSP不收取导入ID的费用。

将[!DNL AdFixus]区段导入DSP后，您可以将投放位置定向到[!DNL AdFixus] ID和[!DNL AdFixus]中的特定第一方区段。 您还可以将[!DNL AdFixus]区段添加到可重用受众。 任何区段的详细信息包括适用的[!DNL AdFixus] ID计数。

您可以在自定义报表中查看具有[!DNL AdFixus] ID的用户的展示、点击、频率和其他量度。 具有[!DNL Analytics for Advertising]的广告商还可以在DSP中查看Adobe Analytics中[!DNL AdFixus] ID的浏览数据，以及来自Adobe Analytics的数据。

1. 使用[!DNL AdFixus]将贵组织的第一方数据转换为具有[!DNL AdFixus] ID的区段。

   这需要具有[!DNL AdFixus]的单独帐户和有效的许可证密钥。 您还需要为网站属性和域实施特定于[!DNL AdFixus]的代码。 直接使用[!DNL AdFixus]生成具有ID的区段。

1. （具有[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)的广告商）为[!DNL Analytics]度量设置跟踪：

   1. （如果尚未这样做）完成实施 [!DNL Analytics for Advertising][&#128279;](/help/integrations/analytics/prerequisites.md)以及跟踪URL[&#128279;](/help/integrations/analytics/ids.md)中的AMO ID和EF ID的所有先决条件。

   1. 在网页上部署特定于[!DNL AdFixus]的代码，以匹配从桌面浏览器和移动设备Web浏览器（但不包括移动应用程序）上的[!DNL AdFixus] ID到显示到达次数的转换。

1. 导入您的第一方[!DNL AdFixus]区段：

   1. [创建受众源](source-manage.md)，共[!UICONTROL Type]个&#x200B;**[!UICONTROL AdFixus ID]**。 您必须同意服务协议的条款。

      源设置将包括自动生成的源密钥。

   1. 与您的[!DNL AdFixus]团队共享源密钥，以便他们能够将所需的区段流式传输到DSP。

1. 在受众库的[!UICONTROL First Party Segments]部分中验证区段是否正在填充（当您从[!UICONTROL Audiences] > [!UICONTROL All Audiences]或在版面设置中创建或编辑受众时可用）。 比较[!DNL AdFixus] ID数量与[!DNL AdFixus]内的用户ID数量。

   区段创建后即可在DSP中使用。

区段会刷新一次，并且每三小时可用于定位一次，尽管DSP中显示的计数每24小时刷新一次。 **注意：**&#x200B;区段中的包含操作将在指定的过期时间（您在[!DNL AdFixus]中配置）后过期。 在到期之前从[!DNL AdFixus]重新推送区段，以刷新区段。

>[!MORELIKETHIS]
>
>* [关于第一方受众源](/help/dsp/audiences/sources/source-about.md)
>* [管理受众源以激活通用ID受众](source-manage.md)
>* [Adobe Advertising DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [目标目录概述](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [支持激活通用ID](/help/dsp/audiences/universal-ids.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
