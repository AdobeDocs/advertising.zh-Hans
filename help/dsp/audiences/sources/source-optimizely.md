---
title: 将用户ID从 [!DNL Optimizely] 转换为通用ID
description: 了解如何使DSP能够摄取您的 [!DNL Optimizely] 第一方区段。
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# 将用户ID从[!DNL Optimizely]转换为通用ID

*Beta功能*

使用DSP与[!DNL Optimizely]客户数据平台的集成，将贵组织的第一方经过哈希处理的电子邮件地址转换为通用ID以进行定向广告。

1. （要将电子邮件地址转换为[!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；广告商具有[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)） [设置跟踪以启用 [!DNL Analytics] 测量](#analytics-tracking)。

1. [在DSP](#source-create)中创建受众源。

1. [准备并推送区段数据](#push-data)。

1. [将通用ID的数量与经过哈希处理的电子邮件地址的数量进行比较](#compare-id-count)。

## 步骤1：为[!DNL Analytics]测量设置跟踪 {#analytics-tracking}

*广告商与[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

要将电子邮件地址转换为[!DNL RampIDs]或[!DNL ID5] ID，您必须执行以下操作：

1. （如果尚未这样做）完成实施 [!DNL Analytics for Advertising][&#128279;](/help/integrations/analytics/prerequisites.md)的所有先决条件，并确保在您的跟踪URL中填充[AMO ID和EF ID](/help/integrations/analytics/ids.md)。

1. 向通用ID合作伙伴注册，并在您的网页上部署特定于通用ID的代码，以便匹配从桌面和移动Web浏览器（但不包括移动应用程序）上的ID到显示到达次数的转换：

   * **对于[!DNL RampIDs]：**，您必须在网页上部署额外的JavaScript标记，以匹配从桌面和移动网页浏览器（但不包括移动应用程序）上的ID到显示到达次数的转换。 请与您的Adobe客户团队联系，他们将为您提供如何从[!DNL LiveRamp]身份验证流量解决方案注册[!DNL LiveRamp] [!DNL LaunchPad]标记的说明。 注册是免费的，但您必须签署协议。 注册后，您的Adobe客户团队将生成并提供一个唯一标记，供贵组织在网页上实施。

## 步骤2：在DSP中创建受众源 {#source-create}

1. [创建受众源](source-manage.md)以将受众导入您的DSP帐户或广告商帐户。 您可以选择将用户标识符转换为[可用的通用ID格式](source-about.md)中的任意格式。

   源设置将包括自动生成的源密钥，您将使用该密钥来推送区段数据。

1. 创建受众源后，与[!DNL Optimizely]用户共享源代码密钥。

## 步骤3：准备和推送区段数据 {#push-data}

广告商必须使用[!DNL Optimizely Data Platform]准备和推送数据。 有关此过程的任何问题，请与您的[!DNL Optimizely]代表联系。

1. 在[!DNL Optimizely Data Platform]内，使用SHA-256算法对受众的电子邮件ID进行哈希处理。

1. 按照[[!DNL Optimizely's] 说明将区段推送到DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads)。 请包含下列信息以启用集成：

   * **Source密钥：**&#x200B;这是在[步骤2](#source-create)中创建的源密钥。

   * **帐户代码：**&#x200B;这是字母数字DSP帐户代码，您可以在DSP中找到，地址为[!UICONTROL Settings] > [!UICONTROL Account]。

区段将按照为广告商配置的内容进行刷新。 无论区段的刷新频率如何，默认情况下，区段中包含的内容会在30天后过期，或者在客户指定的有效期后过期。 在到期之前从[!DNL Optimizely]重新推送区段，以刷新区段。 要请求自定义区段过期，请联系您的Adobe客户团队。

## 步骤4：比较通用ID的数量与经过哈希处理的电子邮件地址的数量 {#compare-id-count}

区段应在24小时内可在DSP中使用。 DSP收到区段数据后，受众计数应在九(9)小时内可见。

验证受众库（在从[!UICONTROL Audiences] > [!UICONTROL All Audiences]创建或编辑受众时或在版面设置内创建或编辑受众时可用）中区段是否可用且正在填充，并将通用ID的数量与原始经过哈希处理的电子邮件地址的数量进行比较。 有关可接受的ID转换率以及区段计数发生变化原因的信息，请参阅[电子邮件ID与通用ID之间的数据差异](#universal-ids-data-variances)。

## 故障排除

若要解决翻译速率和用户计数问题，请参阅“[激活通用ID的支持](/help/dsp/audiences/universal-ids.md)”。

若要排除转换过程的问题，请与您的Adobe客户团队或`adcloud-support@adobe.com`联系。

>[!MORELIKETHIS]
>
>* [关于第一方受众源](/help/dsp/audiences/sources/source-about.md)
>* [管理受众源以激活通用ID受众](source-manage.md)
>* [支持激活通用ID](/help/dsp/audiences/universal-ids.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
