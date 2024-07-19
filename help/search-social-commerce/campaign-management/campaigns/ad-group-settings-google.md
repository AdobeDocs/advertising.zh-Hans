---
title: “[!DNL Google Ads]广告组设置”
description: 引用 [!DNL Google Ads] 广告组的设置。
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 0%

---

# [!DNL Google Ads]广告组设置

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]：**&#x200B;广告组名称在营销活动中是唯一的。 最大长度为255个双字节字符。

**[!UICONTROL Status]：**&#x200B;广告组的显示状态： *活动*&#x200B;或&#x200B;*已暂停*。 新广告组的默认值为&#x200B;*活动*。

**[!UICONTROL Ad Group Type]：** （仅限扩展的动态搜索广告营销活动）广告组的类型：

* *[!UICONTROL Search Standard]* （默认）：对于标准广告。

* 对于动态搜索广告，*[!UICONTROL Search Dynamic]：*。

**[!UICONTROL Ad Rotation Mode]：** [!DNL Google Ads]在广告组中相互关联投放活动广告的频率：

* *[!UICONTROL Optimize]：* Google广告青睐其预期表现优于广告组中其他广告的广告。 这些广告进入广告拍卖的频率更高，随着时间的推移，单个广告会更受青睐。 这可能与您的业务和优化目标不一致。

* *[!UICONTROL Rotate forever]：*   您的每个广告进入广告拍卖的次数更加均匀，这使得Search、Social和Commerce不仅可以根据点进率而且对广告的转化情况进行评分。

* *[!UICONTROL Use campaign setting]*（新广告组的默认设置）：使用现有的营销活动级别的广告轮换设置。 **注意：**&#x200B;营销活动级别的设置在Search、Social和Commerce中不可见。

如果营销活动使用智能竞价策略（如[!UICONTROL Target CPA]、[!UICONTROL Target ROAS]或[!UICONTROL Enhanced CPC]），则[!DNL Google Ads]会自动将选项设置为“[!UICONTROL Optimize]”。

**[!UICONTROL Custom Bid Level]：** （仅针对显示网络的营销活动）竞价方式：竞价方式：竞价方式为&#x200B;*[!UICONTROL Ad Group]* （默认值）、*[!UICONTROL Age]*、*[!UICONTROL Gender]*、*[!UICONTROL Interest and List]* (Google广告中的兴趣和再营销)、*[!UICONTROL Keyword]*、*[!UICONTROL Placement]* （网站）、*[!UICONTROL Unknown]*&#x200B;或&#x200B;*[!UICONTROL Vertical]*。

>[!NOTE]
>
>* 按关键字竞价时，可在关键字级别创建跟踪模板。 同样，在按投放位置竞价时，应在投放位置级别创建跟踪模板。 对于所有其他维度，请在广告级别创建跟踪模板。
>* 当您按年龄、性别、兴趣和列表或垂直方向对项目组合中的营销活动进行竞价时，优化功能不会优化维度的竞价。 此外，所有归因都将应用于广告组。
>* 搜索网络上的广告始终使用关键词竞价。

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]：** （竞价为[!UICONTROL Target CPA]的营销活动；可选）广告组的每次客户获取的目标成本(CPA)。 此值覆盖营销活动级别的目标。

**[!UICONTROL Target ROAS]：** （竞价为[!UICONTROL Target ROAS]的营销活动；可选）广告组的目标广告支出回报率(ROAS)（百分比）。 此值覆盖营销活动级别的目标。

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]：** （仅搜索网络上的营销活动，以及显示网络上的现有只读[!DNL Gmail]营销活动）是否：

* *[!UICONTROL Target and Bid]：*&#x200B;只向与满足广告组任何其他目标的目标受众相关联的用户显示广告。

* *[!UICONTROL Bid Only]：*&#x200B;若要显示广告，甚至向不与目标受众关联的用户显示，只要他们满足其他广告组级别的目标。 但是，您可以通过为特定受众设置更高的竞价来增加向这些受众显示广告的机会。

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
