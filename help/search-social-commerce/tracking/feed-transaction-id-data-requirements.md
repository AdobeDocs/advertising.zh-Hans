---
title: 使用交易ID的数据馈送的数据要求
description: 参考使用交易ID的数据馈送的数据要求。
exl-id: 67e1cadd-b607-465c-9db6-ca76d8ca84c5
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 使用交易ID的数据馈送的数据要求

以下是每种类型馈送文件所需的标题字段和相应的数据字段。

>[!NOTE]
>* 只要后续行中的数据遵循相同的顺序，标头就可以按任意顺序显示。 如果不包含标题，则数据行的顺序必须与每个馈送文件一致。
>* 馈送文件的每一行必须包含一个交易的数据，并且交易必须使用交易ID进行标识。

| 标题字段/列名称 | 类型 | 描述 |
| ---- | ---- | ---- |
| 交易ID (ev_transid) | 区分大小写的字符串 | 与交易关联的广告商生成的标识符。 由于Adobe Advertising转化跟踪标记用于事务的在线部分，因此它必须与Adobe Advertising为事务的早期部分提供的事务ID (ev_transid)相同。 这意味着交易的在线部分的转换标记必须包含唯一交易ID的属性。<br><br>**注意：** Adobe Advertising使用ID来查找旧事务数据，并根据商定的插入模式对其进行更新（例如，替换现有数据或使用新数据扩充现有数据）。 |
| 交易日期 | 日期时间 | 交易的日期。 每个事务的格式必须一致。 |
| 特定于客户端的转换 | 字符串 | 正在跟踪的转化（如交易类型或金额）。 在启动信息源之前，与Adobe Advertising实施团队讨论要包含的转化。 |

## 示例

以下示例文件包含两个交易属性（Product和Revenue）的数据。

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
