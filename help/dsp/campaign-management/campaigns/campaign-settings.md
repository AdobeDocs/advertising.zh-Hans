---
title: Campaign设置
description: 请参阅可用营销活动设置的描述。
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: daf995b0c40d77434d2c86c738351a33552dc555
workflow-type: tm+mt
source-wordcount: '1066'
ht-degree: 0%

---

# Campaign设置

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]：**&#x200B;促销活动名称。

**[!UICONTROL Advertiser]：** （现有营销活动的只读）适用的广告商（品牌）。 选择现有广告商或创建新广告商。

**[!UICONTROL Advertiser URL]：**&#x200B;广告商的官方页面。 此字段可加快您与库存合作伙伴的广告审批流程。

**[!UICONTROL Timezone]：** （现有营销活动的只读）用于报告和竞价的时区。

**[!UICONTROL Customer PO]：**（可选）插入订单/采购订单的客户采购订单。

**[促销活动日期]：**&#x200B;促销活动的开始和结束日期。

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]：** （由使用利润率的代理机构服务的自助帐户）利润管理选项：

* **[!UICONTROL Would you like to manage margins for this campaign?]：**&#x200B;是管理促销活动的边距： *[!UICONTROL Yes]*&#x200B;还是&#x200B;*[!UICONTROL No]*（默认值）。 选择&#x200B;*[!UICONTROL Yes]时，*&#x200B;指定其他设置。 启用利润管理并保存活动后，将无法禁用利润管理。

* **[!UICONTROL How would you like to compute agency fees?]：** （仅具有利润管理的营销活动）如何计算代理费用：

   * *[!UICONTROL Margin % of Total Budget]：*（默认）按[!UICONTROL Gross Budget]的百分比计算费用。 指定[!UICONTROL Agency Fee Type] （固定或复合）和[!UICONTROL Margin %]或[!UICONTROL Composite Margin %]。

   * *[!UICONTROL Apply Markup % on top of individual cost components]：*&#x200B;将[!UICONTROL Gross Budget]的指定百分比添加到您的媒体成本、数据和其他成本和/或[!DNL Adobe]技术费用。 指定[!UICONTROL Markup %]并选择要应用标记的组件。

* **[!UICONTROL Agency Fee Type]：** （使用[!UICONTROL Margin % of Total Budget]的营销活动）代理费用的类型。

   * *[!UICONTROL Fixed]：*（默认）允许DSP根据[!UICONTROL Gross Budget]的固定百分比自动计算和限制支出。 指定[!UICONTROL Margin %]。

   * *[!UICONTROL Composite]：*&#x200B;允许DSP使用代理费和[!UICONTROL Gross Budget]技术费的复合百分比，根据[!DNL Adobe]的百分比自动计算和限制支出。 指定[!UICONTROL Composite Margin %]。

* **[!UICONTROL Margin %]：** （使用具有固定边距的[!UICONTROL Margin % of Total Budget]的营销活动）每个插入订单<!-- impression? -->的默认标记（以百分比表示）。 从[!UICONTROL Gross Budget]中扣除此金额以定义净促销活动预算。 未对[!UICONTROL Estimated Tax Withholding]上的[!UICONTROL Gross Budget]应用边距。

* **[!UICONTROL Composite Margin %]：** （使用具有复合利润的[!UICONTROL Margin % of Total Budget]的营销活动）代理费用和[!DNL Adobe]技术费用的总和（以百分比表示）。 从[!UICONTROL Gross Budget]中扣除此金额以定义净促销活动预算。 未对[!UICONTROL Estimated Tax Withholding]上的[!UICONTROL Gross Budget]应用边距。

* **[!UICONTROL Markup %]：** （使用[!UICONTROL Apply Markup % on top of individual cost components]的营销活动）要添加到指定成本组件的[!UICONTROL Gross Budget]的百分比。

