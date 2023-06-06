---
title: ”[!DNL Google Ads] 广告组设置”
description: 引用设置 [!DNL Google Ads] 广告组。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# [!DNL Google Ads] 广告组设置

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]：** 广告组名称在营销活动中是唯一的。 最大长度为255个双字节字符。

**[!UICONTROL Status]：** 广告组的显示状态： *活动* 或 *已暂停*. 新广告组的默认值为 *活动*.

**[!UICONTROL Ad Group Type]：** （仅限扩展的动态搜索广告营销活动）广告组的类型：

* *[!UICONTROL Search Standard]* （默认）：对于标准广告。

* *[!UICONTROL Search Dynamic]：* 用于动态搜索广告。

**[!UICONTROL Ad Rotation Mode]：** 频率 [!DNL Google Ads] 会在广告组内相互投放活动广告：

* *[!UICONTROL Optimize]：* Google Ads青睐其预计表现优于广告组中其他广告的广告。 这些广告进入广告拍卖的频率更高，随着时间的推移，人们更青睐单个广告。 这可能与您的业务和优化目标不一致。

* *[!UICONTROL Rotate forever]：*   您的每个广告进入广告拍卖的次数更加平均，这使得Search、Social和Commerce不仅可以根据点进率而且对广告转化情况进行评分。

* *[!UICONTROL Use campaign setting]*（新广告组的默认设置）：使用现有的促销活动级别的广告轮换设置。 **注意：** 营销活动级别的设置在“搜索”、“社交”和“商务”中不可见。

如果活动使用智能竞价策略(例如 [!UICONTROL Target CPA]， [!UICONTROL Target ROAS]，或 [!UICONTROL Enhanced CPC])，则 [!DNL Google Ads] 自动将选项设置为&quot;[!UICONTROL Optimize].”

**[!UICONTROL Custom Bid Level]：** （仅针对展示网络的促销活动）竞价方式：竞价者 *[!UICONTROL Ad Group]* （默认）， *[!UICONTROL Age]*， *[!UICONTROL Gender]*， *[!UICONTROL Interest and List]* (Google广告中的兴趣和再营销)， *[!UICONTROL Keyword]*， *[!UICONTROL Placement]* （网站）， *[!UICONTROL Unknown]*，或 *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* 当您按关键字竞价时，请在关键字级别创建跟踪模板。 同样，在按投放位置竞价时，请在投放位置级别创建跟踪模板。 对于所有其他维度，请在广告级别创建跟踪模板。
>* 当您在项目组合中按年龄、性别、兴趣和列表或垂直市场活动竞价时，优化功能不会优化维度的竞价。 此外，所有归因都将应用于广告组。
>* 搜索网络上的广告始终使用关键词竞价。


## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]：** (促销活动包含 [!UICONTROL Target CPA] 竞价；可选)广告组的每次收购目标成本(CPA)。 此值将覆盖营销活动级别的目标。

**[!UICONTROL Target ROAS]：** (促销活动包含 [!UICONTROL Target ROAS] 竞价；可选)广告组的目标广告支出回报率(ROAS)（百分比）。 此值将覆盖营销活动级别的目标。

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]：** (仅搜索网络上的营销活动，以及现有的只读营销活动 [!DNL Gmail] 展示网络上的营销活动)是否：

* *[!UICONTROL Target and Bid]：* 仅向与目标受众相关联的用户显示广告，这些受众也满足广告组的任何其他目标。

* *[!UICONTROL Bid Only]：* 即使向不与目标受众关联的用户显示广告，只要他们满足其他广告组级别的目标。 但是，您可以通过为特定受众设置更高的竞价来提高向这些受众显示广告的几率。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

>[!MORELIKETHIS]
>
>* [管理广告组](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)

