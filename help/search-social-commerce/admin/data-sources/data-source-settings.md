---
title: “[!DNL Google Analytics]数据源设置”
description: 引用 [!DNL Google Analytics] 数据源所需的设置。
role: User, Admin
exl-id: 78422c2c-ed58-410e-8996-882759ed5556
feature: Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# [!DNL Google Analytics]数据源设置

| 部分 | 参数 | 描述 |
| ---- | ---- | ---- |
| [!UICONTROL Connect to Google Analytics] | [!UICONTROL Google Analytics Account ID] | 从中提取数据的[!DNL Google Analytics]帐户的ID。 所有用于拉取数据的API均按指定帐户计费。 该帐户必须向指定的电子邮件地址授予“读取和分析”权限。<br><br>若要查找您的ID，请登录到[!DNL Google Analytics]。 单击左上角的&#x200B;**[!DNL All accounts]**&#x200B;以打开您的帐户列表。 每个帐户的ID都位于帐户名称下。 |
| | [!UICONTROL Google Analytics Login] | 指定用于访问此数据源数据的登录/电子邮件地址。 登录必须注册到[!DNL Google]帐户，并且拥有[!DNL Google Analytics]帐户的“读取和分析”权限。 请参阅[有关在 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587)中分配用户权限的说明。<br><br><b>注意：</b>如果更改此登录帐户的密码，则与该帐户的所有打开连接都将关闭。 若要继续同步数据，请返回此页面并[重新进行身份验证](data-source-reauthenticate.md)。 |
| [!UICONTROL Account Details] | [!UICONTROL Google Analytics Account Name] | （只读；仅连接的帐户）帐户名称。 |
| | [!UICONTROL Google Analytics Property] | 从中为[!DNL Google Analytics]帐户收集数据的属性（网站、移动应用程序或设备）。<br><br>要集成多个属性的量度，请为每个属性设置单独的数据源。 |
| | [!UICONTROL Google Analytics View] | 包含要访问的数据集的视图。 如果属性有多个视图，请考虑以最高级别提取未过滤的视图，其中包含所有数据。<br><br>要为同一属性的多个视图集成量度，请为每个视图设置单独的数据源。 确保视图不包含重叠数据。 |
| | [!UICONTROL Google Analytics Dimension] | 使用Adobe Advertising“ef_id”查询字符串参数的值填充的[!DNL Google Analytics]自定义维度。 如果列出的维度不正确，请联系您的[!DNL Google Analytics]实施团队。<br><br>使用“ef_id”作为主键将数据从[!DNL Google Analytics]传递到Adobe Advertising。 |
| [!UICONTROL Import Metrics] | [!UICONTROL Available Metrics] | 指定[!DNL Google Analytics]属性和视图的所有可用量度（未针对数据源导入），按类别组织。 此列表包括导入的友好名称和后端名称（以“ga”开头）。 每个量度的。 [!UICONTROL Refresh]按钮使用[!DNL Google Analytics]中的任何新量度刷新列表。<br><br>要导入可用的量度，请将其拖动到[!UICONTROL Selected Metrics]部分。<br><br>查看“[可用 [!DNL Google Analytics] Advertising Cloud中的指标](data-source-ga-metrics.md)”。 |
| | 选定的量度 | 为数据源导入的指定[!DNL Google Analytics]属性和视图的所有度量，以及每个度量的验证状态。 该列表包含每个量度的导入友好名称和后端名称（以“`ga.`”开头）。 每个数据源可以包含四个您无法删除的默认流量量度（[!UICONTROL Pageviews]、[!UICONTROL Sessions]、[!UICONTROL Bounces]和[!UICONTROL Session Duration]），以及最多16个没有数据的其他有效量度或量度。 您可以随时编辑指标列表。<br><br>要导入指标，请在[!UICONTROL Available Metrics]窗格中选择该指标，并将其拖动到此处。<br><br><b>警告：</b> [!DNL Google Analytics]在单个数据馈送中最多允许10个量度。 在Search、Social和Commerce中，每个数据源最多可包含两个包含20个量度的馈送，但使用第二个馈送会将您的API调用翻倍到[!DNL Google Analytics]。 如果您有许多量度，请仅选择要在优化目标中使用的量度。 您可以在[ [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas)中查看此项目的配额。 查看有关 [!DNL Google Analytics][&#128279;](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas)的API请求的配额和调用限制的详细信息。<br><br><b>注释：</b><br><ul><li>友好名称被导入为[!UICONTROL Admin] > [!UICONTROL Transactions Properties]视图中量度的显示名称，并附加了“<code>_ga：&lt;在量度标记字段中配置的metric_tag”</code>&quot;（例如“Pageviews_ga：UK”）。 您可以选择编辑自定义目标和自定义量度的显示名称，但所有常用量度的显示名称每天都会被覆盖，带有[!DNL Google Analytics]中的友好名称并附加指定标记。</li><li>页面查看次数、会话数、跳出率（计算公式为跳出次数/会话数）和会话持续时间会自动计入项目组合竞价算法。 您可以手动将任何其他量度添加到项目组合目标。</li><li>从数据源中删除度量时，Adobe Advertising会根据正常的[数据保留策略](/help/search-social-commerce/reports/data-used-for-reports.md)保留历史数据。</li></ul> |
| 量度标记 | 量度标记 | 要附加到Adobe Advertising中每个选定的[!DNL Google Analytics]指标的标记，其前面有“<code>_ga：</code>&quot;（例如“Pageviews_ga：&lt;metric_tag>”）。 标记可以是2-5个字母数字字符，并且对于广告商必须是唯一的。<br><br>此标记可帮助您识别每个量度的数据源。 当您设置多个数据源时，此标记尤其重要，因为每个数据源都包含一些相同的量度名称（包括[!UICONTROL Pageviews]、[!UICONTROL Sessions]、[!UICONTROL Bounces]和[!UICONTROL Session Duration]，可能还包括其他量度）。 附加不同的量度标记可防止量度名称重复。<br><br>例如，如果您为UK资产和JP资产分别设置集成，则可以使用“UK”和“JP”作为量度标记。 这两个属性的[!UICONTROL Pageviews]指标随后在Adobe Advertising中相应地显示为“Pageviews_ga：UK”和“Pageviews_ga：JP”。 |

>[!MORELIKETHIS]
>
>* [关于同步 [!DNL Google Analytics] 转化量度](data-source-about.md)
>* [配置a [!DNL Google Analytics] 数据源的先决条件](data-source-prerequisites.md)
>* [将a [!DNL Google Analytics] 视图配置为数据源](data-source-configure.md)
>* [编辑a [!DNL Google Analytics] 数据源](data-source-edit.md)
>* [暂停同步数据源](data-source-pause.md)
>* [重新验证a [!DNL Google Analytics] 数据源](data-source-reauthenticate.md)
>* [附录 — 可用 [!DNL Google Analytics] 指标](data-source-ga-metrics.md)
