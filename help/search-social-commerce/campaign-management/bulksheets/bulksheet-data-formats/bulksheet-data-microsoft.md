---
title: ' [!DNL Microsoft Advertising] 帐户所需的批量处理工作表数据'
description: 引用 [!DNL Microsoft Advertising] 帐户批量工作表中必需的标题字段和数据字段。
exl-id: 2a5f0e7b-f020-4cca-9b77-807c2ee5c273
feature: Search Bulksheets
source-git-commit: 7a87d3c3827125adb97f50986823568c9aef8c24
workflow-type: tm+mt
source-wordcount: '6895'
ht-degree: 0%

---

# 附录 — [!DNL Microsoft Advertising]帐户必需的批量处理工作表数据

要批量创建和更新[!DNL Microsoft Advertising]营销活动数据，您可以使用专门为[!DNL Microsoft Advertising]帐户设置格式的Search、Social和Commerce批量工作表文件。 您可以a) [为现有帐户](../bulksheet-download.md)生成所需文件格式的批量工作表文件，或b)手动创建这些文件（有关支持的文件格式的一般信息，请参阅[支持的批量工作表文件格式](bulksheet-file-formats.md)）。

每个批量工作表必须包含要执行[特定操作](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md)（如创建广告）所需的标题字段和相应的数据字段。 当字段不是必填字段时，您可以从标题行和数据行中忽略该字段。 上传批量工作表文件时将删除所有自定义列。

以下表格包含所有可用的数据字段和其他表格，这些表格指示添加、编辑或删除单个实体的数据（例如营销活动和关键字）时需要哪些字段。

## 所有可用数据字段 {#bulksheet-fields-all-microsoft}

下表描述了所有可用的数据字段。

