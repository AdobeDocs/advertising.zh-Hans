---
title: “[!DNL Microsoft Advertising]广告组设置”
description: 引用 [!DNL Microsoft Advertising] 广告组的设置。
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# [!DNL Microsoft Advertising]广告组设置

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]：**&#x200B;广告组名称在营销活动中是唯一的。 最大长度为128个字符。

**[!UICONTROL Status]：**&#x200B;广告组的显示状态： *活动*&#x200B;或&#x200B;*已暂停*。 新广告组的默认值为&#x200B;*活动*。

**[!UICONTROL Ad Language]：** （搜索营销活动）广告的目标语言。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]：** （搜索广告）在广告组中放置广告的方式和位置：

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* （默认）：在搜索网络上提出广告投标。

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]：*&#x200B;在联合合作伙伴网站上对广告投标。

* *[!UICONTROL Content network]：*&#x200B;已弃用

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]：**&#x200B;已弃用

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]：** （受众广告组）是否：

* *[!UICONTROL Target and Bid]：*&#x200B;只向与满足广告组任何其他目标的目标受众相关联的用户显示广告。

* *[!UICONTROL Bid Only]：*&#x200B;若要显示广告，甚至向不与目标受众关联的用户显示，只要他们满足其他广告组级别的目标。 但是，您可以通过为特定受众设置更高的竞价来增加向这些受众显示广告的机会。

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

对于受众网络中的[!DNL Microsoft Advertising]个广告组，位置目标的竞价修饰符未在具有“[!UICONTROL Auto-optimize Bid Adjustment Values]”设置的标准项目组合中进行优化。

**[!UICONTROL Genre]：** （[!UICONTROL Audience CTV Video]个促销活动中的广告组；在美国、CA、BR、MX、UK、DE、ES、FR、IT、AU、MY和TH<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->提供）目标类型，用于确定广告出现的节目和渠道：

* *[!UICONTROL All genres]：* （默认）针对所有流派。

* *[!UICONTROL Select From Below List]：*&#x200B;目标选定流派。 从所有可用流派的列表中选择。

连接电视(CTV)广告投放取决于您的视频质量和竞价金额。 查看CTV广告的[技术要求](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements)。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]：** （受众广告组；可选）要作为目标包含或排除的特定性别： *[!UICONTROL Male]*、*[!UICONTROL Female]*&#x200B;和&#x200B;*[!UICONTROL Unknown]*。 默认情况下，会定位所有性别。 排除项始终会覆盖包含项。

* 要定位所有值，请勿选择任何值。

* 若要包含值，请单击相邻圆圈一次，以便显示一个蓝色复选标记（![包含](/help/search-social-commerce/assets/include.png "包含")）。 您可以选择按每个性别目标的指定百分比增加或减少竞价。

* 若要排除值，请单击相邻圆圈两次，以便显示红色复选标记（![排除](/help/search-social-commerce/assets/exclude.png "排除")）。

**[!UICONTROL Age]：** （受众广告组；可选）要作为目标包含或排除的特定年龄类别： *[!UICONTROL 18-24]*、*[!UICONTROL 25-34]*、*[!UICONTROL 35-49]*、*[!UICONTROL 50-64]*、*[!UICONTROL 65+]*&#x200B;和&#x200B;*[!UICONTROL Unknown]*。 默认情况下，会定位所有年龄。 排除项始终会覆盖包含项。

* 要定位所有值，请勿选择任何值。

* 若要包含值，请单击相邻圆圈一次，以便显示一个蓝色复选标记（![包含](/help/search-social-commerce/assets/include.png "包含")）。 您可以选择按指定百分比增加或减少每个目标年龄的竞价。

* 若要排除值，请单击相邻圆圈两次，以便显示红色复选标记（![排除](/help/search-social-commerce/assets/exclude.png "排除")）。

**[!UICONTROL Industry]：** （受众广告组；可选）要作为目标包含或排除的特定行业。 默认情况下，所有行业都是目标行业。 排除项始终会覆盖包含项。

* 要定位所有值，请勿选择任何值。

* 若要包含值，请单击相邻圆圈一次，以便显示一个蓝色复选标记（![包含](/help/search-social-commerce/assets/include.png "包含")）。 您可以选择按指定百分比增加或减少每个目标行业的竞价。

* 若要排除值，请单击相邻圆圈两次，以便显示红色复选标记（![排除](/help/search-social-commerce/assets/exclude.png "排除")）。

**[!UICONTROL Job Function Targets]：** （受众广告组；可选）要作为目标包含或排除的特定工作职能。 默认情况下，所有工作职能都是定向的。 排除项始终会覆盖包含项。

* 要定位所有值，请勿选择任何值。

* 若要包含值，请单击相邻圆圈一次，以便显示一个蓝色复选标记（![包含](/help/search-social-commerce/assets/include.png "包含")）。 您可以选择按指定百分比增加或减少每个目标工作职能的竞价。

* 若要排除值，请单击相邻圆圈两次，以便显示红色复选标记（![排除](/help/search-social-commerce/assets/exclude.png "排除")）。

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]：** （可选）从广告组为客户提供广告的次数。 输入值并选择时间单位（*[!UICONTROL Hour]*、*[!UICONTROL Day]*&#x200B;或&#x200B;*[!UICONTROL Week]*）。

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]：** （仅显示/本地网络上的营销活动；可选）显示网络上不希望显示广告的站点。 请输入有效的URL，如www.example.com。 要指定多个字符串，请用逗号分隔它们，或者在单独的行中输入它们。

有关可用性的信息，请参阅[!DNL Microsoft Advertising]帮助[防止广告出现在特定网站](https://help.ads.microsoft.com/#apex/bae/en/14061/0)。

>[!MORELIKETHIS]
>
>* [管理广告组](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
