---
title: ' [!DNL Yandex] 帐户所需的批量处理工作表数据'
description: 引用 [!DNL Yandex] 帐户批量工作表中必需的标题字段和数据字段。
exl-id: bf5a22dd-75c2-486d-85fd-e042bdb87de3
feature: Search Bulksheets
source-git-commit: 5c750153ff9e4be2d02f572d96b171d7aa293dd9
workflow-type: tm+mt
source-wordcount: '1940'
ht-degree: 0%

---

# 附录 — [!DNL Yandex]帐户必需的批量处理工作表数据

要批量创建和更新[!DNL Yandex]营销活动数据，您可以使用专门为[!DNL Yandex]帐户设置格式的Search、Social和Commerce批量工作表文件。 您可以a)[为现有帐户](../bulksheet-download.md)生成所需文件格式的批量工作表文件，或b)手动创建这些文件（有关支持的文件格式的一般信息，请参阅[支持的批量工作表文件格式](bulksheet-file-formats.md)）。

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
>下表是宽的。 若要扩展查看区域，您可以临时隐藏目录和右侧窗格，方法是单击左侧窗格顶部的![隐藏左侧窗格](/help/dsp/assets/hide-left-pane.png "隐藏左侧窗格")和右侧窗格顶部的![隐藏右侧窗格](/help/dsp/assets/hide-right-pane.png "隐藏右侧窗格")。 您还可以使用表格底部的滚动条查看全部内容。

