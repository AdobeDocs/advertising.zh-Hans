---
title: 广告商帐户设置
description: 请参阅可用广告商设置的描述。
role: User, Admin
source-git-commit: 1f8a76e060612cdcc8ee3709bdf49654faf31b57
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 0%

---

# 广告商帐户设置

*对只读用户不可用*

<!-- Not published -->

## [!UICONTROL General]设置

**[!UICONTROL Advertiser Name]：**&#x200B;广告商名称。

**[!UICONTROL Category]：**&#x200B;广告商业务运营的类别。 当您对库存进行竞价时，会将类别告知发布者。 请确保您选择的类别与您的广告一致，否则发布者可能会拒绝您的广告。

>[!NOTE]
>
>如果选择&#x200B;*[!UICONTROL Other]*，则广告商无法访问DSP [!DNL On Demand Inventory]。

**[!UICONTROL Advertiser URL]：**&#x200B;广告商的主页或主网站URL（以`http://`或`https://`开头）。

**[!UICONTROL Share all private exchange feeds into this advertiser]：** （仅限新广告商帐户）使为组织的DSP帐户配置的所有私有Exchange馈送可供广告商使用。

### [!UICONTROL Adobe IMS IDs]

使用其他Adobe Experience Cloud产品的广告商可以使用组织的Experience Cloud唯一ID在某些产品之间共享数据。 您可以在[!UICONTROL Integrations]部分中配置特定的产品集成。

**[!UICONTROL Account IMS org and ID]：** (通过具有多个广告商的Experience Cloud帐户许可的、具有其他Experience Cloud产品的广告商；可选)广告商的Experience Cloud组织ID。

**[!UICONTROL Advertiser IMS org and ID]：** (具有其他Experience Cloud产品的直接许可证的广告商；可选)广告商的Experience Cloud组织ID。

### [!UICONTROL Integrations]

（可选）链接到DSP帐户的其他Experience Cloud产品。 产品必须与[!UICONTROL Adobe IMS IDs]部分中提供的相同Experience Cloud组织ID关联。

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]：** (具有[!DNL Advertising Search, Social, & Commerce]或使用Adobe Advertising转化像素的广告商)DSP与其交换归因数据的[!DNL Search, Social, & Commerce]帐户。

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]：** (使用Adobe Analytics的广告商；可选；仅适用于使用Adobe Advertising转化跟踪标记（仅包括[!DNL EF Redirect]和令牌）收集的数据)一个或多个[!DNL Analytics]报告包，DSP会向这些报告包发送其从发布者和供应方合作伙伴收集的数据。 Analytics还会将其从客户端站点收集的数据发送到DSP。

对于要在报表包中显示的数据，必须启用相应的[!DNL Search, Social, & Commerce]广告商级别设置。 此外，必须将广告商的[!DNL Analytics]帐户配置为从Adobe Advertising接收数据。

>[!WARNING]
>
>如果删除之前链接的报表包，DSP将不再与该报表包交换数据。 预计会出现数据波动。

有关与[!DNL Analytics]集成的详细信息，请参阅[概述 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)。

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]：** (使用Adobe Audience Manager或Adobe Analytics的广告商；可选)Audience Manager或[!DNL Analytics]帐户，DSP会从中提取广告商的所有Adobe受众的区段元数据、层次结构数据和唯一受众数据。 这包括以下项的数据：

* Audience Manager区段
* 发布到Adobe Experience Cloud的[!DNL Analytics]区段
* 使用Adobe Experience Cloud [!DNL Audience Library]创建的区段
* 在Adobe Experience Platform中创建并通过Audience Manager发送到Adobe Advertising的区段

初始同步大约需要24小时。 之后，数据实时同步，延迟为1到2秒。
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting]设置

您可以选择为广告商的新投放位置配置默认目标。 用户可以覆盖任何新投放位置的默认目标。

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]：**&#x200B;每个投放位置的地理定位的默认国家/地区。 用户可以更改国家/地区，并为每个投放位置配置更具体的地理定位。

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]：**&#x200B;默认情况下禁止显示的任何受众或区段。 用户可以更改每个投放位置的排除项。

### [!UICONTROL Media Quality]

<!-- See placement settings for specs on applicable ad/device types -->

#### [!UICONTROL Contextual Filtering]

要应用的[!DNL Comscore]、[!DNL DoubleVerify]、[!DNL Integral Ad Science]和[!DNL Peer39]上下文筛选器的类型。 您可以覆盖[位置级别](/help/dsp/campaign-management/placements/placement-settings.md)的广告商级别设置。

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]：**（可选）默认情况下阻止一个或多个类型的库存上下文。 可能需额外付费。

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]：**（可选）默认情况下目标的一个或多个类型的库存属性。 可能需额外付费。

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]：**（可选）默认情况下阻止一个或多个类型的库存属性。 可能需额外付费。

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]：** （可选）默认情况下阻止广告的成人内容程度： *[!UICONTROL Do Not Block]* （默认值）、*[!UICONTROL Standard]*&#x200B;或&#x200B;*[!UICONTROL Strict]*。 可能需额外付费。

**[!UICONTROL Alcohol Content]：**（可选）默认情况下阻止广告的酒精含量程度： *[!UICONTROL Do Not Block]*（默认值）、*[!UICONTROL Standard]*&#x200B;或&#x200B;*[!UICONTROL Strict]*。 可能需额外付费。

