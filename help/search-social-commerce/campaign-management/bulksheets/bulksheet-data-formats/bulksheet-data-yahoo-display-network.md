---
title: ' [!DNL Yahoo! Display Network] 帐户的批量工作表数据'
description: 引用 [!DNL Yahoo! Display Network] 帐户的已下载批量处理工作表中的标题字段和数据字段。
exl-id: 8d938009-6edc-4420-8863-21ed241616f8
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# 附录 — [!DNL Yahoo! Display Network]帐户的批量工作表数据

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

您可以批量下载[!DNL Yahoo! Display Network]帐户的数据，但无法将批量工作表上传或发布到广告网络。

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

The following example shows data in comma-delimited values. If you're using tab-separated values, then the data looks different.

Platform,Acct Name,Campaign Name,Ad Group Name,Ad Name, Ad Title,Description Line 1,Description Line 2,Base URL/Final URL,Destination URL,[Advertiser-specific Label Classification],Bid Rules,Constraints,Campaign Status,Ad Group Status,Ad Status,Campaign ID,Ad Group ID,Ad ID,AMO ID,EF Error Message

-->

## 可用的数据字段

| 字段 | 营销活动 | 广告组 | 广告 | 描述 |
|----|----|----|----|----|
| [!UICONTROL Platform] | 不适用 | 不适用 | 不适用 | （包含在生成的批量工作表中，以供参考）广告平台。 |
| [!UICONTROL Acct  Name] | 如果包含 | 如果包含 | 如果包含 | 标识广告网络帐户的唯一名称。 |
| [!UICONTROL Campaign Name] | 如果包含 | 如果包含 | 如果包含 | 为帐户标识营销活动的唯一名称。 |
| [!UICONTROL Ad Group Name] | 不适用 | 如果包含 | 如果包含 | 标识广告组的唯一名称。 |
| [!UICONTROL Ad Name] | 不适用 | 不适用 | 如果包含 | 在广告组中标识广告的唯一名称。 最大长度为50个字符。 |
| [!UICONTROL Ad Title] | 不适用 | 不适用 | 如果包含 | 广告的标题。 |
| [!UICONTROL Description Line 1] | 不适用 | 不适用 | 如果包含 | 广告正文的第一行。 |
| [!UICONTROL Description Line 2] | 不适用 | 不适用 | 如果包含 | 广告正文的第二行。 |
| [!UICONTROL Base URL/Final URL] | 不适用 | 不适用 | 如果包含 | 最终用户单击您的广告时获得的登陆页面URL，包括为营销活动或帐户配置的任何附加参数。 关键字级别的基本/最终URL会覆盖广告级别和更高级别的URL。 |
| [!UICONTROL Destination URL] | 不适用 | 不适用 | 不适用 | （出于信息目的包含在生成的批量工作表中；未发布到广告网络）对于具有目标URL的帐户，此值是将广告链接到广告商网站上的基本URL/登陆页面的URL（有时通过另一个跟踪点击的网站，然后将用户重定向到登陆页面）。 它包括为Search、Social和Commerce营销活动或帐户配置的任何附加参数。 如果您生成了跟踪URL，则此值基于您的帐户设置和促销活动设置中的跟踪参数。 如果您附加了特定于广告网络的参数，则这些参数可能会被等效的搜索、社交和Commerce参数替换。 |
| \[广告商特定的标签分类\] | 如果包含 | 如果包含 | 如果包含 | （以特定于广告商的标签分类命名，例如名为“颜色”的标签分类的“颜色”）与实体关联的指定分类的值。 |
| [!UICONTROL Constraints] | 如果包含 | 如果包含 | 不适用 | 分配给图元的约束。 |
| [!UICONTROL Campaign Status] | 如果包含 | 不适用 | 不适用 | 营销活动的显示状态： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Ad Group Status] | 不适用 | 如果包含 | 不适用 | 广告组的显示状态： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Keyword Status] | 不适用 | 不适用 | 如果包含 | 关键字的显示状态： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i> （仅限现有关键字）。 |
| [!UICONTROL Campaign ID] | 如果包含 | 如果包含 | 如果包含 | 标识现有营销活动的唯一ID。 |
| [!UICONTROL Ad Group ID] | 不适用 | 如果包含 | 如果包含 | 标识现有广告组的唯一ID。 |
| [!UICONTROL Keyword ID] | 不适用 | 不适用 | 如果包含 | 标识现有关键字的唯一ID。 |
| [!UICONTROL AMO ID] | 不适用 | 不适用 | 不适用 | （在生成的批量工作表中）同步实体的Adobe生成的唯一标识符。 |
| [!UICONTROL EF Error Message] | 不适用 | 不适用 | 不适用 | （出于提供信息的目的，包含在生成的批量处理工作表中）用于显示来自搜索、社交和Commerce中有关行中数据的错误消息的占位符；错误消息包含在[!UICONTROL EF Errors]文件中。 |

>[!MORELIKETHIS]
>
>* [下载/创建批量处理工作表文件](../bulksheet-download.md)
