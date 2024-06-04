---
title: Campaign设置
description: 请参阅可用营销活动设置的描述。
feature: DSP Campaigns
exl-id: 461c3f9e-ef69-46e7-8eb1-37ccc085ba1f
source-git-commit: 5d07300ab49b96daf392cb51f8936fa4c0cd20ce
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 0%

---

# Campaign设置

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]：** 营销活动名称。

**[!UICONTROL Advertiser]：** （现有营销活动的只读）适用的广告商（品牌）。 选择现有广告商或创建新广告商。

**[!UICONTROL Advertiser URL]：** 广告商的官方页面。 此字段可加快您与库存合作伙伴的广告审批流程。

**[!UICONTROL Timezone]：** （现有营销活动的只读）用于报告和竞价的时区。

**[!UICONTROL Customer PO]：** （可选）插入订单/采购订单的客户采购订单。

**[促销活动日期]：** 营销活动开始和结束日期。

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]：** 是否管理营销活动的边距： *[!UICONTROL Yes]* 或 *[!UICONTROL No]* （默认）。

当您选择 *[!UICONTROL Yes]，* 指定毛利类型和金额：

* **[!UICONTROL Margin Type]：** 边距的类型。 一旦启用了毛利管理并保存了营销策划，就无法更改毛利类型。

   * *[!UICONTROL Fixed]：* （默认）允许DSP根据的固定利润百分比自动计算和限制支出 [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]：* 允许通过指定单独的边距来管理下至放置级别的边距 [!UICONTROL Budget Reserve %] 和 [!UICONTROL Gross Budget] 促销活动中的每个包和投放位置。 DSP根据每次投放的财务效率进行优化，而不保证一定的利润。 对于由多个行项目组成的插入订单，您可以使用此选项来同意按固定费率提供固定数量的单位或单位类型。

* **[!UICONTROL Fixed Margin %]：** （仅限具有固定边距的促销活动）每个插入订单的默认标记 <!-- impression? -->，以百分比表示。 此金额从以下项目扣除： [!UICONTROL Gross Budget] 以定义净促销活动预算。

* **[!UICONTROL Budget Reserve %]：** （仅限具有固定边距的营销活动；可选）保留指定百分比的 [!UICONTROL Gross Budget] 作为保障。 此金额从以下项目扣除： [!UICONTROL Gross Budget] 以定义净促销活动预算。

**[!UICONTROL Gross Budget]：** （仅限具有毛利管理的营销活动）毛营销活动预算，在应用指定的毛利调整之前。

您可以选择添加额外的每日、每周或每月毛预算：

1. 单击 **[!UICONTROL Add an additional Gross Budget]**.

1. 输入 **[!UICONTROL Gross Budget]** 并选择预算间隔： *[!UICONTROL Daily]，* *[!UICONTROL Weekly]，* 或 *[!UICONTROL Monthly]*.

总净预算（促销活动的支出上限）是根据毛利设置自动计算的，并在此值下表示。

**[!UICONTROL Budget]：** （没有利润管理的营销活动）整体营销活动预算。

**[!UICONTROL Estimated Tax Withholding]：** 在帐户级别预扣国家/地区或地方税的广告费用、广告服务费用和/或数据费用中的总支出百分比。 税率乃为编制预算及调整目的而估计，故发票税率可能有所不同。

要估计要预扣的税额，请执行以下操作：

1. 单击 **[!UICONTROL Update rates here]**.

1. 指定 **[!UICONTROL Estimated tax rate]**，以百分比表示。

1. 选中要预扣税的每个费用类型旁边的复选框。 费用类型包括：

   * *[!UICONTROL Include estimated tax - ads fee]：* 适用于所有Advertising DSP媒体支出，包括促销活动管理费用税。

   * *[!UICONTROL Include estimated tax - ad serving fee]：* 适用于所有在Advertising DSP上支出，媒体和数据除外。 它不包括营销活动管理费用税

   * *[!UICONTROL Include estimated tax - data fee]：* 适用于在Advertising DSP上花费的所有数据。

1. 单击 **[!UICONTROL Submit]**.

>[!NOTE]
>
>* 在美国，各州在包含广告、广告投放和数据的税费方面可能有所不同。 对于其他国家/地区的组织，请包括所有三类税费以便计入增值税。
>
>* 您还可以在帐户的费用设置中配置这些值。<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->

**[!UICONTROL Cross Device Level]：** （对于自2020年6月22日以来创建的现有营销活动为只读；对于2020年6月22日之前创建的营销活动不可用）DSP定位广告并应用频率上限的级别： *同一设备* 定位设备或 *人员* 将用户定位到其所有已知设备上。 **注意：** 跨设备支持不适用于以通用ID为目标的投放位置。

