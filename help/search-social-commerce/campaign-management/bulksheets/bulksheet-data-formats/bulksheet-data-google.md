---
title: 以下项的必需批量处理工作表数据 [!DNL Google Ads] 帐户
description: 引用批量处理工作表中的必填标题字段和数据字段 [!DNL Google Ads] 帐户。
source-git-commit: f7ac5c69f96582d7f9a442a05c333baecc2215df
workflow-type: tm+mt
source-wordcount: '6276'
ht-degree: 0%

---

# 附录 — 必需的批量工作表数据 [!DNL Google Ads] 帐户

创建和更新 [!DNL Google Ads] 批量处理营销活动数据，您可以使用专门格式化的搜索、社交和商务批量工作表文件 [!DNL Google Ads] 帐户。 您可以a) [为现有帐户生成批量工作表文件](../bulksheet-download.md) (b)手动创建它们（请参见）[支持的批量工作表文件格式](bulksheet-file-formats.md)”以了解有关支持的文件格式的一般信息)。

{{$include /help/_includes/bulksheet-appendices-intro.md}}

## 所有可用数据字段

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| 字段 | 描述 |
| ---- | ---- |
| Platform | （包含在生成的批量工作表中，以供参考）广告平台。 除非每行都包含实体的“AMO ID”，否则必需。 |
| 帐户名称 | 标识广告网络帐户的唯一名称。 除非每行都包含实体的“AMO ID”，否则必需。 |
| 营销活动名称 | 标识帐户促销活动的唯一名称。 |
| 营销活动预算 | 竞选活动的每日支出上限，无论是否带有货币符号和标点。 此值将覆盖但不能超过帐户预算。 |
| 投放方法 | <p>每天为促销活动显示广告的速度如何：</p><ul><li><p><i>标准（分布式）</i> （新营销活动的默认设置）：将广告展示次数分散到一整天里。</p></li><li><p><i>加速：</i> （2019年10月弃用）在达到预算之前尽可能多地显示广告。 因此，您的广告可能不会在当天晚些时候显示。</p></li></ul> |
| 渠道类型 | <p>要在其中放置广告的频道。 指定一个或多个选项：</p><ul><li class="p"><p><span style="font-style: italic;"><i>搜索</i></span> （新促销活动的默认设置）：将广告置于Google搜索网络(包括Google搜索和Google搜索合作伙伴网站)上，也可以选择置于Google显示网络上。 <b>注意：</b> 无法向组合中添加同时针对搜索网络和显示网络的促销活动以进行竞价优化。</p></li><li class="p"><p><span style="font-style: italic;"><i>显示</i></span>：仅在Google显示网络上投放广告。</p></li><li class="p"><p><span style="font-style: italic;"><i>购物</i></span>：在Google Shopping（位于选定的国家/地区）和Google搜索网络(包括Google搜索和Google搜索合作伙伴网站)上投放购物广告。 要创建购物广告，您必须在Google商家中心帐户中具有产品，并且 [允许搜索、社交和商务从帐户下载数据](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). 参见“[实施 [!DNL Google Ads] 购物营销活动](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)”以了解有关创建购物广告过程的更多信息。</p></li></ul> |
| 网络 | <p>在何处放置广告。 指定一个或多个选项：</p><ul><li class="p"><p><span style="font-style: italic;"><i>Google搜索</i></span>：仅在Google搜索网络上赞助搜索列表。</p></li><li class="p"><p><span style="font-style: italic;"><i>搜索合作伙伴</i></span>：赞助有关Google搜索合作伙伴的搜索列表。</p></li><li class="p"><p><span style="font-style: italic;"><i>内容</i></span>：对显示网络列表投标。</p></li><li class="p"><p><span style="font-style: italic;"><i>全部</i></span> （新营销活动的默认设置）：定位Google搜索、搜索合作伙伴和内容。</p></li></ul> |
| DSA域名 | <p>（仅限搜索网络；仅适用于扩展的动态搜索广告）广告网络将用来定位动态搜索广告的内容所在网站的根域(如example.com)或子域(如shoes.example.com)。<br><br><b>注释：</b></p><ul><li><p>扩展的动态搜索广告以网站内容为目标，而不是以关键字为目标。</p></li><li><p>域必须按广告网络的自然搜索索引编制索引才能定位。</p></li><li><p>如果您未指定域，则需要创建动态搜索目标，以便为每个广告组定位所有网站页面或其子集。</p></li></ul> |
| DSA域语言 | （仅限搜索网络；仅适用于扩展的动态搜索广告）指定网站域的语言。 <b>注意：</b> 如果域包含使用多种语言的页面，并且您希望定位所有这些语言，请为每种语言创建一个单独的营销活动。 |
| GDN自定义竞价级别 | （仅针对展示网络的促销活动）竞价方式：竞价者 <span style="font-style: italic;"><i>广告组</i></span> （默认）， <span style="font-style: italic;"><i>关键词</i></span>， <span style="font-style: italic;"><i>投放</i></span> （网站），或 <span style="font-style: italic;"><i>无</i></span> （重置现有值）。 其他维度(<span style="font-style: italic;"><i>年龄</i></span>， <span style="font-style: italic;"><i>性别</i></span>， <span style="font-style: italic;"><i>兴趣和列表</i></span>， <span style="font-style: italic;"><i>主题</i></span>、和 <span style="font-style: italic;"><i>垂直</i></span>)从Google Ads界面中可用。 如果您已使用Google广告界面配置其他维度的竞价，则会显示该值，但您无法在此处选择或输入这些维度。</p><p><b>注意：</b></p><ul><li><p>当您按关键字竞价时，请在关键字级别创建跟踪模板。 同样，在按投放位置竞价时，请在投放位置级别创建跟踪模板。 对于所有其他维度，请在广告级别创建跟踪模板。</p></li><li><p>当您通过不受支持的维度（年龄、性别、兴趣和列表或主题）竞价时，搜索、社交和商务不会优化该维度的竞价，并且所有归因都将应用于广告组。</p></li><li><p>搜索网络上的广告始终使用关键词竞价。</p></li></ul> |
| 营销活动优先级 | <p>（仅限购物营销活动）当多个营销活动广告同一产品时，使用该营销活动的优先级：  <span style="font-style: italic;"><i>低</i></span> （新营销活动的默认值）， <span style="font-style: italic;"><i>中</i></span>，或 <span style="font-style: italic;"><i>高</i></span>.</p><p>当同一产品包含在多个促销活动中时，广告网络会首先使用促销活动优先级来确定哪个促销活动（及相关竞价）符合广告拍卖的条件。 如果所有促销活动具有相同的优先级，则具有最高竞价的促销活动符合条件。 |
| 商家ID | （仅限链接到商家馈送的购物营销活动和受众营销活动）其产品用于营销活动的商家帐户的客户ID。 |  |
| 销售国家/地区 | （仅限购物营销活动；现有营销活动为只读）营销活动产品销售的国家/地区。 由于产品与目标国家/地区相关联，因此此设置确定在营销活动中广告的产品。 |
| 产品范围筛选器 | (仅限使用Google购物网络的促销活动)Google商家中心帐户中的产品，可为其创建促销活动购物广告。 可使用格式dimension=attribute输入最多七种产品维度和属性组合，以筛选产品。 使用“>>”分隔符分隔多个过滤器。 有关可用产品维度的列表，请参阅&quot;[购物营销活动产品过滤器](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).”</p><p>示例：“CategoryL1=animals>>CategoryL2=pet supplies>>Brand=Acme Pet Supplies”</p><p>要删除现有值，请使用值 <span class="Code">[delete]</span> （包括括号）。</p> |
| 语言 | <p>（仅限搜索和显示网络）促销活动中广告的目标语言。</p><p>如果您没有为新促销活动的此字段或“地域定位”字段输入值，则为帐户指定的货币将决定默认语言，但具有未映射到特定语言的货币（例如，EUR）的促销活动将定位到所有语言。 如果您没有为此字段输入值，但在新促销活动的“地域定位”字段中输入值，则此字段默认为 <span style="font-style: italic;"><i>全部</i></span>. 如果您将现有营销活动的此字段留空，则将保留现有值。</p><p>要定位所有语言，请输入 <span style="font-style: italic;"><i>全部</i></span>. 要定位特定的语言，请使用以下任一方式输入以分号分隔的值 <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">Google的语言名称</a> (例如 <span style="font-style: italic;"><i>英语；日语</i></span>，将被正确的数字代码替换)或数字代码(例如 <span style="font-style: italic;"><i>1000；1005</i></span>)。 这些值不区分大小写。</p> |

