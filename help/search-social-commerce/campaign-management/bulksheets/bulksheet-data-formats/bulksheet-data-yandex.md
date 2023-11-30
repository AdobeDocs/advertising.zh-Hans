---
title: 以下项的必需批量处理工作表数据 [!DNL Yandex] 帐户
description: 引用批量处理工作表中的必填标题字段和数据字段 [!DNL Yandex] 帐户。
exl-id: bf5a22dd-75c2-486d-85fd-e042bdb87de3
feature: Search Bulksheets
source-git-commit: e15cc54f09f905ee4d3b448d7e766c1513f12afb
workflow-type: tm+mt
source-wordcount: '1921'
ht-degree: 0%

---

# 附录 — 的必需批量处理工作表数据 [!DNL Yandex] 帐户

创建和更新 [!DNL Yandex] 批量处理营销活动数据，您可以使用专门针对以下内容格式化的搜索、社交和商务批量工作表文件 [!DNL Yandex] 帐户。 您可以a) [生成现有帐户的批量工作表文件](../bulksheet-download.md) （或b）手动创建它们(请参阅&quot;[支持的批量处理工作表文件格式](bulksheet-file-formats.md)»以了解支持的文件格式的一般信息)。

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Campaign Start Date,Campaign Budget,Delivery Method,Ad Group Name,Ad Title,Ad Description,Base URL,Destination URL,SiteLink Title,SiteLink Base URL,SiteLink Destination URL,Keyword,Max CPC,Match Type,Search Network Status,Content Network Status,Negative Keywords (Yandex),Param1 (Yandex),Param2 (Yandex),Campaign Status,Ad Group Status,Ad Status,Keyword Status,SiteLink Status,Campaign ID,Ad Group ID, Ad ID,Keyword ID,AMO ID, [Advertiser-specific Label Classification],Constraints,EF Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## 可用的数据字段

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

>[!TIP]
>
>下表是宽的。 如有必要，请使用表格底部的滚动条查看全部内容。 您还可以选择通过单击临时隐藏目录或右窗格 ![隐藏左窗格](/help/search-social-commerce/assets/hide-left-pane.png "隐藏左窗格") 左窗格顶部或 ![隐藏右侧窗格](/help/search-social-commerce/assets/hide-right-pane.png "隐藏右侧窗格") 在右窗格的顶部。