#### [!UICONTROL Pre-Bid Fraud Blocking] {#prebid-fraud-blocking}

要基于通过[!DNL DoubleVerify]、[!DNL Integral Ad Science]和[!DNL Peer39]测量的欺诈性流量和可疑活动阻止的站点类型。 您可以覆盖[位置级别](/help/dsp/campaign-management/placements/placement-settings.md)的广告商级别设置。

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]：**&#x200B;默认情况下，会阻止所有100%无效的流量（包括被劫持设备上的流量）用于新放置。 可能需额外付费。

**[!UICONTROL Also block sites with]：**（可选）额外级别的欺诈和无效流量导致DSP默认阻止广告： *[!UICONTROL None]*（默认值，它不会阻止额外流量）、*[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*、*[!UICONTROL >4% Average Fraud/IVT levels]*、*[!UICONTROL >6% Average Fraud/IVT levels]*、*[!UICONTROL >10% Average Fraud/IVT levels]*&#x200B;或&#x200B;*[!UICONTROL >25% Average Fraud/IVT levels]*。 可能需额外付费。

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]：**（可选）一种或多种类型的欺诈会导致DSP默认阻止广告： *[!UICONTROL Fraud]*（会阻止所有网站进行欺诈行为）、*[!UICONTROL Fraud: Bot Sites_Non-Human traffic]*&#x200B;和/或&#x200B;*[!UICONTROL Fraud: Zero Ads]*。 可能需额外付费。

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]：**（可选）一种可疑DSP阻止广告的网站或应用程序活动类型： *[!UICONTROL None]*（默认值，不阻止基于可疑活动的广告）、*[!UICONTROL Suspicious Activity - High Risk]*&#x200B;或&#x200B;*[!UICONTROL Suspicious Activity - High or Moderate Risk]*。 可能需额外付费。

#### [!UICONTROL Pre-Bid Viewability]

按[!DNL DoubleVerify]和[!DNL Integral Ad Science]显示的可选预竞价可视性筛选器以应用于投放位置。 为新投放位置选择广告商级别的默认值。 您可以覆盖[位置级别](/help/dsp/campaign-management/placements/placement-settings.md)的广告商级别设置。

##### [!UICONTROL DoubleVerify] {#doubleverify-viewability}

###### 视频

**&#x200B;**&#x200B;[!UICONTROL Include URL's whose average video viewability rate is]**。 使用此选项，选择标准。

**&#x200B; **&#x200B;[!UICONTROL Impressions with Insufficient IAB Viewability Data]**

**&#x200B;**&#x200B;[!UICONTROL Include URL's whose average completion & fully viewable rate is]**。 使用此选项，选择标准。

**&#x200B;**&#x200B;[!UICONTROL Include URL's whose average player size composition is]**。 使用此选项，选择标准。

**&#x200B; **&#x200B;[!UICONTROL Impressions with Insufficient Player Size Statistics]**

###### 显示

**&#x200B;**&#x200B;[!UICONTROL Only target URL's or Apps that have historically achieved a display viewability rate of]**。 使用此选项，选择标准。

* **[!UICONTROL Impressions with Insufficient IAB Viewability Performance Data]**

* **[!UICONTROL Include Apps and URL's whose average entire creative (100% of pixels) viewable duration is]**。 使用此选项，选择标准。

* **[!UICONTROL Impressions with Insufficient BXD Performance Data]**

##### [!UICONTROL Integral Ad Science] {#ias-viewability}

可选的&#x200B;**[!UICONTROL Video Viewability Targets]**&#x200B;筛选器和可选的&#x200B;**[!UICONTROL Display Viewability Targets]**&#x200B;筛选器。 可能需额外付费。

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]：**&#x200B;默认情况下，利用每个发布者的[!DNL Authorized Digital Sellers]列表使用哪个级别的[[!DNL Ads.txt] 预竞价筛选](https://iabtechlab.com/ads-txt-about/)：
* *[!UICONTROL Opt out of ads.txt (default)]*：从所有卖家购买库存。
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*：优先从域的授权直销商和经销商处购买库存。
* *[!UICONTROL Ads.txt sellers only]*：仅从域的授权直销商和经销商购买库存。
* *[!UICONTROL Ads.txt sellers only]*：仅从域的授权直销人员购买库存。

您可以覆盖[位置级别](/help/dsp/campaign-management/placements/placement-settings.md)的广告商级别设置。

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]：**&#x200B;默认情况下，启用实时竞价后过滤器，以确保广告在广告商定位的网站上提供。<!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Suitability]

**[!UICONTROL DoubleVerify Account]：** （仅限[!DNL DoubleVerify]个客户；可选）与组织的[!DNL DoubleVerify]帐户关联的[!DNL DoubleVerify Authentic Brand Safety]区段ID，默认用于所有投放。 使用为指定区段ID配置的自定义品牌安全规则指定ID会阻止竞价后的展示次数。 DSP按区段ID的使用情况向帐户收费。

ID必须以“51”开头并且由八位数字组成。 您可以在版面级别更改或删除广告商级别ID。

>[!MORELIKETHIS]
>
>* [创建广告商帐户](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
