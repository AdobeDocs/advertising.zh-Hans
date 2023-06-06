---
title: 下载/创建批量处理工作表文件
description: 了解如何通过下载广告网络的帐户数据来创建批量工作表文件。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1757'
ht-degree: 0%

---

# 下载/创建批量处理工作表文件

您可以使用自定义设置为一个或多个帐户上的一个或多个帐户创建批量工作表 [支持的广告网络](bulksheet-about.md#bulksheet-functionality-by-network). 批量工作表包括搜索、社交和商务中的数据。

对于同步的促销活动，您可以在下载数据之前选择与广告网络同步，以确保包括广告网络端的最新数据更改。 对于所有广告网络，您可以根据需要生成新的点击跟踪URL以包含在文件中。

>[!NOTE]
>
>您还可以 [根据营销活动管理视图中的可见列创建批量处理工作表文件](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md).

1. 在主菜单中，单击 **[!UICONTROL Search]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]**.

1. 在工具栏中，单击 **[!UICONTROL Download Bulksheet]**.

1. 指定 [批量处理工作表设置](#bulksheet-download-settings)：

1. 在**[!UICONTROL Selections] 选项卡，在字段中输入或选择信息。

1. （可选）单击 **[!UICONTROL Rows and Columns]** 选项卡，指定要在批量处理工作表中包含行的帐户组件和组件状态，然后指定每个选定组件要包含的列。

   有关可用批量处理工作表行的列表，请参阅&quot;[按广告网络批量处理工作表行](#bulksheet-rows-by-ad-network).”

1. （可选）单击 **[!UICONTROL Filters]** 选项卡，然后为要包含在批量处理工作表中的特定促销活动、广告组、广告/创意、关键字、投放位置和其他实体指示标准：

   1. 选择参数（实体名称或ID；或广告、关键字或版面的任何元素），选择运算符，然后输入适用的值。 例如，只返回标题中包含“鞋子”的广告 [!DNL Google Ads] 帐户，选择 *标题*，选择 *[!UICONTROL contains]*，然后输入 `shoes` 在输入字段中。

   1. （要应用其他过滤器）对于每个其他过滤器，请单击 **[!UICONTROL +Add Filter]**，选择 **[!UICONTROL AND]** 或 **[!UICONTROL OR]**，选择广告元素或关键字和运算符，然后输入适用的值。

1. 单击 **[!UICONTROL Download].

当任务开始时，窗口会显示一个通知，但窗口保持打开状态，以便您可以根据需要继续创建其他批量工作表。 适用于您选择的任何新帐户的任何指定过滤器和排除项都将保留。 当任务开始时，该文件将列在“批量处理工作表”视图中。 创建文件后，您会收到一封电子邮件通知，其中包含指向文件的链接；根据编译的数据量，该通知可能需要几分钟或更长时间。 但是，如果文件生成失败，则“批量处理工作表”视图中会列出一个错误文件，并且您会收到一封电子邮件通知，其中包含指向该错误文件的链接。

## 批量工作表下载设置 {#bulksheet-download-settings}

| 选项卡 | 参数 | 描述 |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | 要向其上传数据的帐户、营销活动或广告组：<ul><li>要选择帐户及其所有促销活动和广告组，请选中帐户名称旁边的复选框，然后单击>>将其移动到 [!UICONTROL Selected Filters] 列。</li><li>要选择单个促销活动或广告组，请单击帐户旁边以展开它，（如有必要）单击下一个促销活动以展开它，选中促销活动或广告组名称旁边的复选框，然后单击>>以将其移动到 [!UICONTROL Selected Filters] 列。 例如，要仅获取帐户1中促销活动1的数据，请展开帐户1，选中促销活动1旁边的复选框，然后将其移至 [!UICONTROL Selected Filters] 列。</li></ul><b>注释：</b><ul><li>单个批量工作表可以应用于多个广告网络内的多个帐户。 广告网络特定的列在批量工作表中使用广告网络名称进行标记(例如“移动运营商(Google Ads)”)。</li><li>要查看任何项目的组件类型，请将光标悬停在该项目上。</li><li>对于营销活动，广告网络名称的首字母在帐户名称后的括号中(例如， [!DNL Google Ads] 帐户)。</li><li>默认情况下，仅列出活动和已启用的帐户及其活动组件。 要查看暂停的和删除的组件，请单击 ![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭头") 旁边 [!UICONTROL Show] 并选择**[!UICONTROL All]. |
|  | [!UICONTROL Generate Tracking URLs] | （可选）在带有跟踪模板的帐户中包含跟踪模板和登陆页面后缀（适用于适用的广告网络），或在带有目标URL的帐户中包含嵌入跟踪代码的目标URL(适用于关键字、广告、投放位置、站点链接和 [!DNL Google Ads] 批量处理工作表中的产品组。 默认情况下，此选项处于选中状态。<br><br>如果选择该选项，将根据 [!UICONTROL Campaign Tracking] 帐户设置或campaign设置的部分。 默认情况下，如果跟踪URL已存在，则除非需要新的URL（例如，如果关键词匹配类型、广告文本或帐户的跟踪参数已更改），否则不会重新生成这些URL。<br><br><b>注释：</b><ul><li>如果广告商使用Adobe广告转化跟踪，且相关帐户未配置为自动生成和上传跟踪URL，则必须在基本URL发生更改时生成新的跟踪URL。</li><li>如果不选择此选项，您以后在上传或发布文件时仍可以生成跟踪URL。</li></ul> |
|  | [!UICONTROL Perform Pre-sync] | （可选）指示Search、Social和Commerce将其文件与指定的营销活动同步，以确保所有数据都相同。 默认情况下，不选中此选项。<br><b>注意：</b> 搜索、Social和Commerce每天自动与广告网络同步一次，每次在广告网络上检测到新促销活动时，以及每次您从Search、Social和Commerce内更改促销活动数据时。 如果您认为最近对促销活动或帐户数据的更改直接在广告网络中或者使用广告网络的桌面编辑器，请选择此选项。 选择此选项后，批量工作表创建所需的时间会更长。 |
|  | [!UICONTROL Bulksheet Name] | 新批量处理表的名称和文件类型。 默认情况下，该文件会以制表符分隔的值格式创建，并命名为以下名称之一：<ul><li>（适用于广告网络的所有帐户） `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>（适用于单个帐户） `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>（适用于多个帐户） `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`.</li></ul>您可以重命名该文件。 名称不能包含以下字符： `# % &amp; * | \ : &quot; &lt; &gt; . ? or /`.<br><br>（可选）更改文件类型。 这些选项包括 *[!UICONTROL .tsv]* （对于制表符分隔的值）， *[!UICONTROL .txt]* （对于符合Unicode的ASCII文本）， *[!UICONTROL .csv]* （对于逗号分隔的值），或 *[!UICONTROL .zip]* （对于压缩的ZIP格式，将解压缩为TSV文件）。<br><br><b>提示：</b> 对于包含国际字符的批量工作表，请使用TSV或TXT格式。 |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | 实体及其相应状态将包含在批量工作表中，每个条目具有一个数据行。 例如，如果包含活动的营销活动，则批量工作表将为每个活动的营销活动包含一行。 只包含具有选定状态的选定实体。 根据指定的广告网络预先选择默认值。 缺省情况下，只包括所选图元的活动实例。 有关可用批量处理工作表行的列表，请参阅&quot;[按广告网络批量处理工作表行](#bulksheet-rows-by-ad-network).”<br><br>要添加或移除图元，请分别选中或清除图元旁边的复选框。 要添加或删除实体的状态，请单击状态菜单旁的，然后分别选中或清除实体旁的复选框。 |
|  | [!UICONTROL Cascading Status Hierarchy] | 使用AND操作，将子实体的范围筛选为具有指定父实体状态的子实体。 例如，如果您选择“活跃营销活动”、“活跃广告组”和“活跃关键词”，则批量工作表将仅包含活跃营销活动活跃广告组中的活跃关键词。<br><br>如果不选择此选项，则不会考虑父项状态，过滤器将使用OR操作。 例如，如果选择“活动营销活动”、“活动广告组”和“活动关键词”，则批量工作表将包含所有活动的营销活动、所有活动的广告组（无论父营销活动状态如何）和所有活动的关键词（无论父营销活动和广告组状态如何）。 |
|  | [!UICONTROL Bulksheet Columns] | 要包含在已下载批量处理工作表文件中的列：&lt;ul><li><li>*[!UICONTROL AMO ID]*：(如果&quot;，则必需。[!UICONTROL SE ID]”未选中)包含 [!DNL Adobe] — 为每个实体/行生成的唯一标识符。 Search、Social和Commerce会使用该值来确定要编辑的正确身份，但不会将其发布到广告网络。 稍后，可以使用编辑实体的数据 [!UICONTROL AMO ID] 作为标识符，而不是实体ID和父实体ID。</li><li>*[!UICONTROL SE ID]*：(如果&quot;，则必需。[!UICONTROL AMO ID]”未选中)包含广告网络中每个包含的列及其父实体的唯一标识符。 稍后，如果您使用 [!UICONTROL SE ID] 作为标识符，则还必须包含父实体的行(包括父实体的 [!UICONTROL SE ID] 值)。</li><li>*[!UICONTROL Platform]*：包括 [!UICONTROL Platform column] ，以指示广告平台（如“百度”）。</li><li>*[!UICONTROL Acct Name]*：(如果&quot;，则必需。[!UICONTROL AMO ID]”未选中)包含每个实体/行的广告网络帐户名称。</li><li>\[要包含的列\]：要包含所有、无或仅包含与中每个选定实体相关的选定列 [!UICONTROL Bulksheet Rows] 部分。 要查看与实体相关的各个列，请单击 ![右箭头](/help/search-social-commerce/assets/compressed-item.png "右箭头") 在实体名称旁边。 默认情况下，每个选定的实体行都包含所有相关列。 取消选中任何实体旁边的复选框或任何单个列旁边的复选框，以将其从批量处理表中排除。</li></ul><br><br><b>提示：</b> 确保包含足够的列，以标识批量处理工作表文件的每一行中的项目。 例如，假设您根据 [!UICONTROL Bulksheet Rows] 选择器，但会排除所有与关键词相关的列。 生成的批量工作表包含每个关键字实例的一行。 但是，由于未包含与关键字相关的列（甚至包括AMO ID或SE ID ），因此您无法识别哪个关键字实例属于特定行，并且除非手动添加相应的ID列和值，否则无法使用批量工作表来更新数据。 |
| [!UICONTROL Filters] |  | 要包含在批量处理工作表中的特定促销活动、广告组、广告/创意、关键字和/或版面的标准：<ol><li>选择参数（实体名称或ID；或创意、关键词或版面的任何元素），选择运算符，然后输入适用的值。<br><br>例如，只返回标题中包含“鞋子”的广告 [!DNL Google Ads] 帐户，选择 *[!UICONTROL Headline]*，选择 *[!UICONTROL contains]*，然后输入 `shoes` 在输入字段中。</li><li>（要应用其他过滤器）对于每个其他过滤器，请单击 **[!UICONTROL +Add Filter]**，选择 **[!UICONTROL AND]** 或 **[!UICONTROL OR]**，选择广告元素或关键字和运算符，然后输入适用的值。</li></ul> |

## 按广告网络批量处理工作表行 {#bulksheet-rows-by-ad-network}

| 批量工作表行 | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft® Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | 扬代克斯 | 注释 |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | — |
| [!UICONTROL Adgroup] | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | — |
| [!UICONTROL Creative] *或* [!UICONTROL Creative (except RSA)] | 是 | 是 | 是 | — | — | 是 | 是 | 是 | 是 | ([!DNL Google  Ads])适用于所有广告类型，但响应式搜索广告除外，此类广告可在 [!UICONTROL Responsive Search Ad] row。 |
| [!UICONTROL Responsive Search Ad] | — | 是 | 是 | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | 是 | 是 | 是 | 是 | 是 | — | 是 | 是 | 是 | 仅用于非负关键字。 要查看在营销活动或广告组级别创建的负关键字，请使用 [!UICONTROL Campaign Negative Keyword] 或 [!UICONTROL Adgroup Negative Keyword] 行（如果可用）。 |
| [!UICONTROL Promoted Pin] | — | — | — | — | 是 | — | — | — | — | — |
| [!UICONTROL Placement] | — | 是 | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | 是 | 是 | — | — | — | — | — | — | 用于广告组的动态搜索目标。 |
| [!UICONTROL Shopping Product Group] | — | 是 | 是 | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | 是 | 是 | — | — | — | — | 是 | — | — |
| [!UICONTROL Campaign Negative Keyword] | 是 | 是 | 是 | — | — | — | 是 | 是 | — | 仅用于营销活动或广告组级别创建的负关键字。 要查看非负关键字，请使用 [!UICONTROL Keyword] 行（如果可用）。 |
| [!UICONTROL Campaign Negative Website] | — | 是 | 是 | — | — | — | — | 是 | — | — |
| [!UICONTROL Adgroup Site Link] | — | 是 | — | — | — | — | — | 是 | — | — |
| [!UICONTROL Creative Site Link] | — | — | — | — | — | — | — | — | 是 | — |
| [!UICONTROL Adgroup Negative Keyword] | 是 | 是 | 是 | — | — | — | 是 | 是 | — | — |
| [!UICONTROL Adgroup Negative Website] | — | 是 | 是 | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Location Target] | 是 | 是 | 是 | — | — | — | 是 | 是 | — | — |
| [!UICONTROL Adgroup Location Target] | — | — | 是 | — | — | — | — | 是 | — | — |
| [!UICONTROL Campaign Device Target] | — | 是 | 是 | — | — | — | — | 是 | — | — |
| [!UICONTROL Adgroup Device Target] | — | 是 | 是 | — | — | — | — | 是 | — | — |
| [!UICONTROL Campaign RLSA Target] | — | 是 | 是 | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Target] | — | 是 | 是 | — | — | — | — | — | — | — |
| [!UICONTROL Campaign RLSA Negative] | — | 是 | — | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Negative] | — | 是 | — | — | — | — | — | — | — | — |

>[!MORELIKETHIS]
>
>* [关于使用批量处理工作表管理营销活动数据](bulksheet-about.md)
>* [发布批量工作表或已更正的错误文件](bulksheet-post.md)
>* [验证批量处理工作表文件中的登陆页面](bulksheet-validate-landing-pages.md)
>* [导出生成或上传的批量处理工作表文件](bulksheet-export.md)

