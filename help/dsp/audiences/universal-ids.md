---
title: 支持激活通用 ID
description: 了解以下方面的支持信息：导入通用 ID 细分受众群、创建自定义细分受众群以跟踪通用 ID，以及将第一方细分受众群中的其他用户标识符转换为通用 ID，以便进行无 Cookie 定位。
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: ea50b94ebc6d27fda9c0bd9f61da16750fa58f83
workflow-type: tm+mt
source-wordcount: '1403'
ht-degree: 0%

---

# 支持激活通用 ID

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*测试功能*

DSP 支持以人为本的通用 ID，用于跨 DSP 支持的数字格式的无 Cookie 单设备（非跨设备）定位。

* 您可以使用仪表板[!DNL LiveRamp][!DNL Connect]手动将经过身份验证的 [ ][!DNL LiveRamp] [!DNL RampIDs]直接发送到 DSP。请参阅“[手动从中 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)导入经过身份验证的段”。

* DSP 可以摄取由客户数据平台 （CDP） 中内置的散列电子邮件 ID 组成的第一方细分，并将其转换为 [!DNL LiveRamp] [!DNL RampIDs] ID [!DNL Unified ID 2.0 (UID2.0)] 和。 如需详细了解受支持的客户数据平台、每种受支持的通用 ID 类型的可用功能以及相关工作流程，请参阅“[第一方受众来源](/help/dsp/audiences/sources/source-about.md)简介”。

* 您可以创建自定义细分，跟踪与 ID5 通用 ID 关联的用户、通过桌面设备和移动设备接触广告以及访问特定网页的用户。 ID5 使用概率模型来分配从各种用户信号和浏览器信号派生的 ID。 有关说明，请参阅“[创建和实现自定义分段](/help/dsp/audiences/custom-segment-create.md)”。

* 除了通过 Cookie 或设备 ID 跟踪的用户之外，来自某些供应商的第三方细分还可能自动包含通用 ID。 例如，来自 [!DNL Eyeota] 的分段可能自动包含 ID5 ID，而来自 [!DNL Lotame] 的分段可能包含 UID2.0 ID。 细分详细信息包括每种类型的尺寸。 每个段的通常使用费（在段名称旁边注明）适用;ID5 ID不收取额外费用。

## 按通用 ID 类型报告

* **自定义报告：** 自定义报告中提供了按通用 ID 类型划分的费用、展示次数、点击次数、转化次数和频次数据。

* **[!DNL Analytics]报告：** 已实施所有必需步骤的广告客户 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) 可以在 中 [!DNL Analytics]按通用 ID 类型查看浏览型转化。

  >[!IMPORTANT]
  >
  >要进行正确的转化归因，请确保广告的点击后到达网址同时 [包含 EF ID 和 AMO ID](/help/integrations/analytics/ids.md)。

* **细分受众群详情：** 对于所有细分受众群类型，细分受众群详细信息包括按通用 ID 类型以及通过 Cookie 或设备 ID 跟踪的设备类型划分的受众群体规模。

## 如何在版位定位通用 ID 受众群体

>[!NOTE]
>
>您无法更改实际展示位置中的目标 ID 类型。 如有必要，您可以复制实际展示位置，并在新展示位置中更改目标 ID 类型。

在新的、已排定的或已暂停的展示位置中，请执行以下操作：

1. 在该 [!UICONTROL Geo-Targeting] 部分中，指定要定位的地理区域。 每个通用 ID 合作伙伴仅允许用户定位特定地理区域，并且设置中 [!UICONTROL Targeting] 仅提供符合条件的 ID 类型。

1. 在本节 [!UICONTROL Audience Targeting] 中，执行以下操作：

   1. 在设置中 [!UICONTROL Included Audiences] ，选择用户数据已转换为通用 ID 的分段。

      如果需要，您可以添加其他细分。

   1. 在设置中 [!UICONTROL Targeting] ：

      1. 选择要定位的通用 ID 类型。

         此设置包括选项“[!UICONTROL Legacy IDs]”和“，”[!UICONTROL Universal ID]其中可能包括子选项“，”[!UICONTROL ID5][!UICONTROL RampID]“，”和“[!UICONTROL Unified ID2.0].”选定的地理目标确定可用的次级选项。

         您可以选择“[!UICONTROL Legacy IDs]”和“[!UICONTROL Universal ID]，但每个展示位置只能选择一种通用 ID。 当您同时选择旧 ID 和通用 ID 时，出价会优先选择通用 ID。

      1. （如有必要）接受有关使用通用 ID 的服务条款协议。

         在将数据转换为新的 ID 类型之前，DSP 帐户中的用户必须接受服务条款协议。 每个 ID 类型、每个帐户只能接受一次这些条款。