**[!UICONTROL Device Graph]：** （对于现有营销活动为只读；仅限具有基于人员的跨设备定位的营销活动）用于跨设备定位和频率管理的设备图：

* *[!UICONTROL LiveRamp - U.S. only]：* 面向所有广告商，提供跨设备定位的$0.35 CPM展示次数，展示次数通过使用 [!DNL LiveRamp] 设备图（即，对于在目标受众区段中未找到设备的设备）。 您可以在投放级别设置跨设备定位。

  此外，所有广告商也可以免费使用此选项进行频率管理和归因测量。

  跨设备支持仅适用于以旧版ID为目标的投放位置，不适用于以通用ID为目标的投放位置(包括 [!DNL LiveRamps])。 通用ID的定位、频率管理和归因仅在ID级别应用。

**[!UICONTROL Frequency Cap]：** （可选）独特设备、通用ID或人员(取决于指定的 [!UICONTROL Cross Device Level] 和投放位置的 [!UICONTROL Targeting] 设置)可用作营销活动中的广告。 选项包括 *[!UICONTROL Unlimited]* 或每天、每周或每月的特定金额。

>[!NOTE]
>
> 您可以在营销活动、包和投放级别设置频率上限。 DSP遵循营销活动层次结构中最严格的频率限制。

**[!UICONTROL Packages]：** 此 [包](/help/dsp/campaign-management/packages/package-about.md) 以包含在营销活动中。 选择现有包和/或创建要包含的包。 如果您创建包，请参阅关于以下内容的说明： [包设置](/help/dsp/campaign-management/packages/package-settings.md) 以了解更多信息。

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>以下设置仅启用测量和报告功能。 性能优化仅在包级别和放置级别执行。

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]：** （可选）启用 [!DNL IAS] 使用指定设置进行可见性、欺诈、品牌安全和受众验证的测量和报告。 需支付额外费用。

* **[!UICONTROL Measure On]：** 要测量的库存： *[!UICONTROL Display and VPAID video inventory]* （默认）或 *[!UICONTROL Display, VPAID & VAST video inventory]*.

  >[!NOTE]
  >
  >视频可视性仅在VPAID内容库中可测量。

* **[!UICONTROL IAS Account ID (AnID)]：** (有自己的广告商 [!DNL IAS] 帐户；可选)组织的 [!DNL IAS] 帐户ID，其中 [!DNL IAS] 将直接计费使用。

* **[!UICONTROL IAS Team ID]：** (有自己的广告商 [!DNL IAS] 帐户；可选)组织的团队ID [!DNL IAS] 帐户，其中 [!DNL IAS] 将直接计费使用。 <!-- verify -->

**[!UICONTROL MOAT]：** （可选）启用 [!DNL MOAT] 可视性、欺诈、品牌安全和受众验证的测量和报告。 需支付额外费用。

#### 受众验证

**[!UICONTROL Nielsen]：** （可选）启用 [!DNL Nielsen] 使用指定设置进行受众验证的测量和报告。 需支付额外费用。

* **[!UICONTROL Target Gender]：** 目标性别： *[!UICONTROL Both]* （默认）， *[!UICONTROL Male]*，或 *[!UICONTROL Female]*

* **[!UICONTROL Target Age]：** 目标年龄范围。 根据需要使用左右滑杆缩小范围。

* **[!UICONTROL Target Country]：** （可选）要定位的国家/地区。 [!DNL Nielsen] 仅向受支持国家提供阅听。

**[!UICONTROL comScore vCE]：** （可选）启用 [!DNL Comscore validated Campaign Essentials (vCE)] 使用指定设置进行受众验证的测量和报告。 需支付额外费用。

* **[!UICONTROL Target Gender]：** 目标性别： *[!UICONTROL Both]* （默认）， *[!UICONTROL Male]*，或 *[!UICONTROL Female]*

* **[!UICONTROL Target Age]：** 目标年龄范围。 根据需要使用左右滑杆缩小范围。

* **[!UICONTROL Target Country]：** （可选）要定位的国家/地区。 [!DNL Comscore] 仅向受支持国家提供阅听。

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]：** 使用启用第一方可见性测量和报告 [!DNL IAB Open Video Viewability (OpenVV)] 技术，根据指定的敏感度级别：

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [关于Campaign Management](campaign-about.md)
>* [创建活动](campaign-create.md)
>* [编辑营销活动](campaign-edit.md)
>* [查看营销活动的更改日志](campaign-change-log.md)
