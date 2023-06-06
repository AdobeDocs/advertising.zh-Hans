---
title: 以下项的必需批量处理工作表数据 [!DNL Baidu] 帐户
description: 引用批量处理工作表中的必填标题字段和数据字段 [!DNL Baidu] 帐户。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1882'
ht-degree: 0%

---

# 附录 — 必需的批量工作表数据 [!DNL Baidu] 帐户

创建和更新 [!DNL Baidu] 批量处理营销活动数据，您可以使用专门格式化的搜索、社交和商务批量工作表文件 [!DNL Baidu] 帐户。 您可以a) [为现有帐户生成批量工作表文件](../bulksheet-download.md) (b)手动创建它们（请参见）[支持的批量工作表文件格式](bulksheet-file-formats.md)”以了解有关支持的文件格式的一般信息)。

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Campaign Budget,Location,Excluded IPs (Baidu), Ad Serving (Baidu),Ad Group Name,Max CPC,Keyword,Match Type,Ad Title,Description Line 1,Description Line 2,Display URL,Base URL,Destination URL,Custom URL Param,Campaign Status,Ad Group Status,Keyword Status,Ad Status,Location Status,[Advertiser-specific Label Classification],Campaign ID,Ad Group ID,Keyword ID,Ad ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## 可用数据字段

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| 字段 | Campaign | 广告组 | 关键词 | 文本广告 | 位置目标 | 描述 |
|----|----|----|----|----|----|----|
| [!UICONTROL Platform] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （包含在生成的批量工作表中，以供参考）广告平台。 除非每行都包含实体的AMO ID，否则必需。 |
| [!UICONTROL Acct Name] | 必需/可选 | R/O | 必需/可选 | 必需/可选 | 必需/可选 | （包含在生成的批量工作表中，以供参考）广告平台。 除非每行都包含实体的AMO ID，否则必需。 |
| [!UICONTROL Campaign Name] | 必需 | 必需 | 必需 | 必需 | 必需 | 标识帐户促销活动的唯一名称。 |
| [!UICONTROL Campaign Budget] | 必需：创建<br>可选：编辑或删除 | 不适用 | 不适用 | 不适用 | 不适用 | 竞选活动的每日支出上限，无论是否带有货币符号和标点。 此值将覆盖但不能超过帐户预算。 |
| [!UICONTROL Location] | 不适用 | 不适用 | 不适用 | 不适用 | 必需 | 为营销活动放置广告的地理位置。 要排除位置，请用减号(`-`)。 如果不输入促销活动的特定值，则会定位所有位置。 |
| [!UICONTROL Excluded IPs (Baidu)] | 可选 | 不适用 | 不适用 | 不适用 | 不适用 | 不应显示广告的网站的IP地址。 用逗号分隔多个值。 |
| [!UICONTROL Ad Serving (Baidu)] | 可选 | 不适用 | 不适用 | 不适用 | 不适用 | 在广告组中相互关联投放活动广告的频率：<ul><li><i>旋转</i> （新促销活动的默认值）：您的每个广告进入广告拍卖的次数大致相同，从而使Search、Social和Commerce不仅可以根据点进率而且对广告转化情况进行评分。</li><li><i>优化：</i> 广告网络青睐高点进率和高质量分数的广告。 这些广告进入广告拍卖的频率更高，随着时间的推移，人们更青睐单个广告。 此结果可能与您的业务和优化目标不一致。</li></ul> |
| [!UICONTROL Ad Group Name] | 不适用 | 必需 | 必需 | 必需 | 不适用 | 标识广告组的唯一名称。 |
| [!UICONTROL Max CPC] | 不适用 | O | O | 不适用 | 不适用 | 最大每次点击成本(CPC)，这是您在搜索网络上为广告点击支付的最高金额，无论是否带有货币符号和标点。 您可以设置广告组和关键字的值。 新关键字的默认值继承自广告组级别。 |
| [!UICONTROL Keyword] | 可选/不适用 | 可选/不适用 | 必需 | 不适用 | 不适用 | 关键词字符串。<br><br>要在广告组或营销策划级别排除关键词，请设置 [!UICONTROL Match Type] 到 [!UICONTROL Negative]. 如果行包含广告组名称，则会为广告组排除关键字。 如果行不包含广告组名称，则该关键字将排除在整个营销活动中。<br><br><b>注意：</b>更改Baidu关键字会删除现有关键字，并创建一个具有新关键字ID的新关键字。 但是，您可以更改匹配类型，而无需删除现有关键字。 |
| [!UICONTROL Match Type] | 可选/不适用 | 可选/不适用 | 可选：创建<br>必需/可选：编辑或删除 | 不适用 | 不适用 | 关键字的关键字匹配选项： <i>[!UICONTROL Broad]</i>， <i>[!UICONTROL Exact]</i>， <i>[!UICONTROL Phrase]</i>， <i>[!UICONTROL Negative Broad]</i>，或 <i>[!UICONTROL Negative Exact]</i>. 在营销活动级别或广告组级别定义负关键字。<br><br>对于新关键字，缺省值为 <i>[!UICONTROL Broad]</i>. 只有在编辑具有多个匹配类型的关键字时，才需要匹配类型或关键字ID的值。<br><br><b>注意：</b>您可以更改匹配类型 [!DNL Baidu] 关键字，而不删除现有关键字。 |
| [!UICONTROL Ad Title] | 不适用 | 不适用 | 不适用 | 必需 | 不适用 | 广告的标题。 最大长度为14个双字节字符或28个单字节字符。<br><br><b>注意：</b> 更改广告副本会删除现有广告，并创建具有相同属性的新广告。 |
| [!UICONTROL Description Line 1] | 不适用 | 不适用 | 不适用 | 必需 | 不适用 | 广告正文的第一行。 最小长度为4个双字节字符或8个单字节字符，最大长度为20个双字节字符或40个单字节字符。<br><br><b>注意：</b> 更改广告副本会删除现有广告，并创建具有相同属性的新广告。 |
| [!UICONTROL Description Line 2] | 不适用 | 不适用 | 不适用 | 必需 | 不适用 | 广告正文的第二行。 最小长度为4个双字节字符或8个单字节字符，最大长度为20个双字节字符或40个单字节字符。<br><br><b>注意：</b> 更改广告副本会删除现有广告，并创建具有相同属性的新广告。 |
| [!UICONTROL Display URL] | 不适用 | 不适用 | 不适用 | 必需 | 不适用 | 广告中显示的URL。 最大长度为35个单字节字符。 |
| [!UICONTROL Base URL] | 不适用 | 不适用 | 可选 | 必需 | 不适用 | 最终用户单击广告时获得的登陆页面URL，包括为营销活动或帐户配置的任何附加参数。<br><br>关键词级别的基本/最终URL会覆盖广告级别和更高级别的URL。 |
| [!UICONTROL Destination URL] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （出于信息目的包含在生成的批量工作表中；未发布到广告网络）对于具有目标URL的帐户，此值是将广告链接到广告商网站上的基本URL/登陆页面的URL（有时通过另一个跟踪点击的网站，然后将用户重定向到登陆页面）。 它包括为Search、Social和Commerce营销活动或帐户配置的任何附加参数。 如果您生成了跟踪URL，则此值基于帐户设置和促销活动设置中的跟踪参数。 如果附加了特定于广告网络的参数，则这些参数可能会被等效的Search、Social和Commerce参数替换。<br><br>对于具有最终URL的帐户，此列显示的值与 [!UICONTROL Base URL/Final URL column]. |
| [!UICONTROL Custom URL Param] | 不适用 | 不适用 | 可选 | 可选 | 不适用 | 要替换的数据 `{custom_code}` 动态变量（当变量包含在搜索帐户或促销活动设置的跟踪参数中时）。 要在跟踪URL中插入自定义值，请使用 [!UICONTROL Generate Tracking URLs] 选项。 |
| [!UICONTROL Campaign Status] | 可选：创建或编辑<br>必需：删除 | 不适用 | 不适用 | 不适用 | 不适用 | 营销活动的显示状态： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Deleted]</i> （仅限现有营销活动）。 新营销活动的默认值为 <i>[!UICONTROL Active]</i>. 要删除活动或暂停的营销活动，请输入值»[!UICONTROL Deleted]“。 |
| [!UICONTROL Ad Group Status] | 不适用 | 可选：创建或编辑<br>必需：删除 | 不适用 | 不适用 | 不适用 | 广告组的显示状态： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Deleted]</i> （仅限现有广告组）。 新广告组的默认值为 <i>[!UICONTROL Active]</i>. 要删除活动或暂停的广告组，请输入值»[!UICONTROL Deleted]“。 |
| [!UICONTROL Keyword Status] | 不适用 | 不适用 | 可选：创建或编辑<br>必需：删除 | 不适用 | 不适用 | 关键字的显示状态： <i>[!UICONTROL Active]</i>， <i>[!UICONTROL Deleted]</i> （仅限现有关键词）， <i>[!UICONTROL Inactive]</i> （不可编辑）， <i>[!UICONTROL Paused]</i> （仅限现有关键词），或 <i>[!UICONTROL Pending]</i>（不可编辑）。 新关键字的默认值为 <i>[!UICONTROL Active]</i>.<br><br>要删除关键字，请输入值 <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | 不适用 | 不适用 | 不适用 | 可选：创建或编辑<br>必需：删除 | 不适用 | 广告的显示状态： <i>[!UICONTROL Active]</i>（新广告的默认值）， <i>[!UICONTROL Deleted]</i> （仅限现有广告）、 <i>[!UICONTROL Disapproved]</i> （不可编辑）， <i>[!UICONTROL Inactive]</i> （不可编辑）， <i>[!UICONTROL Paused]</i>，或 <i>[!UICONTROL Pending (not editable)]</i>.<br><br>要删除广告，请输入值 <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Location Status] | 不适用 | 不适用 | 不适用 | 不适用 | 可选：创建或编辑<br>必需：删除 | 位置目标的状态： <i>[!UICONTROL Active]</i> 或 <i>[!UICONTROL Deleted] （仅限现有位置）。 新位置的默认值是 <i>[!UICONTROL Active]. 要删除活动位置，请输入值 <i>[!UICONTROL Deleted]. |
| \[广告商特定的标签分类\] | 可选 | 可选 | 可选 | 可选 | 不适用 | （以特定于广告商的标签分类命名，例如称为颜色的标签分类的“颜色”）与实体关联的指定分类的值。 每个实体的每个分类只能包含一个值（例如，促销活动A的“颜色”标签分类为“红色”）。 最大长度为100个字符，该值可以包含ASCII和非ASCII字符。<br><br>标签分类及其标签值将应用于所有子组件；以后添加的新组件会自动与标签关联。 <br><br>分类名称和分类值不区分大小写。 |
| [!UICONTROL Constraints] | 可选 | 可选 | 可选 | 不适用 | 不适用 | 分配给图元的约束。 每个图元只能分配一个约束。<br><br>约束由子实体继承，因此，除非要覆盖继承的值，否则无需为子实体输入值。 |
| [!UICONTROL Campaign ID] | 不适用：创建<br>必需/可选：编辑和删除 | 可选 | 可选 | 可选 | 不适用 | 标识现有营销活动的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅在更改促销活动名称时需要，除非行包含促销活动的AMO ID。 |
| [!UICONTROL Ad Group ID] | 不适用 | 不适用：创建<br>必需/可选：编辑和删除 | 可选 | 可选 | 不适用 | 标识现有广告组的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅在更改广告组名称时需要，除非行包含广告组的AMO ID。 |
| [!UICONTROL Keyword ID] | 不适用 | 不适用 | 不适用：创建<br>必需/可选：编辑和删除 | 不适用 | 不适用 | 标识现有关键字的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅当更改关键词名称时才需要，除非行包含a)足够的属性列来标识关键词或b) AMO ID。 |
| [!UICONTROL Ad ID] | 不适用 | 不适用 | 不适用 | 不适用：创建<br>必需/可选：编辑和删除 | 不适用 | 标识现有关键字的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅当更改关键词名称时才需要，除非行包含a)足够的属性列来标识关键词或b) AMO ID。 |
| [!UICONTROL AMO ID] | 不适用：创建<br>可选：编辑和删除 | 不适用：创建<br>可选：编辑和删除 | 不适用：创建<br>可选：编辑和删除 | 不适用：创建<br>可选：编辑和删除 | 不适用：创建<br>可选：编辑和删除 | （在生成的批量处理工作表中） [!DNL Adobe]已同步实体生成的唯一标识符。 对于响应式搜索广告，编辑或删除广告时需要AMO ID，除非您包含 [!UICONTROL Ad ID]. 要使用AMO ID编辑所有其他实体类型的数据，需要使用AMO ID来编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce会使用该值来确定要编辑的正确身份，但不会将ID发布到广告网络。 |
| [!UICONTROL EF Error Message] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （出于提供信息的目的，包含在生成的批量工作表中）用于显示来自搜索、社交和商务中与行中的数据有关的错误消息的占位符；错误消息包含在 [!UICONTROL EF Errors] 文件。 此值未发布到广告网络。 |
| [!UICONTROL SE Error Message] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （出于信息目的包含在生成的批量处理工作表中）用于显示来自广告网络的关于行中数据的错误消息的占位符；错误消息包含在 [!UICONTROL SE Errors] 文件。 此值未发布到广告网络。 |

<table style="table-layout:auto">

[^1]：Excel在打开文件时将大数转换为科学记号(如2.12E+09 for 2115585666)。 要查看标准表示法中的数字，请选择列中的任意单元格，然后单击公式栏中的。

>[!MORELIKETHIS]
>
>* [附录 — 批量处理工作表错误](../bulksheet-errors.md)
>* [可在批量工作表中执行的操作](bulksheet-operations.md)
>* [支持的批量工作表文件格式](bulksheet-file-formats.md)
>* [下载/创建批量处理工作表文件](../bulksheet-download.md)
>* [的点击跟踪格式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [上传批量处理工作表文件或更正的错误文件](../bulksheet-upload.md)

