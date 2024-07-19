---
title: 可用 [!DNL Google Analytics] 个量度
description: 引用可用于数据源的 [!DNL Google Analytics] 指标。
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 附录 — 可用的[!DNL Google Analytics]指标

在[!DNL Google Analytics]中的客户实施中启用以下量度时，除了上述排除项外，这些量度均可用。

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
>* [配置a [!DNL Google Analytics] 数据源的先决条件](data-source-prerequisites.md)
>* [将a [!DNL Google Analytics] 视图配置为数据源](data-source-configure.md)
>* [编辑a [!DNL Google Analytics] 数据源](data-source-edit.md)
>* [暂停同步数据源](data-source-pause.md)
>* [重新验证a [!DNL Google Analytics] 数据源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 数据源设置](data-source-settings.md)