请参阅“放置设置](/help/dsp/campaign-management/placements/placement-settings.md)”。[

## 测试和数据验证的最佳实践

对支持 Adobe Analytics 测量功能的基于 ID 的区段和基于 ID5 的区段使用以下 [!DNL RampID]最佳实践。

* 激活分段后约 24 小时，检查 > [!UICONTROL All Audiences]内[!UICONTROL Audiences]分段的转换 ID 计数。如果 ID 计数意外，请联系您的 Adobe 帐户团队。

  请参阅“[电子邮件 ID 和通用 ID](#universal-ids-data-variances) 之间数据差异的原因”，了解有关细分计数如何变化的更多信息。

* 不要更改现有的包和展示位置。 但是，如果您没有任何增量预算来测试通用 ID，请减少原始预算以资助测试。

* 复制原始套餐和展示位置，根据测试规模调整预算，将受众群体更改为使用 [!DNL RampID]基于细分受众群（适用于经过身份验证的用户）或基于 ID5 的细分受众群（适用于未经身份验证的用户），并验证新套餐和展示位置是否用完了全部预算。

   * 要将基于通用 ID 的细分的效果与定位到其他受众群体标识符（例如 Cookie 或移动广告 ID）的展示位置的效果进行比较，请创建一个包含单独的基于通用 ID 的展示位置和基于旧版 ID 的展示位置的广告系列。

     对于完整的重定向测试，请为经过身份验证的用户定位 RampID，为未经身份验证的用户定位 ID5。

     获得最佳性能不应是主要的比较。 相反，请确定哪些 ID 可以很好地扩展，这可能会在稍后为您的优化和预算分配提供信息。 长期目标是在 Cookie 被弃用后弥补失去的展示次数和网站流量。

   * 要比较浏览器的总覆盖面，请在同一版位中定位基于通用 ID 的细分受众群和基于旧版 ID 的细分受众群。 使用与上一个用例相同的广告系列设置，但您无需拆分广告系列预算。

     通用 ID 优先出价，但当通用 ID 不可用时，旧 ID 会收到出价。 请务必比较不同浏览器（包括 Chrome、Safari 和 Mozilla）的覆盖面。

     >[!NOTE]
     >
     >频次上限适用于单个 ID。 如果用户有多种 ID 类型，您接触该用户的次数可能会超出预期。

* 请记住，经过身份验证的细分受众群的覆盖面自然小于基于 Cookie 的细分受众群的覆盖面，使用其他定位选项会进一步减少您的覆盖面。 明智地使用精细定位，尤其是将多个目标与 AND 语句联接在一起时。

## 电子邮件 ID 和通用 ID 之间存在数据差异的原因 {#universal-ids-data-variances}

* 将经过哈希处理的电子邮件 ID 转换为 ID5 ID：

  概率模型的误差方差为 +/- 5%。 这意味着它可以高估或低估 5% 的受众数量。

* 经过哈希处理的电子邮件 ID 翻译为 [!DNL RampIDs]：

   * 当多个配置文件使用相同的电子邮件 ID 时，DSP 段计数可能低于客户数据平台中的配置文件计数。 例如，在 Adobe Photoshop 中，您可以使用一个电子邮件 ID 创建公司帐户和个人帐户。 但是，如果两个配置文件都属于同一个人，则配置文件映射到一个电子邮件 ID 并相应地映射到一个 [!DNL RampID].

   * A [!DNL RampID] 可以升级到新值。 如果 [!DNL LiveRamp] 无法识别电子邮件 ID 或无法将其映射到其数据库中的现有 [!DNL RampID] ID，则会为电子邮件 ID 分配一个新 [!DNL RampID] ID。 将来，当他们可以将电子邮件 ID 映射到另一个 [!DNL RampID] ID 或可以收集有关同一电子邮件 ID 的更多信息时，他们会将该 [!DNL RampID] 升级到新值。 [!DNL LiveRamp]将此操作称为从“派生”[!DNL RampID]升级到“维护”。 [!DNL RampID]但是，DSP 不会获取派生和维护 [!DNL RampIDs] 之间的映射，因此无法从 DSP 段中删除以前版本的 RampID。 在这种情况下，段计数可能超过配置文件计数。

     示例：用户登录到 [!DNL Adobe] 网站并访问 Photoshop 页面。 如果 [!DNL LiveRamp] 没有任何关于电子邮件 ID 的现有信息，那么他们会为其分配一个派生 [!DNL RampID]的 ，比如 D123。 15 天后，用户访问了同一页面，但在 [!DNL LiveRamp] 这 15 天内升级了 [!DNL RampID] 该页面，并已将其重新分配给 [!DNL RampID] M123。 尽管客户数据平台的“Photoshop Enthusiast”细分市场只有一个用户电子邮件ID，但DSP细分市场有两个RampID：D123和M123。

## 故障排除

如果您没有看到用户数量，或者您的受众规模较低，请检查以下内容：

* 如果您使用 [!DNL Flashtalking] 或 [!DNL Google Campaign Manager 360] 广告，请确保您广告的点击后到达网址附加了正确的宏。 请参阅广告](/help/integrations/analytics/macros-flashtalking.md)和[[!DNL Google Campaign Manager 360] 广告](/help/integrations/analytics/macros-google-campaign-manager.md)的[[!DNL Flashtalking] 宏。

* 确保在您的网站上实施正确的通用 ID 合作伙伴特定代码，以匹配网站活动和广告曝光。 根据需要与您或[!DNL ID5]代表合作[!DNL LiveRamp]。

* （For [!DNL RampIDs] 和 [!DNL UID 2.0] ID）确保您的 [DSP 数据源配置正确](/help/dsp/audiences/sources/source-manage.md#source-settings)，并且已为生成的细分受众群填充用户计数。

* 如果您的覆盖面低于预期，请检查受众细分逻辑是否过于精细。

* 确保您的广告系列、包装和展示位置设置正确无误。<!-- wording-->

如果您无法解决此问题，请联系您的 Adobe 帐户团队。

>[!MORELIKETHIS]
>
>* [第一方受众来源简介](/help/dsp/audiences/sources/source-about.md)
>* [管理受众来源以激活通用 ID 受众](/help/dsp/audiences/sources/source-manage.md)
>* [创建和实现自定义区段](/help/dsp/audiences/custom-segment-create.md)
>* [从 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [受众管理简介](/help/dsp/audiences/audience-about.md)
>* [放置设置](/help/dsp/campaign-management/placements/placement-settings.md)
