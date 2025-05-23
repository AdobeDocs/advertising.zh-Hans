---
title: 库存馈送的文本广告和响应式搜索广告模板设置
description: 引用库存馈送的文本广告和响应式搜索广告模板的设置。
exl-id: bf57fbb5-b7b0-4bd6-9dd2-def3825a1da6
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '3325'
ht-degree: 0%

---

# 库存馈送的文本广告和响应式搜索广告模板设置


*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （仅删除操作）和仅[!DNL Yandex]帐户*

>[!NOTE]
>
>* 以下字符是为模板中的列名称和修饰符名称而保留的，因此禁止在所有属性字段中作为文本： `[ ] < > `
>* 在[!DNL Yandex templates]中，您只能在URL中使用动态参数`{param1}`和`{param2}`，并且不能在广告描述中使用动态价格插入。

## \[所有选项卡上方\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[左侧面板\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

**[!UICONTROL Map Only]：**（可选）将所有新广告组（不适用于[!DNL Yandex]）、关键字和广告映射到现有营销活动，而不是创建营销活动。 如果启用此选项，请选择映射方法。

在营销活动级别使用[!UICONTROL Map Only]需要与产品分类紧密联系并轻松映射到数据馈送的现有帐户结构。

**[!UICONTROL Map Method]：** （为促销活动启用[!UICONTROL Map Only]时）新广告组（不适用于[!DNL Yandex]）、关键字和广告映射到现有促销活动的方法：

* *[!UICONTROL Contains Anywhere]：*&#x200B;将数据添加到其名称包含指定字符串（如果存在）的现有营销活动。

* *[!UICONTROL Contains Exactly]：*&#x200B;将数据添加到其名称包含指定字符串（如果存在）的现有营销活动。

* *[!UICONTROL Exactly Matches]*（默认）：将数据添加到具有相同名称的现有营销活动（如果存在）。

当未找到匹配项时，将忽略营销活动的所有数据。 如果找到多个促销活动匹配项，则关键词和广告将映射到所有这些匹配项。

**[!UICONTROL Campaign Tracking Template]：** （仅具有最终/高级URL的帐户；可选）营销活动级别的跟踪模板，该模板指定所有登入外域重定向和跟踪参数，并将最终URL嵌入到参数中。 此值将覆盖帐户级别的设置，但更细粒度级别（使用关键字作为最细粒度级别）的跟踪模板将覆盖此值。

* 对于Adobe Advertising转化跟踪（在营销活动设置包括“[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]”时应用），Search、Social和Commerce会在您保存记录时自动附加重定向和跟踪代码。

* 嵌入最终URL：

   * （仅限[!DNL Google Ads]和[!DNL Microsoft Advertising]）有关指示跟踪模板中最终URL的参数列表，请参阅[[!DNL Google Ads] 文档](https://support.google.com/google-ads/answer/6305348)中“可用的[!DNL ValueTrack]参数”部分中的（[!DNL Microsoft Advertising]仅限）[[!DNL Microsoft Advertising] 文档](https://help.ads.microsoft.com/#apex/3/en/56799/2)或（[!DNL Google Ads]仅限）跟踪模板参数。

   * （仅限[!DNL Yahoo! Japan Ads]）使用参数`!{unescapedurl}`指示登陆页面URL。

   * 您可以选择包含URL参数以及为营销活动定义的任何自定义参数，这些参数以&amp;号分隔，如`{lpurl}?matchtype={matchtype}&device={device}`。

* 对于第三方重定向和跟踪，请输入一个值。

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]：** （在[!DNL Google Ads]和[!DNL Yandex]促销活动设置中）要向其投放广告的网络：

* *[!UICONTROL Search]：*&#x200B;对赞助商搜索列表投标。

  （[!DNL Google Ads]个营销活动）要包括[!DNL Google Ads]个搜索合作伙伴的列表投标，请选中&#x200B;**[!UICONTROL Search partners]**&#x200B;旁边的复选框。

