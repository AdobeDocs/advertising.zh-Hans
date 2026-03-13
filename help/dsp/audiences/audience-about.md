---
title: 广告数字信号处理中的受众管理
description: 了解受众管理功能。
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: ddd55586ed895962b8f6da0390a3d76fe43ca1ca
workflow-type: tm+mt
source-wordcount: '1322'
ht-degree: 0%

---

# 广告数字信号处理中的受众管理

在DSP中，您可以创建和管理受众区段和受众集，并将其用作放置的目标：

* 通过创建和实施DSP片段来收集您自己的第一方受众数据。 您以后可以使用广告重新定位区段中的用户，或阻止区段中的用户接收广告。 可以创建以下类型的段：

   * [自定义区段](/help/dsp/audiences/custom-segment-create.md)用于跟踪a)暴露于桌面和移动设备广告的用户和b)访问特定网页的用户。 跟踪标签可以跟踪基于Cookie的用户或与ID5通用ID关联的用户。

   * [CCPA opt-out-of-sale segments](/help/dsp/audiences/ccpa-opt-out-segment-create.md) to track the users IDs from consumer opt-out-of-sale requests on your website, per the California Consumer Privacy Act (CCPA). 您可以从选择退出销售请求中检索用户ID的月度报表。

     有关Adobe Advertising对CCPA选择退出销售请求的支持的更多信息，请参阅[Adobe Advertising对《加州消费者隐私法案》的支持：消费者选择退出支持](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)。

* （Beta功能）[获取并使用通用ID进行无令牌定位](/help/dsp/audiences/universal-ids.md)：

   * 手动将经过身份验证的[!DNL LiveRamp] [!DNL RampID]区段直接发送到DSP。

   * 允许DSP从您的客户数据平台导入第一方区段，并将它们转换为支持的通用ID类型。

   * 在放置目标中包含包含通用ID的第三方区段，无需任何额外步骤。

* 创建包含[可重用受众](/help/dsp/audiences/reusable-audience-create.md)的受众库。 Saved audiences are composed of any of your available audience segments and any of your other saved audiences. Any changes you make to a saved audience are automatically applied to all placements that target or exclude the audience and to all other audiences that include the saved audience.

  Saved audiences allow media planners to group audiences as needed, by including and excluding multiple segments using complex Boolean logic. The  (targetable) size of each individual segment and the overall active audience size are indicated as you build an audience. Campaign executioners can then simply select one or more saved audiences as placement targets rather than manually configure audience targets for each placement.

其他受众类型也可用于投放定位。

## 导入第一方和第三方数据区段

您可以使用DSP用户界面和/或通过自定义导入服务，将第一方和第三方数据区段导入到DSP中，选项很多。

* DSP可以拉入您的Adobe Audience Manager和其他[!DNL Adobe]受众来进行定位。 有关先决条件和说明，请参阅&#39;&#39;[为广告定位导入Adobe Audience Manager区段](/help/integrations/audience-manager/import-audiences.md)&#39;。

* DSP可以使用[源功能](/help/dsp/audiences/sources/source-about.md)将第一方数据区段从支持的客户数据平台转换为具有通用ID的区段。 您也可以[手动将经过身份验证的 [!DNL LiveRamp] [!DNL RampID]区段直接发送到DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md)。

* DSP可以直接从数据管理平台(DMP)导入您的其他第一方数据区段，并根据需要将其提供给任何一组广告商。

* DSP可以导入自定义第三方区段，包括第三方区段的复杂组合。 您可以根据需要将区段提供给任何一组广告商。

有关更多信息，请与您的Adobe客户团队联系。

## 可用作投放目标的受众

您可以将投放位置定位到以下所有类型的受众。

* 存储在DSP中的用户创建的所有受众集。

* 在DSP中创建的所有用户创建受众区段：

   * 自定义片段，适用于访问特定网页的用户和公开展示特定广告印象的用户。

     使用提供给通用ID的印象不会产生任何费用。

   * 根据《加州消费者隐私法》(CCPA)，CCPA会针对在您的网站上提交选择退出销售请求的用户，选择退出销售受众群体。

* 所有导入的第一方数据区段，包括转换为通用ID的区段。

  为向通用ID投放展示次数而收取额外费用。 有关费率，请参阅“[关于第一方受众源](/help/dsp/audiences/sources/source-about.md)”。

* 所有导入的自定义第三方数据段。

* （仅针对美国的位置） [适用于来自30多个提供商的DSP客户的所有第三方数据段](/help/dsp/audiences/third-party-data-providers.md)，包括[!DNL eXelate]、([!DNL Eyeota])、([!DNL LiveRamp])、[!DNL Lotame]、[!DNL Neustar]等。

  您可以针对特定的用户段，这些用户段基于受众数据（例如，具有特定人口统计、兴趣或意图和/或行为配置文件的用户）。 您可以按数据提供者和类别进行浏览，按名称或段ID搜索段，或按数据提供者、活动段大小、Web浏览器计数或设备计数筛选结果。

  第三方分部会产生额外费用，于各分部名称旁边列出。

