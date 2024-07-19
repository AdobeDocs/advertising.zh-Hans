---
title: 转换信息源文件的文件要求
description: 参考转换信息源文件的要求。
exl-id: abc28394-3e00-447f-a04e-078fa9883a64
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# 转换信息源文件的文件要求

以下是源文件的文件格式、必需和可选数据字段、文件名和文件传输协议的要求。

## 文件格式

数据文件必须为纯文本(TXT)、逗号分隔值(CSV)或制表符分隔值(TSV)格式。 文件可能由标题行和数据行组成，这些行的值由制表符、逗号或其他字符（但不包括空格）分隔：

* **标题行：**（可选）文件的第一行是标题，它以特定顺序指定必填字段名称（或列名称），并以制表符或逗号分隔。 必需的列名称包括Adobe Advertising作为转化跟踪的转化量度。

* **数据行：**&#x200B;每个后续行包含的数据字段与标题的顺序相同，并以制表符或逗号分隔。 如果第一个记录不是标题，则每个数据行必须按指定顺序包括所有可能的字段。 所有ID和转化量度的值都必须是字母数字。

  如果一次或多次广告点击导致一次交易，则必须确定要归因于该交易的点击ID和跟踪ID。 由于每个交易都会报告一个唯一ID，因此您可以更新各个交易。

## 文件命名约定

文件名必须包含日期并且必须一致。 例如，如果使用格式YYYYMMDD.txt，则在2011年5月15日发送的文件必须命名为20110515.txt。

## 文件传输协议

使用端口22通过SFTP传输协议发送文件。 您需要提供公钥信息。  您的Adobe帐户团队或实施团队为您提供服务器位置以及系统传输文件所需的凭据。

>[!TIP]
>
>转化数据馈送每天处理多次。 请于当地时间午夜12:00后尽快上传每日馈送，以便Adobe Advertising能够处理您的数据，并在凌晨在报表UI中提供。

>[!MORELIKETHIS]
>
>* [使用EF ID的数据馈送的数据要求](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
>* [使用交易ID的数据馈送的数据要求](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
