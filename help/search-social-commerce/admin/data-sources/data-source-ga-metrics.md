---
title: 可用 [!DNL Google Analytics] 量度
description: 参考 [!DNL Google Analytics] 可用于数据源的量度。
role: User, Admin
exl-id: f7ac93e3-1aed-4165-ae65-7966ca192c84
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 附录 — 可用 [!DNL Google Analytics] 量度

在客户的实施中启用以下量度时，除了上述排除项外，其余均可用 [!DNL Google Analytics].

<!-- Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| 类别 | 已排除 | 评论 |
| ---- | ---- | ---- |
| \[全部\] | 数据类型为“PERCENT”的指标 | 始终排除以百分比显示的量度。 |
| 用户 | ga：1dayUsers， ga：7dayUsers， ga：14dayUsers， ga：28dayUsers， ga：sessionsPerUser | — |
| 会话 | ga：uniqueDimensionCombinations | — |
| 目标转化 | — | — |
| 页面跟踪 | ga：entraces， ga：timeOnPage， ga：exits | — |
| 内部搜索 | — | 内部搜索中所有量度的友好名称前面加有值“InternalSearch： ” |
| 事件跟踪 | — | — |
| 电子商务 | — | — |
| 社交 | — | — |
| 例外 | — | — |
| 自定义变量或列 | ga：calcMetric_* | 计算量度始终被排除。 |

>[!MORELIKETHIS]
>
>* [关于同步 [!DNL Google Analytics] 转化量度](data-source-about.md)
>* [配置的前提条件 [!DNL Google Analytics] 数据源](data-source-prerequisites.md)
>* [配置 [!DNL Google Analytics] 作为数据源查看](data-source-configure.md)
>* [编辑 [!DNL Google Analytics] 数据源](data-source-edit.md)
>* [暂停数据源同步](data-source-pause.md)
>* [重新验证 [!DNL Google Analytics] 数据源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 数据源设置](data-source-settings.md)
