---
title: 将用户ID从 [!DNL Amperity] 转换为通用ID
description: 了解如何使DSP能够摄取您的 [!DNL Amperity] 第一方区段。
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# 将用户ID从[!DNL Amperity]转换为通用ID

*Beta功能*

使用DSP与[!DNL Amperity]客户数据平台的集成，将贵组织的第一方经过哈希处理的电子邮件地址转换为通用ID以进行定向广告。

1. （要将电子邮件地址转换为[!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；广告商具有[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)） [设置跟踪以启用 [!DNL Analytics] 测量](#analytics-tracking)。

1. [在DSP](#source-create)中创建受众源。

1. [准备并共享区段映射数据](#map-data)。

1. [请求从 [!DNL Amperity] 向DSP](#push-data)推送数据。

1. [将通用ID的数量与经过哈希处理的电子邮件地址的数量进行比较](#compare-id-count)。

## 步骤1：为[!DNL Analytics]测量设置跟踪 {#analytics-tracking}

*广告商与[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

要将电子邮件地址转换为[!DNL RampIDs]或[!DNL ID5] ID，您必须执行以下操作：

1. （如果尚未这样做）完成实施 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)的所有[先决条件，并确保在您的跟踪URL中填充[AMO ID和EF ID](/help/integrations/analytics/ids.md)。

1. 向通用ID合作伙伴注册，并在您的网页上部署特定于通用ID的代码，以便匹配从桌面和移动Web浏览器（但不包括移动应用程序）上的ID到显示到达次数的转换：

   * **对于[!DNL RampIDs]：**，您必须在网页上部署额外的JavaScript标记，以匹配从桌面和移动网页浏览器（但不包括移动应用程序）上的ID到显示到达次数的转换。 请与您的Adobe客户团队联系，他们将为您提供如何从[!DNL LiveRamp]身份验证流量解决方案注册[!DNL LiveRamp] [!DNL LaunchPad]标记的说明。 注册是免费的，但您必须签署协议。 注册后，您的Adobe客户团队将生成并提供一个唯一标记，供贵组织在网页上实施。

## 步骤2：在DSP中创建受众源 {#source-create}

1. [创建受众源](source-manage.md)以将受众导入您的DSP帐户或广告商帐户。 您可以选择将用户标识符转换为[可用的通用ID格式](source-about.md)中的任意格式。

   源设置将包括自动生成的源密钥，您将使用该密钥来推送区段数据。

1. 创建受众源后，与[!DNL Amperity]用户共享源代码密钥。

## 步骤3：准备和共享区段映射数据 {#map-data}

广告商必须准备并共享区段映射数据。

1. 在[!DNL Amperity]内，使用SHA-256算法对受众的电子邮件ID进行哈希处理。

1. 广告商必须向Adobe客户团队提供区段映射数据，才能在DSP中创建区段。 在逗号分隔的值文件中使用以下列名和值：

   * **外部区段键：**&#x200B;与该区段关联的[!DNL Amperity]区段键。

   * **区段名称：**&#x200B;区段名称。

   * **区段描述：**&#x200B;区段的用途或规则，或同时使用两者。

   * **父ID：**&#x200B;保留为空

   * **视频CPM：** 0

   * **显示CPM：** 0

   * **区段窗口：**&#x200B;区段生存时间。

## 步骤4：请求从[!DNL Amperity]向DSP推送数据 {#push-data}

1. 在DSP中映射区段后，广告商必须与其[!DNL Amperity]代表合作，以将区段数据分发到DSP。

1. 然后，广告商必须与Adobe客户团队确认已收到区段数据。

区段应在24小时内可在DSP中使用。 验证受众库（在从[!UICONTROL Audiences] > [!UICONTROL All Audiences]创建或编辑受众时或在版面设置内创建或编辑受众时可用）中该区段是否可用且是否正在填充。

区段将按为[!DNL Amperity]中的广告商配置的方式刷新。 无论区段的刷新频率如何，默认情况下，区段中包含的内容会在30天后过期，或者在客户指定的有效期后过期。 在到期之前从[!DNL Amperity]重新推送区段，以刷新区段。 要请求自定义区段过期，请联系您的Adobe客户团队。

## 步骤5：比较通用ID的数量与经过哈希处理的电子邮件地址的数量 {#compare-id-count}

DSP收到区段数据后，受众计数应在九(9)小时内可见。

在受众库中（在从[!UICONTROL Audiences] > [!UICONTROL All Audiences]创建或编辑受众时或在版面设置内可用），将通用ID的数量与原始经过哈希处理的电子邮件地址的数量进行比较。 有关可接受的ID转换率以及区段计数发生变化原因的信息，请参阅[电子邮件ID与通用ID之间的数据差异](#universal-ids-data-variances)。

## 故障排除

若要解决翻译速率和用户计数问题，请参阅“[激活通用ID的支持](/help/dsp/audiences/universal-ids.md)”。

若要排除转换过程的问题，请与您的Adobe客户团队或`adcloud-support@adobe.com`联系。

>[!MORELIKETHIS]
>
>* [关于第一方受众源](/help/dsp/audiences/sources/source-about.md)
>* [管理受众源以激活通用ID受众](source-manage.md)
>* [支持激活通用ID](/help/dsp/audiences/universal-ids.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