* *[!UICONTROL Content]：*&#x200B;要对内容（显示）网络列表上的投放位置投标。 **注意：**&#x200B;您无法使用模板创建版面。 选择此选项时，请使用<!-- insert link -->批量工作表或[!UICONTROL Search] > [!UICONTROL Campaigns]视图中的<!-- insert links -->广告组和版面设置，为每个广告组创建版面，并指定显示网络上要为每个广告组定位的页面。

**[!UICONTROL Languages]：** （仅限[!DNL Google Ads]个搜索和显示网络）促销活动中广告的一个或多个目标语言。

[!DNL Google Ads]根据用户的[!DNL Google]语言设置或搜索查询的语言、当前页面或最近在[!DNL Google Display Network]上查看的页面确定用户的语言。

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]：** （仅具有最终/高级URL的帐户）广告组级别跟踪模板，该模板指定所有离登陆域重定向和跟踪参数，并将最终URL嵌入到参数中。

对于Adobe Advertising转化跟踪（在营销活动设置包括“[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]”时应用），Search、Social和Commerce会在您保存记录时自动附加重定向和跟踪代码。

对于第三方重定向和跟踪，请输入一个值。 要指示登陆页面URL，请执行以下操作：

* 适用于Yahoo！ Japan Ads帐户，使用参数{lpurl}。

* 有关Microsoft Advertising和Google Ads帐户可用的参数，请参阅[[!DNL Google Ads] 文档](https://support.google.com/google-ads/answer/6305348)中“可用的[!DNL ValueTrack]参数”部分的[[!DNL Microsoft Advertising] 文档](https://help.ads.microsoft.com/#apex/3/en/56799)或“仅跟踪模板”参数。

此值将覆盖帐户级别和营销活动级别的设置，但更细粒度级别（以关键词最细粒度）的跟踪模板将覆盖此值。

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Keywords]

**[!UICONTROL Keywords]：**&#x200B;指定广告组（或[!DNL Yandex]帐户的营销活动）的关键字，这些关键字可由静态文本、指定文件中的列和修饰符的任意组合组成。 通过模板传播指定的馈送文件时，列名和修饰符将替换为实际数据。

要将列名或修饰符组作为动态参数插入，请单击输入字段，然后单击列列表中的列名或修饰符列表中的[修饰符名称](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md)。 要为同一关键字指定多个关键字或多个匹配类型，请在单独的行中输入它们。 要指定关键字匹配类型，请在列名前后使用以下匹配类型语法：

* 对于[!DNL Google Ads]、[!DNL Microsoft Advertising]和[!DNL Yahoo! Japan Ads]模板：

   * 对于动态参数： Broad Match = `[keyword]`，[!UICONTROL Keyword]列中第一个词的Broad Match修饰符（如+blue suede shoes） = `+[keyword]`， Keyword列中每个词的Broad Match修饰符（如+blue +suede +shoes） = `+[keyword]+`，短语匹配= `"[keyword]"`，完全匹配= `[[keyword]]`

   * 对于静态关键字：广泛匹配= `keyword`，广泛匹配修饰符= `+keyword`，或短语匹配= `"keyword"`

     您无法在此处输入具有完全匹配和标准匹配语法的静态关键字，因为它们被括号(`[]`)括起来，就像动态参数一样。

