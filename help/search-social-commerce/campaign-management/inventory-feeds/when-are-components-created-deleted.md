---
title: 清单信息源何时会创建或删除帐户组件？
description: 了解在发布清单源时创建和删除帐户组件的情况。
exl-id: 39a3cc2c-f956-4a89-a69d-687a27a38a1e
feature: Search Inventory Feeds
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---

# 清单信息源何时会创建或删除帐户组件？

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （仅删除操作）和仅[!DNL Yandex]帐户*

通过模板传播库存信息源文件时，将按如下方式创建和删除帐户组件。

>[!NOTE]
>
>广告组中永远不会创建重复的广告。

| 方案 | 示例 | 操作 |
|----|----|----|
| 信息源数据包括促销活动名称、广告组名称、关键字或产品组中使用的列的新值。 | 以前的文件：<br>Campaign=Hats<br>Campaign=Gloves<br><br>新文件：<br>Campaign=Shoes | 如果广告网络上不存在新的促销活动、广告组、关键词或产品组，则会创建新促销活动、广告组、关键词或产品组。 |
| 馈送数据包含在广告中使用的列的新值。 | 上一个文件：广告包含的价格=20<br><br>新文件：对于同一广告，价格=10 | 更改[!DNL Microsoft Advertising]扩展文本广告、[!DNL Yahoo! Japan ads]或[!DNL Yandex]广告的广告副本时，将删除现有广告并创建一个新广告。<br><br>当为其他广告类型更改广告副本或将适用的列用于广告中的[!DNL Google Ads]广告参数（{param1}或{param2}）时，则会更新现有广告。 |
| 自上次传播以来，营销活动、广告组、关键字或产品组的模板设置已更改。 | 以前的设置:Keyword=[Keyword]<br><br>新设置： Keyword=&lt;Color>[Keyword] | 如果广告网络上不存在新的促销活动、广告组、关键词或产品组，则会创建新促销活动、广告组、关键词或产品组。 |
| 自上次传播以来，广告的模板设置发生了更改。 | 以前的设置：广告描述=“立即购买[类别]。”<br><br>新设置：广告描述=“立即购买[品牌]”。 | 更改[!DNL Microsoft Advertising]扩展文本广告、[!DNL Yahoo! Japan ads]或[!DNL Yandex]广告的广告副本时，将删除现有广告并创建一个新广告。<br><br>如果更改了其他广告类型的广告副本，或者更改反映了广告中用于单个[!DNL Google Ads]广告参数（{param1}或{param2}）的列的更改，则会更新现有广告。 |
| 新的馈送数据不包含现有营销活动或广告组的行。 | 不适用 | 现有营销活动和广告组保持不变。 |
| 新的馈送数据不包含现有广告组、广告、关键字或产品组的行。 | 不适用 | 根据[信息源数据设置](feed-settings-manage.md#feed-data-settings)，现有的广告组、广告、关键字或产品组将保持不变、已暂停或已被删除。 |
| 现有父产品组的新馈送数据不包含其现有子产品组的行。 | 不适用 | 根据[信息源数据设置](feed-settings-manage.md#feed-data-settings)，现有父产品组保持原样或已被删除。 <b>注意：</b>如果馈送数据设置配置为暂停缺少的行项目，则父产品组仍会被删除，因为您无法暂停产品组。 |
| 新的馈送数据包含广告组、广告、关键字或产品组的行，这些行以前的数据中为a)，但此后被忽略b)，并根据[馈送数据设置](feed-settings-manage.md#feed-data-settings)暂停。 | 不适用 | 现有广告组、广告、关键词或产品组将被重新激活，且不会丢失任何历史记录或质量分数。 |
| 新的馈送数据包含广告组、广告、关键字或产品组的行，这些行以前的数据中为a)，但此后被忽略，并根据[馈送数据设置](feed-settings-manage.md#feed-data-settings)被删除。 | 不适用 | 将创建一个新的广告组、广告、关键字或产品组。 |
| 您已对“[!UICONTROL Delete negative keywords when omitted from list]”禁用了营销活动或广告组级别选项。 | 负面关键词列表包括“coupe”和“sport car”。<br><br>广告组已包含负关键字“SUV”。 | 任何不在列表中的现有负关键字将保持原样。 |
| 您已为“[!UICONTROL Delete negative keywords when omitted from list]”启用了营销活动或广告组级别的选项，并且存在不在列表中的负关键字。 | 负面关键词列表包括“coupe”和“sport car”。<br><br>广告组已包含负关键字“SUV”。 | 通过模板传播馈送文件时，会删除之前使用该模板创建的任何未指定的负关键字。 但是，使用其他方式创建的任何未指定的负面关键字（例如在纯批量处理工作表、[!UICONTROL Campaigns]视图或广告网络的广告编辑器中）将保持不变。 |
| 已发布的信息源文件的组件计划结束日期出现。 | 不适用 | 现有营销活动保持不变。 根据[馈送数据设置](feed-settings-manage.md#feed-data-settings)，现有广告组、广告和关键字将保持不变、暂停或删除。 |
| 物料的库存水平下降到低于[馈送数据设置](feed-settings-manage.md#feed-data-settings)中指定的最低值。 | 上一个文件： stock=10<br><br>新文件： stock=0 | 现有营销活动保持不变。 根据[馈送数据设置](feed-settings-manage.md#feed-data-settings)，现有广告组、广告、关键字和产品组已暂停或删除。 |
| 物料的库存级别回溯到[馈送数据设置](feed-settings-manage.md#feed-data-settings)中指定的最低值以上。 | 上一个文件： stock=0<br><br>新文件： stock=10 | 暂停现有广告、关键词或产品组后，它们将被重新激活，而不会丢失任何历史记录或质量分数。 当不存在广告、关键字或产品组时（例如，如果由于库存级别低于最低值而以前删除了这些广告、关键字或产品组），则会创建新广告、关键字或产品组。 |

>[!MORELIKETHIS]
>
>* [关于使用库存信息源自动进行广告管理](inventory-feeds-about.md)
