---
title: 支持的批量处理工作表文件格式
description: 请参阅批量处理工作表的一般文件要求。
exl-id: b14aaf11-e2e9-4f7c-b6bc-831f668b93a6
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# 支持的批量处理工作表文件格式

## 文件格式

您可以以下列任何格式下载、上传和发布受支持的广告网络的批量工作表文件：

* CSV（逗号分隔值）
* TSV（制表符分隔的值）
* TXT（Unicode文本），用逗号或制表符分隔
* ZIP（压缩）文件，其中包含以逗号或制表符分隔的CSV格式、TSV格式或TXT格式的文件

创建/下载批量处理工作表时，它会以指定的文件格式创建，并且文件中包含所有相关数据。 使用以下信息编辑文件中的数据或手动创建自己的批量处理工作表。

## 批量处理工作表的基本内容

批量工作表文件的第一个记录（行）包含一组特定的列名称，统称为 <i>标题</i>. 标题中的列名称以指定的顺序排列，对应于后续数据记录中的每个字段。 标头中所需的列名称因广告网络而异。

每个后续记录（行）都包含数据，其中字段包含标题中每列的值（或没有值）。

## 最大文件大小

批量工作表文件最大可达2.5 GB，约为250万行。

>[!NOTE]
>
>在为多个营销活动生成批量处理工作表时，如果组合的数据包含超过500,000行，则数据会按营销活动拆分为两个或多个文件，名为 `<bulksheet name>_1.tsv`， `<bulksheet name>_2.tsv`，等等。

## 不同文件类型的格式要求

由制表符和逗号分隔的数据字段需要不同的格式。

### 以制表符分隔的TSV文件和TXT文件

以制表符分隔的TSV文件和TXT文件中的数据字段必须采用如下格式：

* 每条记录中的字段用制表符分隔。 要忽略字段的值，请仅使用制表符。

  示例： `Cruises<TAB>5000<TAB>Caribbean<TAB><TAB><TAB>`

* 字段不能包含嵌入的制表符字符。

### 以逗号分隔的CSV文件和TXT文件

CSV文件和TXT文件中以逗号分隔的数据字段必须采用如下格式：

* 记录中的字段以逗号分隔。 要忽略字段的值，请仅使用逗号。

  示例： `Cruises,5000,Caribbean,,,`

* 任何字段都可以选择用双引号(`""`)。

  示例：  `"Cruises","5000","Caribbean",`

* 包含嵌入逗号的字段必须用双引号(`""`)。

  示例： `Cruises,5000,Caribbean,"Luxurious, spacious cabins",`

* 带有嵌入双引号的字段必须用双引号(`""`)。

  示例： `Cruises,5000,Caribbean,"Customers say ""We wish we could stay forever."",`

* 带前导或尾随空格的字段必须用双引号(`""`)。

  示例： `Cruises,5000,Caribbean,"  Come see what we mean.  ",`

>[!MORELIKETHIS]
>
>* [关于使用批量处理工作表管理营销活动数据](../bulksheet-about.md)
>* [可在批量处理工作表中执行的操作](bulksheet-operations.md)
>* [附录 — 批量处理工作表错误](../bulksheet-errors.md)
>* [下载/创建批量处理工作表文件](../bulksheet-download.md)
