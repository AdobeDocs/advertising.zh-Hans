---
title: 有关家庭报表的常见问题解答
description: 进一步了解家庭覆盖率、频率和转化数据，包括家庭报表与其他报表和故障排除有何不同。
exl-id: aaaf6f6d-b133-4cda-8fc6-bd686b3b1ebb
source-git-commit: bd925c41f7b949c56402edd4e2dc393f0c5bed57
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---

# 有关家庭报表的常见问题解答

## 此 [!UICONTROL Household Reach & Frequency] 报告

### 如何 [!UICONTROL Household Reach & Frequency] 报表是否与其他自定义报表不同？

此 [!UICONTROL Household Reach & Frequency] 报告根据IP地址在家庭级别跨各种维度测量访问范围、展示次数和频率。 其他自定义报表在设备或Cookie级别生成。

例如，即使一个家庭中的三个设备具有一个展示次数，但已实现的独特家庭数指标仍为1。

#### 支持的Dimension

此 [!UICONTROL Household Reach & Frequency] 报告支持 [以下维度](/help/dsp/reports/report-columns.md)： &quot;[!UICONTROL Campaign]，&quot; &quot;[!UICONTROL Package]，&quot; &quot;[!UICONTROL Placement]，&quot; &quot;[!UICONTROL Site/Apps]“（不提供对重叠量度的访问权限）， ”[!UICONTROL Media Type]，&quot; &quot;[!UICONTROL Feed Type]，&quot; &quot;[!UICONTROL Device]，&quot; &quot;[!UICONTROL Publisher]，&quot; &quot;[!UICONTROL Audience]，&quot; &quot;[!UICONTROL Creative Length]，”和用户创建的投放位置“[!UICONTROL Tags].” |

#### 支持的指标

此 [可用量度](/help/dsp/reports/report-columns.md) 包括：

* 重叠量度： [!UICONTROL Frequency Overlap]， [!UICONTROL Measurable Impressions (Overlap)]、和 [!UICONTROL Unique Household (Overlap)].

  重叠量度是仅针对报告的维度或维度组合出现的值，而不针对其他维度出现的值。 <!-- For example, it might show the ?? -->

* 非重叠量度： [!UICONTROL Frequency]， [!UICONTROL Incremental Household Reached]， [!UICONTROL % Incremental Household Reached]， [!UICONTROL Impressions]， [!UICONTROL Measurable Impressions]、和 [!UICONTROL Unique Household Reached]

不支持转化量度和自定义目标。

### 重叠量度与非重叠量度之间有何区别？

下图显示了3个促销活动（A、B和C）的3个量度(已到达独特家庭、已到达增量家庭和增量家庭（重叠）)。

![家庭重叠量度的插图](/help/dsp/assets/household-overlap-metrics-illustration.png "家庭重叠量度的插图")

* “已实现的独特家庭”（总计）提供每个营销活动已实现的独特家庭或每个圆圈的总面积。 在图中，A达到的独特家庭=A + (A+B) + (A+C) +(A+B+C)达到的递增家庭

* Incremental Household Accessed是仅通过营销活动到达的唯一家庭。 在图中，A、B、C所实现的增量家庭是A、B、C所实现的增量家庭。

* Incremental Household (Overlap)是营销活动或营销活动组合访问的唯一家庭。 在图中，A， C所实现的增量家庭为A+C。

### 工作流

按照常规步骤执行以下操作 [创建自定义报表](report-create.md).

此 [!UICONTROL Household Reach & Frequency] 报表只能包含一个维度。 它还可以包括a)按任何维度（网站/应用程序除外）划分的重叠量度或b)非重叠量度，但不能同时包括两者。

### 有哪些限制 [!UICONTROL Household Reach & Frequency] 报告？

具有重叠量度的报表输出交叉点，最多三个值。 例如，如果您使用量度 [!UICONTROL Unique Household (Overlap)] 对于10个位置，您可以看到由单个位置到达的独特家庭、由任意两个位置组合到达的普通家庭、以及由任意三个位置组合到达的普通家庭。 你看不到有四个或更多安置点的普通家庭。

对于除营销活动、资源包或投放位置以外的维度，报表在每个维度中最多支持10个值。 例如，要生成 [!UICONTROL Unique Household Reached] 报告 [!UICONTROL Audience] 维度时，独特受众的数量应少于或等于10。 如果包括10个以上的独特受众，则会生成一个空白报表。

