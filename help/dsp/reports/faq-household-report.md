---
title: 有关家庭报表的常见问题解答
description: 详细了解家庭覆盖率、频率和转化数据，包括家庭报表与其他报表和故障排除有何不同。
exl-id: 3ffd178e-de41-4663-b85f-bd8ce3eb0dad
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---

# 有关家庭报表的常见问题解答

## [!UICONTROL Household Reach & Frequency]报告

### [!UICONTROL Household Reach & Frequency]报告与其他自定义报告有何不同？

[!UICONTROL Household Reach & Frequency]报表根据IP地址在家庭级别跨各种维度测量访问范围、展示次数和频率。 其他自定义报表在设备或Cookie级别生成。

例如，即使一个展示次数提供给一个家庭中的三个设备，独特访问家庭数量度仍为1。

#### 支持的Dimension

[!UICONTROL Household Reach & Frequency]报表支持[以下维度](/help/dsp/reports/report-columns.md)：“[!UICONTROL Campaign]”、“[!UICONTROL Package]”、“[!UICONTROL Placement]”、“[!UICONTROL Site/Apps]”（不提供对重叠量度的访问权限）、“[!UICONTROL Media Type]”、“[!UICONTROL Feed Type]”、“[!UICONTROL Device]”、“[!UICONTROL Publisher]”、“[!UICONTROL Audience]”、“[!UICONTROL Creative Length]”和用户创建的投放位置“[!UICONTROL Tags]”。 |

#### 支持的指标

[可用量度](/help/dsp/reports/report-columns.md)包括：

* 重叠量度： [!UICONTROL Frequency Overlap]、[!UICONTROL Measurable Impressions (Overlap)]和[!UICONTROL Unique Household (Overlap)]。

  重叠量度是仅针对报告的维度或维度组合出现的值，而不针对其他维度出现的值。<!-- For example, it might show the ?? -->

* 非重叠量度： [!UICONTROL Frequency]、[!UICONTROL Incremental Household Reached]、[!UICONTROL % Incremental Household Reached]、[!UICONTROL Impressions]、[!UICONTROL Measurable Impressions]和[!UICONTROL Unique Household Reached]

不支持转化量度和自定义目标。

### 重叠量度与非重叠量度之间有何区别？

下图显示了三个营销活动（A、B和C）的三个量度(已实现的独特家庭、已实现的增量家庭和已实现的增量家庭（重叠）)。

![家庭重叠量度的图示](/help/dsp/assets/household-overlap-metrics-illustration.png "家庭重叠量度的图示")

* 独特家庭访问量（总计）提供每个营销活动访问的独特家庭或每个圆的总面积。 在图中，A到达的唯一家庭=A + (A+B) + (A+C) +(A+B+C)到达的递增家庭

* Incremental Household Accessed是仅通过营销活动访问的独特家庭。 在图中，A、B、C到达的增量家庭是A、B、C分别到达的增量家庭。

* Incremental Household (Overlap)是活动或活动组合访问的唯一家庭。 在图中，A、C所实现的增量家庭为A+C。

### 工作流

按照正常步骤[创建自定义报告](report-create.md)。

[!UICONTROL Household Reach & Frequency]报表只能包含一个维度。 它还可以包括a)按任何维度（网站/应用程序除外）列出的重叠量度，或b)非重叠量度，但不能同时包括两者。

### [!UICONTROL Household Reach & Frequency]报表有哪些限制？

具有重叠量度的报表输出交叉点，最多三个值。 例如，如果对10个投放位置使用量度[!UICONTROL Unique Household (Overlap)]，则可以查看由单个投放位置到达的唯一家庭、由任意两个投放位置组合到达的共同家庭，以及由任意三个投放位置组合到达的共同家庭。 你看不到有四个或更多安置点的普通家庭。

对于营销活动、资源包或投放位置以外的维度，报表在每个维度中最多支持10个值。 例如，要为[!UICONTROL Audience]维度生成[!UICONTROL Unique Household Reached]报告，唯一受众的数量应少于或等于10。 如果包含10个以上的独特受众，则会生成空白报表。

