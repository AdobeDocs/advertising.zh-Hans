---
title: 关于同步 [!DNL Google Analytics] 转化量度
description: 了解同步 [!DNL Google Analytics] 转化量度以进行优化和报告。
role: User, Admin
exl-id: 32d0ba22-5c27-4f50-9886-1c09d2da952c
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# 关于同步[!DNL Google Analytics]转化量度

搜索、Social和Commerce可以同步特定[!DNL Google Analytics]帐户、属性的转化量度，以及视图组合以实现优化和报表。 自动包括[页面查看次数](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews)、[会话](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions)、[跳出率](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate)（计算为跳出次数/会话数）和[会话持续时间](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration)。 每个数据源最多可以包含16个其他量度。

>[!NOTE]
>
>Advertising DSP用户可以将转化量度用作自定义目标和报表。

数据传输的所有API使用情况都评估为适用的[!DNL Google Analytics]帐户中的项目。 您可以在[&#x200B; [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas)中查看此项目的配额。 有关报告API请求的[配额和调用限制](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas)的详细信息，请参阅[!DNL Google Analytics]文档。

以下步骤概述了从[!DNL Google Analytics]同步转换数据的过程。

1. [执行先决任务](data-source-prerequisites.md)

   * 在登陆页面URL中为所有适用的广告帐户实施Adobe Advertising令牌（`ef_id`查询字符串参数）。

   * 在[!DNL Google Analytics]的[!DNL Custom Dimension]中捕获Adobe Advertising令牌（`ef_id`查询字符串参数）。

1. （仅限代理帐户管理员、代理帐户管理员、[!DNL Adobe]帐户管理员和管理员用户）[为每个 [!DNL Google Analytics] 帐户、属性和视图组合创建一个数据源](data-source-configure.md)。

   要集成多个属性的量度或集成单个属性的多个视图的量度，请为每个属性设置单独的数据源。

   配置数据源后，Search、Social和Commerce每天从广告商所在时区的05:00开始提取数据。 在量度可用后，您可以将其包含在营销活动和项目组合管理视图以及报表中，并根据需要在优化目标中使用它们。

>[!MORELIKETHIS]
>
>* [配置a [!DNL Google Analytics] 数据源的先决条件](data-source-prerequisites.md)
>* [将a [!DNL Google Analytics] 视图配置为数据源](data-source-configure.md)
>* [编辑a [!DNL Google Analytics] 数据源](data-source-edit.md)
>* [暂停同步数据源](data-source-pause.md)
>* [重新验证a [!DNL Google Analytics] 数据源](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] 数据源设置](data-source-settings.md)
>* [附录 — 可用 [!DNL Google Analytics] 指标](data-source-ga-metrics.md)
