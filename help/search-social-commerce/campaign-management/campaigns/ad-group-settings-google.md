---
title: ’[!DNL Google Ads] 广告组设置
description: 引用设置 [!DNL Google Ads] 广告组。
exl-id: 00aaa936-796f-4e22-9bee-4bb5121cd887
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
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

**[!UICONTROL Ad Rotation Mode]：** 频率 [!DNL Google Ads] 会在广告组内相互关联投放活动广告：

* *[!UICONTROL Optimize]：* Google广告青睐其预计表现优于广告组中其他广告的广告。 这些广告进入广告拍卖的频率更高，随着时间的推移，单个广告会更受青睐。 这可能与您的业务和优化目标不一致。

* *[!UICONTROL Rotate forever]：*   您的每个广告进入广告拍卖的次数更加均匀，这使得Search、Social和Commerce不仅可以根据点进率而且对广告的转化情况进行评分。

* *[!UICONTROL Use campaign setting]*（新广告组的默认设置）：使用现有的促销活动级别的广告轮换设置。 **注意：** 营销活动级别的设置在“搜索”、“社交”和“商务”中不可见。

如果活动使用智能竞价策略(例如 [!UICONTROL Target CPA]， [!UICONTROL Target ROAS]，或 [!UICONTROL Enhanced CPC])，则 [!DNL Google Ads] 自动将选项设置为&quot;[!UICONTROL Optimize]“

**[!UICONTROL Custom Bid Level]：** （仅针对显示网络的促销活动）竞价方式：竞价依据 *[!UICONTROL Ad Group]* （默认）， *[!UICONTROL Age]*， *[!UICONTROL Gender]*， *[!UICONTROL Interest and List]* (Google广告中的兴趣和再营销)， *[!UICONTROL Keyword]*， *[!UICONTROL Placement]* （网站）， *[!UICONTROL Unknown]*，或 *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* 按关键字竞价时，可在关键字级别创建跟踪模板。 同样，在按投放位置竞价时，应在投放位置级别创建跟踪模板。 对于所有其他维度，请在广告级别创建跟踪模板。
>* 当您按年龄、性别、兴趣和列表或垂直方向对项目组合中的营销活动进行竞价时，优化功能不会优化维度的竞价。 此外，所有归因都将应用于广告组。
>* 搜索网络上的广告始终使用关键词竞价。

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]：** (促销活动与 [!UICONTROL Target CPA] 竞价；可选)广告组的每次收购目标成本(CPA)。 此值覆盖营销活动级别的目标。

**[!UICONTROL Target ROAS]：** (促销活动与 [!UICONTROL Target ROAS] 竞价；可选)广告组的目标广告支出回报率(ROAS)（百分比）。 此值覆盖营销活动级别的目标。

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]：** (仅搜索网络上的营销活动，以及现有的只读营销活动 [!DNL Gmail] 展示网络上的营销活动)是否：

* *[!UICONTROL Target and Bid]：* 用于仅显示与满足广告组任何其他目标的目标受众相关联的用户使用的广告。

* *[!UICONTROL Bid Only]：* 用于即使向不与目标受众关联的用户显示广告，只要他们满足其他广告组级别的目标。 但是，您可以通过为特定受众设置更高的竞价来增加向这些受众显示广告的机会。

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
