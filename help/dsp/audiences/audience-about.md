---
title: 关于Advertising DSP中的受众管理
description: 了解受众管理功能。
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 31f20bcfb79265326f515218a02d8a4fa3efd586
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# 关于Advertising DSP中的受众管理

在DSP中，您可以创建和管理受众区段和受众集，并将其用作投放位置的目标：

* 通过创建和实施DSP区段来收集您自己的第一方受众数据。 之后，您可以使用广告重新定位区段中的用户，或阻止区段中的用户接收广告。 您可以创建以下类型的区段：

   * [自定义区段](/help/dsp/audiences/custom-segment-create.md)，用于跟踪a)从桌面和移动设备向广告公开的用户和b)访问特定网页的用户。 跟踪标记可以跟踪基于Cookie的用户或与ID5通用ID关联的用户。

   * [CCPA选择退出销售区段](/help/dsp/audiences/ccpa-opt-out-segment-create.md)，用于根据加州消费者隐私法案(CCPA)跟踪您网站上消费者选择退出销售请求的用户ID。 您可以从选择退出销售请求中检索用户ID的月度报表。

     有关Adobe Advertising对CCPA选择退出销售请求的支持的更多信息，请参阅[Adobe Advertising对《加州消费者隐私法案》的支持：消费者选择退出支持](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)。

* (Beta功能) [获取并使用通用ID进行无令牌定位](/help/dsp/audiences/universal-ids.md)：

   * 手动将经过身份验证的[!DNL LiveRamp] [!DNL RampID]区段直接发送到DSP。

   * 允许DSP从您的客户数据平台导入第一方区段，并将它们转换为支持的通用ID类型。

   * 无需执行任何额外步骤，即可在投放目标中包含包含通用ID的第三方区段。

* 创建[可重用受众](/help/dsp/audiences/reusable-audience-create.md)的受众库。 保存的受众由任何可用受众区段和任何其他保存的受众组成。 您对保存的受众所做的任何更改将自动应用于所有定向或排除该受众的投放位置，并应用于包括保存的受众的所有其他受众。

  保存的受众允许媒体规划者根据需要对受众进行分组，具体做法是使用复杂的布尔逻辑包含和排除多个区段。 在构建受众时，将指示每个单个区段的大小和总受众大小。 然后，Campaign执行者只需选择一个或多个保存的受众作为投放目标，而无需为每个投放手动配置受众目标。

其他受众类型也可用于投放定位。

## 导入第一方和第三方数据区段

您可以使用DSP用户界面和/或通过自定义导入服务，将第一方和第三方数据区段导入DSP中，选项很多。

* DSP可以拉入您的Adobe Audience Manager和其他[!DNL Adobe]受众以进行定位。 有关先决条件和说明，请参阅&#39;&#39;[为广告定位导入Adobe Audience Manager区段](/help/integrations/audience-manager/import-audiences.md)&#39;。

* DSP可以使用[源功能](/help/dsp/audiences/sources/source-about.md)将第一方数据区段从支持的客户数据平台转换为具有通用ID的区段。 您也可以[手动将经过身份验证的 [!DNL LiveRamp] [!DNL RampID]区段直接发送到DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md)。

* DSP可以直接从数据管理平台(DMP)导入您的其他第一方数据区段，并根据需要将其提供给任何一组广告商。

* DSP可以导入自定义第三方区段，包括第三方区段的复杂组合。 您可以根据需要将区段提供给任何一组广告商。

有关更多信息，请与您的Adobe客户团队联系。

## 可用作投放目标的受众

您可以将投放位置定位到以下所有类型的受众。

* 所有用户创建的受众集，保存在DSP中。

* 在DSP中创建的所有用户创建的受众区段：

   * 访问特定网页的用户和展示特定广告印象的用户适用的自定义区段。

     对于传送到通用ID的展示，不产生任何费用。

   * CCPA根据《加州消费者隐私法案》(CCPA)的规定，对在您的网站上提交选择退出销售请求的用户的选择退出销售受众区段。

* 所有导入的第一方数据区段，包括转换为通用ID的区段。

  为向通用ID投放展示次数而收取额外费用。 有关费率，请参阅[关于第一方受众源](/help/dsp/audiences/sources/source-about.md)。

* 所有导入的自定义第三方数据区段。

* （仅针对美国的版面） [所有第三方数据区段均可供来自30多家提供商的DSP客户使用](/help/dsp/audiences/third-party-data-providers.md)，包括[!DNL eXelate]、([!DNL Eyeota])、([!DNL LiveRamp])、[!DNL Lotame]、[!DNL Neustar]等。

  您可以定位特定的区段，这些区段根据受众数据定位用户（例如，具有特定人口统计信息、兴趣或意图和/或行为配置文件的用户）。 您可以按数据提供商和类别浏览，按名称或区段ID搜索区段，或按数据提供商、区段总大小、Web浏览器计数或设备计数过滤结果。

  第三方区段会产生额外费用，这些费用显示在每个区段名称旁边。