* 对于[!DNL Yandex]模板：

   * 对于动态参数：插入列名称，如`[keyword]`。 要指示匹配类型，请使用特定于[[!DNL Yandex]的语法](https://yandex.com/support/direct/keywords/symbols-and-operators.html)。 **注意：**&#x200B;对于广泛匹配项，请使用以下语法：“关键字”列中第一个项的Broad Match修饰符（如+blue suede shoes） = `+[keyword]`，“关键字”列中每个项的Broad Match修饰符（如+blue +suede +shoes） = `+[keyword]+`

   * 对于静态关键字：仅支持搜索关键字。 对关键字使用特定于[[!DNL Yandex]的语法](https://yandex.com/support/direct/keywords/symbols-and-operators.html)。 不支持用于指示单词顺序的括号(`[]`)。

>[!NOTE]
>
>* 通过在关键字参数之前或之后（但并非同时在这两处）将逗号分隔的值包含在括号中，您可以在“关键字”字段中手动包含多个修饰符值。 例如，`(cheap, discount, affordable)[product]`为每个产品生成三个单独的广告。
>* 如果未指定匹配类型，则使用默认匹配类型“broad”。
>* 不支持负匹配。
>* Google广泛匹配修饰符现在具有与某些语言的短语匹配相同的匹配行为，并且您无法创建新的广泛匹配修饰符关键字。 有关详细信息，请参阅[[!DNL Google Ads] 文档](https://support.google.com/google-ads/answer/10286719)。

**[!UICONTROL Map Only]：**&#x200B;将任何新广告添加到在其中找到指定关键字的广告组（或[!DNL Yandex]帐户的营销活动），而不是创建新关键字。 要启用此选项，请选中复选框。 启用此选项后，指定关键字中的任何Param 1和Param 2变量均不适用，因为存在关键字。

**[!UICONTROL Keyword Final URL]：** （具有最终/高级URL的帐户；可选）广告网络用户单击您的广告时获得的登陆页面URL。 它必须包含与显示URL相同的域，并且最终URL中的任何参数都必须与广告单击后登陆页面URL中的参数相匹配。 登陆页面域或子域中可能包含重定向，但登陆页面域外部则不包含重定向。

如果您使用[!DNL Google Merchant Center]信息源并将此值包含在“[!DNL Link]”列中，请将该列插入此字段。

>[!NOTE]
>
>* 如果在发布通过模板传播的数据时生成跟踪URL，则跟踪参数会根据帐户跟踪设置附加到此值。
>* （[!DNL Google Ads]个帐户）避免使用宏，宏不会替代来自启用并行跟踪的源的点击。 如果广告商必须使用宏，则Adobe客户团队应与客户支持或实施团队合作来添加宏。

**[!UICONTROL Keyword Tracking Template]：** （具有最终/高级URL的帐户；可选）跟踪模板，该模板指定所有登陆/登陆域重定向和跟踪参数，并将最终URL嵌入到参数中。 最细粒度级别的跟踪模板（以关键字作为最细粒度级别）会覆盖所有其他级别的值。

* 对于Adobe Advertising转化跟踪（在营销活动设置包括“[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]”时应用），Search、Social和Commerce会在您保存记录时自动附加重定向和跟踪代码。

* 您可以选择输入第三方重定向和跟踪。

* 要指示登陆页面URL，请执行以下操作：

   * （仅限[!DNL Google Ads]和[!DNL Microsoft Advertising]）有关指示跟踪模板中最终URL的参数列表，请参阅[[!DNL Google Ads] 文档](https://support.google.com/google-ads/answer/6305348)中“可用的[!DNL ValueTrack]参数”部分中的（[!DNL Microsoft Advertising]仅限）[[!DNL Microsoft Advertising] 文档](https://help.ads.microsoft.com/#apex/3/en/56799)或（[!DNL Google Ads]仅限）跟踪模板参数。

   * （仅限[!DNL Yahoo! Japan Ads]）使用参数`!{lpurl}`指示登陆页面URL。

**[!UICONTROL Param 1]**，**[!UICONTROL Param 2]\[[!DNL Google Ads]模板\]：** （仅限[!DNL Google Ads]模板）指定文件中表示[!DNL Google Ads] `{param1}`或`{param2}`变量的列，您可以将其包含在使用该模板创建的任何广告的广告复制或显示URL中。 要插入动态参数，请在输入字段中单击，然后单击列列表中的列名。 通过模板传播馈送文件时，列名称会替换为实际数据。

如果使用任一参数，则可以选择仅将参数应用到新关键字，或者同时更新不是从模板创建的现有关键字的值：

* **[!UICONTROL Do Not Apply to Existing Keywords]** （默认值）：只为使用该模板创建的新关键字插入参数的值。

* **[!UICONTROL Apply to Existing Keywords: Constant]：**&#x200B;除了从信息源创建新关键字外，Search、Social和Commerce还会更新广告组中所有现有关键字（不是使用模板创建的）的参数值。 输入用于所有这些关键字的单个数值。 模板必须至少包含一个关键字。

* **[!UICONTROL Apply to Existing Keywords: Min]：**&#x200B;除了从信息源创建新关键字外，Search、Social和Commerce还会更新广告组中所有现有关键字（不是使用模板创建的）的参数值，前提是信息源文件包含参数的数字值，最多包含一个小数点，但不包含逗号、货币符号或代码或任何其他字符。 馈送文件中参数的最小值用于所有现有关键词。 例如，如果信息源文件具有[!UICONTROL Param1]个值(21500和22000)，则现有关键字的[!UICONTROL Param1]值将更改为21500。 模板必须至少包含一个关键字。 **提示：**&#x200B;只有在您严格设置了广告组主题以便关键字具有相同的值时才使用此选项。

馈送文件中的数据字段最长可包含25个字符，并且只能由具有以下非数字字符的数字数据组成：

* （使用“[!UICONTROL Apply to Existing Keywords: Min]”参数时）最多只能有一个小数点。

* （当您不使用&quot;[!UICONTROL Apply to Existing Keywords: Min]&quot;参数时）：

   * 值可以添加货币符号或代码，也可以添加货币符号或代码。 例如，2.000,000英镑和2000GBP有效。

   * 该值可以包括逗号(，)或句点(.) 作为分隔符，带可选句点(.) 或逗号(，)表示小数值。 例如，1,000.00和2.000,10有效。

   * 该值可以添加前缀，也可以附加百分号(%)、加号(+)或减号(-)。 例如， 20% 、 208+和–42.32有效。

   * 两个数字可以用正斜杠嵌入。 例如，4/1和0.95/0.45有效。

**[!UICONTROL Param 2]\[[!DNL Microsoft Advertising]模板\]：** （仅限[!DNL Microsoft Advertising]模板）在标题、文本、显示URL或最终URL包含`{Param2}`动态替换字符串时，用作广告中替换值的字符串。 最大长度为70个字符，但请注意，在其中使用它的广告元素的最大长度（例如，广告标题最多可包含25个字符）。

**[!UICONTROL Param 3]：** （仅限[!DNL Microsoft Advertising]模板）在标题、文本、显示URL或最终URL包含`{Param3}`动态替换字符串时，用作广告中替换值的字符串。 最大长度为70个字符，但请注意，在其中使用它的广告元素的最大长度（例如，广告标题最多可包含25个字符）。

**[!UICONTROL Initial Bid (&lt;Match Type or Ad Type>)]：**&#x200B;具有指定匹配类型或广告类型的每个关键字的初始出价。

## [!UICONTROL Ads]

**[!UICONTROL Ad Type]：** （仅限[!DNL Google Ads]和[!DNL Microsoft Advertising]促销活动）广告类型： *[!UICONTROL Expanded Search Ads]*&#x200B;或&#x200B;*[!UICONTROL Responsive Search Ads]*。

**[!UICONTROL Prefill]：**（可选）使用原始广告副本字段中的文本预填充所有备用广告副本字段。

### [!UICONTROL Headlines]

**[!UICONTROL Pin]：** （仅限响应式搜索广告）必须包含标题/标题的广告位置（如&quot;[!UICONTROL Pinned at position 1]&quot;）。 默认值为[!UICONTROL Unpinned]。

每个职位必须至少有一个标题。 如果将多个标题固定到同一位置，则最终广告始终会在指定位置包含这些标题之一。 固定到位置3的标题不能与广告一起显示。

**[!UICONTROL Headline 1]**，**[!UICONTROL Headline 2]**，**[!UICONTROL Headline 3]：** （仅限响应式搜索广告）广告标题（标题）。 每个广告变体必须至少包括三个广告标题，最多包括15个广告标题。 广告网络显示最多有三个标题的广告。 每个标题的最大长度为30个字符，包括任何动态文本（例如关键字和广告自定义项的值）。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Ad Title]：** (现有Microsoft Advertising标准文字广告仅限；只读)广告的标题或第一行。 Microsoft Advertising已弃用创建和编辑标准文字广告。

**[!UICONTROL Headline 1]**，**[!UICONTROL Headline 2]：** （仅[!DNL Google Ads]和[!DNL Yahoo! Japan Ads]扩展/扩展文本广告模板）广告的标题。 每行的最大长度（替换任何动态参数后）为30个字符或15个双字节字符。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Headline 3]：** （[!DNL Google Ads]仅扩展了文本广告模板；可选）广告的第三个标题。 最大长度（替换任何动态参数后）为30个字符或15个双字节字符。

**[!UICONTROL Title]：** （仅限[!DNL Yandex]）广告的标题或第一行。 最多为33个字符。

**[!UICONTROL Title Part 1]**，**[!UICONTROL Title Part 2]：** (Microsoft Advertising仅扩展了文本广告)广告的标题。 每行的最大长度（替换任何动态参数后）为30个字符或15个双字节字符。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Ad Text]：** (Microsoft Advertising仅扩展了文字广告)广告正文。 最大长度（替换任何动态参数后）为80个字符或40个双字节字符（例如中文、日语和韩语）。

### [!UICONTROL Descriptions]

**[!UICONTROL Description]：**&#x200B;广告正文。

* (Google Ads扩展的文本广告模板)最大长度（替换任何动态参数后）为90个字符或45个双字节字符。

* (Yahoo！ 日本广告模板)最大长度（替换任何动态参数后）为80个字符或40个双字节字符。

* （Yandex模板）最大长度（替换任何动态参数后）为75个字符，单个单词不能超过22个字符。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-dynamic-parameter}}

