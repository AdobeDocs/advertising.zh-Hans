---
title: 使用EF ID的数据馈送的数据要求
description: 参考使用EF ID的数据馈送的数据要求。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# 使用EF ID的数据馈送的数据要求

以下是每种类型馈送文件所需的标题字段和相应的数据字段。

>[!NOTE]
>* 标头可以按任意顺序显示，只要后续行中的数据遵循相同的顺序。 如果不包含标题，则数据行的顺序必须与每个馈送文件一致。
>* 馈送文件的每一行必须包含一个交易的数据，并且交易必须由Adobe广告生成的ef_id （令牌）标识。


| 标题字段/列名称 | 类型 | 描述 |
| ---- | ---- | ---- |
| EF ID | 区分大小写的字符串 | 您在点击事务处理时捕获的ef_id （令牌），包括冲浪者ID、点击时间和网络类型。 请勿更改该值。 |
| 交易ID | 区分大小写的字符串 | （可选，但推荐）广告商生成的交易ID。 最佳做法是为每个事务包含此属性，即使重定向时使用ef_id跟踪事务也是如此。 |
| 交易日期 | 日期时间 | 交易记录的日期。 每个事务的格式必须一致。 |
| 特定于客户端的转换 | 字符串 | 正在跟踪的转化（如交易记录类型或金额）。 在启动信息源之前，与Adobe广告实施团队讨论要包含的转化。 |

## 示例

以下示例文件包含两个交易属性（Product和Revenue）的数据。

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [转换信息源文件的文件要求](feed-file-requirements.md)
>* [使用EF ID馈送的转化跟踪](/help/search-social-commerce/tracking/feed-efid.md)