有关与帐户实体相关的数据字段，请参阅“[创建、编辑或删除每个帐户组件](#bulksheet-fields-per-component-microsoft)所需的字段”。

| 字段 | 描述 |
|----|----|
| [!UICONTROL Platform] | （包含在生成的批量工作表中，以供参考）广告平台。 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Acct Name] | 标识广告网络帐户的唯一名称。 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 为帐户标识营销活动的唯一名称。 最大长度为128个字符。 |
| [!UICONTROL Campaign Budget] | 每日或每月营销活动预算，无论是否带有货币符号和标点。 不能小于0.05。 |
| [!UICONTROL Channel Type] | 营销活动定位的渠道类型： <i>[!UICONTROL Audience]</i>、<i>[!UICONTROL DynamicSearchAds]</i>、<i>[!UICONTROL Search]</i>或<i>[!UICONTROL Shopping]</i>。 |
| [!UICONTROL Delivery Method] | （仅限具有每日预算的促销活动）如何快速显示促销活动的每日广告：<ul><li><i>[!UICONTROL Standard (Distributed)]</i>（新营销活动的默认值）：用于将广告展示次数分散到一整天里。</li><li><i>[!UICONTROL Accelerated]：</i>在达到预算之前，尽可能多地显示您的广告。 因此，您的广告可能不会在当天晚些时候显示。</li></ul> |
| [!UICONTROL Campaign Priority] | （仅限购物营销活动）当多个营销活动播发同一产品时，使用该营销活动的优先级：<i>[!UICONTROL Low]</i>（新营销活动的默认值）、<i>[!UICONTROL Medium]</i>或<i>[!UICONTROL High]</i>。<br><br>如果同一产品包含在多个促销活动中，广告网络会首先使用促销活动优先级来确定哪个促销活动（及相关竞价）符合广告竞价的条件。 如果所有促销活动具有相同的优先级，则具有最高竞价的促销活动符合条件。 |
| [!UICONTROL Merchant ID] | （仅限链接到商家馈送的购物营销活动和受众营销活动）其产品用于营销活动的商家帐户的客户ID。 |
| [!UICONTROL Sales Country] | （仅限购物营销活动；现有营销活动为只读）营销活动产品销售的国家/地区。 由于产品与目标国家/地区相关联，因此此设置确定在营销活动中广告的产品。 |
| [!UICONTROL Product Scope Filter] | （仅限使用购物网络的促销活动）您的商家帐户中的产品，可以为促销活动创建产品广告。 您可以使用格式dimension=attribute最多输入七种产品维度和属性组合，以筛选产品。 使用“>>”分隔符分隔多个过滤器。 有关可用产品维度的列表，请参阅“[购物营销活动产品过滤器](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)”。<br><br>示例：“`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`”<br><br>要删除现有值，请使用值`[delete]`（包括括号）。 |
| [!UICONTROL DSA Domain Name] | （类型为a）“<i>[!UICONTROL DynamicSearchAds]</i>”或b)“<i>[!UICONTROL Search]</i>”的营销活动（未设置[!DNL ExperimentId]元素时）动态搜索广告所定位的网站的域名。 最大长度为2,048个字符。 如果域名包含`www`，则已修剪而不使用。<br><br>对于现有营销活动，您无法编辑域，但必须包含该域才能更新其他属性。 |
| [!UICONTROL DSA Domain Language] | （类型为a） &quot;<i>[!UICONTROL DynamicSearchAds]</i>&quot;或b) &quot;<i>[!UICONTROL Search]</i>&quot; （未设置[!DNL ExperimentId]元素时）动态搜索广告的目标网站页面的语言。 支持的域语言为[!UICONTROL Dutch]、[!UICONTROL English]、[!UICONTROL French]、[!UICONTROL German]、[!UICONTROL Italian]、[!UICONTROL Spanish]和[!UICONTROL Swedish]。<br><br>对于现有营销活动，您无法编辑语言，但必须包含该语言才能更新其他属性。 |
| [!UICONTROL Ad Group Name] | 标识广告组的唯一名称。 最大长度为128个字符。 不保存尾随空白字符（例如，“广告组1”另存为“广告组1”）。 |
| [!UICONTROL Ad Group Type] | （搜索网络上的营销活动；现有广告组的只读）广告组类型： <i>[!UICONTROL Audience]</i>（仅适用于受众营销活动）、<i>[!UICONTROL Search Dynamic]</i>（仅适用于动态搜索广告）和<i>[!UICONTROL Search Standard]</i>（仅适用于响应式搜索广告和现有的扩展文本广告）。 某些营销活动类型可以包括多种广告组类型。 |
| [!UICONTROL Keyword] | （仅限搜索网络上的促销活动）关键词字符串。 最大长度为50个字符。<br><br><b>注释：</b><ul><li>要在广告组或营销活动级别排除关键字，请将[!UICONTROL Match Type]设置为`Negative`。 如果行包含广告组名称，则会为广告组排除关键字。 如果行不包含广告组名称，则该关键字将排除在整个营销活动中。</li><li>更改[!DNL Microsoft Advertising]关键字会删除现有关键字，并使用新的关键字ID创建新关键字。 但是，更改匹配类型不会删除现有关键字。</li></ul> |
| 投放 | 已弃用 |
| [!UICONTROL Audience] | 搜索广告的再营销列表(RLSA)以促销活动或广告组的受众为目标。 |
| [!UICONTROL Target Type] | （仅限RLSA目标）目标类型： <i>[!UICONTROL Inclusion]</i>或<i>[!UICONTROL Exclusion]</i>。 |
| [!UICONTROL Auto Target Expression] | 广告组的动态搜索目标。 对于所有目标，请使用“[!UICONTROL All Web Pages]”。<br><br>若要定位最多三个动态搜索条件，请使用格式`<category>=<target>`，其中&lt;category>可以包含以下任意类别。 使用“`[blank space] and [blank space]`”为单个类别连接多个目标，使用“`[blank space] and [blank space]`”为多个类别连接。<br><ul><li><i>类别：</i>为具有特定Google内容类别的索引页面显示动态搜索广告。</li><li><i>URL：</i>显示具有特定URL的索引页面的动态搜索广告，其中值可能包含在URL中的任何位置。</li><li><i>页面标题：</i>显示索引页面的动态搜索广告，这些索引页面在页面标题中具有特定文本。</li><li><i>页面内容：</i>为具有特定内容的索引页面显示动态搜索广告。</li></ul>示例： url=shoes.example.com and page title=footwear<br>示例：所有网页 |
| [!UICONTROL Location] | 为营销活动或广告组放置广告的地理位置；值不区分大小写。 如果您没有为营销活动或广告组输入任何值，则所有位置都会被定位。 若要定位特定位置，请使用[!DNL Microsoft Advertising]位置代码格式输入位置。 要下载位置列表，请使用您的[!DNL Microsoft Advertising]广告帐户凭据登录到[!DNL Microsoft Advertising]开发人员门户。 <b>注意：</b>若要排除位置，请在位置代码前面加一个减号(`-`)，如`-United States`。 |
| [!UICONTROL Location Type] | 位置类型，如城市、国家/地区、都市区、邮政编码和州/省。 要下载位置列表，请使用您的[!DNL Microsoft Advertising]广告帐户凭据登录到[!DNL Microsoft Advertising]开发人员门户。 |
| [!UICONTROL Match Type] | （仅限搜索网络上的促销活动）关键词匹配选项。 这可能包括动态搜索目标或产品组的关键字匹配选项。 值包括： <i>[!UICONTROL Broad]</i> （新关键字的默认值）、<i>[!UICONTROL Exact]</i>、<i>[!UICONTROL Phrase]</i>、<i>[!UICONTROL Content]</i> （当广告组定位内容网络时自动为关键字设置）、<i>[!UICONTROL Negative]</i> （排除内容网络上的关键字）、<i>[!UICONTROL Dynamic Ad Target]</i> （新动态搜索目标的默认值）、<i>[!UICONTROL Product Group]</i> （新产品组的默认值）或<i>[!UICONTROL Negative Product Group]</i> （排除产品组）。  要编辑或删除具有多个匹配类型的关键字，需要匹配类型或关键字ID的值。<br><br>对于Broad Match Modifier，请选择“Broad”，并在关键词中需要的任何单词前插入`+`（如“`+red +shoes`”，要求“红色”和“鞋子”）。<br><br>更改[!DNL Microsoft Advertising]关键字的匹配类型不会删除现有关键字。 |
| [!UICONTROL Max CPC] | （搜索网络上的促销活动）最大每次点击成本(CPC)，这是根据关键词、产品组或动态搜索目标为广告点击支付的最高金额，无论是否带有货币符号和标点。  对于优化项目组合中的现有关键字和产品组记录，更新仅在一天内有效，并在下一个优化周期中被覆盖。 <b>注意：</b>不能为负关键字设置出价。 |
| [!UICONTROL Max Content CPC] | （对于在内容网络之前创建的CPC营销活动，只读，仅在2017年弃用）每次点击的最大内容成本(CPC)，这是为来自显示网络站点的广告点击支付的最高金额，无论是否带有货币符号和标点。 |
| [!UICONTROL Audience Target Method] | （受众广告组）是否：<ul><li><i>[!UICONTROL Target and Bid]：</i>只向与满足广告组任何其他目标的目标受众相关联的用户显示广告。</li><li><i>[!UICONTROL Bid Only]：</i>为了向不与目标受众关联的用户显示广告，只要他们满足其他广告组级别的目标。</li></ul> 但是，您可以通过为特定受众设置更高的竞价来增加向这些受众显示广告的可能性。 |
| [!UICONTROL Parent Product Groupings] | 任何父产品组的层次结构。<br><br>示例： `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | 产品组（如“brand=acme”或“所有产品”）。<br><br><b>注释：</b><ul><li>当指定的产品组在父产品组层次结构中不存在时，Search、Social和Commerce会创建层次结构中所需的任何部分。</li><li>当您在购物营销活动中使用设置为广告组默认竞价的广告组创建广告组时，搜索、Social和Commerce会自动创建“[!UICONTROL All Products]”组。 Search、Social和Commerce会在产品组层次结构的每个级别自动创建一个具有广告组默认竞价的“[!UICONTROL Everything Else]”组。 您仍然可以显式创建这些默认组，并排除它们或更改它们的竞价。</li><li>每个广告组最多可包含八层产品组，包括“[!UICONTROL All Products]”和七个其他层。</li></ul> |
| [!UICONTROL Partition Type] | 产品组的分区类型： <i>[!UICONTROL subdivision]</i> （当它有子产品组时）或<i>[!UICONTROL unit]</i> （当它没有子产品组时）。 |
| [!UICONTROL Ad Title]，[!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | （仅限扩展的文本广告、多媒体广告、响应式广告和响应式搜索广告）广告的头条。 每个广告标题字段的最大长度为30个字符或15个双字节字符，包括任何动态文本（例如关键字、`{Param2}`和`{Param3}`动态替代变量以及广告自定义项的值）。<br><br>对于响应式搜索广告，请使用以下格式插入广告自定义程序，其中“默认文本”是当馈送文件不包含有效值时要插入的可选值： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>对于展开的文本广告，广告标题和广告标题2是必需的，而[!UICONTROL Ad Title 3]是可选的。 [!DNL Microsoft Advertising]已于2022年8月弃用扩展文本广告，您现在只能报告和删除它们。<br><br>对于多媒体广告、响应式广告和响应式搜索广告，[!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]和[!UICONTROL Ad Title 3]是必需的，所有其他广告标题字段都是可选的。<br><br>要删除非必填字段的现有值，请使用值`[delete]`（包括括号）。<br><br>对于除扩展文本广告之外的所有广告类型，更改广告副本将删除现有广告并创建具有相同属性的新广告。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | （仅限响应式搜索广告；可选）固定相应广告标题的位置： `[null]`（没有值，因此广告标题适用于所有位置）、1、2或3。 例如，如果[!UICONTROL Ad Title Position]的值为1，则[!UICONTROL Ad Title]只能出现在位置1中。 默认情况下，所有广告标题为空（没有值）。 要删除现有值，请使用值`[delete]`（包括括号）。<br><br><b>注意：</b>您可以将多个广告标题固定到同一位置。 广告网络使用固定到该位置的广告标题之一。 固定到位置3的标题不能与广告一起显示。 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | （仅限文本广告、动态搜索广告、多媒体广告、响应式广告、响应式搜索广告和增强型营销活动级别的站点链接）广告或站点链接的正文。<br><br>对于站点链接，可以选择同时使用[!UICONTROL Description Line 1]和[!UICONTROL Description Line 2]以包含广告网络可能在链接文本下显示的额外文本。 每个描述字段最多可包含35个单字节字符或17个双字节字符。<br><br>对于广告，每个描述字段的最大长度为90个字符或45个双字节字符，包括任何动态文本（例如关键字和广告自定义项的值）。<br><br>对于响应式搜索广告，请使用以下格式插入广告自定义项，其中“默认文本”是当馈送文件不包含有效值时要插入的可选值： `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>对于文本广告和动态搜索广告，说明第1行是必需的，[!UICONTROL Description Line 2]是可选的。<br><br>对于多媒体广告、响应式广告和响应式搜索广告，[!UICONTROL Description Line 1]和[!UICONTROL Description Line 2]是必需的，[!UICONTROL Description Line 3]和[!UICONTROL Description Line 4]是可选的。<br><br>要删除现有值，请使用值`[delete]`（包括括号）。<br><br><b>注释：</b><ul><li>（标准文本广告）组合的标题和文本必须至少为三个字。</li><li>（扩展的文本广告）此字段可以选择包括{Param2}和{Param3}动态替换变量。 如果是，则广告文本的最大长度为300个单字节字符或150个双字节字符。 [!DNL Microsoft Advertising]已于2022年8月弃用扩展文本广告，您现在只能报告和删除它们。</li><li>（动态搜索广告）不允许动态替换文本。</li><li>对于除扩展文本广告之外的所有广告类型，更改广告副本将删除现有广告并创建新广告。</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | （仅限响应式搜索广告；可选）固定相应说明的位置： `[null]`（没有值，因此说明适用于所有位置）、1、2或3。 例如，如果[!UICONTROL Description 1 Position]的值为1，则描述1只能出现在位置1中。 默认情况下，不会将任何描述固定到位置。<br><br>要删除现有值，请使用值`[delete]`（包括括号）。<br><br><b>注意：</b>您可以将多个描述固定到同一位置。 广告网络使用固定到该位置的描述之一。 固定到位置2的描述可能无法与广告一起显示。 |
| [!UICONTROL Business Name] | （仅限多媒体广告）企业名称，最长为25个字符。 |
| [!UICONTROL Promotion Line] | （仅限产品列表广告）要包含在搜索结果中的产品列表的唯一促销行（例如“立即免费送货！”）。 最大长度为45个字符。<br><br>根据广告在页面上的显示位置，促销活动行可能会出现在与广告相关的不同位置（例如广告下方）。 |
| [!UICONTROL Display URL] | 广告中包含的URL。<br><br>对于扩展的动态搜索广告，广告网络从网站域动态生成此值，您无需输入值。<br><br>对于扩展的文本广告和响应式搜索广告，无需输入值。 显示URL将自动从最终URL中的域提取。 您可以选择使用“路径1”和“路径2”字段自定义URL。<br><br><b>注释：</b><ul><li>（具有最终URL的帐户）显示URL和最终URL中的域名必须匹配。</li><li>[!DNL Microsoft Advertising]已于2022年8月弃用扩展文本广告，您现在只能报告和删除它们。</li></ul> |
| [!UICONTROL Display Path 1] | （仅限扩展的文本广告、动态搜索广告和响应式搜索广告）添加到显示URL的文本，将自动从最终URL中提取。 URL中的每个路径前面都有一个正斜杠(/)。 路径不能包含正斜杠(/)或换行符(\n)。 每个路径的最大长度为15个字符或7个双字节字符。<br><br>要插入广告自定义程序，请使用以下格式，其中“默认文本”是当馈送文件不包含有效值时要插入的可选值： `{CUSTOMIZER.Attribute name:Default text}`，如`{CUSTOMIZER.Discount:10%}`<br><br>例如，如果[!UICONTROL Display Path 1]是“交易”，则显示URL将为&lt;显示URL>/交易，如www.example.com/deals。<br><br>[!DNL Microsoft Advertising]已于2022年8月弃用扩展文本广告，您现在只能报告和删除它们。 |
| [!UICONTROL Display Path 1] | （仅限扩展的文本广告、动态搜索广告和响应式搜索广告）其他显示路径；请参阅[!UICONTROL Display Path 1]对应的条目。<br><br>示例：如果[!UICONTROL Display Path 1]为“deals”，[!UICONTROL Display Path 2]为“local”，则显示URL应为&lt;<i>显示URL</i>>/deals/local，如www.example.com/deals/local。 |
| [!UICONTROL Start Date] | （仅限增强型站点链接）对站点链接发出投标的第一个日期，采用广告商所在的时区以及以下格式之一： m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 新的增强型站点链接的默认值为当天。 <b>注意：</b>只能在具有现有增强型站点链接或没有站点链接的营销活动中创建新的增强型站点链接。 |
| [!UICONTROL End Date] | 站点链接可以随广告一起显示的最后日期，以广告商所在的时区为单位并采用以下格式之一： m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 对于新的sitelink，默认值为`[blank]`（即无结束日期）。 |
| [!UICONTROL Call To Action] | 要包含在广告中的call to action。 查看[API引用以获取可能值](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction)的列表，但在批量处理工作表中输入多个单词的调用操作（例如“Bet Now”而不是“BetNow”）。 |
| [!UICONTROL Call To Action Language] | call to action选项的语言。 请参阅[API参考以获取可能语言的列表](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename)。 |
| [!UICONTROL Base URL/Final URL] | 搜索引擎用户在单击您的广告时进入的登陆页面URL，包括为促销活动或帐户配置的任何附加参数。 关键字级别的基本/最终URL将覆盖广告级别和更高级别的URL。<br><br>要删除现有值，请使用值`[delete]`（包括括号）。 |
| [!UICONTROL Destination URL] | （出于提供信息的目的包含在生成的批量工作表中；未发布到搜索引擎）对于具有目标URL的帐户，此URL可将广告链接到广告商网站上的基本URL/登陆页面（有时通过另一个跟踪点击的网站，然后将用户重定向到登陆页面）。 它包括为Search、Social和Commerce营销活动或帐户配置的任何附加参数。 如果您生成了跟踪URL，则跟踪URL将基于帐户设置和促销活动设置中的跟踪参数。 如果附加了特定于搜索引擎的参数，则可能会将其替换为与搜索、社交和Commerce等效的参数。<br><br>对于具有最终URL的帐户，此列显示的值与基本URL/最终URL列显示的值相同。 |
| [!UICONTROL Custom URL Param] | 当搜索帐户或促销活动设置的跟踪参数中包含变量时，用于替代`{custom_code}`动态变量的数据。 要在跟踪URL中插入自定义值，必须使用生成跟踪URL选项上传批量工作表文件。 |
| [!UICONTROL Creative Type] | 广告格式： <i>[!UICONTROL Dynamic Search Ad]</i>、<i>[!UICONTROL Expanded Text Ad]</i>、<i>[!UICONTROL Expanded Dynamic Search Ad]</i>、<i>[!UICONTROL Multimedia Ad]</i>、<i>[!UICONTROL Product Ad]</i>（购物广告）、<i>[!UICONTROL Responsive Search Ad]</i>或<i>[!UICONTROL Text ad]</i>。 新广告的默认值为<i>[!UICONTROL Text ad]</i>。 |
| [!UICONTROL Ad Group Start Date] | 可以在广告商所在时区且以下列格式之一为广告组投标的第一个日期：m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 对于新的广告组，默认日期为当前日期。 |
| [!UICONTROL Ad Group End Date] | 可以在广告商所在的时区以及以下格式之一为广告组投标的最后日期：m/d/yyyy、m/d/yy、m-d-yyyy或m-d-yy。 对于新的广告组，默认值为[blank]（即无结束日期）。 |
| [!UICONTROL Tracking Template] | （可选）跟踪模板，用于指定所有离岸域重定向和跟踪参数，并将最终URL嵌入到参数中。 最粒度级别的跟踪模板（使用关键字作为最粒度级别）将覆盖所有更高级别的值。<br><br>对于Adobe Advertising转化跟踪（在营销活动设置包括“[!UICONTROL EF Redirect]”和“[!UICONTROL Auto Upload]”时应用），Search、Social和Commerce会在您保存记录时自动附加重定向和跟踪代码。<br><br>对于第三方重定向和跟踪，请输入一个值。<br><br>有关指示跟踪模板中最终URL的参数列表，请参阅[!DNL Microsoft Advertising]文档。<br><br>要删除现有值，请使用值`[delete]`（包括括号）。 |
| [!UICONTROL Landing Page Suffix] | 附加到最终URL末尾以跟踪信息的任何参数。 示例：`param2=value1&param3=value2`<br><br>请参见[的 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)点击跟踪格式。<br><br>较低级别的最终URL后缀将覆盖帐户级别的后缀。 为便于维护，除非需要对各个帐户组件进行不同的跟踪，否则请仅使用帐户级别的后缀。 要在广告组级别或更低级别配置后缀，请使用[!DNL Microsoft Advertising]编辑器。 |
| 搜索网络状态 | 是否将广告组的广告放在搜索网络的各种元素上：<ul><li><i>全部：</i>在所有Bing搜索网络和联合搜索合作伙伴上刊登广告。</li><li><i>OwnedAndOperatedOnly：</i>仅在Bing和Yahoo上投放广告！ 网站。</li><li><i>SyndicatedSearchOnly：</i>仅在Bing和Yahoo上投放广告！ 联合搜索合作伙伴。</li><li><i>关：</i>仅在内容网络（而非搜索网络）上刊登广告。</li></ul> 对于新的广告组，默认为“启用”。 |
| [!UICONTROL Content Network Status] | 已弃用 |
| [!UICONTROL Languages] | 广告组中广告的目标语言： [!UICONTROL English]、[!UICONTROL French]、[!UICONTROL Finnish]、[!UICONTROL German]、[!UICONTROL Norwegian]、[!UICONTROL Spanish]或[!UICONTROL Swedish]。 新营销活动的默认值为[!UICONTROL English]。<br><br>此设置确定广告可以显示的国家和地区。 确保选择与营销活动的位置目标兼容的语言。 |
| [!UICONTROL Budget Type] | 预算是<i>[!UICONTROL Daily]</i> （默认）还是<i>[!UICONTROL Monthly]</i>。<br><br>注意：如果将促销活动分配给优化的项目组合，此值将自动设置为[!UICONTROL Daily]。 |
| [!UICONTROL Device] | 在营销活动或广告组级别进行竞价调整的设备类型： <i>[!UICONTROL smartphone]</i>、<i>[!UICONTROL tablet]</i>或<i>[!UICONTROL desktop]</i>。 |
| [!UICONTROL Bid Adjustment] | 指定目标类型的竞价调整。 例如，如果关键词级别的竞价为1美元，而智能手机的竞价调整为50%，则智能手机的竞价为1.50美元。 默认情况下，所有目标均按关键字级别竞价进行竞价。 有效百分比可以包括：<ul><li>智能手机和平板电脑： -100（不为设备类型出价）以及从–90到900</li><li>台式机：从0到900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | 您更喜欢显示广告或站点链接的设备类型： <i>[!UICONTROL All]</i> （默认值）或<i>[!UICONTROL Mobile]</i>。 当指定了“移动设备”时，网络会尝试向移动设备用户（而非桌面或平板电脑用户）显示广告或站点链接。 否则，网络会在任何设备类型上显示广告或站点链接。 <b>注意：</b>网络不保证会在首选设备类型上显示广告。 |
| [!UICONTROL Param2] | 如果关键字的基本URL或广告的标题、描述或基本URL包含`{Param2}`动态替换字符串，则用作替换值的字符串。 最大长度为70个字符，但请注意，在其中使用它的广告元素的最大长度（例如，标题1和标题2组合可能最多为76个字符）。 要删除现有值，请使用值`[delete]`（包括括号）。 |
| [!UICONTROL Param3] | 如果关键字的基本URL或广告的标题、描述或基本URL包含`{Param3}`动态替换字符串，则用作替换值的字符串。 最大长度为70个字符，但请注意，在其中使用它的广告元素的最大长度（例如，标题1和标题2组合可能最多为76个字符）。 要删除现有值，请使用值`[delete]`（包括括号）。 |
| [!UICONTROL Link Name] | 站点链接文本。 它在营销策划中必须是唯一的。 如果指定“说明1”和“说明2”，则站点链接文本最多可包含25个单字节字符或12个双字节字符；否则，站点链接文本最多可包含35个单字节字符或17个双字节字符。<br><br>[!DNL Microsoft Advertising]可以显示带有说明的两个、四个或六个增强型站点链接，也可以显示带有广告的单个行中的四个或六个不带说明的站点链接。<br><br>您只能在具有现有增强型站点链接或没有站点链接的营销活动中创建新的增强型站点链接。 |
| [!UICONTROL Campaign Status] | 营销活动的显示状态： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i>（仅限现有营销活动）。 新营销活动的默认值为[!UICONTROL Active]。 要删除活动或暂停的活动，请输入值`Deleted`。 |
| [!UICONTROL Ad Group Status] | 广告组的显示状态： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i>（仅限现有广告组）。 新广告组的默认值为[!UICONTROL Active]。 要删除活动或暂停的广告组，请输入值`Deleted`。 |
| [!UICONTROL Keyword Status] | 关键字的显示状态： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i> （仅限现有关键字）。 新关键字的默认值为[!UICONTROL Active]。 要删除活动或暂停的关键字，请输入值`Deleted`。 <b>注意：</b>如果您为具有多个匹配类型的关键字创建跟踪URL，则每个匹配类型的关键字状态必须相同。 |
| [!UICONTROL Placement Status] | 已弃用 |
| [!UICONTROL Ad Status] | 广告的显示状态： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Deleted]</i> （仅限现有广告）、<i>[!UICONTROL Disapproved]</i> （不可编辑）或<i>[!UICONTROL Paused]</i>。 新广告的默认值为[!UICONTROL Active]。 要删除活动或暂停的广告，请输入值`Deleted`。 |
| [!UICONTROL Target Status] | 动态搜索目标的状态： <i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>或<i>[!UICONTROL Deleted]</i>（仅限现有目标）。 新目标的默认值为[!UICONTROL Active]。 要删除活动或暂停的目标，请输入值`Deleted`。 |
| [!UICONTROL Sitelink Status] | 站点链接的显示状态： <i>[!UICONTROL Active]</i>或<i>[!UICONTROL Deleted]</i> （仅限现有的站点链接）。 新站点链接的默认值为[!UICONTROL Active]。 要删除活动的站点链接，请输入值`Deleted`。 |
| [!UICONTROL Location Status] | 位置目标的状态： <i>[!UICONTROL Active]</i>或<i>[!UICONTROL Deleted]</i> （仅限现有位置）。 新位置的默认值为[!UICONTROL Active]。 要删除活动位置，请输入值`Deleted`。 |
| [!UICONTROL Product Group Status] | 产品组的显示状态： <i>[!UICONTROL Active]</i>或<i>[!UICONTROL Deleted]</i> （仅限现有产品组）。 新产品组的默认值为[!UICONTROL Active]。 要删除活动的产品组，请输入值`Deleted`。 |
| [!UICONTROL Device Target Status] | 营销活动或广告组级别设备目标的状态： <i>[!UICONTROL Active]</i>或<i>[!UICONTROL Deleted]</i>。 对于新的营销活动和广告组，默认值为[!UICONTROL Active]。 |
| [!UICONTROL RLSA Target Status] | 促销活动或广告组级别RLSA目标或(仅限Google广告)排除的状态： <i>[!UICONTROL Active]</i>或<i>[!UICONTROL Deleted]</i>（仅限现有目标）。 新目标或排除项的默认值为[!UICONTROL Active]。 要删除活动目标或排除项，请输入值`Deleted`。 |
| \[广告商特定的标签分类\] | （以特定于广告商的标签分类命名，例如名为“颜色”的标签分类的“颜色”）与实体关联的指定分类的值。 每个实体的每个分类只能包含一个值（例如，促销活动A的“颜色”标签分类为“红色”）。 最大长度为100个字符，该值可以包含ASCII和非ASCII字符。<br><br>标签分类及其标签值将应用于所有子组件；以后添加的新组件会自动与标签关联。 产品组的标签分类将应用于单元（最细化）级别。<br><br>分类名称和分类值都不区分大小写。 |
| [!UICONTROL Constraints] | 分配给图元的约束。 每个图元只能分配一个约束。<br><b>>约束由子实体继承，因此，除非要覆盖继承的值，否则不需要为子实体输入值。 |
| [!UICONTROL Campaign ID] | 标识现有营销活动的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1]仅在您更改营销活动名称时需要，除非该行包含营销活动的“[!UICONTROL AMO ID]”。 |
| [!UICONTROL Ad Group ID] | 标识现有广告组的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1]仅在您更改促销活动名称时需要，除非行包含广告组的“[!UICONTROL AMO ID]”。 |
| [!UICONTROL Placement ID] | 已弃用 |
| [!UICONTROL Keyword ID] | 标识现有关键字的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1]仅在您更改关键字时才需要，除非该行包含a)足够的属性列来标识关键字，或者b) &quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL Ad ID] | <p>标识现有广告的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1]对于响应式搜索广告，编辑或删除广告数据需要广告ID或AMO ID。 对于所有其他实体类型，只有在更改广告状态时才需要AMO ID，除非该行包含a)足够的广告属性列来标识广告或b)“[!UICONTROL AMO ID]”。 但是，如果您既不包括[!UICONTROL Ad ID]也不包括[!UICONTROL AMO ID]，并且广告属性列匹配多个广告，则只有一个广告的状态会更改。</p><p><b>注意：</b>如果您编辑a)广告属性列（现有广告的状态除外）或b)响应式搜索广告的任何数据，并且既不包括[!UICONTROL Ad ID]也不包括[!UICONTROL AMO ID]，则会创建新广告，并且现有广告不会发生更改。 </p> |
| [!UICONTROL Sitelink ID] | 标识现有站点链接的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1]仅在更改或删除站点链接时需要，除非该行包含a)足够的属性列以标识站点链接或b)“[!UICONTROL AMO ID]”。 但是，如果您既不包括[!UICONTROL Sitelink ID]也不包括[!UICONTROL AMO ID]，并且属性列与多个站点链接匹配，则只有其中一个站点链接的状态会更改。</p><p><b>注意：</b>如果您编辑的站点链接属性列（现有Sitelink的状态除外），并且您既不包括[!UICONTROL Sitelink ID]也不包括[!UICONTROL AMO ID]，则会创建一个新的Sitelink，并且现有Sitelink不会发生更改。 |
| [!UICONTROL Product Group ID] | 标识现有产品组的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1]仅在更改或删除产品组时才需要，除非该行包含a)足够的属性列来标识产品组或b)“[!UICONTROL AMO ID]”。 |
| 位置ID | 位置目标的唯一[!DNL Microsoft Advertising]标识符。 要下载位置列表，请使用您的[!DNL Microsoft Advertising]广告帐户凭据登录到[!DNL Microsoft Advertising]开发人员门户。 仅在更改或删除位置目标时需要，除非行包含目标的“[!UICONTROL AMO ID]”。 |
| [!UICONTROL Target ID] | 标识现有自动目标的唯一ID。 仅在更改或删除自动定位时需要，除非行包含目标的“[!UICONTROL AMO ID]”。 |
| [!UICONTROL RLSA Target ID] | 标识现有营销活动或广告组级别RLSA目标的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1]仅在您更改或删除目标或排除项时需要，除非该行包含目标的“[!UICONTROL AMO ID]”。 |
| [!UICONTROL AMO ID] | （在生成的批量工作表中）Adobe为同步实体生成的唯一标识符。 对于响应式搜索广告，编辑或删除广告时需要AMO ID，除非您包含广告ID。 要编辑所有其他具有AMO ID的实体类型的数据，需要使用AMO ID来编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |
| [!UICONTROL EF Error Message] | （出于信息目的包含在生成的批量工作表中）用于显示来自广告网络的关于行中数据的错误消息的占位符；错误消息包含在[!UICONTROL EF Errors]文件中。 此值未发布到广告网络。 |
| [!UICONTROL SE Error Message] | （出于信息目的包含在生成的批量工作表中）用于显示来自广告网络的关于行中数据的错误消息的占位符；错误消息包含在[!UICONTROL SE Errors]文件中。 此值未发布到广告网络。 |
| [!UICONTROL Exemption Request] | （出于信息目的包含在生成的批量处理工作表中）用于显示广告违反的任何Google广告策略的名称和文本的占位符。 |
| [!UICONTROL Retail Hash] | （包括在使用高级促销活动管理生成的批量处理工作表中的信息用途）字母数字哈希代码(如f9639f40cdf56524b541e5dacf55a991)，表示项目是使用高级(ACM)视图生成的。 |