**[!UICONTROL Pin]：** （仅限响应式搜索广告）必须包含描述的广告位置（如“[!UICONTROL Pinned at position 1]”）。 默认值为[!UICONTROL Unpinned]。 每个职位必须至少有一个描述。

如果将多个描述固定到同一位置，则最终广告始终会在指定位置包含这些描述之一。 固定到位置2的描述可能无法与广告一起显示。

**[!UICONTROL Description 1]**，**[!UICONTROL Description 2]：** （仅限响应式搜索广告）广告描述。 每个广告变体必须至少包括两个、最多四个广告描述。 广告网络显示的广告最多包含两个描述；至少输入两个。 每个描述的最大长度为90个字符，包括任何动态文本（例如关键字和广告自定义项的值）。

<!-- using a snippet for the note instead of an include because this is used multiple times on the page, which ExL doesn't support for includes -->

{{inventory-feed-template-insert-ad-customizer}}

**[!UICONTROL Description 2]：** (Google仅扩展了文本广告模板；可选)广告的第二行。 最大长度（替换任何动态参数后）为90个字符或45个双字节字符。

### [!UICONTROL Path]

**[!UICONTROL Display Path 1]**，**[!UICONTROL Display Path 2]：** （仅限扩展文本和响应式搜索广告；可选）要在基本URL之后连续包含的一或两个URL路径。 他们应在广告中更详细地描述产品或服务。 例如，如果将[!UICONTROL Display Path 1]个“鞋子”和[!UICONTROL Display Path 2]个“户外”添加到基本URL www.example.com中，则URL为www.example.com/Shoes/Outdoor。 每个字段的最大长度（替换任何动态参数后）为15个字符或7个双字节字符。

