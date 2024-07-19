---
title: 下载/创建批量处理工作表文件
description: 了解如何通过下载广告网络的帐户数据来创建批量工作表文件。
exl-id: a3fcef52-3d36-462e-a975-c741d003326e
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1759'
ht-degree: 0%

---

# 下载/创建批量处理工作表文件

您可以使用自定义设置为一个或多个受支持的[广告网络](bulksheet-about.md#bulksheet-functionality-by-network)上的一个或多个帐户创建批量工作表。 批量工作表包括搜索、社交和Commerce中的数据。

对于同步的促销活动，您可以在下载数据之前选择与广告网络同步，以确保包括广告网络端的最新数据更改。 对于所有广告网络，您可以选择生成新的点击跟踪URL以包含在文件中。

>[!NOTE]
>
>您还可以[根据促销活动管理视图](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)中的可见列创建批量处理工作表文件。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]** > **[!UICONTROL Campaigns]** > **[!UICONTROL Bulksheets]**。

1. 单击工具栏中的&#x200B;**[!UICONTROL Download Bulksheet]**。

1. 指定[批量工作表设置](#bulksheet-download-settings)：

1. 在&#x200B;**[!UICONTROL Selections]**&#x200B;选项卡上，在字段中输入或选择信息。

1. （可选）单击&#x200B;**[!UICONTROL Rows and Columns]**&#x200B;选项卡，指定要在批量处理工作表中包含行的帐户组件和组件状态，然后指定每个选定组件要包含的列。

   有关可用批量处理工作表行的列表，请参阅“[按广告网络批量处理工作表行](#bulksheet-rows-by-ad-network)”。

1. （可选）单击&#x200B;**[!UICONTROL Filters]**&#x200B;选项卡，然后为要包含在批量处理工作表中的特定促销活动、广告组、广告/创意、关键字、投放位置和其他实体指示条件：

   1. 选择参数（实体名称或ID；或广告、关键字或版面的任何元素），选择运算符，然后输入适用的值。 例如，要仅返回[!DNL Google Ads]帐户标题中包含“鞋子”的广告，请选择&#x200B;*标题*，选择&#x200B;*[!UICONTROL contains]*，然后在输入字段中输入`shoes`。

   1. （要应用其他过滤器）对于每个其他过滤器，请单击&#x200B;**[!UICONTROL +Add Filter]**，选择&#x200B;**[!UICONTROL AND]**&#x200B;或&#x200B;**[!UICONTROL OR]**，选择广告元素或关键字和运算符，然后输入适用的值。

1. 单击&#x200B;**[!UICONTROL Download]**。

当任务开始时，窗口会显示通知，但将保持打开状态，以便您可以根据需要继续创建其他批量工作表。 适用于您选择的任何新帐户的任何指定过滤器和排除项都会保留。 当任务开始时，该文件将列在“批量处理工作表”视图中。 创建文件时，您会收到一封电子邮件通知，其中包含指向文件的链接；根据编译的数据量，该通知可能需要几分钟或更长时间。 但是，如果文件生成失败，则“批量处理工作表”视图中会列出一个错误文件，并且您会收到一封电子邮件通知，其中包含指向该错误文件的链接。

## 批量工作表下载设置 {#bulksheet-download-settings}

| 选项卡 | 参数 | 描述 |
|----|----|----|
| [!UICONTROL Selections] | [!UICONTROL SE Accounts] | 要向其上传数据的帐户、营销活动或广告组：<ul><li>要选择帐户及其所有营销活动和广告组，请选中帐户名称旁边的复选框，然后单击>>以将其移至[!UICONTROL Selected Filters]列。</li><li>要选择单个营销活动或广告组，请单击帐户旁边以展开它，（如有必要）单击营销活动旁边以展开它，选中营销活动或广告组名称旁边的复选框，然后单击>>以将其移动到[!UICONTROL Selected Filters]列。 例如，要仅获取帐户1中促销活动1的数据，请展开帐户1，选中促销活动1旁边的复选框，然后将其移至[!UICONTROL Selected Filters]列。</li></ul><b>注释：</b><ul><li>单个批量工作表可以应用于多个广告网络中的多个帐户。 广告网络特定的列在批量工作表中使用广告网络名称进行标记(例如“移动运营商(Google Ads)”)。</li><li>要查看任何项目的组件类型，请将光标悬停在其上。</li><li>对于营销活动，广告网络名称的第一个字母在帐户名称后面用括号括起来(如[!DNL Google Ads]帐户的“Acme Realty (G)”)。</li><li>默认情况下，仅列出活动和已启用的帐户及其活动组件。 要查看暂停的和删除的组件，请单击[!UICONTROL Show]旁边的![向下箭头](/help/search-social-commerce/assets/arrow-down-expand.png "向下箭头")并选择**[!UICONTROL All]。 |
| | [!UICONTROL Generate Tracking URLs] | （可选）在具有跟踪模板的帐户中包含跟踪模板和登陆页面后缀（适用于适用的广告网络），或者在具有目标URL的帐户中包含嵌入跟踪代码的目标URL，适用于批量处理工作表中的关键字、广告、投放位置、站点链接和[!DNL Google Ads]产品组。 默认情况下，此选项处于选中状态。<br><br>选择此选项后，将根据帐户设置或营销活动设置的[!UICONTROL Campaign Tracking]部分中的参数生成URL。 默认情况下，如果跟踪URL已存在，则不会重新生成这些URL，除非需要新的URL（例如，如果关键词匹配类型、广告文本或帐户的跟踪参数已更改）。<br><br><b>注释：</b><ul><li>如果广告商使用Adobe Advertising转化跟踪，并且相关帐户未配置为自动生成和上传跟踪URL，则当基本URL发生更改时，您必须生成新的跟踪URL。</li><li>如果不选择此选项，您以后在上传或发布文件时仍可以生成跟踪URL。</li></ul> |
| | [!UICONTROL Perform Pre-sync] | （可选）指示Search、Social和Commerce将其文件与指定的营销活动同步，以确保所有数据都相同。 默认情况下，不选中此选项。<br><b>注意：</b> Search、Social和Commerce每天与广告网络自动同步一次，每次在广告网络上检测到新促销活动时，以及每次从Search、Social和Commerce中更改促销活动数据时。 如果您认为最近对促销活动或帐户数据的更改直接在广告网络中或者使用广告网络的桌面编辑器进行，请选择此选项。 选择此选项时，批量工作表创建需要较长时间。 |
| | [!UICONTROL Bulksheet Name] | 新批量表单的名称和文件类型。 默认情况下，该文件会以制表符分隔的值格式创建，并命名为以下名称之一：<ul><li>（适用于广告网络的所有帐户） `&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>（对于单个帐户） `&lt;account name&gt;_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`</li><li>（适用于多个帐户） `MultipleAccounts_&lt;search_engine name&gt;_&lt;creation date in the format MMDDYYYY&gt;.tsv`。</li></ul>您可以重命名该文件。 名称不能包含以下字符： `# % &amp; * | \ : &quot; &lt; &gt; . ? or /`。<br><br>更改文件类型（可选）。 选项包括&#x200B;*[!UICONTROL .tsv]* （用于制表符分隔的值）、*[!UICONTROL .txt]* （用于符合Unicode的ASCII文本）、*[!UICONTROL .csv]* （用于逗号分隔的值）或&#x200B;*[!UICONTROL .zip]* （用于解压缩到TSV文件的压缩ZIP格式）。<br><br><b>提示：</b>对于包含国际字符的批量工作表，请使用TSV或TXT格式。 |
| [!UICONTROL Rows and Columns] | [!UICONTROL Bulksheet Rows] | 实体及其相应状态将包含在批量工作表中，每个条目具有一个数据行。 例如，如果包含活动的营销活动，则批量处理工作表将针对每个活动的营销活动包含一行。 只包含具有选定状态的选定实体。 根据指定的广告网络预先选择默认值。 默认情况下，只包括所选实体的活动实例。 有关可用批量处理工作表行的列表，请参阅“[按广告网络批量处理工作表行](#bulksheet-rows-by-ad-network)”。<br><br>若要添加或删除实体，请分别选中或清除实体旁边的复选框。 要添加或删除实体的状态，请单击状态菜单旁的，然后分别选中或清除实体旁的复选框。 |
| | [!UICONTROL Cascading Status Hierarchy] | 使用AND操作，将子实体的范围筛选为具有指定父实体状态的子实体。 例如，如果您选择“活跃营销活动”、“活跃广告组”和“活跃关键词”，则批量处理工作表将仅包含活跃营销活动活跃广告组中的活跃关键词。<br><br>如果不选择此选项，则不会考虑父项状态，筛选器将使用OR操作。 例如，如果您选择“活跃营销活动”、“活跃广告组”和“活跃关键词”，则批量工作表将包含所有活跃营销活动；所有活跃的广告组（无论父级营销活动状态如何）和所有活跃关键词（无论父级营销活动和广告组状态如何）。 |
| | [!UICONTROL Bulksheet Columns] | 要包含在下载的批量处理工作表文件中的列：<ul><li>*[!UICONTROL AMO ID]*： （如果未选择“[!UICONTROL SE ID]”，则为必需）包含每个实体/行[!DNL Adobe]生成的唯一标识符。 Search、Social和Commerce会使用该值确定要编辑的正确身份，但不会将其发布到广告网络。 稍后，您可以使用[!UICONTROL AMO ID]作为标识符来编辑实体的数据，而不是使用实体ID和父实体ID。</li><li>*[!UICONTROL SE ID]*： （如果未选择“[!UICONTROL AMO ID]”，则为必需）包含每个包含的列及其父实体的广告网络的唯一标识符。 稍后，如果您使用[!UICONTROL SE ID]作为标识符编辑任何实体的数据，则还必须包括父实体的行（包括其[!UICONTROL SE ID]值）。</li><li>*[!UICONTROL Platform]*：每行的开头都包含[!UICONTROL Platform column]以指示广告平台（如“百度”）。</li><li>*[!UICONTROL Acct Name]*： （未选择“[!UICONTROL AMO ID]”时必需）包含每个实体/行的广告网络帐户名称。</li><li>\[要包含的列\]：要包含与[!UICONTROL Bulksheet Rows]节中每个选定实体相关的所有、无或仅选定列。 要查看与实体相关的各个列，请单击实体名称旁边的![向右箭头](/help/search-social-commerce/assets/compressed-item.png "向右箭头")。 默认情况下，每个选定的实体行都包含所有相关列。 取消选中任何实体旁边的复选框，或取消选中任何单个列旁边的复选框，以将其从批量处理表中排除。</li></ul><br><br><b>提示：</b>请确保您包含足够的列，以标识批量处理工作表文件的每一行中的项。 例如，假设您在[!UICONTROL Bulksheet Rows]选择器中包括关键字行，但排除所有与关键字相关的列。 生成的批量工作表包含每个关键字实例的一行。 但是，由于不包含与关键字相关的列（甚至包括AMO ID或SE ID ），因此您无法识别哪个关键字实例属于特定行，并且除非手动添加相应的ID列和值，否则无法使用批量工作表来更新数据。 |
| [!UICONTROL Filters] | | 要包含在批量处理工作表中的特定促销活动、广告组、广告/创意、关键字和/或版面的标准：<ol><li>选择参数（实体名称或ID；或创意、关键词或版面的任何元素），选择运算符，然后输入适用的值。<br>例如，要仅返回[!DNL Google Ads]帐户标题中带有“鞋子”的广告，请选择&#x200B;*[!UICONTROL Headline]*，选择&#x200B;*[!UICONTROL contains]*，然后在输入字段中输入`shoes`。</li><li>（要应用其他过滤器）对于每个其他过滤器，请单击&#x200B;**[!UICONTROL +Add Filter]**，选择&#x200B;**[!UICONTROL AND]**&#x200B;或&#x200B;**[!UICONTROL OR]**，选择广告元素或关键字和运算符，然后输入适用的值。</li></ul> |

## 按广告网络批量处理工作表行 {#bulksheet-rows-by-ad-network}

| 批量处理工作表行 | [!DNL Baidu] | [!DNL Google Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo! Japan Ads] | [!DNL Yahoo Native] | 扬代克斯 | 注释 |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | — |
| [!UICONTROL Adgroup] | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | — |
| [!UICONTROL Creative] *或* [!UICONTROL Creative (except RSA)] | 是 | 是 | 是 | — | — | 是 | 是 | 是 | 是 | ([!DNL Google  Ads])用于所有广告类型，但响应式搜索广告除外，这些广告在[!UICONTROL Responsive Search Ad]行中可用。 |
| [!UICONTROL Responsive Search Ad] | — | 是 | 是 | — | — | — | — | — | — | — |
| [!UICONTROL Keyword] | 是 | 是 | 是 | 是 | 是 | — | 是 | 是 | 是 | 仅用于非负关键字。 要查看在营销活动或广告组级别创建的负关键字，请使用可用的[!UICONTROL Campaign Negative Keyword]或[!UICONTROL Adgroup Negative Keyword]行。 |
| [!UICONTROL Promoted Pin] | — | — | — | — | 是 | — | — | — | — | — |
| [!UICONTROL Placement] | — | 是 | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | 是 | 是 | — | — | — | — | — | — | 用于广告组的动态搜索目标。 |
| [!UICONTROL Shopping Product Group] | — | 是 | 是 | — | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | 是 | 是 | — | — | — | — | 是 | — | — |
| [!UICONTROL Campaign Negative Keyword] | 是 | 是 | 是 | — | — | — | 是 | 是 | — | 仅用于营销活动或广告组级别创建的负关键字。 要查看非负关键字，请在可用时使用[!UICONTROL Keyword]行。 |
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
>* [导出生成或上载的批量工作表文件](bulksheet-export.md)
