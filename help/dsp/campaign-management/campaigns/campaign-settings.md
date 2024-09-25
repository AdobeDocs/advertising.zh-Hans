---
title: Campaign设置
description: 请参阅可用营销活动设置的描述。
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 7ee798e11375863e776ac3e802efc9112280e750
workflow-type: tm+mt
source-wordcount: '1034'
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

**[!UICONTROL Margin Management]：**&#x200B;是管理促销活动的边距： *[!UICONTROL Yes]*&#x200B;还是&#x200B;*[!UICONTROL No]*（默认值）。

当您选择&#x200B;*[!UICONTROL Yes]，*&#x200B;时，请指定毛利类型和金额：

* **[!UICONTROL Margin Type]：**&#x200B;边距的类型。 一旦启用了毛利管理并保存了营销策划，就无法更改毛利类型。

   * *[!UICONTROL Fixed]：*（默认）允许DSP根据[!UICONTROL Gross Budget]的固定利润百分比自动计算和限制支出。

   * *[!UICONTROL Dynamic]：*&#x200B;允许您通过为营销活动中的每个包和投放位置指定单独的[!UICONTROL Budget Reserve %]和[!UICONTROL Gross Budget]，管理低至投放位置的边距。 DSP根据每次投放的财务效率进行优化，而不保证一定的利润。 对于由多个行项目组成的插入订单，您可以使用此选项来同意按固定费率提供固定数量的单位或单位类型。

* **[!UICONTROL Fixed Margin %]：** （仅具有固定边距的促销活动）每个插入订单<!-- impression? -->的默认标记（百分比）。 从[!UICONTROL Gross Budget]中扣除此金额以定义净促销活动预算。

* **[!UICONTROL Budget Reserve %]：** （仅具有固定边距的营销活动；可选）保留[!UICONTROL Gross Budget]的指定百分比作为保障。 从[!UICONTROL Gross Budget]中扣除此金额以定义净促销活动预算。

**[!UICONTROL Gross Budget]：** （仅具有毛利管理的营销活动）应用指定的边际调整之前的毛营销活动预算。

您可以选择添加额外的每日、每周或每月毛预算：

1. 单击&#x200B;**[!UICONTROL Add an additional Gross Budget]**。

1. 输入&#x200B;**[!UICONTROL Gross Budget]**&#x200B;并选择预算间隔： *[!UICONTROL Daily]、* *[!UICONTROL Weekly]、*&#x200B;或&#x200B;*[!UICONTROL Monthly]*。

总净预算（促销活动的支出上限）是根据毛利设置自动计算的，并在此值下表示。

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

* *[!UICONTROL LiveRamp - U.S. only]：*&#x200B;对于使用[!DNL LiveRamp]设备图交付的展示次数（即，在目标受众区段中未找到设备），适用于跨设备定位为$0.35 CPM的所有广告商。 您可以在投放级别设置跨设备定位。

  此外，所有广告商也可以免费使用此选项进行频率管理和归因测量。

  跨设备支持仅适用于以旧版ID为目标的投放位置，不适用于以通用ID（包括[!DNL LiveRamps]）为目标的投放位置。 通用ID的定位、频率管理和归因仅在ID级别应用。

**[!UICONTROL Frequency Cap]：**（可选）从营销活动中为独特设备、通用ID或人员（取决于指定的[!UICONTROL Cross Device Level]和投放位置的[!UICONTROL Targeting]设置）提供广告的次数。 选项包括&#x200B;*[!UICONTROL Unlimited]*&#x200B;或每天、每周或每月的特定金额。

>[!NOTE]
>
> 您可以在营销活动、包和投放级别设置频率上限。 DSP遵循营销活动层次结构中最严格的频率限制。

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

**[!UICONTROL Adelaide]：**&#x200B;启用投放位置级别[!UICONTROL Attention Score]量度的跟踪（展示次数中[!DNL Adelaide]“[!DNL Attention Units]”的加权平均数）。 指标可用于除[!DNL Roku]连接的电视、仅VPAID前置播放和非播客音频之外的所有投放类型。 DSP会自动将JavaScript标记附加到所有关联的创意内容，并且[!DNL Adelaide]会跟踪曝光数据并每天将其发送给DSP。 您可以使用日期来手动优化投放策略，以获得更高的关注度分数。

[!UICONTROL Attention Score]字段在报告的[!UICONTROL Metrics]部分中可用；在[!UICONTROL Campaigns]、[!UICONTROL Packages]和[!UICONTROL Placements]视图中；以及在[位置详细信息视图](/help/dsp/campaign-management/reports/placement-details-view.md)的[!UICONTROL Sites]、[!UICONTROL Ads]和[!UICONTROL Inventory]选项卡中可用。

将[!DNL Adelaide]区段用于测量会为从包含[!DNL Adelaide]测量标记的广告投放的每个展示产生CPM费用。 此费用与[投放级别关注目标](/help/dsp/campaign-management/placements/placement-settings.md)的费用无关。

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
>* [关于Campaign Management](campaign-about.md)
>* [创建营销活动](campaign-create.md)
>* [编辑营销活动](campaign-edit.md)
>* [查看营销活动的更改日志](campaign-change-log.md)