[^1]： [!DNL Excel]在打开文件时将大数转换为科学记号(如2115585666的2.12E+09)。 要查看标准表示法的位数，请选择列中的任意单元格，然后在公式栏中单击。

## 创建、编辑或删除每个帐户组件所需的字段 {#bulksheet-fields-per-component-microsoft}

以下部分包含与特定帐户实体相关的字段。

>[!NOTE]
>
>当字段不适用于操作时，在字段中输入的任何值都会被忽略。

### 营销活动字段

有关每个数据字段的说明，请参阅“[所有可用数据字段](#bulksheet-fields-all-microsoft)”。

| 字段 | 必需？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必需。 |
| [!UICONTROL Campaign Budget] | 需要创建营销策划。 |
| [!UICONTROL Channel Type] | 需要创建营销策划。 |
| [!UICONTROL Delivery Method] | 可选 |
| [!UICONTROL Campaign Priority] | 需要创建购物营销活动。 |
| [!UICONTROL Merchant ID] | 需要创建购物营销活动。 |
| [!UICONTROL Sales Country] | 需要创建购物营销活动。 |
| [!UICONTROL Product Scope Filter] | （购物营销活动）可选 |
| [!UICONTROL DSA Domain Name] | 需要创建类型为a)“[!UICONTROL DynamicSearchAds]”或b)“[!UICONTROL Search]”的营销活动（如果未设置[!DNL ExperimentId]元素） |
| [!UICONTROL DSA Domain Language] | 需要创建类型为a)“[!UICONTROL DynamicSearchAds]”或b)“[!UICONTROL Search]”的营销活动（如果未设置[!DNL ExperimentId]元素） |
| [!UICONTROL Tracking Template] | 可选 |
| [!UICONTROL Landing Page Suffix] | <p>可选 |
| [!UICONTROL Budget Type] | 需要创建营销策划。 |
| [!UICONTROL Device] | 可选 |
| [!UICONTROL Bid Adjustment] | 可选 |
| [!UICONTROL Campaign Status] | 仅删除营销活动时需要。 |
| \[广告商特定的标签分类\] | 可选 |
| [!UICONTROL Constraints] | 可选 |
| [!UICONTROL Campaign ID] | 仅在更改营销活动名称时需要，除非行包含营销活动的“[!UICONTROL AMO ID]”。 |
| [!UICONTROL AMO ID] | 需要编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |

### 广告组字段

有关每个数据字段的说明，请参阅“[所有可用数据字段](#bulksheet-fields-all-microsoft)”。

| 字段 | 必需？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Ad Group Type] | 需要创建广告组。 |
| [!UICONTROL Audience Target Method] | 仅在创建受众广告组时才需要。 |
| [!UICONTROL Ad Group Start Date] | 可选 |
| [!UICONTROL Ad Group End Date] | 可选 |
| [!UICONTROL Tracking Template] | 可选 |
| [!UICONTROL Search Network Status] | （仅限搜索网络上的营销活动）可选 |
| [!UICONTROL Languages] | 可选 |
| [!UICONTROL Device] | 可选 |
| [!UICONTROL Bid Adjustment] | 可选 |
| [!UICONTROL Ad Group Status] | 仅删除广告组时才需要。 |
| \[广告商特定的标签分类\] | 可选 |
| [!UICONTROL Constraints] | 可选 |
| [!UICONTROL Ad Group ID] | 仅在更改广告组名称时需要，除非行包含广告组的“[!UICONTROL AMO ID]”。 |
| [!UICONTROL AMO ID] | 需要编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |

### 关键字字段

有关每个数据字段的说明，请参阅“[所有可用数据字段](#bulksheet-fields-all-microsoft)”。

| 字段 | 必需？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Keyword] | 必填 |
| [!UICONTROL Match Type] | 要编辑或删除具有多个匹配类型的关键字，需要匹配类型或关键字ID的值。 |
| [!UICONTROL Max CPC] | 可选 |
| [!UICONTROL Base URL/Final URL] | 可选 |
| [!UICONTROL Custom URL Param] | 可选 |
| [!UICONTROL Tracking Template] | 可选 |
| [!UICONTROL Param1] | 可选 |
| [!UICONTROL Param2] | 可选 |
| [!UICONTROL Keyword Status] | 仅删除关键字时才需要。 |
| \[广告商特定的标签分类\] | 可选 |
| [!UICONTROL Constraints] | 可选 |
| [!UICONTROL Campaign ID] | 可选 |
| [!UICONTROL Ad Group ID] | 可选 |
| [!UICONTROL Keyword ID] | 仅当编辑或删除关键字时才需要此变量，除非该行包含a)足以标识关键字的属性列或b) &quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL AMO ID] | 需要编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |

### 动态搜索广告字段

>[!NOTE]
>
>创建支持不可用。

对于此广告类型，请使用[!UICONTROL Creative (except RSA)]对话框中的“[!UICONTROL Download Bulksheet]”行。

有关每个数据字段的说明，请参阅“[所有可用数据字段](#bulksheet-fields-all-microsoft)”。

| 字段 | 必需？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | 需要编辑描述。 <b>注意：</b>对于此广告类型，更改广告副本将删除现有广告并创建新广告。 |
| [!UICONTROL Display Path 1] | 需要此项才能编辑字段。 |
| [!UICONTROL Display Path 2] | 需要此项才能编辑字段。 |
| [!UICONTROL Creative Type] | 需要创建或编辑产品广告的状态。 |
| [!UICONTROL Creative Preferred Devices] | 可选 |
| [!UICONTROL Ad Status] | 删除广告时需要。 |
| \[广告商特定的标签分类\] | 可选 |
| [!UICONTROL Campaign ID] | 可选 |
| [!UICONTROL Ad Group ID] | 可选 |
| [!UICONTROL Ad ID] | 仅在更改广告状态时需要，除非行包含a&amp;amp；rpar；足够的广告属性列来标识广告或b&amp;amp；rpar；“[!UICONTROL AMO ID]”。 但是，如果您既不包括[!UICONTROL Ad ID]也不包括[!UICONTROL AMO ID]，并且广告属性列与多个广告匹配，则只有其中一个广告的状态会更改。 |
| [!UICONTROL AMO ID] | 需要编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |

### 产品（购物）广告字段

有关创建购物广告的更多信息，请参阅“[实施 [!DNL Microsoft Advertising] 购物营销活动](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/microsoft-shopping-campaigns.html?lang=zh-Hans)”。

对于此广告类型，请使用[!UICONTROL Creative (except RSA)]对话框中的“[!UICONTROL Download Bulksheet]”行。

有关每个数据字段的说明，请参阅“[所有可用数据字段](#bulksheet-fields-all-microsoft)”。

| 字段 | 必需？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Promotion Line] | 可选 |
| [!UICONTROL Base URL/Final URL] | 可选 |
| [!UICONTROL Custom URL Param] | 可选 |
| [!UICONTROL Creative Type] | 需要创建或编辑产品广告的状态。 |
| [!UICONTROL Tracking Template] | 可选 |
| [!UICONTROL Ad Status] | 删除广告时需要。 |
| \[广告商特定的标签分类\] | 可选 |
| [!UICONTROL Constraints] | 可选 |
| [!UICONTROL Campaign ID] | 可选 |
| [!UICONTROL Ad Group ID] | 可选 |
| [!UICONTROL Ad ID] | 仅在更改广告状态时需要，除非行包含a)足够的广告属性列来标识广告或b) &quot;[!UICONTROL AMO ID]&quot;。 但是，如果您既不包括[!UICONTROL Ad ID]也不包括[!UICONTROL AMO ID]，并且广告属性列与多个广告匹配，则只有其中一个广告的状态会更改。 |
| [!UICONTROL AMO ID] | 需要编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |

### 响应式（多媒体）广告字段

对于此广告类型，请使用[!UICONTROL Creative (except RSA)]对话框中的“[!UICONTROL Download Bulksheet]”行。

有关每个数据字段的说明，请参阅“[所有可用数据字段](#bulksheet-fields-all-microsoft)”。

| 字段 | 必需？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Ad Title]，[!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | 对于响应式广告，[!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]和[!UICONTROL Ad Title 3]是创建广告所必需的，而所有其他广告标题字段都是可选的。 要删除非必填字段的现有值，请使用值`[delete]`（包括括号）。 <b>注意：</b>对于此广告类型，更改广告副本将删除现有广告并创建新广告。 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | [!UICONTROL Description Line 1]和[!UICONTROL Description Line 2]是创建广告所必需的，而[!UICONTROL Description Line 3]和[!UICONTROL Description Line 4]是可选的。 <b>注意：</b>对于此广告类型，更改广告副本将删除现有广告并创建新广告。 |
| [!UICONTROL Business Name] | 需要创建或删除广告。 |
| [!UICONTROL Call To Action] | 需要创建广告。 |
| [!UICONTROL Call To Action Language] | 需要创建广告。 |
| [!UICONTROL Base URL/Final URL] | 需要创建广告。 |
| [!UICONTROL Creative Type] | 可选。 |
| [!UICONTROL Tracking Template] | 可选 |
| [!UICONTROL Ad Status] | 删除广告时需要。 |
| \[广告商特定的标签分类\] | 可选 |
| [!UICONTROL Campaign ID] | 可选 |
| [!UICONTROL Ad Group ID] | 可选 |
| [!UICONTROL Ad ID] | 仅在更改广告状态时需要，除非行包含a)足够的广告属性列来标识广告或b) &quot;[!UICONTROL AMO ID]&quot;。 但是，如果您既不包括[!UICONTROL Ad ID]也不包括[!UICONTROL AMO ID]，并且广告属性列与多个广告匹配，则只有其中一个广告的状态会更改。 |
| [!UICONTROL AMO ID] | 需要编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |

### 响应式搜索广告字段

对于此广告类型，请使用[!UICONTROL Responsive Search Ad]对话框中的“[!UICONTROL Download Bulksheet]”行。

有关每个数据字段的说明，请参阅“[所有可用数据字段](#bulksheet-fields-all-microsoft)”。

| 字段 | 必需？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Ad Title]，[!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | 对于响应式搜索广告，[!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]和[!UICONTROL Ad Title 3]是创建广告所必需的，而所有其他广告标题字段都是可选的。 要删除非必填字段的现有值，请使用值`[delete]`（包括括号）。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | 可选 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | 对于响应式搜索广告，[!UICONTROL Description Line 1]和[!UICONTROL Description Line 2]是创建广告所必需的，[!UICONTROL Description Line 3]和[!UICONTROL Description Line 4]是可选的。 要删除现有值，请使用值`[delete]`（包括括号）。 |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | 可选 |
| [!UICONTROL Display Path 1] | 可选 |
| [!UICONTROL Display Path 2] | 可选 |
| [!UICONTROL Base URL/Final URL] | 需要创建广告。 |
| [!UICONTROL Custom URL Param] | 可选 |
| [!UICONTROL Creative Type] | 可选 |
| [!UICONTROL Tracking Template] | 可选 |
| [!UICONTROL Ad Status] | 删除广告时需要。 |
| \[广告商特定的标签分类\] | 可选 |
| [!UICONTROL Campaign ID] | 可选 |
| [!UICONTROL Ad Group ID] | 可选 |
| [!UICONTROL Ad ID] | 需要编辑或删除广告，除非行包含“[!UICONTROL AMO ID]”。 |
| [!UICONTROL AMO ID] | 需要编辑或删除广告，除非您包含广告ID。 |

### 文本广告字段

对于此广告类型，请使用[!UICONTROL Creative (except RSA)]对话框中的“[!UICONTROL Download Bulksheet]”行。

>[!NOTE]
>
>已弃用扩展的文本广告。 您只能删除现有的文字广告。

有关每个数据字段的说明，请参阅“[所有可用数据字段](#bulksheet-fields-all-microsoft)”。

| 字段 | 必需？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Ad Title]，[!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | 只读 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | 只读 |
| [!UICONTROL Display URL] | 只读 |
| [!UICONTROL Display Path 1] | 只读 |
| [!UICONTROL Display Path 2] | 只读 |
| [!UICONTROL Base URL/Final URL] | 只读 |
| [!UICONTROL Custom URL Param] | 只读 |
| [!UICONTROL Creative Type] | 可选 |
| [!UICONTROL Tracking Template] | 只读 |
| [!UICONTROL Creative Preferred Devices] | 只读 |
| [!UICONTROL Ad Status] | 必填 |
| \[广告商特定的标签分类\] | 可选 |
| [!UICONTROL Campaign ID] | 可选 |
| [!UICONTROL Ad Group ID] | 可选 |
| [!UICONTROL Ad ID] | 仅在更改广告状态时需要，除非行包含“[!UICONTROL AMO ID]”。 |
| [!UICONTROL AMO ID] | 需要编辑或删除数据，除非您包含广告ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |

### 动态搜索目标（自动定位）字段

>[!NOTE]
>
>创建支持不可用。

有关每个数据字段的说明，请参阅“[所有可用数据字段](#bulksheet-fields-all-microsoft)”。

| 字段 | 必需？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Auto Target Expression] | 必需。 |
| [!UICONTROL Match Type] | 可选 |
| [!UICONTROL Max CPC] | 可选 |
| [!UICONTROL Custom URL Param] | 可选 |
| [!UICONTROL Target Status] | 需要删除目标 |
| \[广告商特定的标签分类\] | 可选 |
| [!UICONTROL Constraints] | 可选 |
| [!UICONTROL Campaign ID] | 可选 |
| [!UICONTROL Ad Group ID] | 可选 |
| [!UICONTROL Target ID] | 仅在更改或删除自动定位时需要，除非行包含目标的“[!UICONTROL AMO ID]”。 |
| [!UICONTROL AMO ID] | 需要编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |

### 购物产品组字段

有关每个数据字段的说明，请参阅“[所有可用数据字段](#bulksheet-fields-all-microsoft)”。

| 字段 | 必需？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 必填 |
| [!UICONTROL Match Type] | 需要创建产品组。 |
| [!UICONTROL Max CPC] | 需要创建产品组。 |
| [!UICONTROL Parent Product Groupings] | 必填 |
| [!UICONTROL Product Grouping] | 必填 |
| [!UICONTROL Partition Type] | 需要创建产品组。 |
| [!UICONTROL Base URL/Final URL] | 必填 |
| [!UICONTROL Tracking Template] | 可选 |
| [!UICONTROL Product Group Status] | 仅需删除产品组。 |
| \[广告商特定的标签分类\] | 可选 |
| [!UICONTROL Constraints] | 可选 |
| [!UICONTROL Campaign ID] | 可选 |
| [!UICONTROL Ad Group ID] | 可选 |
| [!UICONTROL Product Group ID] | 仅在更改或删除产品组时才需要此变量，除非该行包含a)足够的属性列来标识产品组或b) &quot;[!UICONTROL AMO ID]&quot;。 |
| [!UICONTROL AMO ID] | 需要编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |

### 营销活动级别的站点链接字段

有关每个数据字段的说明，请参阅“[所有可用数据字段](#bulksheet-fields-all-microsoft)”。

| 字段 | 必需？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 |
| 描述行1 | 可选 |
| [!UICONTROL Description Line 2] | 可选 |
| [!UICONTROL Start Date] | 可选 |
| [!UICONTROL End Date] | 可选 |
| [!UICONTROL Base URL/Final URL] | 必填 |
| [!UICONTROL Custom URL Param] | 可选 |
| [!UICONTROL Tracking Template] | 可选 |
| [!UICONTROL Creative Preferred Devices] | 可选 |
| [!UICONTROL Link Name] | 必填 |
| [!UICONTROL Sitelink Status] | 仅删除站点链接时需要。 |
| [!UICONTROL Campaign ID] | 可选 |
| [!UICONTROL Sitelink ID] | 仅在更改或删除站点链接时需要，除非该行包含a)足够的属性列以标识站点链接或b) &quot;[!UICONTROL AMO ID]&quot;。 但是，如果您既不包括[!UICONTROL Sitelink ID]也不包括[!UICONTROL AMO ID]，并且属性列与多个站点链接匹配，则只有其中一个站点链接的状态会更改。<br><br><b>注意：</b>如果您编辑的站点链接属性列（现有Sitelink的状态除外），并且您既不包括[!UICONTROL Sitelink ID]也不包括[!UICONTROL AMO ID]，则会创建一个新的Sitelink，并且现有Sitelink不会发生更改。 |
| [!UICONTROL AMO ID] | 需要编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |

### 位置目标字段

有关每个数据字段的说明，请参阅“[所有可用数据字段](#bulksheet-fields-all-microsoft)”。

| 字段 | 必需？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Location] | 必填 |
| [!UICONTROL Location Type] | 创建目标所需 |
| [!UICONTROL Bid Adjustment] | 可选 |
| [!UICONTROL Location Status] | 仅删除位置目标时需要。 |
| [!UICONTROL Campaign ID] | 可选 |
| [!UICONTROL AMO ID] | 需要编辑或删除数据，除非您包含营销活动ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |

### 营销活动级别和广告组级别设备目标字段

有关每个数据字段的说明，请参阅“[所有可用数据字段](#bulksheet-fields-all-microsoft)”。

| 字段 | 必需？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Device] | 删除设备目标时需要。 |
| [!UICONTROL Bid Adjustment] | 可选 |
| [!UICONTROL Ad Group Name] | 对于广告组级设备目标，此变量是必需的。 不适用于营销活动级别的设备目标。 |
| [!UICONTROL Device Target Status] | 仅删除设备目标时需要。 |
| [!UICONTROL Campaign ID] | 可选 |
| [!UICONTROL Ad Group ID] | 可选；仅适用于广告组级设备目标。 |
| [!UICONTROL AMO ID] | 需要编辑或删除数据，除非您包含设备目标ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |

### 营销活动级别和广告组级别的RLSA目标字段

有关每个数据字段的说明，请参阅“[所有可用数据字段](#bulksheet-fields-all-microsoft)”。

| 字段 | 必需？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 除非每行都包含实体的“[!UICONTROL AMO ID]”，否则此为必填字段。 |
| [!UICONTROL Campaign Name] | 必填 |
| [!UICONTROL Ad Group Name] | 对于广告组级别目标，此为必需字段。 不适用于营销活动级别的目标。 |
| [!UICONTROL Audience] | 需要创建新目标。 |
| [!UICONTROL Target Type] | 可选 |
| [!UICONTROL Bid Adjustment] | 可选 |
| [!UICONTROL RLSA Target Status] | 删除目标时需要。 |
| [!UICONTROL Campaign ID] | 可选 |
| [!UICONTROL Ad Group ID] | 可选；仅适用于广告组级别目标。 |
| [!UICONTROL RLSA Target ID] | 仅在更改或删除目标时需要，除非行包含目标的“[!UICONTROL AMO ID]”。 |
| [!UICONTROL AMO ID] | 需要编辑或删除数据，除非您包含RLSA目标ID。<br><br>Search、Social和Commerce使用此值确定要编辑的正确身份，但不会将ID发布到广告网络。 |

>[!MORELIKETHIS]
>
>* [附录 — 批量处理工作表错误](../bulksheet-errors.md)
>* [可在批量处理工作表中执行的操作](bulksheet-operations.md)
>* [支持的批量处理工作表文件格式](bulksheet-file-formats.md)
>* [下载/创建批量处理工作表文件](../bulksheet-download.md)
>* [的 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)点击跟踪格式
>* [上载批量工作表文件或更正的错误文件](../bulksheet-upload.md)