* **[!UICONTROL Select cost components on which markup will be applied]：** （使用[!UICONTROL Apply Markup % on top of individual cost components]的营销活动）应用[!UICONTROL Markup %]的成本组件。 选择所有适用的组件： *[!UICONTROL Media cost]*、*[!UICONTROL Data and Other costs]*&#x200B;和/或&#x200B;*[!UICONTROL Adobe tech fees]*。

**[!UICONTROL Gross Budget]：** （仅具有毛利管理的营销活动）应用指定的边际调整之前的毛营销活动预算。

**[!UICONTROL Budget]：** （没有利润管理的营销活动）整体营销活动预算。

**[!UICONTROL Estimated Tax Withholding]：**&#x200B;在帐户级别预扣国家/地区或地方税的广告费用、广告服务费用和/或数据费用中的总支出百分比。 税率乃为编制预算及调整目的而估计，故发票税率可能有所不同。

要估计要预扣的税额，请执行以下操作：

1. 单击&#x200B;**[!UICONTROL Update rates here]**。

1. 以百分比形式指定&#x200B;**[!UICONTROL Estimated tax rate]**。

1. 选中要预扣税的每个费用类型旁边的复选框。 费用类型包括：

   * *[!UICONTROL Include estimated tax - ads fee]：*&#x200B;适用于所有Advertising DSP媒体支出，包括促销活动管理费用税。

   * *[!UICONTROL Include estimated tax - ad serving fee]：*&#x200B;适用于所有在Advertising DSP上支出（媒体和数据除外）。 它不包括营销活动管理费用税

   * *[!UICONTROL Include estimated tax - data fee]：*&#x200B;适用于在Advertising DSP上花费的所有数据。

1. 单击&#x200B;**[!UICONTROL Submit]**。

>[!NOTE]
>
>* 在美国，各州在包含广告、广告投放和数据的税费方面可能有所不同。 对于其他国家/地区的组织，请包括所有三类税费以便计入增值税。
>
>* 您还可以在帐户的费用设置中配置这些值。<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]：** （对于自2020年6月22日以来创建的现有营销活动为只读；对于2020年6月22日之前创建的营销活动不可用）DSP定位广告并应用频度上限的级别： *同一设备*&#x200B;定位设备或&#x200B;*人员*&#x200B;定位所有已知设备的人员。 **注意：**&#x200B;跨设备支持不适用于以通用ID为目标的投放位置。

**[!UICONTROL Device Graph]：** （对于现有营销活动为只读；仅具有基于人员的跨设备定位的营销活动）用于跨设备定位和频率管理的设备图：

* *[!UICONTROL LiveRamp - U.S. only]：*&#x200B;对于使用[!DNL LiveRamp]设备图交付的展示次数（即，在目标受众区段中未找到设备），适用于以$0.35 CPM为目标的跨设备广告商。 您可以在投放级别设置跨设备定位。

  此外，所有广告商也可以免费使用此选项进行频率管理和归因测量。

  跨设备支持仅适用于以旧版ID为目标的投放位置，不适用于以通用ID（包括[!DNL LiveRamps]）为目标的投放位置。 通用ID的定位、频率管理和归因仅在ID级别应用。

**[!UICONTROL Frequency Cap]：**（可选）从营销活动中为独特设备、通用ID或人员（取决于指定的[!UICONTROL Cross Device Level]和投放位置的[!UICONTROL Targeting]设置）提供广告的次数。 选项包括&#x200B;*[!UICONTROL Unlimited]*&#x200B;或每天、每周或每月的特定金额。

>[!NOTE]
>
> 您可以在营销活动、包和投放级别设置频率上限。 DSP遵循营销活动层级中最严格的频率限制。

**[!UICONTROL Packages]：**&#x200B;要包含在营销活动中的[包](/help/dsp/campaign-management/packages/package-about.md)。 选择现有包和/或创建要包含的包。 如果您创建包，请参阅有关[包设置](/help/dsp/campaign-management/packages/package-settings.md)的说明，以了解更多信息。

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>以下设置仅启用测量和报告功能。 性能优化仅在包级别和放置级别执行。

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]：**（可选）使用指定的设置启用[!DNL IAS]可视性、欺诈、品牌安全和受众验证的测量和报告。 需支付额外费用。

