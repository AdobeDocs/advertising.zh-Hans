---
title: 关于 [!UICONTROL CCPA Opt-out-of-Sale] 区段和报表
description: 了解如何创建区段以跟踪CCPA选择退出销售请求中的ID，以及如何检索ID报表。
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# 关于 [!UICONTROL CCPA Opt-out-of-Sale] 区段和报表

您可以根据《加州消费者隐私法案》(CCPA)，通过以下方式跟踪您网站上消费者选择退出销售请求的用户ID [创建和实施CCPA选择退出销售区段](ccpa-opt-out-segment-create.md). 用户无限期地停留在CCPA选择退出销售区段中。

实施区段像素标记后，Adobe Advertising即开始代表广告商收集ID池。

## 消费者选择退出销售报表

Adobe Advertising会每月生成客户为帐户的选择退出销售请求提交的ID报表。 数据合并使用在DSP中创建的CCPA选择退出销售区段捕获的请求以及通过Privacy ServiceAPI提交的任何提交。  在上个月的每月第一天生成报告。 例如，6月的每月用户列表可在7月1日发布。

每个报表都以制表符分隔的文本文件形式提供，并压缩为GZIP格式。 在CCPA选择退出销售区段中捕获的用户ID由区段和广告商标识。

您可以 [检索指向每月报表的链接](ccpa-opt-out-segment-report-retrieve.md) 之前三个月通过DSP或使用DSP创建的客户群 [!DNL Trafficking API]. 每个链接的有效期为七天，但每当客户尝试检索一个链接时，都会刷新。

>[!MORELIKETHIS]
>
>* [Adobe Advertising对《加州消费者隐私法案》的支持：消费者选择退出支持](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [创建和实施 [!UICONTROL CCPA Opt-Out-of-Sale] 区段](ccpa-opt-out-segment-create.md)
>* [检索消费者选择退出销售报表](ccpa-opt-out-segment-report-retrieve.md)
>* [关于受众管理](audience-about.md)