| 字段 | 营销活动 | 广告组 | 关键词 | 文本广告 | 站点链接 | 描述 |
|----|----|-----|-----|----|----|----|
| [!UICONTROL Platform] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （包含在生成的批量工作表中，以供参考）广告平台。 除非每行都包含实体的AMO ID，否则此为必填字段。 |
| [!UICONTROL Acct Name] | 必需/可选 | 必需/可选 | 必需/可选 | 必需/可选 | 必需/可选 | （包含在生成的批量工作表中，以供参考）广告平台。 除非每行都包含实体的AMO ID，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 | 必填 | 必填 | 必填 | 必填 | 为帐户标识营销活动的唯一名称。 |
| [!UICONTROL Campaign Start Date] | 必需： Create<br>可选：编辑或删除 | 不适用 | 不适用 | 不适用 | 不适用 | 营销活动可能进行竞价的第一个日期，以广告商所在的时区为单位并采用以下格式之一： m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 新营销活动的默认日期为当天。 |
| [!UICONTROL Campaign Budget] | 必需： Create<br>可选：编辑或删除 | 不适用 | 不适用 | 不适用 | 不适用 | 竞选活动的终生支出限制，无论是否带有货币符号和标点。 |
| [!UICONTROL Delivery Method] | 必需： Create<br>可选：编辑或删除 | 不适用 | 不适用 | 不适用 | 不适用 | 每天显示促销活动广告的速度：<ul><li><i>[!UICONTROL Standard (Distributed)]</i>（新营销活动的默认值）：用于将广告展示次数分散到一整天里。</li><li><i>[!UICONTROL Accelerated]：</i>在达到预算之前，尽可能多地显示您的广告。 因此，您的广告可能不会在当天晚些时候显示。</li></ul> |
| [!UICONTROL Ad Group Name] | 不适用 | 必填 | 必填 | 必填 | 不适用 | 广告组。 |
| [!UICONTROL Ad Title] | 不适用 | 不适用 | 不适用 | 必填 | 不适用 | 横幅（广告）的标题。 最大长度为33个字符，单个单词不能包含超过23个字符。<br><br><b>注意：</b>更改广告副本将删除现有广告并创建新广告。 |
| [!UICONTROL Ad Description] | 不适用 | 不适用 | 不适用 | 必填 | 不适用 | 横幅（广告）的正文。 最大长度为75个字符，单个单词不能超过22个字符。<br><br><b>注意：</b>更改广告副本将删除现有广告并创建新广告。 |
| [!UICONTROL Base URL] | 不适用 | 不适用 | 可选 | 必填 | 不适用 | 最终用户单击您的广告时获得的登陆页面URL，包括为营销活动或帐户配置的任何附加参数。 包括协议在内，最大长度为1024个字符。关键字级别的<br><br>基本/最终URL将覆盖广告级别和更高级别的URL。 |
| [!UICONTROL Destination URL] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （出于信息目的包含在生成的批量工作表中；未发布到广告网络）对于具有目标URL的帐户，此值是将广告链接到广告商网站上的基本URL/登陆页面的URL（有时通过另一个跟踪点击的网站，然后将用户重定向到登陆页面）。 它包括为Search、Social和Commerce营销活动或帐户配置的任何附加参数。 如果您生成了跟踪URL，则此值基于您的帐户设置和促销活动设置中的跟踪参数。 如果附加了特定于广告网络的参数，则可能会将其替换为与搜索、社交和Commerce等效的参数。 |
| [!UICONTROL SiteLink Title] | 不适用 | 不适用 | 不适用 | 不适用 | 必填 | 站点链接文本。 对于新的站点链接，请将促销活动名称包含在站点链接行中。 对于广告组级别或广告级别的站点链接，还应分别包括广告组名称或广告标题及文本。<br><br><b>注意：</b>您最多可以有4个站点链接。 |
| [!UICONTROL SiteLink Base URL] | 不适用 | 不适用 | 不适用 | 不适用 | 必填 | 站点链接的基本URL；它必须是横幅的基本URL。 请参阅“[!UICONTROL Base URL]”。 |
| [!UICONTROL SiteLink Destination URL] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | 站点链接的目标URL；它必须是横幅的目标URL。 请参阅“[!UICONTROL Destination URL]”。 |
| [!UICONTROL Keyword] | 可选/不适用 | 不适用 | 必填 | 不适用 | 不适用 | 短语（关键词字符串）。 广告必须至少包含一个短语。 除停用词外，每个关键字最多可以有7个词。<br><br><b>注释：</b><ul><li>要在营销活动级别排除短语，请将[!UICONTROL Match Type]设置为[!UICONTROL Negative]。</li><li>更改短语会删除现有短语并创建新短语。</li><li>更改[!DNL Yandex]关键字短语或匹配类型会删除现有的关键字短语并创建一个新短语。</li></ul> |
| [!UICONTROL Max CPC] | 不适用 | 必需： Create<br>可选：编辑或删除 | 可选 | 不适用 | 不适用 | 最大每次点击成本(CPC)，这是为搜索网络上的横幅（广告）点击支付的最高金额，无论是否带有货币符号和标点。 您可以设置广告组和关键字的值。 新关键字的默认值继承自广告组级别。 |
| [!UICONTROL Match Type] | 可选/不适用 | 不适用 | 可选：创建<br>必需/可选：编辑或删除 | 不适用 | 不适用 | 短语的关键字匹配选项： <i>[!UICONTROL Content]</i>或<i>[!UICONTROL Search]</i>。 使用“[!UICONTROL Negative Keywords]”列定义负关键字。<br><br><b>注意：</b>更改[!DNL Yandex]关键字短语或匹配类型将删除现有的关键字短语并创建一个新短语。 |
| [!UICONTROL Search Network Status] | 可选 | 不适用 | 不适用 | 不适用 | 不适用 | 是否在搜索网络上放置广告： <i>[!UICONTROL Yes]</i> （默认值）或<i>[!UICONTROL No]</i>。 |
| 内容网络状态 | 可选 | 不适用 | 不适用 | 不适用 | 不适用 | 是在[!DNL Yandex]广告（显示）网络上放置广告： <i>[!UICONTROL Yes]</i> （默认）还是<i>[!UICONTROL No]</i>。 |
| [!UICONTROL Negative Keywords (Yandex)] | 不适用 | 不适用 | 可选 | 不适用 | 不适用 | 广告组中由所有短语共享的负关键字（短语），前面加有减号（如`-mykeyword`）。 如果负关键字与短语中的关键字匹配，则该负关键字不应用于该短语。 |
| [!UICONTROL Param1 (Yandex)] | 不适用 | 不适用 | 可选 | 不适用 | 不适用 | `{param1}`替换变量的值。 它最多可包含255字节。 要删除现有值，请使用值`[delete]`（包括括号）。 |
| [!UICONTROL Param2 (Yandex)] | 不适用 | 不适用 | 可选 | 不适用 | 不适用 | `{param2}`替换变量的值。 它最多可包含255字节。 要删除现有值，请使用值`[delete]`（包括括号）。 |
| [!UICONTROL Campaign Status] | 可选：创建或编辑<br>必需：删除 | 不适用 | 不适用 | 不适用 | 不适用 | 营销活动的显示状态： <i>[!UICONTROL active]</i>、<i>[!UICONTROL archived]</i>、<i>[!UICONTROL deleted]</i>、<i>[!UICONTROL disapproved]</i>、<i>[!UICONTROL pending]</i>或<i>[!UICONTROL stop]</i> （已暂停）。 新营销活动的默认值为<i>[!UICONTROL active]</i>。<br><br><b>注释：</b><ul></li>如果营销活动曾经处于活动状态，则无法将其删除。 相反，请将其存档。</li><li>在某些情况下，可能会自动存档或删除营销活动。</li><li>您不能手动将状态设置为<i>[!UICONTROL disapproved]</i>或<i>[!UICONTROL pending]</i>，也不能更改这些状态。</li></ul> |
| [!UICONTROL Ad Group Status] | 不适用 | 可选：创建或编辑<br>必需：删除 | 不适用 | 不适用 | 不适用 | 广告组的显示状态： <i>[!UICONTROL active]</i>、<i>[!UICONTROL archived]</i>、<i>[!UICONTROL deleted]</i>、<i>[!UICONTROL disapproved]</i>、<i>[!UICONTROL pending]</i>或<i>[!UICONTROL stop]</i> （已暂停）。 新广告组的默认值为<i>[!UICONTROL active]</i>。<br><br><b>注释：</b><ul></li>如果广告组曾经处于活动状态，则无法将其删除。 相反，请将其存档。</li><li>您不能手动将状态设置为<i>[!UICONTROL disapproved]</i>或<i>[!UICONTROL pending]</i>，也不能更改这些状态。</li></ul> |
| [!UICONTROL Ad Status] | 不适用 | 不适用 | 不适用 | 可选：创建或编辑<br>必需：删除 | 不适用 | 横幅（广告）的显示状态： <i>[!UICONTROL active]</i>、<i>[!UICONTROL archived]</i>、<i>[!UICONTROL deleted]</i>、<i>[!UICONTROL disapproved]</i>、<i>[!UICONTROL pending]</i>或<i>[!UICONTROL stop]</i> （已暂停）。 新横幅的默认值为<i>[!UICONTROL active]</i>。<br><br><b>注意：您不能手动将状态设置为<i>[!UICONTROL disapproved]</i>或<i>[!UICONTROL pending]</i>，也不能更改这些状态。 |
| [!UICONTROL Keyword Status] | 不适用 | 不适用 | 可选：创建或编辑<br>必需：删除 | 不适用 | 不适用 | 短语（关键字）的显示状态： <i>[!UICONTROL active]</i>。 新短语的默认值为<i>[!UICONTROL active]</i>。<br><br><b>注意：您不能手动将状态设置为<i>[!UICONTROL disapproved]</i>或<i>[!UICONTROL pending]</i>，也不能更改这些状态。 |
| [!UICONTROL SiteLink Status] | 不适用 | 不适用 | 不适用 | 不适用 | 可选：创建或编辑<br>必需：删除 | Sitelink的显示状态： <i>[*UICONTROL Active]</i>或<i>[*UICONTROL已暂停]</i>。 新站点链接的默认值为<i>[*UICONTROL Active]</i>。 |
| [!UICONTROL Campaign ID] | 不适用：创建<br>必需/可选：编辑<br>可选：删除 | 可选 | 可选 | 可选 | 可选 | 标识现有营销活动的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1]仅在您更改促销活动名称时需要，除非行包含促销活动的AMO ID。 |
| [!UICONTROL Ad Group ID] | 不适用 | 不适用：创建<br>必需/可选：编辑<br>可选：删除 | 可选 | 可选 | 不适用 | 标识现有广告组的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1]仅在您更改广告组名称时需要，除非行包含广告组的AMO ID。 |
| [!UICONTROL Ad ID] | 不适用 | 不适用 | 不适用 | 不适用：创建<br>必需/可选：编辑或删除 | 不适用 | 标识现有关键字的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1]仅当更改关键字名称时才需要，除非该行包含a)足够的属性列来标识关键字或b) AMO ID。 |
| [!UICONTROL Keyword ID] | 不适用 | 不适用 | 不适用：创建<br>必需/可选：编辑<br>必需：删除 | 不适用 | 不适用 | 标识现有关键字的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1]仅当更改关键字名称时才需要，除非该行包含a)足够的属性列来标识关键字或b) AMO ID。 |
| [!UICONTROL AMO ID] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （在生成的批量工作表中）已同步实体的[!DNL Adobe]生成的唯一标识符。 对于响应式搜索广告，编辑或删除广告时需要AMO ID，除非包含[!UICONTROL Ad ID]。 要编辑所有其他具有AMO ID的实体类型的数据，需要使用AMO ID来编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |
| \[广告商特定的标签分类\] | 可选 | 可选 | 可选 | 可选 | 不适用 | （以特定于广告商的标签分类命名，例如名为“颜色”的标签分类的“颜色”）与实体关联的指定分类的值。 每个实体的每个分类只能包含一个值（例如，促销活动A的“颜色”标签分类为“红色”）。 最大长度为100个字符，该值可以包含ASCII和非ASCII字符。<br><br>标签分类及其标签值将应用于所有子组件；以后添加的新组件会自动与标签关联。 产品组的标签分类将应用于单元（最细化）级别。<br><br>分类名称和分类值不区分大小写。 |
| [!UICONTROL Constraints] | 可选 | 可选 | 可选 | 不适用 | 不适用 | 分配给图元的约束。 每个图元只能分配一个约束。<br><br>约束由子实体继承，因此，除非要覆盖继承的值，否则不需要为子实体输入值。 |
| [!UICONTROL EF Error Message] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （出于提供信息的目的，包含在生成的批量处理工作表中）用于显示来自搜索、社交和Commerce中有关行中数据的错误消息的占位符；错误消息包含在[!UICONTROL EF Errors]文件中。 此值未发布到广告网络。 |

[^1]： Excel在打开文件时将大数转换为科学记号(如2.12E+09 for 2115585666)。 要查看标准表示法的位数，请选择列中的任意单元格，然后在公式栏中单击。

>[!MORELIKETHIS]
>
>* [附录 — 批量处理工作表错误](../bulksheet-errors.md)
>* [可在批量处理工作表中执行的操作](bulksheet-operations.md)
>* [支持的批量处理工作表文件格式](bulksheet-file-formats.md)
>* [下载/创建批量处理工作表文件](../bulksheet-download.md)
>*  [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)的[点击跟踪格式
>* [上载批量工作表文件或更正的错误文件](../bulksheet-upload.md)
