---
title: 关于自定义报表的常见问题解答
description: 详细了解自定义报表，包括家庭报表和转化路径分析报表。
exl-id: 3ffd178e-de41-4663-b85f-bd8ce3eb0dad
source-git-commit: a1ece707f43af4a6a3fc5573e41c75622f9b502f
workflow-type: tm+mt
source-wordcount: '1178'
ht-degree: 0%

---

# 关于自定义报表的常见问题解答

## 家庭报表

### [!UICONTROL Household Reach & Frequency]报告

#### [!UICONTROL Household Reach & Frequency]报告与其他自定义报告有何不同？

[!UICONTROL Household Reach & Frequency]报表根据IP地址在家庭级别跨各种维度测量访问范围、展示次数和频率。 其他自定义报表在设备或Cookie级别生成。

例如，即使一个展示次数提供给一个家庭中的三个设备，独特访问家庭数量度仍为1。

##### 支持的维度

[!UICONTROL Household Reach & Frequency]报表支持[以下维度](/help/dsp/reports/report-columns.md)：“[!UICONTROL Campaign]”、“[!UICONTROL Package]”、“[!UICONTROL Placement]”、“[!UICONTROL Site/Apps]”（不提供对重叠量度的访问权限）、“[!UICONTROL Media Type]”、“[!UICONTROL Feed Type]”、“[!UICONTROL Device]”、“[!UICONTROL Publisher]”、“[!UICONTROL Audience]”、“[!UICONTROL Creative Length]”和用户创建的投放位置“[!UICONTROL Tags]”。 |

##### 支持的指标

[可用量度](/help/dsp/reports/report-columns.md)包括：

* 重叠量度： [!UICONTROL Frequency Overlap]、[!UICONTROL Measurable Impressions (Overlap)]和[!UICONTROL Unique Household (Overlap)]。

  重叠量度是仅针对报告的维度或维度组合出现的值，而不针对其他维度出现的值。<!-- For example, it might show the ?? -->

* 非重叠量度： [!UICONTROL Frequency]、[!UICONTROL Incremental Household Reached]、[!UICONTROL % Incremental Household Reached]、[!UICONTROL Impressions]、[!UICONTROL Measurable Impressions]和[!UICONTROL Unique Household Reached]

不支持转化量度和自定义目标。

#### 重叠量度与非重叠量度之间有何区别？

下图显示了三个营销活动（A、B和C）的三个量度(已实现的独特家庭、已实现的增量家庭和已实现的增量家庭（重叠）)。

![家庭重叠量度的图示](/help/dsp/assets/household-overlap-metrics-illustration.png "家庭重叠量度的图示")

* 独特家庭访问量（总计）提供每个营销活动访问的独特家庭或每个圆的总面积。 在图中，A到达的唯一家庭=A + (A+B) + (A+C) +(A+B+C)到达的递增家庭

* Incremental Household Accessed是仅通过营销活动访问的独特家庭。 在图中，A、B、C到达的增量家庭是A、B、C分别到达的增量家庭。

* Incremental Household (Overlap)是活动或活动组合访问的唯一家庭。 在图中，A、C所实现的增量家庭为A+C。

#### 工作流

按照正常步骤[创建自定义报告](report-create.md)。

[!UICONTROL Household Reach & Frequency]报表只能包含一个维度。 它还可以包括a)按任何维度（网站/应用程序除外）列出的重叠量度，或b)非重叠量度，但不能同时包括两者。

#### [!UICONTROL Household Reach & Frequency]报表有哪些限制？

具有重叠量度的报表输出交叉点，最多三个值。 例如，如果对10个投放位置使用量度[!UICONTROL Unique Household (Overlap)]，则可以查看由单个投放位置到达的唯一家庭、由任意两个投放位置组合到达的共同家庭，以及由任意三个投放位置组合到达的共同家庭。 你看不到有四个或更多安置点的普通家庭。

对于营销活动、资源包或投放位置以外的维度，报表在每个维度中最多支持10个值。 例如，要为[!UICONTROL Unique Household Reached]维度生成[!UICONTROL Audience]报告，唯一受众的数量应少于或等于10。 如果包含10个以上的独特受众，则会生成空白报表。

#### 为什么我的[!UICONTROL Custom]报表与[!UICONTROL Household Reach & Frequency]报表之间的频度和唯一范围值不同？

[!UICONTROL Household]报表中的这些量度使用IP地址的实际计数进行计算，而[!UICONTROL Custom]报表中的量度使用使用使用模型计算的预计数量。 但是，差异应小于10%。

#### 如何为[!UICONTROL Placement Tags]维度配置报表？

若要创建投放位置的标记，请[打开投放位置设置](/help/dsp/campaign-management/placements/placement-edit.md)，然后在[投放位置标记字段](/help/dsp/campaign-management/placements/placement-settings.md)中输入值。

当投放位置包含多个标记时，报表会将整个字符串视为一个标记。 对于每个唯一字符串，报表都包含一行。

### [!UICONTROL Household Conversions]报告

#### [!UICONTROL Household Conversions]报表支持哪些归因方法？

支持两种类型的归因方法：

* [!UICONTROL Unique]：计算维度值（如设备或投放位置）在转化路径上的次数。

