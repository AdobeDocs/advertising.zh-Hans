---
title: 使用交易ID的数据馈送的数据要求
description: 参考使用交易ID的数据馈送的数据要求。
exl-id: 055b1417-3185-4081-83f0-9f4798058c04
feature: Search Tracking
TQID: https://experienceleague.adobe.com/TONScPVaJyxsORRD-sOrYXwEzO9rsa6ERPUo8oSRono
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 0%

---

# 使用交易ID的数据馈送的数据要求

以下是每种类型馈送文件所需的标题字段和相应的数据字段。

>[!NOTE]
>* 只要后续行中的数据遵循相同的顺序，标头就可以按任意顺序显示。 如果不包含标题，则数据行的顺序必须与每个馈送文件一致。
>* 馈送文件的每一行必须包含一个交易的数据，并且交易必须使用交易ID进行标识。

| 标题字段/列名称 | 类型 | 描述 |
| ---- | ---- | ---- |
| 交易ID (ev_transid) | 区分大小写的字符串 | 与交易关联的广告商生成的标识符。 由于Adobe Advertising转化跟踪标记用于交易的在线部分，因此它必须与Adobe Advertising为交易早期部分提供的交易ID (ev_transid)相同。 这意味着交易的在线部分的转换标记必须包含唯一交易ID的转换量度。<br><br>**注意：** Adobe Advertising使用该ID来查找旧的交易数据，并根据商定的插入模式对其进行更新（例如，替换现有数据或使用新数据扩充现有数据）。 |
| 交易日期 | 日期时间 | 交易的日期。 每个事务的格式必须一致。 |
| 特定于客户端的转换 | 字符串 | 正在跟踪的转化（如交易类型或金额）。 在开始馈送之前，讨论要包含在Adobe Advertising实施团队中的转化。 |

## 示例

以下示例文件包含两个转化量度（“产品”和“收入”）的数据。

```
Transaction ID,Transaction Date,Product,Revenue
12345,2010-02-17,Coffee,15.00
12346,2010-02-17,Tea,42.00
12347,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [转换信息源文件的文件要求](feed-file-requirements.md)
>* [使用交易ID馈送进行转化跟踪](/help/search-social-commerce/tracking/feed-transaction-id.md)