* **[!UICONTROL Measure On]：**&#x200B;要测量的库存： *[!UICONTROL Display and VPAID video inventory]* （默认值）或&#x200B;*[!UICONTROL Display, VPAID & VAST video inventory]*。

  >[!NOTE]
  >
  >视频可视性仅在VPAID内容库中可测量。

* **[!UICONTROL IAS Account ID (AnID)]：** （具有自己[!DNL IAS]帐户的广告商；可选）组织的[!DNL IAS]帐户ID，该ID将直接向[!DNL IAS]收取使用费。

* **[!UICONTROL IAS Team ID]：** （具有自己[!DNL IAS]帐户的广告商；可选）组织[!DNL IAS]帐户的团队ID，[!DNL IAS]将直接对使用收费。<!-- verify -->

#### 受众验证

**[!UICONTROL Comscore Campaign Ratings]：**（可选）使用指定的设置启用[!DNL Comscore]已验证的[!DNL Campaign Ratings]受众验证度量和报表。 需支付额外费用。

* **[!UICONTROL Target Gender]：**&#x200B;目标的性别： *[!UICONTROL Both]* （默认）、*[!UICONTROL Male]*&#x200B;或&#x200B;*[!UICONTROL Female]*

* **[!UICONTROL Target Age]：**&#x200B;目标的时间范围。 根据需要使用左右滑杆缩小范围。

* **[!UICONTROL Target Country]：**（可选）要定位的国家/地区。 [!DNL Comscore]度量展示次数仅在被支持的国家/地区提供。

### [!UICONTROL Attention Measurement]{#attention-measurement}

**[!UICONTROL Adelaide]：**&#x200B;启用投放位置级别[!UICONTROL Attention Score]量度的跟踪（展示次数中[!DNL Adelaide]“[!DNL Attention Units]”的加权平均数）。 指标可用于除[!DNL Roku]连接的电视、仅VPAID前置播放和非播客音频之外的所有投放类型。 DSP会自动将JavaScript标记附加到所有关联的创意人员，并且[!DNL Adelaide]会跟踪曝光数据并每天将其发送给DSP。 您可以使用日期来手动优化投放策略，以获得更高的关注度分数。

[!UICONTROL Attention Score]字段在报告的[!UICONTROL Metrics]部分中可用；在[!UICONTROL Campaigns]、[!UICONTROL Packages]和[!UICONTROL Placements]视图中；以及在[!UICONTROL Sites]位置详细信息视图[!UICONTROL Ads]的[!UICONTROL Inventory]、[和](/help/dsp/campaign-management/reports/placement-details-view.md)选项卡中可用。

如果将[!DNL Adelaide]区段用于测量，则对于从带有[!DNL Adelaide]测量标记的广告投放的每个展示，将产生CPM费用。 此费用与[投放级别关注目标](/help/dsp/campaign-management/placements/placement-settings.md)的费用无关。

<!--
Example JavaScript tag:

`<script src="https://www.example.com/aam?asid=0123456789&ad=${TM_AD_ID_NUM}&adv=${TM_ADVERTISER_ID}&ca=${TM_CAMPAIGN_ID_NUM}&df=${NS_PLATFORM_ID}&dt=${NS_DEVICE_GROUPING}&pl=${TM_PLACEMENT_ID_NUM}&ra=${TM_RANDOM}&st=${TM_SITE_URL_URLENC}"></script>`
-->

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]：**&#x200B;基于指定的敏感度级别，使用[!DNL IAB Open Video Viewability (OpenVV)]技术启用第一方可见性测量和报告：

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [关于营销活动管理](campaign-about.md)
>* [创建营销活动](campaign-create.md)
>* [编辑营销活动](campaign-edit.md)
>* [查看营销活动的更改日志](campaign-change-log.md)
