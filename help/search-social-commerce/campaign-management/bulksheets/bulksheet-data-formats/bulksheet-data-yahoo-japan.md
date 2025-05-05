---
title: ' [!DNL Yahoo! Japan] 帐户的批量工作表数据'
description: 引用 [!DNL Yahoo! Japan] 帐户的已下载批量处理工作表中的标题字段和数据字段。
exl-id: 78eb41ce-3854-454c-adf2-ba0339e2aef7
feature: Search Bulksheets
source-git-commit: 5c750153ff9e4be2d02f572d96b171d7aa293dd9
workflow-type: tm+mt
source-wordcount: '2672'
ht-degree: 0%

---

# 附录 — [!DNL Yahoo! Japan]帐户的批量工作表数据

您可以批量下载[!DNL Yahoo! Japan]帐户的数据，但无法将批量工作表上传或发布到广告网络。

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Campaign Budget,Delivery Method,Mobile Bid Adjustment,Location,Location Type,Ad Group Name,Max CPC,Keyword,Match Type,First Page Bid, Quality Score,Ad Name (Yahoo JP),Creative Preferred Devices,Ad Title,Ad Title2,Description Line 1,Description Line 2,Creative Type,Display URL,Display Path 1,Display Path 2,Base URL/Final URL,Destination URL,Tracking Template,Campaign Status,Ad Group Status,Keyword Status,Ad Status,Location Status,[Advertiser-specific Label Classification],Constraints,Campaign ID,Ad Group ID,Keyword ID,Ad ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## 可用的数据字段

>[!TIP]
>
>下表是宽的。 若要扩展查看区域，您可以临时隐藏目录和右侧窗格，方法是单击左侧窗格顶部的![隐藏左侧窗格](/help/dsp/assets/hide-left-pane.png "隐藏左侧窗格")和右侧窗格顶部的![隐藏右侧窗格](/help/dsp/assets/hide-right-pane.png "隐藏右侧窗格")。 您还可以使用表格底部的滚动条查看全部内容。