* (仅使用Adobe AdvertisingJavaScript转换标记的具有Adobe Experience Platform和[!DNL Real-Time CDP]、Adobe Audience Manager或Adobe Analytics的广告客户)在[!DNL Real-Time CDP]中创建的所有可用的第一、第二或第三方受众区段，在Audience Manager中创建或从Audience Manager或[!DNL Analytics]发布到Adobe Experience Cloud。

  各分部使用之定价乃经预先磋商后厘定，且不会于DSP中显示。

  [!DNL Analytics]中的段将在您创建或发布为Experience Cloud受众约一小时后可用。 直接来自Audience Manager或[!DNL Real-Time CDP]的段在您共享它们后的24小时内可用。

  >[!NOTE]
  >
  >有关在这些解决方案中为段设置和收集数据的信息，请参阅[Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html)、[分析](https://experienceleague.adobe.com/docs/analytics.html)和[分析 [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html)的文档。

## 受众大小数据

在“受众”>“所有受众”以及位置设置的“受众目标”部分中，您可以按大小范围筛选每个区段列表，包括特定设备类型或通用ID类型的单独范围。

![按受众大小筛选](/help/dsp/assets/audience-size-filter.png)

您还可以查看详细的受众规模数据：

* 将显示所有选定片段和已保存受众的活动重复数据消除受众大小，您可以按设备类型（浏览器、移动设备或已连接的电视机）查看详细信息。

  ![组合受众规模](/help/dsp/assets/audience-size.png)

* 对于单个区段，活动受众规模和CPM（如果适用）会显示在区段名称旁边。

  ![单个段大小](/help/dsp/assets/audience-size-segment.png)

* 您可以查看有关单个细分市场或所保存受众的更多详细信息，包括浏览器、移动设备、联网电视和通用ID类型合作伙伴所占大小。 对于保存的受众，活动受众总大小是经过重复数据删除的总大小。

  ![单个区段或保存的受众详细信息](/help/dsp/assets/audience-size-segment-details.png)

## Audiences视图

### “所有访问群体”视图

在[!UICONTROL All Audiences]视图或受众库中，您可以保存和管理可重复使用的受众，包括受众区段组甚至其他保存的受众。 您可以使用受众作为多个放置的目标。 每个受众使用的置入数量在置入名称旁边指示。

您可以编辑、克隆、删除、导出或共享任何受众。

### 区段视图

在[!UICONTROL Segments]视图中，所有用户都可以创建其他自定义段。

[!UICONTROL Segments]视图还列出了以下段类型：

* 所有用户创建的自定义区段均可供用户使用。

  您可以查看所创建的任何自定义线段的跟踪标签，并与其他用户共享这些线段。 也可以编辑或删除创建的自定义线段。

  您无法编辑或共享其他用户已与您共享的自定义区段。

* All first-party segments imported as-is that are available to the user.

  您无法编辑或共享与您共享的第一方区段。 如果您需要与其他用户共享第一方区段，请联系您的Adobe客户团队。

* 所有自定义的第三方区段均可供用户使用。

  您无法编辑或共享与您共享的第三方区段。 如果需要与其他用户共享第三方区段，请联系您的Adobe客户团队。

### “源”视图

In the [!UICONTROL Sources] view, you can configure sources for first-party segments in supported customer data platforms that you want to convert to segments containing specified universal ID types. The source settings include an auto-generated source key, which you&#39;ll provide to your customer data platform to establish the connection.

For more information about the supported customer data platforms, supported universal ID types, and the workflows to set up connections to each customer data platform, see &quot;[About Sources](/help/dsp/audiences/sources/source-about.md).&quot;

The translated segments are available to include in reusable audiences and in placement settings for cookieless targeting.

>[!MORELIKETHIS]
>
>* [Support for Activating Universal IDs](/help/dsp/audiences/universal-ids.md)
>* [创建可重复使用的受众](reusable-audience-create.md)
>* [创建和实施自定义区段](custom-segment-create.md)
>* [创建并实施[!UICONTROL CCPA Opt-Out-of-Sale]区段](ccpa-opt-out-segment-create.md)
>* [关于第一方受众源](/help/dsp/audiences/sources/source-about.md)
>* [管理受众源以激活通用ID受众](/help/dsp/audiences/sources/source-manage.md)
>* [从 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)手动导入经过身份验证的区段
>* [可用的第三方数据提供程序](third-party-data-providers.md)
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
