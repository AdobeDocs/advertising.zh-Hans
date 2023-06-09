---
title: 清单信息源何时创建或删除帐户组件？
description: 了解在发布库存信息源时创建和删除帐户组件的情况。
source-git-commit: f8d17ba787496917f4011f9dcbcb5587fe5c83cb
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# 清单信息源何时创建或删除帐户组件？

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （仅删除操作），以及 [!DNL Yandex] 仅限帐户*

通过模板传播库存信息源文件时，将按如下方式创建和删除帐户组件。

>[!NOTE]
>
>广告组中永远不会创建重复的广告。

| 方案 | 示例 | 操作 |
|----|----|----|
| 信息源数据包含在营销活动名称、广告组名称、关键字或产品组中使用的列的新值。 | 以前的文件：<br>Campaign=Hats<br>Campaign=手套<br><br>新文件：<br>Campaign=鞋子 | 如果广告网络上不存在新的促销活动、广告组、关键词或产品组，则会创建该营销活动、广告组、关键词或产品组。 |
| 馈送数据包含广告中使用的列的新值。 | 上一个文件：广告包含的价格=20<br><br>新文件：对于同一广告，价格为10 | 当广告副本用于 [!DNL Microsoft® Advertising] 扩展的文本广告， [!DNL Yahoo! Japan ads]，或 [!DNL Yandex] 广告发生更改，现有广告被删除并创建新广告。<br><br>为其他广告类型更改广告副本或将适用的列用于 [!DNL Google Ads] 广告参数({param1} 或 {param2})，则会更新现有广告。 |
| 自上次传播以来，营销活动、广告组、关键字或产品组的模板设置已更改。 | 以前的设置：Keyword=[关键词]<br><br>新设置： Keyword=&lt;color>[关键词] | 如果广告网络上不存在新的促销活动、广告组、关键词或产品组，则会创建该营销活动、广告组、关键词或产品组。 |
| 自上次传播以来，广告的模板设置发生了更改。 | 以前的设置：广告描述=&quot;购买 [类别] 现在。”<br><br>新设置：广告描述=&quot;购买 [品牌] 现在。” | 当广告副本用于 [!DNL Microsoft® Advertising] 扩展的文本广告， [!DNL Yahoo! Japan ads]，或 [!DNL Yandex] 广告发生更改，现有广告被删除并创建新广告。<br><br>当针对其他广告类型更改广告副本时，或者当更改反映用于单个广告的列中的更改时 [!DNL Google Ads] 广告参数({param1} 或 {param2})，则会更新现有广告。 |
| 新的馈送数据不包含现有营销活动或广告组的行。 | 不适用 | 现有营销活动和广告组保持不变。 |
| 新的馈送数据不包含现有广告组、广告、关键字或产品组的行。 | 不适用 | 现有的广告组、广告、关键词或产品组将保持不变，或者将暂停或删除，具体情况请参见 [馈送数据设置](feed-settings-manage.md#feed-data-settings). |
| 现有父产品组的新馈送数据不包含其现有子产品组的行。 | 不适用 | 现有的父产品组将保持原样或已被删除，根据 [馈送数据设置](feed-settings-manage.md#feed-data-settings). <b>注意：</b> 如果馈送数据设置配置为暂停缺少的行项目，则父产品组仍会被删除，因为您无法暂停产品组。 |
| 新的馈送数据包含广告组、广告、关键词或产品组的一行，该行以前的数据中为a)，但b)此后被忽略，并根据 [馈送数据设置](feed-settings-manage.md#feed-data-settings). | 不适用 | 重新激活现有的广告组、广告、关键词或产品组，而不会丢失任何历史记录或质量分数。 |
| 新的馈送数据包含广告组、广告、关键词或产品组的一行，该行以前的数据中为a)，但b)此后被忽略，并根据 [馈送数据设置](feed-settings-manage.md#feed-data-settings). | 不适用 | 将创建一个新的广告组、广告、关键字或产品组。 |
| 您已对“”禁用了营销活动或广告组级别选项[!UICONTROL Delete negative keywords when omitted from list].” | 负面关键字列表包括“coupe”和“sports car”。<br><br>广告组已包含负关键字“SUV”。 | 任何不在列表中的现有负关键字将保持原样。 |
| 您已为“ ”启用营销活动或广告组级别选项[!UICONTROL Delete negative keywords when omitted from list]“ ”和负关键字不存在于列表中。 | 负面关键字列表包括“coupe”和“sports car”。<br><br>广告组已包含负关键字“SUV”。 | 在馈送文件通过模板传播时，将删除之前使用该模板创建的任何未指定负关键字。 但是，使用其他方式创建的任何未指定的负关键字(例如，在普通批量处理工作表中， [!UICONTROL Campaigns] 视图或广告网络的广告编辑器中的视图将保持不变。 | | 已发布信息源文件的组件计划结束日期出现。 | 不适用 | 现有营销活动保持不变。 现有的广告组、广告和关键词将保持不变、暂停或删除，具体情况将根据 [馈送数据设置](feed-settings-manage.md#feed-data-settings). |
| 物料的库存水平下降到低于中指定的最小值。 [馈送数据设置](feed-settings-manage.md#feed-data-settings). | 上一个文件： stock=10<br><br>新文件： stock=0 | 现有营销活动保持不变。 现有的广告组、广告、关键词和产品组已暂停或删除，具体情况如下 [馈送数据设置](feed-settings-manage.md#feed-data-settings). |
| 物料的库存水平可回溯到早于以下日期指定的最小值： [馈送数据设置](feed-settings-manage.md#feed-data-settings). | 上一个文件： stock=0<br><br> 新文件： stock=10 | 暂停现有广告、关键词或产品组后，这些内容将重新激活，而不会丢失任何历史记录或质量分数。 当不存在广告、关键字或产品组时（例如，如果之前删除了广告、关键字或产品组，因为库存水平低于最低值），则会创建新广告、关键字或产品组。 |

>[!MORELIKETHIS]
>
>* [关于使用库存信息源自动化广告管理](inventory-feeds-about.md)