| 字段 | 营销活动 | 广告组 | 关键词 | 文本广告 | 站点链接 | 描述 |
|----|----|-----|-----|----|----|----|
| [!UICONTROL Platform] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （包含在生成的批量工作表中，以供参考）广告平台。 除非每行都包含实体的AMO ID，否则此为必填字段。 |
| [!UICONTROL Acct Name] | 必需/可选 | 必需/可选 | 必需/可选 | 必需/可选 | 必需/可选 | （包含在生成的批量工作表中，以供参考）广告平台。 除非每行都包含实体的AMO ID，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 | 必填 | 必填 | 必填 | 必填 | 为帐户标识营销活动的唯一名称。 |
| [!UICONTROL Campaign Start Date] | 必需：创建<br>可选：编辑或删除 | 不适用 | 不适用 | 不适用 | 不适用 | 营销活动可能进行竞价的第一个日期，以广告商所在的时区为单位并采用以下格式之一： m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 新营销活动的默认日期为当天。 |
| [!UICONTROL Campaign Budget] | 必需：创建<br>可选：编辑或删除 | 不适用 | 不适用 | 不适用 | 不适用 | 竞选活动的终生支出限制，无论是否带有货币符号和标点。 |
| [!UICONTROL Delivery Method] | 必需：创建<br>可选：编辑或删除 | 不适用 | 不适用 | 不适用 | 不适用 | 每天显示促销活动广告的速度：<ul><li><i>[!UICONTROL Standard (Distributed)]</i> （新营销活动的默认）：将广告展示次数分散到一整天中。</li><li><i>[!UICONTROL Accelerated]：</i> 在达到预算之前，尽可能多地显示广告。 因此，您的广告可能不会在当天晚些时候显示。</li></ul> |
| [!UICONTROL Ad Group Name] | 不适用 | 必填 | 必填 | 必填 | 不适用 | 广告组。 |
| [!UICONTROL Ad Title] | 不适用 | 不适用 | 不适用 | 必填 | 不适用 | 横幅（广告）的标题。 最大长度为33个字符，单个单词不能包含超过23个字符。<br><br><b>注意：</b> 更改广告副本将删除现有广告并创建新广告。 |
| [!UICONTROL Ad Description] | 不适用 | 不适用 | 不适用 | 必填 | 不适用 | 横幅（广告）的正文。 最大长度为75个字符，单个单词不能超过22个字符。<br><br><b>注意：</b> 更改广告副本将删除现有广告并创建新广告。 |
| [!UICONTROL Base URL] | 不适用 | 不适用 | 可选 | 必填 | 不适用 | 最终用户单击您的广告时获得的登陆页面URL，包括为营销活动或帐户配置的任何附加参数。 包括协议在内，最大长度为1024个字符。<br><br>关键字级别的基本/最终URL会覆盖广告级别和更高级别的URL。 |
| [!UICONTROL Destination URL] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （出于信息目的包含在生成的批量工作表中；未发布到广告网络）对于具有目标URL的帐户，此值是将广告链接到广告商网站上的基本URL/登陆页面的URL（有时通过另一个跟踪点击的网站，然后将用户重定向到登陆页面）。 它包括为Search， Social， &amp; Commerce营销活动或帐户配置的任何附加参数。 如果您生成了跟踪URL，则此值基于您的帐户设置和促销活动设置中的跟踪参数。 如果您附加了特定于广告网络的参数，则这些参数可能会被等效的“搜索”、“社交”和“商务”参数替换。 |
| [!UICONTROL SiteLink Title] | 不适用 | 不适用 | 不适用 | 不适用 | 必填 | 站点链接文本。 对于新的站点链接，请将促销活动名称包含在站点链接行中。 对于广告组级别或广告级别的站点链接，还应分别包括广告组名称或广告标题及文本。<br><br><b>注意：</b> 您最多可以有四个站点链接。 |
| [!UICONTROL SiteLink Base URL] | 不适用 | 不适用 | 不适用 | 不适用 | 必填 | 站点链接的基本URL；它必须是横幅的基本URL。 请参阅&quot;[!UICONTROL Base URL]“ |
| [!UICONTROL SiteLink Destination URL] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | 站点链接的目标URL；它必须是横幅的目标URL。 请参阅&quot;[!UICONTROL Destination URL]“ |
| [!UICONTROL Keyword] | 可选/不适用 | 不适用 | 必填 | 不适用 | 不适用 | 短语（关键词字符串）。 广告必须至少包含一个短语。 除停用词外，每个关键字最多可以有7个词。<br><br><b>注释：</b><ul><li>要在营销活动级别排除短语，请设置 [!UICONTROL Match Type] 到 [!UICONTROL Negative].</li><li>更改短语会删除现有短语并创建新短语。</li><li>更改 [!DNL Yandex] 关键字短语或匹配类型删除现有的关键字短语并创建一个新短语。</li></ul> |
| [!UICONTROL Max CPC] | 不适用 | 必需：创建<br>可选：编辑或删除 | 可选 | 不适用 | 不适用 | 最大每次点击成本(CPC)，这是为搜索网络上的横幅（广告）点击支付的最高金额，无论是否带有货币符号和标点。 您可以设置广告组和关键字的值。 新关键字的默认值继承自广告组级别。 |
| [!UICONTROL Match Type] | 可选/不适用 | 不适用 | 可选：创建<br>必需/可选：编辑或删除 | 不适用 | 不适用 | 短语的关键字匹配选项： <i>[!UICONTROL Content]</i> 或 <i>[!UICONTROL Search]</i>. 使用&#39;&#39;定义负关键字[!UICONTROL Negative Keywords]“ ”列。<br><br><b>注意：</b> 更改 [!DNL Yandex] 关键字短语或匹配类型删除现有的关键字短语并创建一个新短语。 |
| [!UICONTROL Search Network Status] | 可选 | 不适用 | 不适用 | 不适用 | 不适用 | 是否在搜索网络上放置广告： <i>[!UICONTROL Yes]</i> （默认）或 <i>[!UICONTROL No]</i>. |
| 内容网络状态 | 可选 | 不适用 | 不适用 | 不适用 | 不适用 | 是否将广告置于 [!DNL Yandex] 广告（显示）网络： <i>[!UICONTROL Yes]</i> （默认）或 <i>[!UICONTROL No]</i>. |
| [!UICONTROL Negative Keywords (Yandex)] | 不适用 | 不适用 | 可选 | 不适用 | 不适用 | 由广告组中的所有短语共享的负关键字（短语），前面加有一个减号(如 `-mykeyword`)。 如果负关键字与短语中的关键字匹配，则该负关键字不应用于该短语。 |
| [!UICONTROL Param1 (Yandex)] | 不适用 | 不适用 | 可选 | 不适用 | 不适用 | 的值 `{param1}` 替代变量。 它最多可包含255字节。 要删除现有值，请使用值 `[delete]` 括号)。 |
| [!UICONTROL Param2 (Yandex)] | 不适用 | 不适用 | 可选 | 不适用 | 不适用 | 的值  `{param2}` 替代变量。 它最多可包含255字节。 要删除现有值，请使用值 `[delete]` 括号)。 |
| [!UICONTROL Campaign Status] | 可选：创建或编辑<br>必需：删除 | 不适用 | 不适用 | 不适用 | 不适用 | 营销活动的显示状态： <i>[!UICONTROL active]</i>， <i>[!UICONTROL archived]</i>， <i>[!UICONTROL deleted]</i>， <i>[!UICONTROL disapproved]</i>， <i>[!UICONTROL pending]</i>，或 <i>[!UICONTROL stop]</i> （已暂停）。 新营销活动的默认值为 <i>[!UICONTROL active]</i>.<br><br><b>注释：</b><ul></li>如果营销活动曾经处于活动状态，则无法将其删除。 相反，请将其存档。</li><li>在某些情况下，可能会自动存档或删除营销活动。</li><li>您不能手动将状态设置为 <i>[!UICONTROL disapproved]</i> 或 <i>[!UICONTROL pending]</i>，也不会更改这些状态。</li></ul> |
| [!UICONTROL Ad Group Status] | 不适用 | 可选：创建或编辑<br>必需：删除 | 不适用 | 不适用 | 不适用 | 广告组的显示状态： <i>[!UICONTROL active]</i>， <i>[!UICONTROL archived]</i>， <i>[!UICONTROL deleted]</i>， <i>[!UICONTROL disapproved]</i>， <i>[!UICONTROL pending]</i>，或 <i>[!UICONTROL stop]</i> （已暂停）。 新广告组的默认值为 <i>[!UICONTROL active]</i>.<br><br><b>注释：</b><ul></li>如果广告组曾经处于活动状态，则无法将其删除。 相反，请将其存档。</li><li>您不能手动将状态设置为 <i>[!UICONTROL disapproved]</i> 或 <i>[!UICONTROL pending]</i>，也不会更改这些状态。</li></ul> |
| [!UICONTROL Ad Status] | 不适用 | 不适用 | 不适用 | 可选：创建或编辑<br>必需：删除 | 不适用 | 横幅（广告）的显示状态： <i>[!UICONTROL active]</i>， <i>[!UICONTROL archived]</i>， <i>[!UICONTROL deleted]</i>， <i>[!UICONTROL disapproved]</i>， <i>[!UICONTROL pending]</i>，或 <i>[!UICONTROL stop]</i> （已暂停）。 新横幅的默认值为 <i>[!UICONTROL active]</i>.<br><br><b>注意：您不能手动将状态设置为 <i>[!UICONTROL disapproved]</i> 或 <i>[!UICONTROL pending]</i>，也不会更改这些状态。 |
| [!UICONTROL Keyword Status] | 不适用 | 不适用 | 可选：创建或编辑<br>必需：删除 | 不适用 | 不适用 | 短语（关键字）的显示状态： <i>[!UICONTROL active]</i>. 新短语的默认值为 <i>[!UICONTROL active]</i>.<br><br><b>注意：您不能手动将状态设置为 <i>[!UICONTROL disapproved]</i> 或 <i>[!UICONTROL pending]</i>，也不会更改这些状态。 |
| [!UICONTROL SiteLink Status] | 不适用 | 不适用 | 不适用 | 不适用 | 可选：创建或编辑<br>必需：删除 | 站点链接的显示状态： <i>[*UICONTROL活动]</i> 或 <i>[*UICONTROL已暂停]</i>. 新站点链接的默认值是 <i>[*UICONTROL活动]</i>. |
| [!UICONTROL Campaign ID] | 不适用：创建<br>必需/可选：编辑<br>可选：删除 | 可选 | 可选 | 可选 | 可选 | 标识现有营销活动的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅在更改营销活动名称时需要，除非行中包含营销活动的AMO ID。 |
| [!UICONTROL Ad Group ID] | 不适用 | 不适用：创建<br>必需/可选：编辑<br>可选：删除 | 可选 | 可选 | 不适用 | 标识现有广告组的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅在更改广告组名称时才需使用此字段，除非行中包含广告组的AMO ID。 |
| [!UICONTROL Ad ID] | 不适用 | 不适用 | 不适用 | 不适用：创建<br>必需/可选：编辑或删除 | 不适用 | 标识现有关键字的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅当更改关键字名称时才需要此变量，除非该行包含a)足够的属性列来标识关键字或b) AMO ID。 |
| [!UICONTROL Keyword ID] | 不适用 | 不适用 | 不适用：创建<br>必需/可选：编辑<br>必需：删除 | 不适用 | 不适用 | 标识现有关键字的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅当更改关键字名称时才需要此变量，除非该行包含a)足够的属性列来标识关键字或b) AMO ID。 |
| [!UICONTROL AMO ID] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （在生成的批量处理工作表中） [!DNL Adobe]已同步实体的生成唯一标识符。 对于响应式搜索广告，编辑或删除广告时需要AMO ID，除非您包含 [!UICONTROL Ad ID]. 要编辑所有其他具有AMO ID的实体类型的数据，需要使用AMO ID来编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce会使用该值确定要编辑的正确身份，但不会将ID发布到广告网络。 |
| \[广告商特定的标签分类\] | 可选 | 可选 | 可选 | 可选 | 不适用 | （以特定于广告商的标签分类命名，例如名为“颜色”的标签分类的“颜色”）与实体关联的指定分类的值。 每个实体的每个分类只能包含一个值（例如，促销活动A的“颜色”标签分类为“红色”）。 最大长度为100个字符，该值可以包含ASCII和非ASCII字符。<br><br>标签分类及其标签值将应用于所有子组件；以后添加的新组件会自动与标签关联。 产品组的标签分类将应用于单元（最细化）级别。<br><br>分类名称和分类值不区分大小写。 |
| [!UICONTROL Constraints] | 可选 | 可选 | 可选 | 不适用 | 不适用 | 分配给图元的约束。 每个图元只能分配一个约束。<br><br>约束由子实体继承，因此，除非要覆盖继承的值，否则不需要为子实体输入值。 |
| [!UICONTROL EF Error Message] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （出于提供信息的目的，包含在生成的批量处理工作表中）用于显示来自搜索、社交和商务中与行中的数据有关的错误消息的占位符；错误消息包含在 [!UICONTROL EF Errors] 文件。 此值未发布到广告网络。 |

[^1]：Excel在打开文件时将大量数字转换为科学表示法(例如，2.12E+09 for 2115585666)。 要查看标准表示法的位数，请选择列中的任意单元格，然后在公式栏中单击。

>[!MORELIKETHIS]
>
>* [附录 — 批量处理工作表错误](../bulksheet-errors.md)
>* [可在批量处理工作表中执行的操作](bulksheet-operations.md)
>* [支持的批量处理工作表文件格式](bulksheet-file-formats.md)
>* [下载/创建批量处理工作表文件](../bulksheet-download.md)
>* [的点击跟踪格式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [上传批量处理工作表文件或更正的错误文件](../bulksheet-upload.md)