* [!UICONTROL Multi-Touch Attribution (MTA)]：根据维度值（如设备或投放位置）在转换路径上的出现频率分配每次转换的点数。 例如，如果在转化前总共有10次展示，其中8次在CTV上，2次在移动设备上，则80%的点数(0.8)将授予CTV屏幕，0.2次授予Mobile。

#### 在Adobe Analytics中，家庭转化报表与CTV浏览转化报表有何不同？

* 在[!DNL Analytics]中，[!DNL CTV View-Through Conversion]报告显示转化之前CTV展示为最后一个接触点的转化次数。 相反，DSP [!UICONTROL Household Conversions]报表显示在转化之前定义的回顾时间范围内随时接触CTV展示的唯一家庭数量。

* 在[!DNL Analytics]中，归因逻辑将转化专门分配给Adobe Advertising中的最后一个接触点。 相比之下，DSP [!UICONTROL Household Conversions]报表支持其他归因模型&#x200B;*[!UICONTROL Unique]*&#x200B;和&#x200B;*[!UICONTROL Multi-Touch Attribution (MTA)]*。

* [!DNL Analytics]报表数据对于按营销渠道、网站参与量度等进行分析，尤其有用。 DSP [!UICONTROL Household Conversions]报表允许将转化数据拆分为各种维度（如媒体类型和发布者），以提供更细粒度的洞察。

### [!UICONTROL Household Reach & Frequency]和[!UICONTROL Household Conversions]报告与来自[!DNL Advanced Measurement Services]的数据

对于基于家庭的覆盖范围和频率或转化率的高级报告，[[!DNL Strategic Advertising Consulting] 团队](/help/dsp/introduction/advanced-measurement-services.md)可以提供高度可自定义的报告以及整体战略建议。 有关[!DNL Advanced Measurement Services]的详细信息，请与您的Adobe客户团队联系。

#### 如果我已经使用[!DNL Advanced Measurement Services]，为什么要使用[!UICONTROL Household Reach & Frequency]和[!UICONTROL Household Conversions]报告？

[!UICONTROL Household Reach & Frequency]和[!UICONTROL Household Conversions]报告使客户端能够分别实时自主提取家庭级访问范围、频率和转化量度。

#### 我可以同时使用[!UICONTROL Household Reach & Frequency]、[!UICONTROL Household Conversions]报告和[!DNL Advanced Measurement Services]吗？

理想的用例是同时使用[!UICONTROL Household]报表和[!DNL Advanced Measurement Services]报表和咨询服务。 将[!UICONTROL Household]报表视为事务型报表，旨在告知日常优化；将[!DNL Advanced Measurement Services]视为更具战略性的报表，旨在告知与总体业务目标相关的全面学习情况和收获。

## 转化路径分析报表

### 与[!DNL Advanced Measurement Services]和Adobe Analytics Analysis Workspace创建的报表相比，转化路径报表如何？

| | 转化报表路径 | 高级测量服务对搜索报表的光晕影响 | Analysis Workspace中的报表 |
| --- | --- | --- |---|
| 客户价值 | 生成自助自定义报表，以了解广告历程的哪些路径导致了更多转化，从而促进优化 | 了解联网电视(CTV)策略对搜索点击量的影响 | 了解您的Adobe Advertising整体投资以及其他营销渠道对搜索点击量的影响 |
| 家庭级别 | 是 | 是 | 否 |
| 是否支持CTV？ | 是 | 是 | 是 |
| 归因方法 | 最近联系事件（展示或点击）必须在回顾窗口内。 | 独特 | 最近联系 |
| | 转化路径会考虑距上次接触事件超过30天的交互点。 | （CTV将获得点数，无论用户的单击路径中出现CTV暴露的位置） | （如果印象是回顾时间范围中的最后一个事件，并且在CTV曝光之前或之后没有来自其他格式的付费点击，则CTV获得点击） |
| 报告级别 | 粒度 | 粒度 | 广泛 |
| | (渠道类型、Creative/广告、关键字、路径、长度、转化时间) | (CTV Strategy， CTV App/Publisher) | (Adobe Advertising和其他营销渠道) |
| 营销渠道 | DSP +搜索(来自搜索、社交和Commerce) | DSP +搜索(来自搜索、社交和Commerce) | Adobe Advertising未通过EF ID跟踪的营销渠道（例如免费搜索、免费社交、电子邮件和附属活动） |
| 支持的转化量度 | 使用Adobe Advertising事件像素(AMO ID)和Adobe Analytics跟踪跟踪的指标 | 点击次数（无转化） | 使用Adobe Analytics跟踪跟踪的指标 |

有关高级测量服务对搜索报表的光晕影响的详细信息，请参阅[高级测量服务](/help/dsp/introduction/advanced-measurement-services.md)。

>[!MORELIKETHIS]
>
>* [关于自定义报告](/help/dsp/reports/report-about.md)
>* [创建自定义报告](/help/dsp/reports/report-create.md)
>* [编辑自定义报告](/help/dsp/reports/report-edit.md)
>* [自定义报表设置](/help/dsp/reports/report-settings.md)
>* [可用报告列](/help/dsp/reports/report-columns.md)
