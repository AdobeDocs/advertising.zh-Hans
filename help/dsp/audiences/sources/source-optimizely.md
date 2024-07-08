---
title: 将用户 ID 从 ID 转换为 [!DNL Optimizely] 通用 ID
description: 了解如何启用 DSP 以引入您的 [!DNL Optimizely] 第一方细分受众群。
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 2c42e8e4b7ca7e0cfaaf7895f067e4ccf7a2a40e
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 0%

---

# 将用户 ID 从 ID 转换为 [!DNL Optimizely] 通用 ID

*测试功能*

将 DSP 与客户数据平台集成， [!DNL Optimizely] 将组织的第一方哈希电子邮件地址转换为通用 ID，以便投放有针对性的广告。

1. （要将电子邮件地址[!DNL RampIDs]<!-- or [!DNL ID5] IDs -->转换为 ;具有 ） [的广告[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)客户设置跟踪以启用 [!DNL Analytics] 衡量](#analytics-tracking)。

1. [在 DSP](#source-create) 中创建受众来源。

1. [准备和推送段数据](#push-data)。

1. [将通用 ID 的数量与经过哈希处理的电子邮件地址](#compare-id-count)的数量进行比较。

## 第 1 步：设置用于衡量的 [!DNL Analytics] 跟踪 {#analytics-tracking}

*具有 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)） 的广告主*

要将电子邮件地址 [!DNL RampIDs] 转换为 ID [!DNL ID5] 或 ID，您必须执行以下操作：

1. （如果您尚未这样做）完成实施的所有[先决条件，并确保[在跟踪 URL 中填充 AMO ID 和 EF ID](/help/integrations/analytics/ids.md)。 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)

1. 向通用 ID 合作伙伴注册并在您的网页上部署特定于通用 ID 的代码，以匹配从桌面和移动 Web 浏览器（但不是移动应用）上的 ID 到浏览型的转化：

   * **对于 [!DNL RampIDs]：** 您必须在网页上部署额外的 JavaScript 标记，以便将桌面和移动 Web 浏览器（但不是移动应用）上的 ID 转化为浏览型的转化相匹配。 请联系您的 Adobe 客户团队，他们将指导您注册[!DNL LiveRamp][!DNL LaunchPad]身份验证流量解决方案中的[!DNL LiveRamp]标签。注册是免费的，但您必须签署协议。 注册后，您的 Adobe 帐户团队将生成并提供一个唯一标记，供您的组织在您的网页上实施。

## 第 2 步：在 DSP 中创建受众源 {#source-create}

1. [创建受众群体来源](source-manage.md) ，将受众群体导入您的 DSP 帐号或广告客户帐号。 您可以选择将用户标识符转换为任何 [可用的通用 ID 格式](source-about.md)。

   源设置将包括一个自动生成的源密钥，您将使用该密钥推送区段数据。

1. 创建受众群体来源后，请与 [!DNL Optimizely] 用户共享源代码密钥。

## 步骤 3：准备和推送分段数据 {#push-data}

广告商必须在其 [!DNL Optimizely] 代表的帮助下准备和推送数据。

1. 在 中 [!DNL Optimizely Data Platform]，使用 SHA-256 算法对广告客户受众的电子邮件 ID 进行哈希处理。

1. 按照 [[!DNL Optimizely's] 说明将分段推送到 DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads)。 包括以下信息以启用集成：

   * **源密钥：**&#x200B;这是在步骤 2](#source-create) 中创建[的源密钥。

   * **帐户代码：**&#x200B;这是字母数字 DSP 帐户代码，您可以在 > [!UICONTROL Account]的 [!UICONTROL Settings] DSP 中找到。

这些细分受众群应在 24 小时内在 DSP 中可用，并按照针对广告客户的配置进行刷新。 无论刷新分段的频率如何，默认情况下，分段中包含的内容都会在 30 天后或客户指定的过期期限之后过期。 通过在到期前重新推送 [!DNL Optimizely] 细分来刷新您的区段。 要请求自定义细分过期，请联系您的 Adobe 帐户团队。

## 步骤 4：将通用 ID 的数量与经过哈希处理的电子邮件地址的数量进行比较 {#compare-id-count}

完成所有步骤后，请在受众群体库（当您通过 [!UICONTROL Audiences] > [!UICONTROL All Audiences] 或在展示位置设置中创建或编辑受众时可用）中验证该细分是否可用并在 24 小时内填充。 将通用 ID 的数量与原始哈希电子邮件地址的数量进行比较。

经过哈希处理的电子邮件地址到通用 ID 的转换率应大于 90%。 例如，如果您从客户数据平台发送 100 个经过哈希处理的电子邮件地址，则应将其转换为 90 多个通用 ID。 90% 或更低的翻译率是一个问题。 有关段计数如何变化的更多信息，请参阅“[电子邮件 ID 和通用 ID](#universal-ids-data-variances) 之间数据差异的原因”。

如需疑难解答支持，请联系您的 Adobe 帐户团队或 `adcloud-support@adobe.com`。

>[!MORELIKETHIS]
>
>* [第一方受众来源简介](/help/dsp/audiences/sources/source-about.md)
>* [管理受众来源以激活通用 ID 受众](source-manage.md)
>* [支持激活通用 ID](/help/dsp/audiences/universal-ids.md)
>* [受众管理简介](/help/dsp/audiences/audience-about.md)
