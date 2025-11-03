---
title: Campaign设置
description: 请参阅可用营销活动设置的描述。
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 9d26e097f007b570c0f0e3b7f02c683a84d5e647
workflow-type: tm+mt
source-wordcount: '1434'
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

* **[!UICONTROL How would you like to compute agency fees?]：** （仅具有利润管理的营销活动）如何计算代理费用，代理费用是营销活动总预算中预扣且未包括在净支出中的部分：

   * *[!UICONTROL Margin % of Total Budget]：*（默认）计算费用占总支出的百分比。 指定[!UICONTROL Agency Fee Type] （固定或复合）和[!UICONTROL Margin %]或[!UICONTROL Composite Margin %]。

   * *[!UICONTROL Apply Markup % on top of individual cost components]：*&#x200B;按媒体成本、数据和其他成本的指定百分比计算费用和/或[!DNL Adobe]技术费用。 指定[!UICONTROL Markup %]并选择要应用标记的组件。

* **[!UICONTROL Agency Fee Type]：** （使用[!UICONTROL Margin % of Total Budget]的营销活动）代理费用的类型。

   * *[!UICONTROL Fixed]：*（默认）允许DSP保留总支出的固定百分比作为代理费用。 指定[!UICONTROL Margin %]。

   * *[!UICONTROL Composite]：*&#x200B;允许DSP保留总支出的百分比以计入代理费和[!DNL Adobe]技术费。 指定[!UICONTROL Composite Margin %]。

* **[!UICONTROL Margin %]：** （使用具有固定利润的[!UICONTROL Margin % of Total Budget]的促销活动）作为代理费用预扣的总支出的百分比。 毛利值的任何更改仅应用于将来总支出，而不应用于促销活动的历史总支出。 在应用毛利之前，[!UICONTROL Estimated Tax Withholding]值将从总支出中排除。 请参阅以下示例，其中假设促销活动没有支出不足或超支。

   * 示例1：假设[!UICONTROL Gross Budget]是`100 USD`，在整个航班中[!UICONTROL Margin %]是`5%`。 促销活动结束后，代理费用计算为`5 USD` （即`5% of 100 USD`），净支出为`95 USD` （即`campaign budget [100 USD] - agency fees [5 USD]`）。

   * 示例2的毛利发生了更改：对于同一促销活动，假设[!UICONTROL Margin %]在总支出为`5%`时从`10%`更改为`40 USD`。 在更改之前的期间，代理费计算为`2 USD`（即`5% of 40 USD`）；在更改之后的期间，代理费计算为`6 USD`（即`10% of 60 USD`）。 总代理费用计算为`8 USD` （即`2 USD + 6 USD`），净支出为`92 USD` （即`campaign budget [100 USD] - total agency fees [8 USD]`）。

   * 示例3（含预缴税金）：假设[!UICONTROL Gross Budget]为`100 USD`，促销活动投放位置末尾的[!UICONTROL Estimated Tax Withholding]为`10 USD`，且整个投放位置中的[!UICONTROL Margin %]为`5%`。 促销活动结束后，代理费用计算为`4.5 USD` （即`5% of (campaign budget [100 USD] - tax withholding [USD 10])`），净支出为`85.5 USD` （即`campaign budget [100 USD] - agency fees [4.5 USD] - tax withholding [10 USD]`）。

* **[!UICONTROL Composite Margin %]：** （使用具有复合利润的[!UICONTROL Margin % of Total Budget]的营销活动）将预扣为[!DNL Adobe]技术费和代理费的总支出的百分比。 代理费的计算方法是，从综合保证金数额中扣除Adobe的技术费用。 对综合毛利值所做的任何更改仅应用于将来总支出，而不应用于促销活动的历史总支出。 在应用复合利润之前，[!UICONTROL Estimated Tax Withholding]值将从总支出中排除。

  例如，假设[!UICONTROL Gross Budget]为`100 USD`，促销活动航班结束时的[!DNL Adobe]技术费用为`10 USD`，且整个航班中的[!UICONTROL Composite Margin %]为`17%`。 在促销活动结束后（假定促销活动没有支出不足或超支），代理费用将计算为`7 USD`（即`(17% of 100 USD) - 10`），而净支出为`93 USD`（即`campaign budget [100 USD] - agency fees [7 USD]`）。

* **[!UICONTROL Markup %]：** （使用[!UICONTROL Apply Markup % on top of individual cost components]的营销活动）要应用于指定成本组件以计算代理费用的百分比。 对加价值所做的任何更改仅应用于将来成本，而不应用于促销活动的历史成本。

* **[!UICONTROL Select cost components on which markup will be applied]：** （使用[!UICONTROL Apply Markup % on top of individual cost components]的营销活动）应用[!UICONTROL Markup %]的成本组件。 选择所有适用的组件： *[!UICONTROL Media cost]*、*[!UICONTROL Data and Other costs]*&#x200B;和/或&#x200B;*[!UICONTROL Adobe tech fees]*。 对组件选择所做的任何更改只会应用于将来成本，而不会应用于营销活动的历史成本。

  例如，“[!UICONTROL Markup %]”和“`10%`”的[!UICONTROL Media cost]为[!UICONTROL Data and Other costs]。 如果在营销活动小众测试中的任一时刻，媒体成本为`20 USD`，数据和其他成本为`5 USD`，[!DNL Adobe]技术费用为`2 USD`，则代理费用将计算为`2.50 USD`(即`10% of (20 USD + 5 USD)`，总支出为`29.50 USD`（即`media cost [20 USD] + data and other costs [5 USD] + [!DNL Adobe] tech fees [2 USD] + agency fees [2.50 USD]`）。

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