| 字段 | 营销活动 | 广告组 | 关键词 | 文本广告 | 营销活动位置目标 | 描述 |
|----|----|----|----|----|----|----|
| [!UICONTROL Platform] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （包含在生成的批量工作表中，以供参考）广告平台。 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Acct Name] | 必需/可选 | 必需/可选 | 必需/可选 | 必需/可选 | 必需/可选 | 标识广告网络帐户的唯一名称。 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 | 必填 | 必填 | 必填 | 必填 | 为帐户标识营销活动的唯一名称。 |
| [!UICONTROL Campaign Budget] | 必需： Create<br><br>可选：编辑或删除 | 不适用 | 不适用 | 不适用 | 不适用 | 竞选活动的每日支出限制，无论是否带有货币符号和标点。 此值将覆盖但不能超过帐户预算。 |
| [!UICONTROL Delivery Method] | 必需： Create<br><br>可选：编辑或删除 | 不适用 | 不适用 | 不适用 | 不适用 | 每天显示促销活动广告的速度：<ul><li>*[!UICONTROL Standard (Distributed)]*（新营销活动的默认值）：用于将广告展示次数分散到一整天里。</li><li>*[!UICONTROL Accelerated]：*&#x200B;在达到预算之前，尽可能多地显示您的广告。 因此，您的广告可能不会在当天晚些时候显示。</li></ul> |
| [!UICONTROL Mobile Bid Adjustment] | 可选 | 可选 | 不适用 | 不适用 | 不适用 | 是否要在移动设备上竞标广告，可以在促销活动级别或广告组级别进行：<ul><li>要使用现有的移动竞价调整，请将此项留空。</li><li>若要不为移动设备上的广告竞价，请输入`-100`。</li><li>要在移动设备上与桌面设备和平板设备上的广告使用相同的竞价来竞价广告（差异为0%），请输入`0`。 对于新的营销策划，您也可以将此项留空。</li><li>要在使用其他竞价的移动设备上竞价广告，请输入增加或减少竞价的百分比。 该值可以介于`-90`到`300`之间。</li></ul>如果在营销活动级别排除设备，则无法覆盖广告组级别的排除项。<br><br><b>注释：</b><ul><li>广告组会继承营销活动级别的设置，但您可以覆盖这些设置。</li><li>如果将促销活动分配给优化的项目组合，则优化功能会自动确定基本关键字级别的竞价，以帮助项目组合实现其目标。 然后，广告网络会按照为移动广告指定的方式调整竞价。</li><li>如果将促销活动或广告组分配给优化的项目组合：<ul><li>优化功能会自动确定基本关键字级别的竞价，以帮助项目组合实现其目标。 然后，搜索网络按照为移动广告指定的方式调整竞价。</li><li>如果将项目组合配置为“[!UICONTROL Auto-optimize Bid Adjustment Values]”，则优化功能会更改广告组级别的竞价调整，前提是它计算的理想值落在项目组合设置中指定的最小值和最大值内，并且广告组不排除移动广告的竞价。</li></ul></li></ul> |
| [!UICONTROL Location] | 不适用 | 不适用 | 不适用 | 不适用 | 可选 | 投放营销活动广告的地理位置。 对于城市，请使用格式“&lt;<i>City</i>>， &lt;</i>Previous</i>>”（如Adachi， Tokyo）。 要排除位置，请用减号(`-`)为位置添加前缀。 如果不输入促销活动的特定值，则会定位所有位置。 |
| [!UICONTROL Location Type] | 不适用 | 不适用 | 不适用 | 不适用 | 必需/可选 | （定位特定位置时必需）指定的位置是[!UICONTROL Prefecture]类型还是[!UICONTROL City]类型。 |
| [!UICONTROL Ad Group Name] | 不适用 | 必填 | 必填 | 必填 | 不适用 | 广告组名称在营销活动中是唯一的。 最大长度为50个字符。 |
| [!UICONTROL Max CPC] | 不适用 | 可选 | 可选 | 不适用 | 不适用 | 最高每次点击成本(CPC)，在搜索网络上为广告点击支付的最高金额，无论是否带有货币符号和标点。 您可以设置广告组和关键字的值。 新关键字的默认值继承自广告组级别。 |
| [!UICONTROL Keyword] | 可选/不适用 | 可选/不适用 | 必填 | 不适用 | 不适用 | 关键词字符串。 [!DNL Yahoo! Japan]关键字和匹配类型是可变的，这意味着您可以编辑它们而不删除现有关键字。<br><br>要在广告组或营销活动级别排除关键字，请将[!UICONTROL Match Type]设置为“负值”。 如果行包含广告组名称，则会为广告组排除关键字。 如果行不包含广告组名称，则该关键字将排除在整个营销活动中。 |
| [!UICONTROL Match Type] | 可选/不适用 | 可选/不适用 | 可选：创建<br><br>必需/可选：编辑或删除 | 不适用 | 不适用 | 关键字的关键字匹配选项： *[!UICONTROL Broad]* （新关键字的默认值）、*[!UICONTROL Exact]*、*[!UICONTROL Phrase]*、*[!UICONTROL Negative Broad]或&#x200B;*[!UICONTROL Negative Exact]*。 在营销活动级别或广告组级别定义负关键字。 [!DNL Yahoo! Japan]关键字和匹配类型是可变的，这意味着您可以编辑它们而不删除现有关键字。<br><br>只有编辑具有多个匹配类型的关键字时，才需要匹配类型或关键字ID的值。 |
| [!UICONTROL First Page Bid] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （出于提供信息的目的包含在生成的批量工作表中）在搜索结果的第一页上放置广告所需的出价。 此值未发布到广告网络。 |
| [!UICONTROL Quality Score] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （出于信息目的包含在生成的批量工作表中）广告网络分配给关键字的当前质量分数。 此值未发布到广告网络。 |
| [!UICONTROL Ad Name (Yahoo JP)] | 不适用 | 不适用 | 不适用 | 可选：创建<br><br>必需/可选：编辑或删除 | 不适用 | 在广告组中标识广告图像的唯一名称。 最大长度为50个字符。 除非对行使用[!UICONTROL AMO ID]或[!UICONTROL Ad ID]，否则必需。 |
| [!UICONTROL Creative Preferred Devices] | 不适用 | 不适用 | 不适用 | 可选 | 不适用 | 您喜欢在其中显示广告的设备类型： *[!UICONTROL All]* （默认值）或&#x200B;*[!UICONTROL Mobile]*。 对于[!UICONTROL Mobile]，广告网络会尝试向移动设备用户显示广告，而不是桌面或平板电脑用户。 否则，会在任何设备类型上显示广告。<br><br>只有管理员和[!DNL Adobe]帐户管理员用户可以编辑此设置。 |
| [!UICONTROL Ad Title] | 不适用 | 不适用 | 不适用 | 必填 | 不适用 | 广告的标题。 最大长度为30个单字节字符或15个双字节字符。 更改广告副本将删除现有广告并创建新广告。 |
| [!UICONTROL Ad Title 2] | 不适用 | 不适用 | 不适用 | 必需/不适用 | 不适用 | （仅限扩展文本广告）第二个标题。 最大长度为30个字符或15个双字节字符。 更改广告副本将删除现有广告并创建新广告。 |
| [!UICONTROL Description Line 1] | 不适用 | 不适用 | 不适用 | 必填 | 不适用 | 广告正文。 对于扩展文本广告，最大长度为80个单字节字符或40个双字节字符。 更改广告副本将删除现有广告并创建新广告。 |
| [!UICONTROL Description Line 2] | 不适用 | 不适用 | 不适用 | 必填 | 不适用 | （仅限标准文本广告）广告正文的第二行。 最大长度为38个单字节字符或19个双字节字符。 更改广告副本将删除现有广告并创建新广告。 <b>注释：</b> [!DNL Yahoo! Japan Ads]不再允许创建和编辑标准文字广告。 |
| [!UICONTROL Creative Type] | 不适用 | 不适用 | 不适用 | 可选 | 不适用 | 广告格式：<ul><li>*[!UICONTROL Text]* （新广告的默认值）：可能在计算机、平板电脑和智能手机上显示的文本广告。</li><li>*[!UICONTROL Mobile]：*&#x200B;已弃用。</li></ul> |
| [!UICONTROL Display URL] | 不适用 | 不适用 | 不适用 | 必需/ n/a：创建<br><br>可选/ n/a：编辑或删除 | 不适用 | （仅限现有的标准文字广告；只读）广告中显示的URL。 最大长度为255个单字节字符或127个双字节字符。 此外，显示URL和登陆页面URL的域必须相同。 <b>注释：</b> [!DNL Yahoo! Japan Ads]已弃用创建和编辑标准文本和扩展文本广告。 |
| [!UICONTROL Display Path 1]，[!UICONTROL Display Path 2] | 不适用 | 不适用 | 不适用 | 可选/不适用 | 不适用 | （仅限扩展文本广告；可选）添加到显示URL的文本，将自动从最终URL中提取。 在URL中，它前面有正斜杠(`/`)。 路径不能包含正斜杠(`/`)或换行符(`\n`)。 最大长度为15个字符或7个双字节字符。<br><br>要插入广告自定义程序，请使用以下格式，其中`Default text`是当馈送文件不包含有效值时要插入的可选值：<ul><li>[!DNL Google Ads]： `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`</li><li>[!DNL Microsoft Advertising]： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`</li></ul>例如，如果[!UICONTROL Display Path 1]是“交易”，则显示URL将为`&lt;display URL&gt;/deals`，如www.example.com/deals。 |
| [!UICONTROL Base URL/Final URL] | 不适用 | 不适用 | 可选 | 必填 | 不适用 | 最终用户单击您的广告时获得的登陆页面URL，包括为营销活动或帐户配置的任何附加参数。 关键字级别的基本/最终URL会覆盖广告级别和更高级别的URL。 |
| [!UICONTROL Destination URL] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （出于信息目的包含在生成的批量工作表中；未发布到广告网络）对于具有目标URL的帐户，此URL是将广告链接到广告商网站上的基本URL/登陆页面的URL（有时通过另一个跟踪点击的网站，然后将用户重定向到登陆页面）。 它包括为Search、Social和Commerce营销活动或帐户配置的任何附加参数。 如果您生成了跟踪URL，则跟踪URL将基于帐户设置和促销活动设置中的跟踪参数。 如果附加了特定于广告网络的参数，则可能会将其替换为与搜索、社交和Commerce等效的参数。<br><br>对于具有最终URL的帐户，此列显示的值与基本URL/最终URL列显示的值相同。<br><br>关键字或投放级别的目标URL将覆盖广告级别的URL。 |
| [!UICONTROL Tracking Template] | 可选 | 可选 | 可选 | 可选 | 可选 | （可选）跟踪模板或跟踪URL，用于指定所有登陆域重定向和跟踪参数，并将最终/登陆页面URL嵌入到参数中。 使用参数`!{lpurl}`指示登陆页面URL。 示例： `{lpurl}?source={network}&id=5`或`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`以包含重定向。<br><br>您可以选择添加第三方重定向和跟踪。<br><br>对于Adobe Advertising转化跟踪（在营销活动设置包括“[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]”时应用），Search、Social和Commerce会在您保存记录时自动为其自己的重定向和跟踪代码添加前缀。<br><br>最细粒度级别的跟踪模板将覆盖所有更高级别的值。 例如，如果帐户设置和关键词设置都包含一个值，则会应用关键词值。 |
| [!UICONTROL Campaign Status] | 可选：创建或编辑<br><br>必需：删除 | 不适用 | 不适用 | 不适用 | 不适用 | 营销活动的显示状态：*[!UICONTROL Active]* （新营销活动的默认值）、*[!UICONTROL Paused]*、*[!UICONTROL Ended]* （仅限现有营销活动）或&#x200B;*[!UICONTROL Deleted]* （仅限现有营销活动）。 |
| [!UICONTROL Ad Group Status] | 不适用 | 可选：创建或编辑<br><br>必需：删除 | 不适用 | 不适用 | 不适用 | 广告组的显示状态：  *[!UICONTROL Active]*、*[!UICONTROL Paused]*&#x200B;或&#x200B;*[!UICONTROL Deleted]*（仅限现有广告组）。 新广告组的默认值为[!UICONTROL Active]。 要删除活动或暂停的广告组，请输入值`Deleted`。 |
| [!UICONTROL Keyword Status] | 不适用 | 不适用 | 可选：创建或编辑<br><br>必需：删除 | 不适用 | 不适用 | 关键字的显示状态： *[!UICONTROL Active]*、*[!UICONTROL Deleted]* （仅限现有关键字）、*[!UICONTROL Disapproved]* （不可编辑）、*[!UICONTROL Paused]* （仅限现有关键字）或&#x200B;*[!UICONTROL Pending]* （不可编辑）。 新关键字的默认值为[!UICONTROL Active]。 要删除关键字，请输入值`Deleted`。 |
| [!UICONTROL Ad Status] | 不适用 | 不适用 | 不适用 | 可选：创建或编辑<br><br>必需：删除 | 不适用 | 广告的显示状态： *[!UICONTROL Active]* （新广告的默认值）、*[!UICONTROL Deleted]* （仅限现有广告）、*[!UICONTROL Disapproved]* （不可编辑）、*[!UICONTROL Paused]*&#x200B;或&#x200B;*[!UICONTROL Pending]* （不可编辑）。 新广告的默认值为[!UICONTROL Active]。 要删除广告，请输入值`Deleted`。 |
| [!UICONTROL Location Status] | 不适用 | 不适用 | 不适用 | 不适用 | 可选 | 位置目标的状态： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Deleted]* （仅限现有位置）。 新位置的默认值为[!UICONTROL Active]。 要删除活动位置，请输入值`Deleted`。 |
| \[广告商特定的标签分类\] | 可选 | 可选 | 可选 | 可选 | 可选 | （以特定于广告商的标签分类命名，例如名为“颜色”的标签分类的“颜色”）与实体关联的指定分类的值。 每个实体的每个分类只能包含一个值（例如，促销活动A的“颜色”标签分类为“红色”）。 最大长度为100个字符，该值可以包含ASCII和非ASCII字符。<br><br>标签分类及其标签值将应用于所有子组件；以后添加的新组件会自动与标签关联。 <br><br>分类名称和分类值不区分大小写。 |
| [!UICONTROL Constraints] | 可选 | 可选 | 可选 | 可选 | 不适用 | 分配给图元的约束。 每个图元只能分配一个约束。<br><br>约束由子实体继承，因此，除非要覆盖继承的值，否则不需要为子实体输入值。 |
| [!UICONTROL Campaign ID] | 不适用：创建<br><br>必需/可选：编辑或删除 | 可选 | 可选 | 可选 | 不适用 | 标识现有营销活动的唯一ID。 在CSV和TSV文件中，它前面必须有一个单引号(`'`)。[^1]仅在您更改营销活动名称时需要，除非该行包含营销活动的“[!UICONTROL AMO ID]”。 |
| [!UICONTROL Ad Group ID] | 不适用 | 不适用：创建<br><br>必需/可选：编辑或删除 | 可选 | 可选 | 不适用 | 标识现有广告组的唯一ID。 在CSV和TSV文件中，它前面必须有一个单引号(`'`)。[^1]仅在您更改广告组名称时需要，除非行包含广告组的“[!UICONTROL AMO ID]”。 |
| [!UICONTROL Keyword ID] | 不适用 | 不适用 | 不适用：创建<br><br>必需/可选：编辑<br><br>必需：删除 | 不适用 | 不适用 | 标识现有关键字的唯一ID。 在CSV和TSV文件中，它前面必须有一个单引号(`'`)。[^1]仅在编辑或删除关键字时才需要，除非该行包含a)足够的属性列来标识关键字或b) &quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL Ad ID] | 不适用 | 不适用 | 不适用 | 不适用：创建<br><br>必需/可选：编辑或删除 | 不适用 | 标识现有广告的唯一ID。 在CSV和TSV文件中，它前面必须有一个单引号(`'`)。[^1]对于响应式搜索广告，需要[!UICONTROL Ad ID]或[!UICONTROL AMO ID]才能编辑或删除广告数据。 对于所有其他实体类型，只有在更改广告状态时才需要[!UICONTROL AMO ID]，除非该行包含a)足够的广告属性列来标识广告或b)“[!UICONTROL AMO ID]”。 但是，如果您既不包括[!UICONTROL Ad ID]也不包括[!UICONTROL AMO ID]，并且广告属性列与多个广告匹配，则只有其中一个广告的状态会更改。<br><br><b>注意：</b>如果您编辑a)广告属性列（现有广告的[!UICONTROL Status]除外）或b)响应式搜索广告的任何数据，并且您既不包括[!UICONTROL Ad ID]也不包括[!UICONTROL AMO ID]，则会创建新广告，并且现有广告不会发生更改。 |
| [!UICONTROL AMO ID] | 不适用：创建<br><br>可选：编辑或删除 | 不适用：创建<br><br>可选：编辑或删除 | 不适用：创建<br><br>可选：编辑或删除 | 不适用：创建<br><br>可选：编辑或删除 | 不适用 | （在生成的批量工作表中）已同步实体的[!DNL Adobe]生成的唯一标识符。 对于响应式搜索广告，编辑或删除广告需要[!UICONTROL AMO ID]，除非您包含[!UICONTROL Ad ID]。 要编辑具有[!UICONTROL AMO ID]的所有其他实体类型的数据，需要[!UICONTROL AMO ID]才能编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |
| [!UICONTROL EF Error Message] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （出于提供信息的目的，包含在生成的批量处理工作表中）用于显示来自搜索、社交和Commerce中有关行中数据的错误消息的占位符；错误消息包含在[!UICONTROL EF Errors]文件中。 此值未发布到广告网络。 |
| [!UICONTROL SE Error Message] | 不适用 | 不适用 | 不适用 | 不适用 | 不适用 | （出于信息目的包含在生成的批量工作表中）用于显示来自广告网络的关于行中数据的错误消息的占位符；错误消息包含在[!UICONTROL SE Errors]文件中。 此值未发布到广告网络。 |

[^1]： Excel在打开文件时将大数转换为科学记号(如2.12E+09 for 2115585666)。 要查看标准表示法的位数，请选择列中的任意单元格，然后在公式栏中单击。

>[!MORELIKETHIS]
>
>* [附录 — 批量处理工作表错误](../bulksheet-errors.md)
>* [可在批量处理工作表中执行的操作](bulksheet-operations.md)
>* [支持的批量处理工作表文件格式](bulksheet-file-formats.md)
>* [下载/创建批量处理工作表文件](../bulksheet-download.md)
>*  [!DNL Naver][&#128279;](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)的点击跟踪格式
>* [上载批量工作表文件或更正的错误文件](../bulksheet-upload.md)
