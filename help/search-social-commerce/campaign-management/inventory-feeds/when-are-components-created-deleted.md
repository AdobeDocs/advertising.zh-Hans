---
title: 清单信息源何时会创建或删除帐户组件？
description: 了解在发布清单源时创建和删除帐户组件的情况。
exl-id: 93b31996-15dd-4215-ae9d-39327910f712
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# 清单信息源何时会创建或删除帐户组件？

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （仅删除操作），以及 [!DNL Yandex] 仅限帐户*

通过模板传播库存信息源文件时，将按如下方式创建和删除帐户组件。

>[!NOTE]
>
>广告组中永远不会创建重复的广告。

| 方案 | 示例 | 操作 |
|----|----|----|
| 信息源数据包括促销活动名称、广告组名称、关键字或产品组中使用的列的新值。 | 以前的文件：<br>Campaign=Hats<br>Campaign=Gloves<br><br>新文件：<br>Campaign=Shoes | 如果广告网络上不存在新的促销活动、广告组、关键词或产品组，则会创建新促销活动、广告组、关键词或产品组。 |
| 馈送数据包含在广告中使用的列的新值。 | 上一个文件：广告包含的价格=20<br><br>新文件：对于同一广告，价格为10 | 当广告复制到 [!DNL Microsoft® Advertising] 扩展的文本广告， [!DNL Yahoo! Japan ads]，或 [!DNL Yandex] 广告发生更改，现有广告被删除并创建一个新广告。<br><br>为其他广告类型更改广告副本或将适用的列用于时 [!DNL Google Ads] 广告参数({param1} 或 {param2})，则会更新现有广告。 |
| 自上次传播以来，营销活动、广告组、关键字或产品组的模板设置已更改。 | 以前的设置：Keyword=[关键词]<br><br>新设置： Keyword=&lt;color>[关键词] | 如果广告网络上不存在新的促销活动、广告组、关键词或产品组，则会创建新促销活动、广告组、关键词或产品组。 |
| 自上次传播以来，广告的模板设置发生了更改。 | 以前的设置：广告描述=&quot;购买 [类别] 现在。”<br><br>新设置：广告描述=&quot;购买 [品牌] 现在。” | 当广告复制到 [!DNL Microsoft® Advertising] 扩展的文本广告， [!DNL Yahoo! Japan ads]，或 [!DNL Yandex] 广告发生更改，现有广告被删除并创建一个新广告。<br><br>当为其他广告类型更改广告副本，或者更改反映用于单个广告的列发生更改时 [!DNL Google Ads] 广告参数({param1} 或 {param2})，则会更新现有广告。 |
| 新的馈送数据不包含现有营销活动或广告组的行。 | 不适用 | 现有营销活动和广告组保持不变。 |
| 新的馈送数据不包含现有广告组、广告、关键字或产品组的行。 | 不适用 | 现有的广告组、广告、关键词或产品组将保持不变，或者将暂停或删除，具体情况请参见 [馈送数据设置](feed-settings-manage.md#feed-data-settings). |
| 现有父产品组的新馈送数据不包含其现有子产品组的行。 | 不适用 | 现有的父产品组将保持不变，或者将根据 [馈送数据设置](feed-settings-manage.md#feed-data-settings). <b>注意：</b> 如果馈送数据设置配置为暂停缺少的行项目，则仍会删除父产品组，因为您无法暂停产品组。 |
| 新的馈送数据包含的广告组、广告、关键词或产品组的行以前的数据中为a)，但后来被忽略，并根据 [馈送数据设置](feed-settings-manage.md#feed-data-settings). | 不适用 | 现有广告组、广告、关键词或产品组将被重新激活，且不会丢失任何历史记录或质量分数。 |
| 新的馈送数据包含的广告组、广告、关键词或产品组的行以前的数据中为a)，但后来被忽略，并根据 [馈送数据设置](feed-settings-manage.md#feed-data-settings). | 不适用 | 将创建一个新的广告组、广告、关键字或产品组。 |
| 您已对“”禁用了营销活动或广告组级别选项[!UICONTROL Delete negative keywords when omitted from list]“ | 负面关键词列表包括“coupe”和“sport car”。<br><br>广告组已包含负关键字“SUV”。 | 任何不在列表中的现有负关键字将保持原样。 |
| 您已为“”启用营销活动或广告组级别选项[!UICONTROL Delete negative keywords when omitted from list]“ ”和不在列表中的负值关键字存在。 | 负面关键词列表包括“coupe”和“sport car”。<br><br>广告组已包含负关键字“SUV”。 | 通过模板传播馈送文件时，会删除之前使用该模板创建的任何未指定的负关键字。 但是，使用其他方式创建的任何未指定的负关键字(例如，在普通批量处理工作表中， [!UICONTROL Campaigns] 视图（或在广告网络的广告编辑器中）保持不变。 | | 已发布的信息源文件的组件计划结束日期出现。 | 不适用 | 现有营销活动保持不变。 现有的广告组、广告和关键字将保持不变、暂停或删除，具体情况如下 [馈送数据设置](feed-settings-manage.md#feed-data-settings). |
| 物料的库存水平下降到低于中指定的最小值。 [馈送数据设置](feed-settings-manage.md#feed-data-settings). | 上一个文件： stock=10<br><br>新文件： stock=0 | 现有营销活动保持不变。 现有广告组、广告、关键词和产品组已暂停或删除，具体情况如下 [馈送数据设置](feed-settings-manage.md#feed-data-settings). |
| 物料的库存水平可回溯至早于中指定的最小值。 [馈送数据设置](feed-settings-manage.md#feed-data-settings). | 上一个文件： stock=0<br><br> 新文件： stock=10 | 暂停现有广告、关键词或产品组后，它们将被重新激活，而不会丢失任何历史记录或质量分数。 当不存在广告、关键字或产品组时（例如，如果由于库存级别低于最低值而以前删除了这些广告、关键字或产品组），则会创建新广告、关键字或产品组。 |

>[!MORELIKETHIS]
>
>* [关于使用库存信息源自动化广告管理](inventory-feeds-about.md)
