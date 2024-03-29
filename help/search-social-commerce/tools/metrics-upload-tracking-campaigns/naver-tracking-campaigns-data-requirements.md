---
title: 流量和转化量度的数据要求 [!DNL Naver] 仅跟踪帐户
description: 参考的数据上传要求 [!DNL Naver] 仅跟踪帐户。
exl-id: 6f79730b-f8d6-4a7f-9d31-f42fe63e6b5d
feature: Search Tools
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# 的量度数据要求 [!DNL Naver] 仅跟踪帐户

以下是的数据要求 [!DNL Naver] 仅跟踪帐户的流量和转化量度。

数据文件必须为TSV、CSV或TXT格式。

以下标头字段为必需字段，可选。 每个数据行必须至少包含一个指标字段的每日汇总值。

| 标题字段/列名称 | 类型 | 描述 |
| ---- | ---- | ---- |
| 期间 | 日期时间 | 数据适用的日期，格式为 `YYYY.MM.DD.` (例如 `2019.11.15.`，在天后有一个时间段)。 |
| 营销活动 | 区分大小写的字符串 | 营销活动名称。 |
| 广告组（作为一个词） | 区分大小写的字符串 | 广告组名称。 |
| 关键词 | 区分大小写的字符串 | （关键词广告）生成广告的关键字。 |
| [量度] | 整数 | （可选）的数量 [无论量度测量什么].</br><br>标准量度包括展示次数、成本和点击次数。 您可以从广告网络包含任何其他所需的量度。 将每个量度包含在一个单独的列中。<br><br><b>注释：</b><ul><li>“成本”的列标题必须为“成本(KRW)”。</li><li>要包含品牌广告的成本(KRW)，请在广告组级别手动将每月固定成本除以日。</li><li>从标准量度值中删除所有逗号。 例如，使用1000而不是1,000。</li><li>对于null值，使用0。</li></ul> |

>[!MORELIKETHIS]
>
>* [实施 [!DNL Naver] 仅跟踪帐户](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [附录 — 的必需批量处理工作表数据 [!DNL Naver] 帐户](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [上传流量和转化量度，用于 [!DNL Naver] 仅跟踪帐户](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
