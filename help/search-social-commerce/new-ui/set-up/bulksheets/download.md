---
title: （新UI）下载/创建批量处理工作表文件
description: 了解如何通过在新的搜索、社交和Commerce UI中下载广告网络的帐户数据来创建批量工作表文件。
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 1637
ht-degree: 0%

---

# （新UI）下载/创建批量处理工作表文件

您可以使用自定义设置为一个或多个受支持的[广告网络](about.md#bulksheet-functionality-by-network)上的一个或多个帐户创建批量工作表。 批量工作表包括搜索、社交和Commerce中的数据。

对于同步的促销活动，您可以在下载数据之前选择与广告网络同步，以确保包括广告网络端的最新数据更改。 对于所有广告网络，您可以选择生成新的点击跟踪URL以包含在文件中。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**。

1. 在工具栏中，单击&#x200B;**[!UICONTROL Bulk Operations]** \> **[!UICONTROL Download Bulksheet]**。

1. 指定[批量工作表设置](#bulksheet-settings)：

   1. 在&#x200B;**[!UICONTROL Selections]**&#x200B;选项卡上，选择要包含并配置批量处理工作表选项的帐户、营销活动或广告组。

   1. （可选）单击&#x200B;**[!UICONTROL Rows and Columns]**&#x200B;选项卡，指定要在批量处理工作表中包含行的帐户组件和组件状态，然后指定每个选定组件要包含的列。

      有关可用批量处理工作表行的列表，请参阅“[按广告网络批量处理工作表行](#bulksheet-rows-by-ad-network)”。

   1. （可选）单击&#x200B;**[!UICONTROL Filters]**&#x200B;选项卡，然后为要包含在批量处理工作表中的特定促销活动、广告组、广告/创意、关键字、投放位置和其他实体指定标准。

1. 单击&#x200B;**[!UICONTROL Download]**。

当任务开始时，窗口会显示通知，但将保持打开状态，以便您可以根据需要继续创建其他批量工作表。 创建文件时，您会收到一封电子邮件通知，其中包含指向文件的链接；根据编译的数据量，该通知可能需要几分钟或更长时间。 如果文件生成失败，“批量处理工作表”视图中会列出一个错误文件，并且您会收到一封电子邮件通知，其中包含指向该错误文件的链接。

## 批量处理工作表设置 {#bulksheet-settings}

### “选择”选项卡 {#bulksheet-selections-settings}

**\[帐户、营销活动和广告组选择\]**

展开网络和帐户层次结构，然后选中要将其数据包含在批量处理工作表中的每个帐户、营销活动或广告组旁边的复选框：

* 要包含帐户的所有营销活动和广告组，请选中帐户名称旁边的复选框。

* 要包含特定营销活动，请展开帐户，然后选中要包含的每个营销活动旁边的复选框。 要包含特定的广告组，请进一步展开某个营销活动，然后选中每个广告组旁边的复选框。

>[!NOTE]
>
>* 单个批量工作表可以应用于多个广告网络中的多个帐户。 广告网络特定的列在批量工作表中使用广告网络名称进行标记(例如“移动运营商(Google Ads)”)。
>* 要查看某个项目的组件类型，请将光标悬停在该项目上。
>* 默认情况下，仅列出活动和已启用的帐户及其活动组件。

**[!UICONTROL Generate Tracking URLs]：**（可选）在具有跟踪模板的帐户中包含跟踪模板和登陆页面后缀（适用于适用的广告网络），或者在具有目标URL的帐户中包含嵌入跟踪代码的目标URL，适用于批量处理工作表中的关键字、广告、投放位置、站点链接和[!DNL Google Ads]产品组。 默认情况下，此选项处于选中状态。

如果选择该选项，将根据帐户设置或营销活动设置的[!UICONTROL Campaign Tracking]部分中的参数生成URL。 默认情况下，如果跟踪URL已存在，则不会重新生成这些URL，除非需要新的URL（例如，如果关键词匹配类型、广告文本或帐户的跟踪参数已更改）。

>[!NOTE]
>
>* 如果广告商使用Adobe Advertising转化跟踪，并且相关帐户未配置为自动生成和上传跟踪URL，则必须在基本URL发生更改时生成新的跟踪URL。
>* 如果不选择此选项，您以后在上传或发布文件时仍可以生成跟踪URL。

**[!UICONTROL Perform pre-sync]：**（可选）指示Search、Social和Commerce将其文件与指定的营销活动同步，以确保所有数据都相同。 默认情况下，不选中此选项。

>[!NOTE]
>
>Search、Social和Commerce每天都会自动与广告网络同步一次，每次在广告网络上检测到新促销活动时，以及每次从Search、Social和Commerce中更改促销活动数据时。 如果您认为最近对促销活动或帐户数据的更改直接在广告网络中或者使用广告网络的桌面编辑器进行，请选择此选项。 选择此选项时，批量工作表创建需要较长时间。

**[!UICONTROL Bulksheet Name]：**&#x200B;新批量处理表的名称和文件类型。 默认情况下，该文件会以制表符分隔的值格式创建，并命名为以下名称之一：

* （适用于广告网络的所有帐户） `<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* （对于单个帐户）`<account name>_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* （适用于多个帐户） `MultipleAccounts_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`

您可以重命名该文件。 名称不能包含以下字符： `# % & * | \ : " < > . ? /`

（可选）更改文件类型。 选项包括&#x200B;*[!UICONTROL .tsv]* （用于制表符分隔的值）、*[!UICONTROL .txt (unicode)]* （用于符合Unicode的ASCII文本）、*[!UICONTROL .csv]* （用于逗号分隔的值）或&#x200B;*[!UICONTROL .zip]* （用于解压缩到TSV文件的压缩ZIP格式）。

>[!TIP]
>
>对于包含国际字符的批量工作表，请使用TSV或TXT格式。

### “行和列”选项卡 {#bulksheet-rows-columns-settings}

**[!UICONTROL Bulksheet Rows]：**&#x200B;实体及其相应状态将作为数据行包含在批量处理工作表中，每个条目包含一行。 例如，如果包含活动的营销活动，则批量处理工作表将针对每个活动的营销活动包含一行。 只包含具有选定状态的选定实体。 根据指定的广告网络预先选择默认值。 默认情况下，只包括所选实体的活动实例。

要添加或删除实体，请选中或清除实体旁边的复选框。 要添加或删除实体的状态，请单击实体旁边的状态菜单，然后选中或清除适用状态的复选框。

有关按广告网络列出的可用行的列表，请参阅[按广告网络批量处理工作表行](#bulksheet-rows-by-ad-network)。

**[!UICONTROL Cascading Status Hierarchy]：**&#x200B;使用AND操作将子实体筛选为具有指定父实体状态的子实体。 例如，如果您选择“活跃营销活动”、“活跃广告组”和“活跃关键词”，则批量处理工作表将仅包含活跃营销活动活跃广告组中的活跃关键词。

如果不选择此选项，则不会考虑父项状态，过滤器将使用OR操作。 例如，如果您选择“活跃营销活动”、“活跃广告组”和“活跃关键词”，则批量工作表将包含所有活跃营销活动；所有活跃的广告组，无论父营销活动状态如何；以及所有活跃关键词，无论父营销活动和广告组状态如何。

**[!UICONTROL Bulksheet Columns]：**&#x200B;要包含在已下载批量处理工作表文件中的列：

* *[!UICONTROL AMO ID]：* （未选择“[!UICONTROL SE ID]”时必需）包含每个实体/行[!DNL Adobe]生成的唯一标识符。 Search、Social和Commerce会使用该值确定要编辑的正确身份，但不会将其发布到广告网络。 稍后，您可以使用[!UICONTROL AMO ID]作为标识符来编辑实体的数据，而不是使用实体ID和父实体ID。

* *[!UICONTROL SE ID]：* （未选择“[!UICONTROL AMO ID]”时必需）包含广告网络每个包含的列及其父实体的唯一标识符。 稍后，如果您使用[!UICONTROL SE ID]作为标识符编辑任何实体的数据，则还必须包括父实体的行（包括其[!UICONTROL SE ID]值）。

* *[!UICONTROL Platform]：*&#x200B;在每行的开头包含一个[!UICONTROL Platform]列，以指示广告平台（如“百度”）。

* *[!UICONTROL Acct Name]：* （如果未选择“[!UICONTROL AMO ID]”，则为必需）包含每个实体/行的广告网络帐户名称。

* \[实体特定的列\]：若要包含与[!UICONTROL Bulksheet Rows]中选择的每个实体相关的所有、无或仅选定列，请单击实体名称旁边的![向右箭头](/help/search-social-commerce/assets/compressed-item.png "向右箭头")以展开该实体，然后选中或清除单个列的复选框。 默认情况下，每个选定的实体行都包含所有相关列。

>[!TIP]
>
>确保包含足够的列，以标识批量处理工作表文件的每一行中的项目。 例如，如果在[!UICONTROL Bulksheet Rows]选择器中包括关键字行，但排除所有与关键字相关的列，则生成的批量工作表将为每个关键字实例包含一个行，但无法识别哪个关键字实例属于特定行。 在这种情况下，除非手动添加相应的ID列和值，否则无法使用批量工作表来更新数据。

### “筛选器”选项卡 {#bulksheet-filters-settings}

要包含在批量处理工作表中的特定促销活动、广告组、广告/创意、关键字和/或版面的标准：

1. 选择参数（实体名称或ID；或创意、关键词或版面的任何元素），选择运算符，然后输入适用的值。

   例如，要仅返回[!DNL Google Ads]帐户标题中包含“鞋子”的广告，请选择&#x200B;*[!UICONTROL Headline]*，选择&#x200B;*[!UICONTROL contains]*，然后在输入字段中输入`shoes`。

1. （要应用其他过滤器）对于每个其他过滤器，请单击&#x200B;**[!UICONTROL +Add Filter]**，选择&#x200B;**[!UICONTROL AND]**&#x200B;或&#x200B;**[!UICONTROL OR]**，选择广告元素或关键字和运算符，然后输入适用的值。

## 按广告网络批量处理工作表行 {#bulksheet-rows-by-ad-network}

| 批量处理工作表行 | [!DNL Baidu] | [!DNL Google Ads] | [!DNL LY Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo DSP] | [!DNL Yahoo Native] | [!DNL Yandex] | 注释 |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | — |
| [!UICONTROL Adgroup] | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | 是 | — |
| [!UICONTROL Creative] *或* [!UICONTROL Creative (except RSA)] | 是 | 是 | 是 | 是 | — | — | 是 | 是 | 是 | ([!DNL Google Ads])用于所有广告类型，但响应式搜索广告除外，它们在[!UICONTROL Responsive Search Ad]行中可用。 |
| [!UICONTROL Responsive Search Ad] | — | 是 | — | 是 | — | — | — | — | — | — |
| [!UICONTROL Keyword] | 是 | 是 | 是 | 是 | 是 | 是 | — | 是 | 是 | 仅用于非负关键字。 要查看在营销活动或广告组级别创建的负关键字，请使用可用的[!UICONTROL Campaign Negative Keyword]或[!UICONTROL Adgroup Negative Keyword]行。 |
| [!UICONTROL Promoted Pin] | — | — | — | — | — | 是 | — | — | — | — |
| [!UICONTROL Placement] | — | 是 | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | 是 | — | 是 | — | — | — | — | — | 用于广告组的动态搜索目标。 |
| [!UICONTROL Shopping Product Group] | — | 是 | — | 是 | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | 是 | — | 是 | — | — | — | 是 | — | — |
| [!UICONTROL Campaign Negative Keyword] | 是 | 是 | 是 | 是 | — | — | — | 是 | — | 仅用于营销活动或广告组级别创建的负关键字。 要查看非负关键字，请在可用时使用[!UICONTROL Keyword]行。 |
| [!UICONTROL Campaign Negative Website] | — | 是 | — | 是 | — | — | — | 是 | — | — |
| [!UICONTROL Adgroup Site Link] | — | 是 | — | — | — | — | — | 是 | — | — |
| [!UICONTROL Creative Site Link] | — | — | — | — | — | — | — | — | 是 | — |
| [!UICONTROL Adgroup Negative Keyword] | 是 | 是 | 是 | 是 | — | — | — | 是 | — | — |
| [!UICONTROL Adgroup Negative Website] | — | 是 | — | 是 | — | — | — | — | — | — |
| [!UICONTROL Campaign Location Target] | 是 | 是 | 是 | 是 | — | — | — | 是 | — | — |
| [!UICONTROL Adgroup Location Target] | — | — | — | 是 | — | — | — | 是 | — | — |
| [!UICONTROL Campaign Device Target] | — | 是 | — | 是 | — | — | — | 是 | — | — |
| [!UICONTROL Adgroup Device Target] | — | 是 | — | 是 | — | — | — | 是 | — | — |
| [!UICONTROL Campaign RLSA Target] | — | 是 | — | 是 | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Target] | — | 是 | — | 是 | — | — | — | — | — | — |
| [!UICONTROL Campaign RLSA Negative] | — | 是 | — | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Negative] | — | 是 | — | — | — | — | — | — | — | — |

有关每个广告网络的必需列和可选列的详细信息，请参阅广告网络特定的批量处理工作表数据格式文章：

* [ [!DNL Baidu] 帐户的必需和可选批量工作表数据](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)
* [ [!DNL Google Ads] 帐户的必需和可选批量工作表数据](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)
* [ [!DNL LY Ads] 帐户的必需和可选批量工作表数据](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)
* [ [!DNL Microsoft Advertising] 帐户的必需和可选批量工作表数据](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)
* [ [!DNL Naver] 帐户的必需和可选批量工作表数据](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
* [ [!DNL Yahoo DSP] 帐户的必需和可选批量工作表数据](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)
* [ [!DNL Yandex] 帐户的必需和可选批量工作表数据](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md)

>[!MORELIKETHIS]
>
>* [（新UI）关于使用批量处理工作表管理营销活动数据](about.md)
>* [（新UI）上载批量工作表或已更正的错误文件](upload.md)
>* [（新UI）发布批量工作表或已更正的错误文件](post.md)
>* [（新UI）验证批量处理工作表文件中的登陆页面](validate-landing-pages.md)