### 为什么我的[!UICONTROL Custom]报表与[!UICONTROL Household Reach & Frequency]报表之间的频度和唯一范围值不同？

[!UICONTROL Household]报表中的这些量度使用IP地址的实际计数进行计算，而[!UICONTROL Custom]报表中的量度使用使用使用模型计算的预计数量。 但是，差异应小于10%。

### 如何为[!UICONTROL Placement Tags]维度配置报表？

若要创建投放位置的标记，请[打开投放位置设置](/help/dsp/campaign-management/placements/placement-edit.md)，然后在[投放位置标记字段](/help/dsp/campaign-management/placements/placement-settings.md)中输入值。

当投放位置包含多个标记时，报表会将整个字符串视为一个标记。 对于每个唯一字符串，报表都包含一行。

## [!UICONTROL Household Conversions]报告

### [!UICONTROL Household Conversions]报表中支持哪些类型的归因方法？

支持两种类型的归因方法：

* [!UICONTROL Unique]：计算维度值（如设备或投放位置）在转化路径上的次数。

* [!UICONTROL Multi-Touch Attribution (MTA)]：根据维度值（如设备或投放位置）在转换路径上的出现频率分配每次转换的点数。 例如，如果在转化前总共有10次展示，其中8次在CTV上，2次在移动设备上，则80%的点数(0.8)将授予CTV屏幕，0.2次授予Mobile。

### 在Adobe Analytics中，家庭转化报表与CTV浏览转化报表有何不同？

[!DNL Analytics]中的CTV观看数据为[!DNL Analytics]跟踪提供支持，家庭转化数据使用通过Adobe Advertising转化跟踪收集的数据。 此外，[!DNL Analytics]中的DSP归因逻辑仅使用最后一个事件，但家庭转化报表支持两种不同的归因方法：唯一和MTA。

### 我能否同时在[!DNL Analytics for Advertising]和自定义报表中查看CTV显示到达数据？

没有[!DNL Analytics for Advertising]的广告商只能将家庭转化报表用于家庭转化报表。

如果您的组织具有[!DNL Analytics for Advertising]，请同时使用这两种类型的报表。 虽然CTV浏览报表适用于宽渠道分析、网站行为等，但自定义报表可提供精细的视图（其中数据按媒体类型、发布者等细分）以指示驱动转化率的因素。

## [!UICONTROL Household Reach & Frequency]和[!UICONTROL Household Conversions]报告与来自[!DNL Advanced Measurement Services]的数据

对于基于家庭的覆盖范围和频率或转化率的高级报告，[[!DNL Strategic Advertising Consulting] 团队](/help/dsp/introduction/advanced-measurement-services.md)可以提供高度可自定义的报告以及整体战略建议。 有关[!DNL Advanced Measurement Services]的详细信息，请与您的Adobe客户团队联系。

### 如果我已经使用[!DNL Advanced Measurement Services]，为什么要使用[!UICONTROL Household Reach & Frequency]和[!UICONTROL Household Conversions]报告？

[!UICONTROL Household Reach & Frequency]和[!UICONTROL Household Conversions]报告使客户端能够分别实时自主提取家庭级访问范围、频率和转化量度。

### 我可以同时使用[!UICONTROL Household Reach & Frequency]、[!UICONTROL Household Conversions]报告和[!DNL Advanced Measurement Services]吗？

理想的用例是同时使用[!UICONTROL Household]报表和[!DNL Advanced Measurement Services]报表和咨询服务。 将[!UICONTROL Household]报表视为事务型报表，旨在告知日常优化；将[!DNL Advanced Measurement Services]视为更具战略性的报表，旨在告知与总体业务目标相关的全面学习情况和收获。

>[!MORELIKETHIS]
>
>* [关于自定义报告](/help/dsp/reports/report-about.md)
>* [创建自定义报告](/help/dsp/reports/report-create.md)
>* [编辑自定义报告](/help/dsp/reports/report-edit.md)
>* [自定义报表设置](/help/dsp/reports/report-settings.md)
>* [可用报告列](/help/dsp/reports/report-columns.md)
