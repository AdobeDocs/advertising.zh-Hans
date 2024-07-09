---
title: 转换用户ID [!DNL Amperity] 到通用ID
description: 了解如何启用DSP以摄取 [!DNL Amperity] 第一方区段。
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: ed74f3fa3d0036e0dc8a529b05452567527f68a1
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# 转换用户ID [!DNL Amperity] 到通用ID

*Beta功能*

将DSP与集成 [!DNL Amperity] 客户数据平台，用于将贵组织的第一方经过哈希处理的电子邮件地址转换为通用ID以进行定向广告。

1. (要将电子邮件地址转换为 [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->；广告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [设置要启用的跟踪 [!DNL Analytics] 测量](#analytics-tracking).

1. [在DSP中创建受众源](#source-create).

1. [准备和共享区段映射数据](#map-data).

1. [请求从推送数据 [!DNL Amperity] 到DSP](#push-data).

1. [将通用ID的数量与经过哈希处理的电子邮件地址的数量进行比较](#compare-id-count).

## 步骤1：设置跟踪 [!DNL Analytics] 测量 {#analytics-tracking}

*广告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

要将电子邮件地址转换为 [!DNL RampIDs] 或 [!DNL ID5] ID之后，您必须执行以下操作：

1. （如果您尚未这样做）完成所有 [实施的先决条件 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) 并确保 [AMO ID和EF ID](/help/integrations/analytics/ids.md) 将在您的跟踪URL中填充。

1. 向通用ID合作伙伴注册，并在您的网页上部署特定于通用ID的代码，以便匹配从桌面和移动Web浏览器（但不包括移动应用程序）上的ID到显示到达次数的转换：

   * **对象 [!DNL RampIDs]：** 您必须在您的网页上部署额外的JavaScript标记，以便匹配从桌面和移动Web浏览器（但不包括移动应用程序）上的ID到显示到达的转换。 请联系您的Adobe客户团队，他们将为您提供注册 [!DNL LiveRamp] [!DNL LaunchPad] 标记自 [!DNL LiveRamp] 身份验证流量解决方案。 注册是免费的，但您必须签署协议。 注册后，您的Adobe客户团队将生成并提供一个唯一标记，供贵组织在网页上实施。

## 步骤2：在DSP中创建受众源 {#source-create}

1. [创建受众源](source-manage.md) 将受众导入您的DSP帐户或广告商帐户。 您可以选择将用户标识符转换为 [可用的通用ID格式](source-about.md).

   源设置将包括自动生成的源密钥，您将使用该密钥来推送区段数据。

1. 创建受众源后，请使用以下对象共享源代码密钥 [!DNL Amperity] 用户。

## 步骤3：准备和共享区段映射数据 {#map-data}

广告商必须准备并共享区段映射数据。

1. 范围 [!DNL Amperity]，使用SHA-256算法对受众的电子邮件ID进行哈希处理。

1. 广告商必须向Adobe客户团队提供区段映射数据，才能在DSP中创建区段。 在逗号分隔的值文件中使用以下列名和值：

   * **外部区段密钥：** 此 [!DNL Amperity] 与区段关联的区段键。

   * **区段名称：** 区段名称。

   * **区段描述：** 区段的目的或规则，或同时使用两者。

   * **父级ID：** 保持空白

   * **视频CPM：** 0

   * **显示CPM：** 0

   * **区段窗口：** 区段的存留时间。

## 步骤4：请求从推送数据 [!DNL Amperity] 到DSP {#push-data}

1. 在DSP中映射区段后，广告商必须结合其 [!DNL Amperity] 代表将区段数据分发到DSP。

1. 然后，广告商必须与Adobe客户团队确认已收到区段数据。

区段应在24小时内可在DSP中使用。 验证受众库（从中创建或编辑受众时可用） [!UICONTROL Audiences] > [!UICONTROL All Audiences] 区段可用且正在填充的用户档案（或位于版面设置内）。

区段将按照为中的广告商配置的方式刷新 [!DNL Amperity]. 无论区段的刷新频率如何，默认情况下，区段中包含的内容会在30天后过期，或者在客户指定的有效期后过期。 通过从重新推送区段来刷新区段 [!DNL Amperity] 到期之前。 要请求自定义区段过期，请联系您的Adobe客户团队。

## 步骤5：比较通用ID的数量与经过哈希处理的电子邮件地址的数量 {#compare-id-count}

DSP收到区段数据后，受众计数应在九(9)小时内可见。 在受众库中（从中创建或编辑受众时可用） [!UICONTROL Audiences] > [!UICONTROL All Audiences] （或者在版面设置内）比较通用ID的数量与原始经过哈希处理的电子邮件地址的数量。

经过哈希处理的电子邮件地址到通用ID的翻译率应大于90%；的翻译率为 [!DNL RampIDs] 如果所有经过哈希处理的电子邮件地址都是唯一的，则尤其应该为95%。 例如，如果您从客户数据平台发送了100个经过哈希处理的电子邮件地址，则应将其翻译为至少95个 [!DNL RampIDs] 或90多种其他类型的通用ID。 较低的翻译率是个问题。 有关区段计数如何变化的更多信息，请参阅&quot;[电子邮件ID与通用ID之间的数据差异原因](#universal-ids-data-variances)“

有关故障排除支持，请联系您的Adobe客户团队或 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [关于第一方受众源](/help/dsp/audiences/sources/source-about.md)
>* [管理受众源以激活通用ID受众](source-manage.md)
>* [支持激活通用ID](/help/dsp/audiences/universal-ids.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