对于响应式搜索广告，请使用以下格式插入广告自定义程序，其中`Default text`是当馈送文件不包含有效值时要插入的可选值：

* [!DNL Google Ads]： `{CUSTOMIZER.AdCustomizerName:Default text}`，如`{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]： `{CUSTOMIZER.Attribute name:Default text}`，如`{CUSTOMIZER.Discount:10%}`

**[!UICONTROL Display URL]：** （仅限现有[!DNL Microsoft Advertising]和[!DNL Yahoo! Japan Ads]标准文字广告；只读）广告中显示的URL。

[!DNL Microsoft Advertising]和[!DNL Yahoo! Japan Ads]已弃用创建和编辑标准文字广告。

**[!UICONTROL Base URL]：** （仅具有目标URL的帐户）用户所属的页面。 它可以包含第三方重定向和跟踪代码。 如果您使用Adobe Advertising转化跟踪服务，并且促销活动设置包括使用[!UICONTROL EF Redirect]和在广告级别添加跟踪，则Search、Social和Commerce会自动将其自身的重定向和跟踪代码添加到广告中。

要将列名或修饰符组作为动态参数插入，请单击输入字段，然后单击列列表中的列名或[!UICONTROL Modifiers]列表中的[修饰符名称](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md)。

**[!UICONTROL Final URL]：** （具有最终/高级URL的帐户）用户单击您的广告时获得的登陆页面URL。 它必须包含与显示URL相同的域，并且最终URL中的任何参数都必须与广告单击后登陆页面URL中的参数相匹配。 登陆页面域或子域中可能包含重定向，但登陆页面域外部则不包含重定向。

如果您使用[!DNL Google Merchant]中心馈送并将此值包含在“[!UICONTROL Link]”列中，请将该列插入此字段。

>[!NOTE]
>
>* 如果在发布通过模板传播的数据时生成跟踪URL，则跟踪参数会根据帐户跟踪设置附加到此值。
>* （[!DNL Google Ads]个帐户）避免使用宏，宏不会替代来自启用并行跟踪的源的点击。 如果广告商必须使用宏，则Adobe客户团队应与客户支持或实施团队合作来添加宏。

**[!UICONTROL Tracking Template]：** （具有最终/高级URL的帐户；可选）跟踪模板，该模板指定所有登陆/登陆域重定向和跟踪参数，并将最终URL嵌入到参数中。 最细粒度级别的跟踪模板（以关键字作为最细粒度级别）会覆盖所有其他级别的值。

对于Adobe Advertising转化跟踪（在营销活动设置包括“[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]”时应用），Search、Social和Commerce会在您保存记录时自动附加重定向和跟踪代码。

对于第三方重定向和跟踪，请输入一个值。 要指示登陆页面URL，请执行以下操作：

* 适用于Yahoo！ Japan Ads帐户，使用参数{lpurl}。

* 有关Microsoft Advertising和Google Ads帐户可用的参数，请参阅[[!DNL Google Ads] 文档](https://support.google.com/google-ads/answer/6305348)中“可用的[!DNL ValueTrack]参数”部分的[[!DNL Microsoft Advertising] 文档](https://help.ads.microsoft.com/#apex/3/en/56799)或“仅跟踪模板”参数。

**\[原始广告字段下的备用广告字段\]：**（可选）广告的备用广告副本集，如果原始广告副本中的任何行超过了传播期间使用数据填充任何动态参数后允许的最大长度，则可以使用该广告副本。

>[!NOTE]
>
>* 如果选择了[!UICONTROL Prefill]选项，则备用字段会预填充原始字段，您可以根据需要编辑它们。
>* 只有超出最大长度的广告文案字段会被替换成替换值。 例如，如果只有原始标题或标题太长，则生成的广告变体使用替代标题或标题以及原始描述。 因此，请确保将备用广告副本与原始广告副本结合使用时有意义。
>* 如果原始广告副本满足搜索引擎的长度要求，则会丢弃替代广告副本。

**\[Component\] [!UICONTROL Ad Label Classifications] > \[Label Classification and Value\]：** （可选）要分配给使用模板创建或编辑的广告变体的最多五个现有标签分类的值。 对于要为其分配标签分类的每个促销活动组件：

1. 单击该复选框。

1. 为广告变体模板配置标签分类值：

   * 对于要分配给组件的每个标签分类和值，请执行以下操作：

      1. 单击&#x200B;**[!UICONTROL Add Label Classification]**。

      1. 选择现有标签分类，然后选择现有值或输入新值。

         每个值的最大长度为100个字符，可包含ASCII和非ASCII字符。

         要插入列名作为标签分类值的动态参数，请在输入字段（第二个字段）中单击，然后单击列列表中的列名。

         每个活动组件的每个分类只能包含一个值。 例如，促销活动可以为Color=Red，但不能为Color=Red和Color=Blue。

         * 要更改现有标签分类值，请选择或输入新值。

         * 要删除现有的标签分类值，请单击该值旁边的&#x200B;**[!UICONTROL X]**。

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [关于使用库存信息源自动进行广告管理](../inventory-feeds-about.md)
>* [管理修饰符](../modifiers-manage.md)
>* [管理清单数据馈送文件](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [通过模板传播馈送数据](../feed-data-propagate.md)
>* [将来自库存馈送的促销活动数据发布到广告网络](../propagated-data-post.md)
