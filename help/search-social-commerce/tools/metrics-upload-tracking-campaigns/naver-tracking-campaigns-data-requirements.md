---
title: ' [!DNL Naver] 仅跟踪帐户的流量和转化量度的数据要求'
description: 引用 [!DNL Naver] 仅跟踪帐户的数据上载要求。
exl-id: cc8ee5de-2bf2-48fd-9fa7-28421aed673f
feature: Search Tools
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# [!DNL Naver]仅跟踪帐户的量度数据要求

以下是仅跟踪帐户的[!DNL Naver]流量和转化量度的数据要求。

数据文件必须为TSV、CSV或TXT格式。

以下标头字段为必需字段，可选。 每个数据行必须至少包含一个指标字段的每日汇总值。

| 标题字段/列名称 | 类型 | 描述 |
| ---- | ---- | ---- |
| 期间 | 日期时间 | 数据应用的日期，格式为`YYYY.MM.DD.` （如`2019.11.15.`，在天后有一个句点）。 |
| 营销活动 | 区分大小写的字符串 | 营销活动名称。 |
| 广告组（作为一个词） | 区分大小写的字符串 | 广告组名称。 |
| 关键词 | 区分大小写的字符串 | （关键词广告）生成广告的关键字。 |
| [指标] | 整数 | （可选）度量度量为&rbrack;的&lbrack;数。</br><br>标准量度包括展示次数、成本和点击次数。 您可以从广告网络包含任何其他所需的量度。 将每个量度包含在一个单独的列中。<br><br><b>注释：</b><ul><li>“成本”的列标题必须为“成本(KRW)”。</li><li>要包含品牌广告的成本(KRW)，请在广告组级别手动将每月固定成本除以日。</li><li>从标准量度值中删除所有逗号。 例如，使用1000而不是1,000。</li><li>对于null值，使用0。</li></ul> |

>[!MORELIKETHIS]
>
>* [实施 [!DNL Naver] 仅跟踪帐户](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [附录 —  [!DNL Naver] 帐户](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)的必需批量工作表数据
>* [上传 [!DNL Naver] 仅跟踪帐户的流量和转化量度](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
