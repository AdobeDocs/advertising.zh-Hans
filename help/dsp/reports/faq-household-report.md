---
title: 关于 [!UICONTROL Household] 报表
description: 进一步了解 [!UICONTROL Household] 报表，包括与其他报表和疑难解答有何不同。
source-git-commit: 95f81dafbe13f40487bad47f7dd41a6c80c589ee
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# 关于 [!UICONTROL Household] 报表

## 如何 [!UICONTROL Household] 范围和频度报表与其他自定义报表不同？

的 [!UICONTROL Household] 报告根据IP地址衡量家庭级别各个维度的访问范围、展示次数和频度。 其他自定义报表在设备或Cookie级别生成。

例如，即使一个家庭内的三台设备有一次展示，“独特家庭已到达”量度也只有一次。

### 支持的Dimension

的 [!UICONTROL Household] 报表支持 [以下维度](/help/dsp/reports/report-columns.md):&quot;[!UICONTROL Campaign], &quot;[!UICONTROL Package], &quot;[!UICONTROL Placement], &quot;[!UICONTROL Site/Apps]&quot;（不提供对重叠量度的访问）， &quot;[!UICONTROL Media Type], &quot;[!UICONTROL Feed Type], &quot;[!UICONTROL Device], &quot;[!UICONTROL Publisher], &quot;[!UICONTROL Audience], &quot;[!UICONTROL Creative Length]、和用户创建的版面“[!UICONTROL Tags].&quot; |

### 支持的量度

的 [可用量度](/help/dsp/reports/report-columns.md) 包括：

* 重叠量度： [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)]和 [!UICONTROL Unique Household (Overlap)].

   重叠量度是指仅针对报告的维度或维度组合，而不针对其他维度出现的值。 <!-- For example, it might show the ?? -->

* 非重叠量度： [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions]和 [!UICONTROL Unique Household Reached]

不支持转化量度和自定义目标。

## 重叠量度和非重叠量度之间有何区别？

下图显示了三个促销活动（A、B和C）的三个量度(独特家庭到达、增量家庭到达和增量家庭（重叠）)。

![家庭重叠量度的插图](/help/dsp/assets/household-overlap-metrics-illustration.png "家庭重叠量度的插图")

* “已达到的独特家庭（总数）”提供每个营销活动或每个圈子的总区域所达到的独特家庭。 在图中，A所达到的独特家庭= A +(A+B)+(A+C)+(A+B+C)所达到的增量家庭

* Incremental Houdel Remained（增量家庭已实现）是仅通过活动实现的独特家庭。 在该图中，A、B、C所达到的增量家庭分别为A、B、C所达到的增量家庭。

* 增量家庭（重叠）是指通过促销活动或促销活动组合实现的独特家庭。 在图中，A、C所达到的增量家庭为A+C。

## 工作流

按照常规步骤操作 [创建自定义报表](report-create.md).

的 [!UICONTROL Household] 报表只能包含一个维度。 它还可以包括a)除网站/应用程序之外的任何维度的重叠量度，或b)非重叠量度，但不能同时包括这两者。

## 的 [!UICONTROL Household] 报告？ 

具有重叠量度的报表输出最多三个值的交集。 例如，如果您使用 [!UICONTROL Unique Household (Overlap)] 对于10个安置点，您可以看到个人安置点所触及的独特家庭、两个安置点所触及的普通家庭以及三个安置点所触及的普通家庭。 你无法看到普通家庭达到四个或四个以上。

对于营销活动、包或版面以外的维度，报表支持每个维度中最多10个值。 例如，要生成 [!UICONTROL Unique Household Reached] 报表 [!UICONTROL Audience] 维度中，独特受众的数量应小于或等于10。 如果您包含的独特受众超过10个，则会生成一个空白报表。

## 为什么频率和独特访问值在我的 [!UICONTROL Custom] 报告和 [!UICONTROL Household] 报告？

这些量度位于 [!UICONTROL Household] 报表是使用IP地址的实际计数计算的，而 [!UICONTROL Custom] 报表使用使用模型计算的估计数。 但是，差异应小于10%。

## 如何为 [!UICONTROL Placement Tags] 维度？

要为版面创建标记，请 [打开版面设置](/help/dsp/campaign-management/placements/placement-edit.md) 并在 [版面标记字段](/help/dsp/campaign-management/placements/placement-settings.md).
 
当版面包含多个标记时，报表会将整个字符串视为一个标记。 报表中每个唯一字符串都包含一行。

## [!UICONTROL Household] 报表与数据 [!DNL Advanced Measurement Services]

关于基于家庭的覆盖面和频度的高级报告， [[!DNL Strategic Advertising Consulting] 团队](/help/dsp/introduction/advanced-measurement-services.md) 可以提供高度可自定义的报告以及全面的战略建议。 有关 [!DNL Advanced Measurement Services]，请联系您的Adobe帐户团队。

### 如果我已在使用 [!DNL Advanced Measurement Services]，为何要使用 [!UICONTROL Household] 报告？

的 [!UICONTROL Household] 报告使客户能够实时自主地获取家庭级别的访问范围和频率量度。

### 我能否同时使用 [!UICONTROL Household] 报告和 [!DNL Advanced Measurement Services]? 

理想的用例是同时使用 [!UICONTROL Household] 报表和 [!DNL Advanced Measurement Services] 报告和咨询服务。 请考虑 [!UICONTROL Household] 报告为事务型，用于指导日常优化，以及 [!DNL Advanced Measurement Services] 更具战略性，旨在提供与总体业务目标相关的全面学习和总结。

>[!MORELIKETHIS]
>
>* [关于自定义报表](/help/dsp/reports/report-about.md)
>* [创建自定义报表](/help/dsp/reports/report-create.md)
>* [编辑自定义报表](/help/dsp/reports/report-edit.md)
>* [自定义报表设置](/help/dsp/reports/report-settings.md)
>* [可用报表列](/help/dsp/reports/report-columns.md)

