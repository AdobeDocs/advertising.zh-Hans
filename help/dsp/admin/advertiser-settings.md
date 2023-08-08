---
title: 广告商帐户设置
description: 请参阅可用广告商设置的描述。
role: User, Admin
source-git-commit: 201eb485e196dc0823dd6d592f67f62122c214b1
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# 广告商帐户设置

*对只读用户不可用*

## [!UICONTROL General] 设置

**[!UICONTROL Advertiser Name]：** 广告商名称。

**[!UICONTROL Category]：** 广告商业务运营的类别。 当您对库存进行竞价时，会将类别告知发布者。 请确保您选择的类别与您的广告一致，否则发布者可能会拒绝您的广告。

>[!NOTE]
>
>如果您选择 *[!UICONTROL Other]*，则广告商将无法访问DSP [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]：** 广告商的主页或主网站URL(以 `http://` 或 `https://`)。

**[!UICONTROL Share all private exchange feeds into this advertiser]：** （仅限新广告商帐户）使为组织的DSP帐户配置的所有私有Exchange馈送可供广告商使用。

### [!UICONTROL Adobe IMS IDs]

使用其他Adobe Experience Cloud产品的广告商可以使用组织的Experience Cloud唯一ID在某些产品之间共享数据。 您可以在中配置特定的产品集成 [!UICONTROL Integrations] 部分。

**[!UICONTROL Account IMS org and ID]：** (通过具有多个广告商的Experience Cloud帐户授予许可的、具有其他Experience Cloud产品的广告商；可选)广告商的Experience Cloud组织ID。

**[!UICONTROL Advertiser IMS org and ID]：** (具有其他Experience Cloud产品的直接许可证的广告商；可选)广告商的Experience Cloud组织ID。

### [!UICONTROL Integrations]

（可选）链接到DSP帐户的其他Experience Cloud产品。 产品必须与中提供的相同Experience Cloud组织ID相关联 [!UICONTROL Adobe IMS IDs] 部分。

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]：** (广告商使用 [!DNL Advertising Search, Social, & Commerce] 或使用Adobe Advertising转换像素的用户) A [!DNL Search, Social, & Commerce] DSP将与其交换归因数据的帐户。

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]：** (使用Adobe AnalyticsAdobe Advertising的广告商；可选；仅适用于使用包含 [!DNL EF Redirect] 仅限和令牌)一个或多个 [!DNL Analytics] DSP将把从发布者和供应方合作伙伴收集的数据发送到哪些报表包。 Analytics还会将其从客户端站点收集的数据发送到DSP。

对于要显示在报表包中的数据，需执行以下操作 [!DNL Search, Social, & Commerce] 必须启用广告商级别设置。 此外，广告商的 [!DNL Analytics] 必须将帐户配置为从Adobe Advertising接收数据。

>[!WARNING]
>
>如果删除以前链接的报表包，DSP将不再与该报表包交换数据。 预计会出现数据波动。

有关集成的详细信息 [!DNL Analytics]，请参见&quot;[概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)“

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]：** (使用Adobe Audience Manager或Adobe Analytics的广告商；可选)Audience Manager或 [!DNL Analytics] DSP将从中为广告商的所有Adobe受众提取区段元数据、层次结构数据和唯一受众数据的帐户。 这包括以下项的数据：

* Audience Manager区段
* [!DNL Analytics] 发布到Adobe Experience Cloud的区段
* 使用Adobe Experience Cloud创建的区段 [!DNL Audience Library]
* 在Adobe Experience Platform中创建并通过Audience Manager发送到Adobe Advertising的区段

初始同步大约需要24小时。 之后，数据实时同步，延迟为1到2秒。
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] 设置

您可以选择为广告商的新投放位置配置默认目标。 用户可以覆盖任何新投放位置的默认目标。

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]：** 每个投放位置的地理定位的默认国家/地区。 用户可以更改国家/地区，并为每个投放位置配置更具体的地理定位。

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]：** 默认情况下要禁止的任何受众或区段。 用户可以更改每个投放位置的排除项。

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

