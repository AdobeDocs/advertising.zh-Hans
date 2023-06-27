---
title: ‘[!DNL Google Analytics] 数据源设置
description: 引用所需的设置 [!DNL Google Analytics] 数据源。
role: User, Admin
exl-id: 531351b4-07f1-43ef-a3d2-892a49ffb5ca
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 0%

---

# [!DNL Google Analytics] 数据源设置

| 章节 | 参数 | 描述 |
| ---- | ---- | ---- |
| [!UICONTROL Connect to Google Analytics] | [!UICONTROL Google Analytics Account ID] | 的ID [!DNL Google Analytics] 从中提取数据的帐户。 提取数据的所有API使用均按指定帐户计费。 该帐户必须向指定的电子邮件地址授予“读取和分析”权限。<br><br>要查找您的ID，请登录 [!DNL Google Analytics]. 在左上角，单击 **[!DNL All accounts]** 以打开您的帐户列表。 每个帐户的ID都位于帐户名称下。 |
| | [!UICONTROL Google Analytics Login] | 指定用于访问此数据源的数据的登录/电子邮件地址。 登录必须注册到 [!DNL Google] 帐户并具有的“读取和分析”权限 [!DNL Google Analytics] 帐户。 请参阅 [在中分配用户权限的说明 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).<br><br><b>注意：</b> 如果更改此登录帐户的密码，则将关闭与该帐户的所有开放连接。 要恢复同步数据，请返回此页面并 [重新身份验证](data-source-reauthenticate.md). |
| [!UICONTROL Account Details] | [!UICONTROL Google Analytics Account Name] | （只读；仅连接的帐户）帐户名称。 |
| | [!UICONTROL Google Analytics Property] | 从中为收集数据的属性（网站、移动应用程序或设备） [!DNL Google Analytics] 帐户。<br><br> 要集成多个属性的量度，请为每个属性设置单独的数据源。 |
| | [!UICONTROL Google Analytics View] | 包含要访问的数据集的视图。 如果属性有多个视图，请考虑从包含所有数据的最高级别提取未筛选的视图。<br><br>要为同一属性的多个视图集成量度，请为每个视图设置单独的数据源。 确保视图不包含重叠数据。 |
| | [!UICONTROL Google Analytics Dimension] | 此 [!DNL Google Analytics] 使用Adobe Advertising“ef_id”查询字符串参数的值填充的自定义维度。 如果列出的维度不正确，请联系贵机构的 [!DNL Google Analytics] 实施团队。<br><br>“ef_id”用作从中传递数据的主键 [!DNL Google Analytics] 以Adobe Advertising。 |
| [!UICONTROL Import Metrics] | [!UICONTROL Available Metrics] | 指定的所有可用量度 [!DNL Google Analytics] 未为数据源导入的属性和视图，按类别组织。 该列表包括导入的友好名称和后端名称（以“ga”开头）。 用于每个指标。 此 [!UICONTROL Refresh] 按钮会使用中的任何新量度刷新列表 [!DNL Google Analytics].<br><br>要导入可用的量度，请将其拖动到 [!UICONTROL Selected Metrics] 部分。<br><br>参见“[可用 [!DNL Google Analytics] Advertising Cloud中的指标](data-source-ga-metrics.md).” |
| | 选定的量度 | 指定的所有量度 [!DNL Google Analytics] 为数据源导入的属性和视图，以及每个量度的验证状态。 该列表包括导入的友好名称和后端名称（以“”开头）`ga.`&quot;)。 每个数据源可以包含四个您无法删除的默认流量量度([!UICONTROL Pageviews]， [!UICONTROL Sessions]， [!UICONTROL Bounces]、和 [!UICONTROL Session Duration])以及最多16个其他有效指标或指标（不含数据）。 您可以随时编辑指标列表。<br><br>要导入指标，请在 [!UICONTROL Available Metrics] 窗格并将其拖动到此处。<br><br><b>注意：</b> [!DNL Google Analytics] 在单个数据馈送中最多允许10个量度。 在Search、Social和Commerce中，您的每个数据源最多可以包含两个包含20个量度的馈送，但使用第二个馈送会将您的API调用翻倍 [!DNL Google Analytics]. 如果您有许多量度，请仅选择要在优化目标中使用的量度。 您可以在中查看此项目的配额 [此 [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). 查看更多关于 [API请求的配额和调用限制为 [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).<br><br><b>注释：</b><br><ul><li>友好名称作为量度的显示名称导入到 [!UICONTROL Admin] > [!UICONTROL Transactions Properties] 查看并附加了&quot;<code>_ga：&lt;metric_tag configured=&quot;&quot; in=&quot;&quot; the=&quot;&quot; metric=&quot;&quot; tag=&quot;&quot; field=&quot;&quot;></code>&quot;（例如“Pageviews_ga：UK”）。 您可以选择编辑自定义目标和自定义量度的显示名称，但所有常用量度的显示名称每天都会被覆盖，并在其中使用友好名称 [!DNL Google Analytics]，并附加指定的标记。</li><li>页面查看次数、会话数、跳出率（以跳出次数/会话数计算）和会话持续时间会自动纳入项目组合竞价算法中。 您可以手动将任何其他指标添加到项目组合目标。</li><li>从数据源中删除量度时，Adobe Advertising会根据正常情况保留历史数据 [数据保留策略](/help/search-social-commerce/reports/data-used-for-reports.md).</li></ul> |
| 量度标记 | 量度标记 | 附加到每个选定项的标记 [!DNL Google Analytics] Adobe Advertising中的指标，前面有“<code>_ga：</code>”(例如“Pageviews_ga：&lt;metric_tag>“)。 标记可以是2-5个字母数字字符，并且对于广告商必须是唯一的。<br><br>此标记可帮助您识别每个指标的数据源。 在设置多个数据源时，此标记尤其重要，因为每个数据源都包含一些相同的量度名称(包括 [!UICONTROL Pageviews]， [!UICONTROL Sessions]， [!UICONTROL Bounces]、和 [!UICONTROL Session Duration]、可能还有其他量度)。 附加不同的量度标记可防止量度名称重复。<br><br>例如，如果您为UK资产和JP资产设置单独的集成，则可能会使用“UK”和“JP”作为量度标记。 此 [!UICONTROL Pageviews] 这两个属性的量度随后在Adobe广告中相应显示为“Pageviews_ga：UK”和“Pageviews_ga：JP”。 |

>[!MORELIKETHIS]
>
>* [关于同步 [!DNL Google Analytics] 转化量度](data-source-about.md)
>* [配置的前提条件 [!DNL Google Analytics] 数据源](data-source-prerequisites.md)
>* [配置 [!DNL Google Analytics] 作为数据源查看](data-source-configure.md)
>* [编辑 [!DNL Google Analytics] 数据源](data-source-edit.md)
>* [暂停数据源同步](data-source-pause.md)
>* [重新验证 [!DNL Google Analytics] 数据源](data-source-reauthenticate.md)
>* [附录 — 可用 [!DNL Google Analytics] 量度](data-source-ga-metrics.md)
