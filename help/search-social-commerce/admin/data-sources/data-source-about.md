---
title: 关于同步 [!DNL Google Analytics] 转化量度
description: 了解同步 [!DNL Google Analytics] 用于优化和报表的转化量度。
role: User, Admin
exl-id: 0c263ced-3774-4d4b-9d61-65289cd74027
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 关于同步 [!DNL Google Analytics] 转化量度

搜索、Social和Commerce可以同步特定用户的转化量度 [!DNL Google Analytics] 帐户、属性和视图的组合，用于优化和报告。 [页面查看次数](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews)， [会话](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions)， [跳出率](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) （以跳出次数/会话数计算），以及 [会话持续时间](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) 自动包含在内。 每个数据源最多可以包含16个其他量度。

>[!NOTE]
>
>Advertising DSP用户可以将转化量度用作自定义目标和报表。

数据传输的所有API使用情况均在适用的中评估为项目 [!DNL Google Analytics] 帐户。 您可以在中查看此项目的配额 [该 [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). 请参阅 [!DNL Google Analytics] 文档，以了解有关 [报告API请求的配额和调用限制](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

以下步骤概述了从中同步转换数据的过程 [!DNL Google Analytics].

1. [执行先决任务](data-source-prerequisites.md)

   * 实施Adobe Advertising令牌(`ef_id` 查询字符串参数)。

   * 捕获Adobe Advertising令牌(`ef_id` 查询字符串参数) [!DNL Custom Dimension] 在 [!DNL Google Analytics].

1. (代理账户管理员、代理账户管理员、 [!DNL Adobe] 帐户管理员和仅管理员用户) [为每个创建一个数据源 [!DNL Google Analytics] 帐户、属性和视图组合](data-source-configure.md).

   要集成多个属性的量度或集成单个属性的多个视图的量度，请为每个属性设置单独的数据源。

   配置数据源后，Search、Social和Commerce每天从广告商所在时区的05:00开始提取数据。 在量度可用后，您可以将其包含在营销活动和项目组合管理视图以及报表中，并根据需要在优化目标中使用它们。

>[!MORELIKETHIS]
>
>* [配置的前提条件 [!DNL Google Analytics] 数据源](data-source-prerequisites.md)
>* [配置 [!DNL Google Analytics] 作为数据源查看](data-source-configure.md)
>* [编辑 [!DNL Google Analytics] 数据源](data-source-edit.md)
>* [暂停数据源同步](data-source-pause.md)
>* [重新验证 [!DNL Google Analytics] 数据源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 数据源设置](data-source-settings.md)
>* [附录 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)