类型 [!DNL Comscore]， [!DNL DoubleVerify]， [!DNL Integral Ad Science]、和 [!DNL Peer39] 要应用的上下文过滤器。 您可以在以下位置覆盖广告商级别的设置： [投放级别](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]：** （可选）默认情况下阻止一种或多种类型的库存上下文。 可能需额外付费。

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]：** （可选）默认情况下，要定位一种或多种类型的库存属性。 可能需额外付费。

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]：** （可选）默认情况下阻止一种或多种类型的库存属性。 可能需额外付费。

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]：** （可选）默认情况下阻止广告的成人内容程度： *[!UICONTROL Do Not Block]* （默认）， *[!UICONTROL Standard]*，或 *[!UICONTROL Strict]*. 可能需额外付费。

**[!UICONTROL Alcohol Content]：** （可选）默认情况下阻止广告的酒精含量级别： *[!UICONTROL Do Not Block]* （默认）， *[!UICONTROL Standard]*，或 *[!UICONTROL Strict]*. 可能需额外付费。

#### [!UICONTROL Pre-Bid Fraud Blocking]

要基于欺诈性流量和通过测量的可疑活动阻止的站点类型 [!DNL DoubleVerify]， [!DNL Integral Ad Science]、和 [!DNL Peer39]. 您可以在以下位置覆盖广告商级别的设置： [投放级别](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]：** 默认情况下，会阻止所有100%的无效流量（包括被劫持设备上的流量）以便新放置。 可能需额外付费。

**[!UICONTROL Also block sites with]：** （可选）额外的欺诈和无效流量会导致DSP默认阻止广告：  *[!UICONTROL None]* （默认情况下，不会阻止其他流量）， *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*， *[!UICONTROL >4% Average Fraud/IVT levels]*， *[!UICONTROL >6% Average Fraud/IVT levels]*， *[!UICONTROL >10% Average Fraud/IVT levels]*，或 *[!UICONTROL >25% Average Fraud/IVT levels]*. 可能需额外付费。

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]：** （可选）一种或多种会导致DSP默认阻止广告的欺诈类型： *[!UICONTROL Fraud]* （会以欺诈方式阻止所有网站）， *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*，和/或 *[!UICONTROL Fraud: Zero Ads]*. 可能需额外付费。

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]：** （可选）一种会导致DSP默认阻止广告的可疑网站或应用程序活动： *[!UICONTROL None]* （默认情况下，不会基于可疑活动阻止广告）， *[!UICONTROL Suspicious Activity - High Risk]*，或 *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. 可能需额外付费。

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]：** 默认情况下，哪个级别 [[!DNL Ads.txt] 预竞价筛选](https://iabtechlab.com/ads-txt-about/) 以利用每个发布者的 [!DNL Authorized Digital Sellers] 列表：
* *[!UICONTROL Opt out of ads.txt (default)]*：从所有销售者处购买库存。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*：优先从域的授权直接销售者和经销商处购买库存。
* *[!UICONTROL Ads.txt sellers only]*：仅从域的授权直接销售者和经销商购买库存。
* *[!UICONTROL Ads.txt sellers only]*：仅从域的授权直销商处购买库存。

您可以覆盖位于以下位置的广告商级别设置： [投放级别](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]：** 默认情况下，启用实时竞价后过滤器，以确保广告在广告商定位的网站上提供。 <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]：** ([!DNL DoubleVerify] 仅限客户；可选)与组织的关联品牌安全区段ID [!DNL DoubleVerify] 帐户。

**[!UICONTROL Enable Authentic Brand Safety]：** （可选）默认情况下，启用 [!DNL DoubleVerify] 正版品牌安全，它会阻止使用为指定区段ID配置的自定义品牌安全规则在竞价后展示次数。 DSP按区段ID对帐户开单。

您可以在版面级别覆盖广告商级别设置。

>[!MORELIKETHIS]
>
>* [创建广告商帐户](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
