---
title: 转换用户ID [!DNL Optimizely] 到通用ID
description: 了解如何启用DSP以摄取 [!DNL Optimizely] 第一方区段。
feature: DSP Audiences
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---

# 转换用户ID [!DNL Optimizely] 到通用ID

将DSP与集成 [!DNL Optimizely] 客户数据平台，用于将贵组织的第一方经过哈希处理的电子邮件地址转换为通用ID以进行定向广告。

1. (要将电子邮件地址转换为 [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；广告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [设置要启用的跟踪 [!DNL Analytics] 测量](#analytics-tracking).

1. [在DSP中创建受众源](#source-create).

1. [在中准备和推送区段数据 [!DNL Optimizely Data Platform]](#push-data).

1. [将通用ID的数量与经过哈希处理的电子邮件地址的数量进行比较](#compare-id-count).

区段应在24小时内可在DSP中使用，并且每24小时刷新一次。 **[是否为Optimizly提供真实或不同的期望？]**

## 步骤1：设置跟踪 [!DNL Analytics] 测量 {#analytics-tracking}

*广告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

要将电子邮件地址转换为 [!DNL RampIDs] 或 [!DNL ID5] ID之后，您必须执行以下操作：

1. （如果您尚未这样做）完成所有 [实施的先决条件 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) 并确保 [AMO ID和EF ID](/help/integrations/analytics/ids.md) 将在您的跟踪URL中填充。

1. 向通用ID合作伙伴注册，并在您的网页上部署特定于通用ID的代码，以便匹配从桌面和移动Web浏览器（但不包括移动应用程序）上的ID到显示到达次数的转换：

   * **对象 [!DNL RampIDs]：** 您必须在您的网页上部署一个额外的JavaScript标记，以便匹配从桌面浏览器和移动浏览器（但不是移动应用程序）上的ID到显示到达次数的转换。 请联系您的Adobe客户团队，他们将为您提供注册 [!DNL LiveRamp] [!DNL LaunchPad] 标记自 [!DNL LiveRamp] 身份验证流量解决方案。 注册是免费的，但您必须签署协议。 注册后，您的Adobe客户团队将生成并提供一个唯一标记，供贵组织在网页上实施。

## 步骤2：在DSP中创建受众源 {#source-create}

1. [创建受众源](source-manage.md) 将受众导入您的DSP帐户或广告商帐户。 您可以选择将用户标识符转换为 [可用的通用ID格式](source-about.md).

   源设置将包括自动生成的源密钥，您将使用该密钥来推送区段数据。

1. 创建受众源后，请使用以下对象共享源代码密钥 [!DNL Optimizely] 用户。

## 步骤3：准备和推送区段数据 {#push-data}

广告商必须准备数据并将其推送到中 [!DNL Optimizely Data Platform].  **[他们是否在使用Optimize Data Platform？]**  <!-- Data Platform? -->

1. 使用SHA-256算法对广告商受众的电子邮件ID进行哈希处理。

1. 将区段推送到DSP，包括以下字段：

   **[他们是否使用Data Platform Web服务、其他类型的API或UI？ 添加说明链接。 他们会在哪里输入这些字段？]**  <!-- Are they using the Data Platform web services or what? Add a link to instructions. And where will they input these fields?  -->

   * **源密钥：** 这是在中创建的源密钥 [步骤2](#source-create).

   * **帐户代码：** 这是字母数字DSP帐户代码，您可以在DSP中找到，网址为 [!UICONTROL Settings] > [!UICONTROL Account].

## 步骤4：比较通用ID的数量与经过哈希处理的电子邮件地址的数量 {#compare-id-count}

完成所有步骤后，在受众库中验证（在从创建或编辑受众时可用） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 区段可用，且会在24小时内填充。 将通用ID的数量与原始经过哈希处理的电子邮件地址的数量进行比较。

经过哈希处理的电子邮件地址到通用ID的转换率应大于90%。 例如，如果您从客户数据平台发送100个经过哈希处理的电子邮件地址，则应将其转换为90个以上的通用ID。 90%或更低的翻译率是一个问题。 有关区段计数如何变化的更多信息，请参阅&quot;[电子邮件ID与通用ID之间的数据差异原因](#universal-ids-data-variances)“

区段每24小时刷新一次。 但是，区段中的包含在30天后过期，因此无法确保隐私合规性，因此请从以下位置重新推送受众以刷新受众： [!DNL Optimizely] 每30天或更短时间。

有关故障排除支持，请联系您的Adobe客户团队或 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [关于第一方受众源](/help/dsp/audiences/sources/source-about.md)
>* [管理受众源以激活通用ID受众](source-manage.md)
>* [转换用户ID [!DNL Adobe Real-Time CDP] 到通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [转换用户ID [!DNL Tealium] 到通用ID](/help/dsp/audiences/sources/source-tealium.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)