|位置 |要在其中投放广告或从中排除广告的地理位置。 如果您没有为新促销活动的此字段或“语言”字段输入任何值，则为帐户指定的货币将决定默认地点，除非其货币未映射到特定地点的促销活动（例如，EUR）将定位到所有地点。 如果您没有为此字段输入值，但在 [!UICONTROL Languages] 字段，则此字段默认为 <i>全部</i>. 如果您将现有营销活动的此字段留空，则会保留现有值。</p><p>要定位特定位置，请使用以下位置之一 [Google的位置名称](https://developers.google.com/adwords/api/docs/appendix/geotargeting) （使用正确的数字代码替换）或位置代码：</p><ul><li><p>国家/地区：输入国家/地区名称(如 <span style="font-style: italic;"><i>美国；日本</i></span>)或数值代码(例如 <span style="font-style: italic;"><i>2840；2392</i></span>)。</p></li><li><p>州/省/地区：输入州/省/地区的名称以及相关国家/地区的缩写(例如 <span style="font-style: italic;"><i>东京，JP；美国纽约</i></span>)或数值代码(例如 <span style="font-style: italic;"><i>20636；21167</i></span>)。</p></li><li><p>非美国城市：输入城市名称、州/省/地区名称以及国家/地区缩写(例如 <span style="font-style: italic;"><i>安达市、东京、JP；Kita、东京、JP</i></span>)或数值代码(例如 <span style="font-style: italic;"><i>1028850；1009293</i></span>)</p></li><li><p>美国都市区：输入城市名称、州名和国家/地区缩写(例如 <span style="font-style: italic;"><i>Buffalo NY，美国；New York NY，美国</i></span>)或数值代码(例如 <span style="font-style: italic;"><i>514；501</i></span>)。</p></li></ul><p>要排除位置，请在位置名称或代码前加减号(-)，例如 <span style="font-style: italic;"><i> — 日本</i></span>.</p><p><b>注意：</b> 这些值不区分大小写。</p> | |位置类型 |（当您包含位置时） [位置类型](https://developers.google.com/google-ads/api/data/geotargets).| |设备 |在营销活动或广告组级别进行竞价调整的设备类型： <i>智能手机</i>， <i>平板电脑</i>，或 <i>桌面</i>. | |竞价调整 | <p>（当您包括位置、设备或RLSA目标时）调整特定位置、特定设备类型还是特定受众目标的广告投标：</p><ul><li><p>要使用关键字级别的竞价（0%的差异），请输入0。 对于新目标，您还可以将此项留空。</p></li><li><p>要对此目标使用不同的竞价，请输入增加或减少竞价的百分比。</p></li><ul><li><p>对于位置和RLSA目标，有效百分比包括从–90到900。</p></li><li><p>对于设备竞价调整，有效百分比包括：</p></li><ul><li><p>（营销活动）–100（不对设备类型的广告投标）或从–90到900。</p></li><li><p>（广告组）–100表示智能手机和平板电脑（表示不对设备类型投标），从–90到900表示所有设备类型。</p></li></ul></ul><li><p>（现有营销活动和广告组）要使用现有竞价调整，请将此项留空。</p></li></ul> | |Adobe记录竞价调整 |（出于信息目的包含在生成的批量处理工作表中）Adobe建议用于营销活动级别位置目标或RLSA的只读竞价调整。 仅当营销活动位于具有加权收入目标（而不是“最大化点击量”目标）的项目组合中，并且营销活动包含至少两个位置目标或在过去90天内具有至少五次点击或成本为5美元的RLSA时，才会计算此值。</p><p>如果要手动编辑位置目标或RLSA以使用推荐值，请在创建位置目标或RLSA后至少等待两周，以允许充分的数据收集，并且不要每周多次更改该值。 | |设备目标 | <p>（仅限旧版促销活动类型）显示广告的设备： <span style="font-style: italic;"><i>全部</i></span>， <span style="font-style: italic;"><i>计算机</i></span>， <span style="font-style: italic;"><i>智能手机</i></span>，或 <span style="font-style: italic;"><i>平板电脑</i></span>. 对于新营销活动，默认为 <span style="font-style: italic;"><i>全部</i></span>.</p> | |设备操作系统目标(Google Adwords) |（仅限旧版促销活动类型；当设备目标包括“智能手机”或“平板电脑”时适用）显示广告的操作系统： <span style="font-style: italic;"><i>全部</i></span>， <span style="font-style: italic;"><i>Android</i></span>， <span style="font-style: italic;"><i>iOS</i></span>，或 <span style="font-style: italic;"><i>掌心</i></span>. 对于新营销活动，默认为 <span style="font-style: italic;"><i>全部</i></span>.</p> | |移动运营商(Google Adwords) | <p>（仅限旧版促销活动类型；当设备目标包括“全部”或“智能手机”时适用）智能手机可能连接的移动运营商： <span style="font-style: italic;"><i>全部</i></span>，或者由指示的一个或多个运营商 &lt;c span=&quot;&quot; id=&quot;2&quot; translate=&quot;no&quot; />运营商代码</i></span>>，&lt;<span style="font-style: italic;"><i>国家/地区代码</i></span>>（例如T-Mobile，US）使用 <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">Google Ads的可用运营商和代码</a>. <span style="font-style: italic;"><i>使用分号（例如T-Mobile、US；T-Mobile、GB）分隔多个运营商。 对于新营销活动，默认为 <span style="font-style: italic;"><i>全部</i></span>.</p> | |广告组名称 | <p>标识广告组的唯一名称。 最大长度为255个字符；不保存结尾的空白字符（例如，“广告组1”另存为“广告组1”）。 此字段不适用于营销活动级别的站点链接或营销活动级别的设备目标。</p> | |广告组类型 | <p>广告组类型： <span class="Option">发现</span> （仅适用于发现活动）， <span class="Option">显示</span> （用于显示促销活动）， <span class="Option">搜索动态</span> （对于扩展的动态搜索广告）， <span class="Option">搜索标准</span> （对于搜索广告）， <span class="Option">购物产品</span> （对于购物产品广告）， <span class="Option">购物展示</span> （不支持创建和编辑），或 <span class="Option">未知</span>.</p> | |最大CPC | <p>（仅限CPC促销活动）最大每次点击成本(CPC)，这是在广告网络上为广告点击支付的最高金额，无论是否带有货币符号和标点。 您可以为广告组和关键字、产品组以及动态搜索目标设置值。 新关键字的默认值继承自广告组级别。 对于产品组，您可以设置最低产品组层的值；新层的默认值继承自父层。</p><p>对于优化项目组合中的现有产品组和动态搜索目标，更新仅在一天内有效，并在下一个优化周期中被覆盖。</p><p><b>注意：</b> 对于版面，使用最大版面CPC字段。</p> | |最大内容CPC | <p>（仅限CPC营销活动）每次点击的最大内容成本(CPC)，这是为来自显示网络站点的广告点击支付的最高金额，无论是否带有货币符号和标点。 您可以在不以投放位置为目标的营销活动中，在广告组级别设置和编辑值。</p> | |受众定位方法 | <p>（仅搜索网络上的营销活动，以及显示网络上现有的只读Gmail营销活动）是否：</p><ul><li><p><span style="font-style: italic;"><i>目标和竞价</i></span>：仅向与目标受众关联、且满足广告组任何其他目标的用户显示广告。</p></li><li><p><span style="font-style: italic;"><i>仅竞价</i></span>：即使向不与目标受众关联的用户显示广告，只要他们满足其他广告组级别的目标即可。</p><p>但是，您可以通过为特定受众设置更高的竞价来增加向这些受众显示广告的几率。</p></li></ul> | |关键词 |关键字字符串。 最大长度为80个字符，不超过10个单词，并且只能包含字母、数字和以下特殊字符：空格 `# $ & _ - " [ ] ' + . / :`</p><p><b>注意：</b></p><ul><li><p>要在广告组或营销策划级别排除关键词，请将“匹配类型”设置为 <span style="font-style: italic;"><i>负面</i></span>. 如果行包含广告组名称，则该广告组将排除关键字。 如果行不包含广告组名称，则该关键字将排除在整个营销活动中。</p></li><li><p>更改Google Ads关键字或匹配类型会删除现有关键字并创建新关键字。</p></li></ul> | |投放 |（仅使用匹配内容的促销活动）显示网络中可能显示广告的版面。 指定以下选项之一：</p><ul><li class="p"><p>网站：输入有效的URL。 它可以是顶级域、第一级子域或具有单个目录名的域。 URL不能包含问号(？)。 示例：<span class="Code"><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</span></p></li><li class="p"><p>特定页面上的广告位置：使用格式 `<URL> >> <location,sublocation>` (例如 `finance.google.com >> Company pages,Top right`)。</p></li><li class="p"><p>主题类别：使用语法 `<category::<category> > <subcategory>` 等等(例如 `category::Industries > Energy & Utilities > Oil & Gas`)。</p></li></ul><p><b>注意：</b> 要在广告组或营销活动级别排除投放位置，请将“匹配类型”设置为 <span style="font-style: italic;"><i>负面</i></span>. 如果行包含广告组名称，则该广告组的版面将被排除。 如果行不包括广告组名称，则该投放位置将在整个营销活动中排除。</p> | |自动定位表达式 | <p>（未启用“使用我的网站内容定位我的广告”营销活动设置时必需；否则可选）广告组的动态搜索目标。</p><p>对于所有目标，请使用星号(*)。</p><p>要定位最多三个动态搜索标准，请使用格式 `<category>=<target>`，其中 `<category>` 可以包括以下任意类别。 使用“\[blank space\]和\[blank space\]”为单个类别连接多个目标，使用“”连接多个类别[空格] 和 [空格]“。</p><ul><li class="p"><p><span style="font-style: italic;"><i>类别</i></span>：为具有特定Google内容类别的索引页面显示扩展的动态搜索广告。</p></li><li class="p"><p><span style="font-style: italic;"><i>URL</i></span>：为具有特定URL的索引页面显示扩展的动态搜索广告，其中值可能包含在URL中的任意位置。</p></li><li class="p"><p><span style="font-style: italic;"><i>页面标题</i></span>：为具有页面标题中特定文本的索引页面显示扩展的动态搜索广告。</p></li><li class="p"><p><span style="font-style: italic;"><i>页面内容</i></span>：为具有特定内容的索引页面显示扩展的动态搜索广告。</p></li></ul><p>示例： url=shoes.example.com和page title=footwear</p> | |父产品分组 |任何父产品组的层次结构。<br><br>示例： `All Products>>ProductTypeL1=a>>ProductTypeL2=b` | |产品分组 | <p>产品组（如“brand=acme”或“所有产品”）。</p><p><b>注意：</b></p><ul><li><p>当指定的产品组在父产品组层次结构中不存在时，Search、Social和Commerce会创建所需的层次结构的任何部分。</p></li><li><p>每当您在Google购物营销活动中通过默认竞价设置为广告组默认竞价创建广告组时，“搜索、Social &amp; Commerce”都会自动创建“所有产品”组。 Search、Social和Commerce会在产品组层次结构的每个级别自动创建一个包含广告组默认竞价的“其他所有项”组。 您仍然可以显式创建这些默认组，并排除它们或更改其竞价。</p></li><li><p>每个广告组最多可包含八层产品组，包括“所有产品”和七个其他层。</p></li></ul> | |分区类型 |产品组的分区类型： <i>细分</i> （当具有子产品组时）或 <i>单位</i> （当它没有子产品组时）。 | |匹配类型 | <p>对于动态搜索目标或产品组：动态搜索目标或产品组的关键词匹配选项： <i>Dynamic Ad Target</i> （新动态搜索目标的默认设置）， <i>产品组</i> （新产品组的默认值）或 <i>负值产品组</i> （用于排除产品组）。</p><p>对于关键字：关键字的关键字匹配选项： <span style="font-style: italic;"><i>广泛</i></span>， <span style="font-style: italic;"><i>短语</i></span>， <span style="font-style: italic;"><i>精确</i></span>，或 <span style="font-style: italic;"><i>负面</i></span> （排除展示网络上的关键字或版面）；将与购物广告一起使用的产品组的匹配类型为 <span style="font-style: italic;"><i>产品组</i></span>. 如果您使用 <span style="font-style: italic;"><i>负面</i></span>，您还必须包含要排除的匹配类型（例如，“负面短语”）。</p><p>对于新关键字，缺省值为 <span style="font-style: italic;"><i>广泛</i></span>. 只有在编辑具有多个匹配类型的关键字时，才需要匹配类型或关键字ID的值。</p><p><b>注意：</b></p><ul><li><p>匹配类型不适用于扩展的动态搜索广告，这些广告不使用关键字。</p></li><li><p>更改Google Ads关键字的匹配类型会删除现有关键字并创建一个新关键字。</p></li><li><p>对于Broad Match修饰符，请选择“Broad”，并在关键词中需要封闭变体的任何单词前插入+（例如“+red +shoes”，需要“red”和“shoes”的封闭变体）。 <b>注意：</b> 广泛匹配修饰符现在与某些语言的短语匹配具有相同的匹配行为，并且自2021年7月以来，您一直无法创建新的广泛匹配修饰符关键词。 参见 [Google文档](https://support.google.com/google-ads/answer/7042511) 了解更多信息。</p> | |首页出价 |（出于信息目的包含在生成的批量工作表中）在搜索结果的第一页上放置广告所需的竞价。 此值未发布到广告网络。 | |质量分数 |（出于信息目的包含在生成的批量工作表中）搜索引擎分配给关键字的当前质量分数。 此值未发布到广告网络。) | |创意首选设备 |（文本广告、扩展的动态搜索广告和增强型站点链接；可选）您喜欢显示广告的设备类型： <span style="font-style: italic;"><i>全部</i></span> （默认）或 <i>移动设备</i>. 时间 <i>移动设备</i> 指定，则网络将尝试向移动设备用户显示广告，而不是桌面或平板电脑用户。 否则，网络会在任何设备类型上显示广告。</p><p><b>注意：</b></p><ul><li><p>仅管理员和 [!DNL Adobe] 帐户管理员用户可以编辑此设置。</p></li><li><p>网络不保证会在首选设备类型上显示广告。</p></li><li><p>新的增强型站点链接只能在具有现有增强型站点链接或没有站点链接的活动中创建。</p></li></ul> | |广告标题，广告标题2-15 |（仅限扩展的文本广告和响应式搜索广告）广告的头条，每个标题用垂直管道分隔(|)。 每个广告标题字段的最大长度为30个字符或15个双字节字符，包括任何动态文本（例如关键字和广告自定义器的值）。</p><p>对于响应式搜索广告，“广告标题”、“广告标题2”和“广告标题3”是必填字段，所有其他广告标题字段都是可选字段。 要删除非必填字段的现有值，请使用值 [delete]</code> （包括括号）。</p><p>对于响应式搜索广告，请使用以下格式插入广告自定义程序：</p><ul><li><p>Google广告： `{CUSTOMIZER.AdCustomizerName:DefaultText}`，例如 `{CUSTOMIZER.Discount:10%}`</p></li><li><p><span>Microsoft Advertising： `{CUSTOMIZER.Attribute name:default text}`，例如 `{CUSTOMIZER.Discount:10%}`</span></p></li></ul><p>您不能创建或编辑，但可以删除扩展的文字广告，Google广告已于2022年6月弃用。 | |广告标题1-15位置 | <p>（仅限响应式搜索广告；可选）固定相应广告标题的位置： `[null]` （无值，这使得广告标题适用于所有职位）， <i>1</i>， <i>2</i>，或 <i>3</i>. 例如，如果“广告标题位置”的值为1，则“广告标题”将仅显示在“位置1”中。 默认情况下，所有广告标题为空（没有值）。</p><p>要删除现有值，请使用值 [delete]</code> （包括括号）。</p><p><b>注意：</b> 您可以将多个广告标题固定到同一位置。 广告网络将使用固定到该位置的广告标题之一。 固定到位置3的标题不能与广告一起显示。</p> | |描述行1-4 | <p>（仅限扩展的动态搜索广告、扩展文本广告和响应式搜索广告）广告的正文。 每个描述字段的最大长度为90个字符或45个双字节字符，包括任何动态文本（例如关键字和广告自定义器的值）。</p><p>对于响应式搜索广告，请使用以下格式插入广告自定义程序：</p><ul><li><p>Google广告： `{CUSTOMIZER.AdCustomizerName:DefaultText}`，例如 `{CUSTOMIZER.Discount:10%}`</p></li><li><p><span>Microsoft Advertising： `{CUSTOMIZER.Attribute name:default text}`，例如 `{CUSTOMIZER.Discount:10%}`</span></p></li></ul><p>对于展开的动态搜索广告，请仅使用“描述行1”和“描述行2”。 <b>注意：</b> 对于此广告类型，更改广告副本会删除现有广告并创建新广告。</p><p>您不能创建或编辑，但可以删除扩展的文字广告，Google广告已于2022年6月弃用。</p><p>对于响应式搜索广告，“说明行1”和“说明行2”为必需字段，“说明行3”和“说明行4”为可选字段。 要删除现有值，请使用值 [delete]</code> （包括括号）。</p> | |描述行1-4位置 |（仅限响应式搜索广告；可选）固定相应描述的位置： `[null]` （无值，因此说明适用于所有职位）， <i>1</i>， <i>2</i>，或 <i>3</i>. 例如，如果“描述1位置”的值为1，则“描述1”将仅显示在“位置1”中。 默认情况下，不会将任何描述固定到位置。</p><p>要删除现有值，请使用值 `[delete]` （包括括号）。</p><p><b>注意：</b> 可以将多个描述固定到同一位置。 广告网络将使用固定到该位置的描述之一。 固定到位置2的描述可能无法与广告一起显示。 | |显示URL |广告中包含的URL。<br><br>对于扩展的动态搜索广告，Google Ads会从网站域动态生成此值，您无需输入值。<br><br>对于响应式搜索广告，您无需输入值。 显示URL将自动从最终URL中的域提取。 您可以选择使用“路径1”和“路径2”字段自定义URL。<br><br>您不能创建或编辑，但可以删除扩展的文字广告，Google广告已于2022年6月弃用。<br><br><b>注意：</b> （具有最终URL的帐户）显示URL和最终URL中的域名必须匹配。</p> | |显示路径1 | <p>(展开的文字广告<span> 和响应式搜索广告</span> 仅限)</p><p>（可选）添加到显示URL的文本，将自动从最终URL中提取。 在URL中，它的前面有一个正斜杠(/)。 路径不能包含正斜杠(/)或换行符(\n)。 最大长度为15个字符或7个双字节字符。</p><p>要插入广告自定义项，请使用以下格式，其中 `Default text` 是一个可选值，可在信息源文件不包含有效值时插入：</p><ul><li><p>Google广告： `{CUSTOMIZER.AdCustomizerName:Default text}`，例如 `{CUSTOMIZER.Discount:10%}`</p></li><li><p>Microsoft Advertising： `{CUSTOMIZER.Attribute name:Default text}`，例如 `{CUSTOMIZER.Discount:10%}`</p></li></ul><p>例如，如果显示路径1为“deals”，则显示URL为&lt;<i>显示URL</i>>/deals，例如www.example.com/deals。</p><p>您不能创建或编辑，但可以删除扩展的文字广告，Google广告已于2022年6月弃用。</p> | |显示路径2 |附加显示路径；请参阅“显示路径1”条目。<br><br>示例：如果显示路径1为“deals”，而显示路径2为“local”，则显示URL为&lt;<i>显示URL</i>>/deals/local，例如www.example.com/deals/local。</p><p>您不能创建或编辑，但可以删除扩展的文字广告，Google广告已于2022年6月弃用。</p> | |促销行 |(仅限Google产品列表广告)要包含在搜索结果中的产品列表内的可选促销行。 最大长度为45个字符。</p><p>根据广告在页面上的显示位置，促销行可能会出现在与广告相关的不同位置（例如广告下方）。 | |链接名称 | <p>站点链接文本。 它最多可包含25个字符。</p><p>对于新的站点链接，您必须在站点链接行中包含促销活动名称。 对于广告组级别的站点链接，您还必须包含广告组名称。</p><p><b>注意：</b> 现有35个字符的文本仍会显示在台式机和平板电脑的广告中，但不会显示在移动设备上。</p> | |移动应用程序平台(Google Adwords) |（仅限现有应用程序安装广告）运行移动应用程序的操作系统： <i>android</i> 或 <i>ios</i>. | |移动设备应用程序ID (Google Adwords) |（仅限现有应用程序安装广告） <p>应用程序ID或包名称。 | |移动设备应用程序名称(Google Adwords) |（仅限现有应用程序安装广告）应用程序的名称。 | |开始日期 | <p>（仅限增强型站点链接）对站点链接进行投标的第一个日期，采用广告商所在的时区以及以下格式之一： <span style="font-style: italic;"><i>m/d/yyyy</i></span>， <span style="font-style: italic;"><i>m/d/yy</i></span>， <span style="font-style: italic;"><i>m-d-yyyy</i></span>，或 <span style="font-style: italic;"><i>m-d-yy</i></span>. 新的增强型站点链接的默认值为当天。</p><p><b>注意：</b> 新的增强型站点链接只能在具有现有增强型站点链接或没有站点链接的活动中创建。</p> | |结束日期 | <p>（仅限增强型站点链接）对站点链接发出投标的最后日期，以广告商的时区为单位并采用以下格式之一：  <span style="font-style: italic;"><i>m/d/yyyy</i></span>， <span style="font-style: italic;"><i>m/d/yy</i></span>， <span style="font-style: italic;"><i>m-d-yyyy</i></span>，或 <span style="font-style: italic;"><i>m-d-yy</i></span>. 默认值为none（无结束日期）。</p><p><b>注意：</b> 新的增强型站点链接只能在具有现有增强型站点链接或没有站点链接的活动中创建。</p> | |排除平板电脑(Google Adwords) |（仅限现有应用程序安装广告）</p><p>（可选）阻止Google Ads向平板电脑用户显示广告。 值可以包括 <i>是</i> 和 <i>否</i>. | |登陆页面后缀 |任何要附加到最终URL末尾以跟踪信息的参数。 示例： `param2=value1&param3=value2`<br><br>参见“[的点击跟踪格式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md).”<br><br>较低级别的最终URL后缀会覆盖帐户级别的后缀。 为便于维护，除非需要对各个帐户组件进行不同的跟踪，否则请仅使用帐户级别的后缀。 要在广告组级别或更低级别配置后缀，请使用Google广告编辑器。 | |跟踪模板 |跟踪模板，用于指定所有离场域重定向和跟踪参数，并将最终URL嵌入到ValueTrack参数中。 最粒度级别的跟踪模板（使用关键字作为最粒度）将覆盖所有更高级别的值。<br><br>对于Adobe广告转化跟踪（在营销活动设置包括“EF重定向”和“自动上传”时应用），Search、Social和Commerce会在您保存记录时自动附加其自身的重定向和跟踪代码。<br><br>对于第三方重定向和跟踪，请输入一个值。 有关在跟踪模板中指示最终URL的ValueTrack参数列表，请参阅 <a href="https://support.google.com/google-ads/answer/2375447?hl=en" target="_blank">Google Ads文档</a>.<br><br>要删除现有值，请使用值 `[delete]` （包括括号）。 | |基本URL/最终URL |搜索引擎用户在单击您的广告时进入的登陆页面URL，包括为促销活动或帐户配置的任何附加参数。 关键词级别的基本/最终URL将覆盖广告级别和更高级别的URL。<br><br>要删除现有值，请使用值 `[delete]` （包括括号）。 | |目标URL |（出于信息目的包含在生成的批量工作表中；未发布到搜索引擎）对于具有目标URL的帐户，此URL可将广告链接到广告商网站上的基本URL/登陆页面（有时通过另一个跟踪点击的网站，然后将用户重定向到登陆页面）。 它包括为Search、Social和Commerce营销活动或帐户配置的任何附加参数。 如果您生成了跟踪URL，则跟踪URL基于帐户设置和促销活动设置中的跟踪参数。 如果附加了特定于搜索引擎的参数，则这些参数可能会被等效的搜索、社交和商务参数替换。<br><br>对于具有最终URL的帐户，此列显示与“基本URL”/“最终URL”列相同的值。 | |自定义URL参数 |要替换的数据 `{custom_code}` 动态变量（当变量包含在搜索帐户或促销活动设置的跟踪参数中时）。 要在跟踪URL中插入自定义值，您必须使用“生成跟踪URL”选项上传批量工作表文件。 | |创意类型 |广告格式： <i>文本广告</i>， <i>扩展的文本广告</i>， <i>动态搜索广告</i> （已弃用的广告类型）， <i>扩展的动态搜索广告</i>， <i>显示广告</i>， <i>应用程序安装广告</i> （已弃用）， <i>图像</i> <i>产品广告</i> （购物广告），或 <i>响应式搜索广告</i>. 新广告的默认值为 <i>文本广告</i>.<br><br>需要创建或编辑产品广告的状态。 | | Param1 | <p>的数值 `{param1}` 广告参数，该参数可以包含在批量处理工作表文件中任何广告的广告副本或显示URL中。 最大长度为25个字符，您可以包含以下非数字字符：</p><ul><li><p>值可以在前面或后面附加货币符号或代码。 例如， `£2.000,00` 和 `2000GBP` 有效。</p></li><li><p>该值可以包括逗号(`,`)或句点(`.`)作为分隔符，并带有可选句点(`.`)或逗号(`,`)表示小数值。 例如， `1,000.00` 和 `2.000,10` 有效。</p></li><li><p>该值可以添加前缀，也可以附加一个百分比符号(`%`)，加号(`+`)或减号(`- `)。 例如， `20%`， `208+`、和 `-42.32` 有效。</p></li><li><p>两个数字可以用正斜杠嵌入。 例如， `4/1` 和 `0.95/0.45` 有效。</p></li></ul><p>要删除现有值，请使用值 `[delete]` （包括括号）。</p> | | Param2 |的数值 `{param2}` 广告参数，该参数可以包含在批量处理工作表文件中任何广告的广告副本或显示URL中。 有关更多信息，请参阅Param1条目。| |受众 |搜索广告(RLSA)目标受众或营销活动或广告组的已排除受众的再营销列表。 您将在“目标类型”字段中指定它是目标还是排除项。 | |目标类型 |（当指定受众时）指定的受众是否为 <i>包含</i> （目标）或 <i>排除项</i>. | |营销活动状态 |营销活动的显示状态： <i>活动</i>， <i>已暂停</i>， <i>已结束</i> （不可编辑），或 <i>已删除</i> （仅限现有营销活动）。 新营销活动的默认值为 <i>活动</i>. 要删除活动或暂停的营销活动，请输入值 <i>已删除</i>. | |广告组状态 |广告组的显示状态： <i>活动</i>， <i>已暂停</i>，或 <i>已删除</i> （仅限现有广告组）。 新广告组的默认值为“活动”。 要删除活动或暂停的广告组，请输入值 `Deleted`. | |关键词状态 |关键字的显示状态： <i>活动</i>， <i>已暂停</i>，或 <i>已删除</i> （仅限现有关键字）。 新关键字的默认值为“活动”。 要删除活动或暂停的关键字，请输入值 <i>已删除</i>. | |广告状态 |广告的显示状态： <i>活动</i>， <i>已删除</i> （仅限现有广告）、 <i>未批准</i> （不可编辑），或 <i>已暂停</i>. 新广告的默认值为“活动”。 要删除活动或暂停的广告，请输入值 <i>已删除</i>. | |投放状态 |网站投放的状态： <span style="font-style: italic;"><i>活动</i></span>， <span style="font-style: italic;"><i>已暂停</i></span>，或 <span style="font-style: italic;"><i>已删除</i></span> （仅限现有广告）。 新网站的默认值是 <span style="font-style: italic;"><i>活动。</i></span> 要删除活动或暂停的投放位置，请输入值 <span style="font-style: italic;"><i>已删除</i></span>. | |目标状态 |动态搜索目标的状态： <span style="font-style: italic;"><i>活动</i></span>， <span style="font-style: italic;"><i>已暂停</i></span>，或 <span style="font-style: italic;"><i>已删除</i></span> （仅限现有目标）。 新目标的默认值为 <span style="font-style: italic;"><i>活动。</i></span> 要删除活动或暂停的目标，请输入值 <span style="font-style: italic;"><i>已删除</i></span>. | |产品组状态 |产品组的显示状态： <span style="font-style: italic;"><i>活动</i></span> <span>或</span> <span style="font-style: italic;"><i>已删除</i></span> （仅限现有产品组）。 新产品组的默认值为 <span style="font-style: italic;"><i>活动</i></span>. 要删除活动的产品组，请输入值 <span style="font-style: italic;"><i>已删除</i></span>. | |站点链接状态 |站点链接的显示状态： <span style="font-style: italic;"><i>活动或删除</i></span> （仅限现有站点链接）。 新站点链接的缺省值为 <span style="font-style: italic;"><i>活动</i></span>. 要删除活动的站点链接，请输入值 <span style="font-style: italic;"><i>已删除</i></span>. | |位置状态 |位置目标的状态： <i>活动</i> 或 <i>已删除</i> （仅限现有位置）。 新位置的缺省值为“活动”。 要删除活动位置，请输入值 <i>已删除</i>. | | RLSA目标状态 |促销活动或广告组级别RLSA目标或(仅限Google广告)排除的状态： <span style="font-style: italic;"><i>活动或删除</i></span> （仅限现有目标）。 新目标或排除项的默认值是 <span style="font-style: italic;"><i>活动</i></span>. 要删除活动目标或排除项，请输入值 <span style="font-style: italic;"><i>已删除</i></span>. | |设备目标状态 | <p>营销活动或广告组级别设备目标的状态： <span class="Option">活动</span> 或 <span class="Option">已删除</span>. 对于新的营销活动和广告组，默认为 <span class="Option">活动</span>.</p> | | \[广告商特定的标签分类\] |（以特定于广告商的标签分类命名，例如名为“颜色”的标签分类的“颜色”）与实体关联的指定分类的值。 每个实体的每个分类只能包含一个值（例如，促销活动A的“颜色”标签分类为“红色”）。 最大长度为100个字符，该值可以包含ASCII和非ASCII字符。<br><br>标签分类及其标签值将应用于所有子组件；以后添加的新组件会自动与标签关联。 产品组的标签分类将应用于单元（最细化）级别。<br><br>分类名称和分类值均不区分大小写。 | |约束 |分配给图元的约束。 每个图元只能分配一个约束。<br><b>>约束由子实体继承，因此，除非要覆盖继承的值，否则不需要为子实体输入值。 | |促销活动ID |标识现有营销活动的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅在更改促销活动名称时需要，除非行中包含促销活动的“AMO ID”。 | |广告组ID |标识现有广告组的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅在更改促销活动名称时需要，除非行包含广告组的“AMO ID”。 | |关键字ID |标识现有关键字的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅当更改关键字时才需要，除非行包含a)足够的属性列来标识关键字或b)“AMO ID”。 | |广告ID | <p>标识现有广告的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 对于响应式搜索广告，编辑或删除广告数据需要广告ID或AMO ID。 对于所有其他实体类型，只有在更改广告状态时才需要AMO ID，除非该行包含a)足以识别广告的广告属性列或b)“AMO ID”。 但是，如果您既不包括广告ID也不包括AMO ID，并且广告属性列与多个广告匹配，则仅其中一个广告的状态将更改。</p><p><b>注意：</b> 如果您编辑a)广告属性列（现有广告的状态除外）或b)响应式搜索广告的任何数据，并且既未包含广告ID也未包含AMO ID，则会创建新广告，并且现有广告不会发生更改。</p> | |投放ID |标识网站投放位置的唯一ID。 仅当更改或删除投放位置时才是必需的，除非该行包含a)足够的属性列来标识投放位置或b)“AMO ID”。 | |目标ID |标识现有自动目标的唯一ID。 仅当更改或删除自动目标时才需要，除非行包含目标的“AMO ID”。 | |产品组Id |标识现有产品组的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅当更改或删除产品组时才需要，除非该行包含a)足够的属性列来标识产品组或b)“AMO ID”。 | |站点链接ID |标识现有站点链接的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅当更改或删除站点链接时才需要，除非该行包含a)足够的属性列来标识站点链接或b)“AMO ID”。 但是，如果您既不包括站点链接广告ID也不包括AMO ID，并且属性列与多个站点链接匹配，则只有其中一个站点链接的状态将更改。</p><p><b>注意：</b> 如果您编辑现有站点链接的“状态”之外的站点链接属性列，并且既不包括站点链接ID也不包括AMO ID，则会创建新的站点链接，并且现有的站点链接不会发生更改。 | | RLSA目标ID |标识现有营销活动或广告组级别RLSA目标或(仅限Google广告)排除项的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅当更改或删除目标或排除项时才需要，除非行包含目标的“AMO ID”。 | |设备目标编号 | <p>标识现有营销活动级别或广告组级别设备目标或排除项的唯一ID。 在CSV和TSV文件中，它的前面必须带有单引号(&#39;)。[^1] 仅在更改或删除目标时需要，除非行包含目标的“AMO ID”。</p> | | AMO ID |（在生成的批量处理工作表中）Adobe生成的同步实体的唯一标识符。 对于响应式搜索广告，除非包含广告ID，否则编辑或删除广告时需要AMO ID。 要使用AMO ID编辑所有其他实体类型的数据，需要使用AMO ID来编辑或删除数据，除非您包含实体ID和父实体ID。<br><br>Search、Social和Commerce会使用该值来确定要编辑的正确身份，但不会将ID发布到广告网络。 | | EF错误消息 |（出于信息目的包含在生成的批量工作表中）用于显示来自广告网络的关于行中数据的错误消息的占位符；错误消息包含在EF错误文件中。 此值未发布到广告网络。 | | SE错误消息 |（出于信息目的包含在生成的批量工作表中）用于显示来自广告网络的有关行中数据的错误消息的占位符；错误消息包含在SE错误文件中。 此值未发布到广告网络。 | |劐免请求 |（出于信息目的包含在生成的批量工作表中）用于显示广告违反的任何Google广告策略的名称和文本的预留位置。 | |零售哈希 |(出于信息目的，包含在使用高级Campaign Management生成的批量工作表中)字母数字哈希代码(如f9639f40cdf56524b541e5dacf55a991)，表示项目是使用高级(ACM)视图生成的。 |

<table style="table-layout:auto">

<!-- 

## Fields required to create, edit, or delete each account component

### Campaign fields

| Acct Name | Required unless each row includes an &quot;AMO ID&quot; for the entity. |
| Campaign Name | Required | The unique name that identifies a campaign for an account. |
| Campaign Budget | Required: Create<br><br>>Optional: Edit or delete | A daily spending limit for the campaign, with or without monetary symbols and punctuation. This value overrides but can't exceed the account budget. |
| Delivery Method | Required: Create<br><br>Optional: Edit or delete |
| Channel Type | Required: Create<br><br>Optional: Edit or delete |
| Networks | Required: Create<br><br>Optional: Edit or delete |
| DSA Domain Name | Required: Create<br><br>Optional: Edit or delete |
| DSA Domain Language | Required: Create<br><br>Optional: Edit or delete |
| Campaign Priority | Required/Optional: Create<br><br>Optional / n/a: Edit or delete  |
| Merchant ID | Required/Optional: Create<br><br>Optional / n/a: Edit or delete |
| Sales Country | Required/Optional: Create<br><br>Optional / n/a: Edit or delete |
| Product Scope Filter | Optional |
| Languages | Optional |
| Device Targets | Optional |
| Device OS Targets (Google Adwords) | Optional |
| Mobile Carriers (Google Adwords) | Optional |
| Audience Target Method | n/a |
| Landing Page Suffix | <p>Optional |
| Tracking Template | Optional |
| Campaign Status | Optional: Create or edit<br><br>Required: Delete |
| \[Advertiser-specific Label Classification\] | Optional |
| Constraints | Optional |
| Campaign ID | Required only when you change the campaign name, unless the row includes an &quot;AMO ID&quot; for the campaign. |
| AMO ID | n/a: Create<br><br>Required/Optional: Edit or delete |

### Ad group fields

| Field | Required? |
| ---- | ---- |
| Acct Name | Required unless each row includes an &quot;AMO ID&quot; for the entity. |
| Campaign Name | Required |
| Networks | n/a |
| GDN Custom Bid Level | Optional |
| Ad Group Name | Required  |
| Ad Group Type | Required |
| Max CPC | Optional |
| Max Content CPC | Optional |
| Audience Target Method | Required |
| Tracking Template | Optional |
| Ad Group Status  | Optional: Create or edit<br><br>Required: Delete |
| \[Advertiser-specific Label Classification\] | Optional |
| Constraints | Optional |
| Ad Group ID | Required only when you change the campaign name, unless the row includes an &quot;AMO ID&quot; for the ad group. |
| AMO ID | The AMO ID is required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |

### Keyword fields

Campaign Name
Ad Group Name
Keyword Status
Max CPC
Tracking Template
URLs (Base URL/Final URL, Destination URL)
Exemption Request (Google Adwords)
First Page Bid
Keyword
Match Type
Param1
Param2
Quality Score
Custom URL Param
Label Classification

| Field | Required? | Description |
| ---- | ---- | ---- |
| Base URL/Final URL |  |

### Placement fields


### Text/Product listing fields

This uses the "[!UICONTROL Creative (except RSA)]" row in the [!UICONTROL Download Bulksheet] dialog.


### Expanded dynamic search ad

This ad type is now called "dynamic search ad" in [!DNL Google Ads].

This uses the "[!UICONTROL Creative (except RSA)]" row in the [!UICONTROL Download Bulksheet] dialog.


### Responsive search ad fields 

This uses the "[!UICONTROL Responsive Search Ad]" row in the [!UICONTROL Download Bulksheet] dialog.


### Dynamic search target (auto target) fields


### Shopping product group fields


### Campaign-level and ad group-level sitelink fields


### Location target fields

| Field | Required? ]
| ---- | ---- |
| Location | Required: Create or edit<br><br>Optional: Delete |
| Location Type | Optional  |

## Campaign-level and ad group-level device target fields

| Field | Required? | Description |
| ---- | ---- | ---- |
| Device Target Status | Optional |
| Device Target ID | Required only when you change or delete the target, unless the row includes an &quot;AMO ID&quot; for the target. |
| AMO ID | The AMO ID is required to edit or delete the data unless you include the entity ID and parent entity ID.<br><br>Search, Social, & Commerce uses the value to determine the correct identity to edit but doesn't post the ID to the ad network. |


## Campaign-level and ad group-level RLSA target/exclusion fields

-->

[^1]： [!DNL Excel] 在打开文件时，将大型数字转换为科学记号(如2.12E+09 for 2115585666)。 要查看标准表示法中的数字，请选择列中的任意单元格，然后单击公式栏中的。

>[!MORELIKETHIS]
>
>* [附录 — 批量处理工作表错误](../bulksheet-errors.md)
>* [可在批量工作表中执行的操作](bulksheet-operations.md)
>* [支持的批量工作表文件格式](bulksheet-file-formats.md)
>* [下载/创建批量处理工作表文件](../bulksheet-download.md)
>* [的点击跟踪格式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [上传批量处理工作表文件或更正的错误文件](../bulksheet-upload.md)