### 为什么我的报表中的频度和唯一范围值不同 [!UICONTROL Custom] 报告和 [!UICONTROL Household Reach & Frequency] 报告？

中的这些量度 [!UICONTROL Household] 报表使用IP地址的实际计数来计算，而 [!UICONTROL Custom] 报表使用使用模型计算的预计数量。 但是，差异应小于10%。

### 如何为配置报表 [!UICONTROL Placement Tags] 维度？

要为投放位置创建标记， [打开版面设置](/help/dsp/campaign-management/placements/placement-edit.md) 并在 [投放位置标记字段](/help/dsp/campaign-management/placements/placement-settings.md).

当投放位置包含多个标记时，报表会将整个字符串视为一个标记。 该报表为每个唯一字符串包含一行。

## 此 [!UICONTROL Household Conversions] 报告

### 中支持哪些类型的归因方法 [!UICONTROL Household Conversions] 报告？

支持两种类型的归因方法：

* [!UICONTROL Unique]：计算维度值（如设备或投放位置）在转化路径上的次数。

* [!UICONTROL Multi-Touch Attribution (MTA)]：根据维度值（如设备或投放位置）在转化路径上的出现频率分配每次转化的点数。 例如，如果在转化前总共有10次展示，其中8次在CTV上展示，2次在移动设备上展示，则信用的80%(0.8)将给予给CTV屏幕，0.2给予移动设备屏幕。

### 在Adobe Analytics中，家庭转化报表与CTV浏览转化报表有何不同？

中的CTV浏览数据 [!DNL Analytics] 已供电 [!DNL Analytics] 家庭转化数据使用通过Adobe Advertising转化跟踪收集的数据。 此外，中的DSP归因逻辑 [!DNL Analytics] 仅使用最后一个事件，但家庭转化报表支持两种不同的归因方法：唯一和MTA。

### 我是否可以在以下两个位置查看CTV浏览数据？ [!DNL Analytics for Advertising] 在自定义报表中？

广告商，无 [!DNL Analytics for Advertising] 只能将家庭转化报表用于家庭转化报表。

如果您的组织具有 [!DNL Analytics for Advertising]，同时使用这两种类型的报表。 虽然CTV显示到达报表适用于宽频分析、网站行为等，但自定义报表可提供精细的视图（其中数据按媒体类型、发布者等细分）以指示驱动转化率的因素。

## [!UICONTROL Household Reach & Frequency] 和 [!UICONTROL Household Conversions] 报表与来自的数据 [!DNL Advanced Measurement Services]

要提前报告基于家庭的覆盖范围和频率或转化率，请 [[!DNL Strategic Advertising Consulting] 团队](/help/dsp/introduction/advanced-measurement-services.md) 可提供高度可自定义的报告以及整体战略建议。 有关详情，请参阅 [!DNL Advanced Measurement Services]，请联系您的Adobe客户团队。

### 如果我已经在使用 [!DNL Advanced Measurement Services]，为何要使用 [!UICONTROL Household Reach & Frequency] 和 [!UICONTROL Household Conversions] 报告？

此 [!UICONTROL Household Reach & Frequency] 和 [!UICONTROL Household Conversions] 报告使客户端能够实时自主地提取家庭级别的可达性、频率和转化量度。

### 我能否同时使用 [!UICONTROL Household Reach & Frequency] 和 [!UICONTROL Household Conversions] 报告和 [!DNL Advanced Measurement Services]？

理想的用例是同时使用 [!UICONTROL Household] 报告和 [!DNL Advanced Measurement Services] 报告与咨询服务相结合。 考虑 [!UICONTROL Household] 以事务型报告，旨在告知日常优化，以及 [!DNL Advanced Measurement Services] 更具战略性，旨在为与总体业务目标相关的全面学习和工作经验提供信息。

>[!MORELIKETHIS]
>
>* [关于自定义报表](/help/dsp/reports/report-about.md)
>* [创建自定义报表](/help/dsp/reports/report-create.md)
>* [编辑自定义报告](/help/dsp/reports/report-edit.md)
>* [自定义报表设置](/help/dsp/reports/report-settings.md)
>* [可用报表列](/help/dsp/reports/report-columns.md)