* (仅使用Adobe Advertising JavaScript转化标记且具有Adobe Experience Platform和[!DNL Real-Time CDP]、Adobe Audience Manager或Adobe Analytics的广告商)您在[!DNL Real-Time CDP]中创建的所有可用第一方、第二方或第三方受众区段，或者在Audience Manager中创建或从Audience Manager或[!DNL Analytics]发布到Adobe Experience Cloud。

  使用分部的定价是预先协商的，在DSP中不可见。

  [!DNL Analytics]中的区段在您创建或发布为Experience Cloud受众后大约一小时内可用。 直接来自Audience Manager或[!DNL Real-Time CDP]的区段在您共享它们后的24小时内可用。

  >[!NOTE]
  >
  >有关在这些解决方案中为区段设置和收集数据的信息，请参阅[Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html?lang=zh-Hans)、[Analytics](https://experienceleague.adobe.com/docs/analytics.html?lang=zh-Hans)和[The [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html?lang=zh-Hans)的文档。

## 受众规模数据

在受众>所有受众和版面设置的“受众定位”部分中，您可以按大小范围筛选每个区段列表，包括总范围以及适用于特定设备类型或通用ID类型的单独范围。

![按受众规模筛选](/help/dsp/assets/audience-size-filter.png)

您还可以查看详细的受众规模数据：

* 系统会显示所有选定区段和已保存受众的活跃去重受众总人数，您可以按设备类型（浏览器、移动设备或连接的电视机）查看详细信息。

  ![组合受众规模](/help/dsp/assets/audience-size.png)

* 对于单个区段，总受众规模和CPM（如果适用）显示在区段名称旁边。

  ![单个区段大小](/help/dsp/assets/audience-size-segment.png)

* 您可以查看有关单个区段或所保存受众的更多详细信息，包括按浏览器、移动设备、联网电视和通用ID类型合作伙伴划分的大小。 对于保存的受众，总大小是去除重复项的总大小。

  ![单个区段或保存的受众详细信息](/help/dsp/assets/audience-size-segment-details.png)

## 受众视图

### “所有受众”视图

在[!UICONTROL All Audiences]视图或受众库中，您可以保存和管理可重用受众，其中包括受众区段组，甚至包括其他保存的受众。 您可以使用受众作为多个投放位置的目标。 每个受众使用的版面数量在版面名称旁显示。

您可以编辑、克隆、删除、导出或共享任何受众。

### 区段视图

在[!UICONTROL Segments]视图中，所有用户都可以创建其他自定义区段。

[!UICONTROL Segments]视图还列出了以下区段类型：

* 所有用户创建的自定义区段均可供用户使用。

  您可以查看所创建的任何自定义区段的跟踪标记，并与其他用户共享这些区段。 您还可以编辑或删除创建的自定义区段。

  您无法编辑或共享其他用户与您共享的自定义区段。

* 用户可按原样导入所有第一方区段。

  您无法编辑或共享与您共享的第一方区段。 如果您需要与其他用户共享第一方区段，请联系您的Adobe客户团队。

* 所有自定义的第三方区段均可供用户使用。

  您无法编辑或共享与您共享的第三方区段。 如果您需要与其他用户共享第三方区段，请联系您的Adobe客户团队。

### “源”视图

在[!UICONTROL Sources]视图中，您可以在受支持的客户数据平台上配置第一方区段的源，以将其转换为包含指定的通用ID类型的区段。 源设置包括自动生成的源密钥，您将将其提供给客户数据平台以建立连接。

有关受支持的客户数据平台、受支持的通用ID类型以及用于设置与每个客户数据平台的连接的工作流的详细信息，请参阅“[关于源](/help/dsp/audiences/sources/source-about.md)”。

翻译后的区段可用于包含在可重用受众和用于无痕定位的放置设置中。

>[!MORELIKETHIS]
>
>* [支持激活通用ID](/help/dsp/audiences/universal-ids.md)
>* [创建可重复使用的受众](reusable-audience-create.md)
>* [创建和实施自定义区段](custom-segment-create.md)
>* [创建并实施[!UICONTROL CCPA Opt-Out-of-Sale]区段](ccpa-opt-out-segment-create.md)
>* [关于第一方受众源](/help/dsp/audiences/sources/source-about.md)
>* [管理受众源以激活通用ID受众](/help/dsp/audiences/sources/source-manage.md)
>* [从 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)手动导入经过身份验证的区段
>* [可用的第三方数据提供程序](third-party-data-providers.md)
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
