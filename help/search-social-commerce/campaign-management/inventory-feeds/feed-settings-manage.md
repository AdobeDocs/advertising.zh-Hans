---
title: 配置馈送数据设置
description: 了解如何配置用于控制如何处理馈送数据的设置。
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# 配置馈送数据设置

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （仅删除操作）和仅[!DNL Yandex]帐户*

您可以通过馈送设置配置如何处理馈送数据文件中的广告组、关键字和广告，以及如何专门在FTP文件中处理数据。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Settings]**。

1. 指定[馈送数据设置](#feed-data-settings)：

   1. 在[!UICONTROL Obsolete Item Auto-Processing]部分中，选择字段中的信息。

   1. （广告商通过FTP或直接链接指向商户中心帐户上传数据）在[!UICONTROL FTP/GMC Account Auto-Processing]部分中，选择字段中的信息。

   1. 在[!UICONTROL Miscellaneous Auto-Processing]部分中，选择字段中的信息。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 馈送数据设置 {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]：**&#x200B;将所有[!UICONTROL Obsolete Item Auto-processing]设置应用于：

* *[!UICONTROL Ad Groups Only]：*&#x200B;仅过时的广告组。

* *[!UICONTROL Keywords Only]：*&#x200B;仅过时关键词和产品组。

* *[!UICONTROL Ad Variations Only]* （默认）：仅过时广告。

* *[!UICONTROL Keywords and Ad Variations]：*&#x200B;过时关键字/产品目标/产品组和过时广告。

>[!NOTE]
>
>* 对于[!DNL Google Ads]个购物广告，只有最低级别的产品组会受到影响。
>* 对于[!DNL Yandex]帐户，无论此设置如何，始终对广告变体执行过时的项目自动处理任务。

**[!UICONTROL When the Scheduled End Date is reached]：** （仅手动发布数据）当结束时间到达时，如何处理以指定结束日期和时间发布的信息源文件中的行项目：

* *[!UICONTROL Delete]* （默认）：当到达指定的结束时间时，删除所有相关组件。 无法撤消此操作。

* *[!UICONTROL Pause]：*&#x200B;到达指定的结束时间时暂停所有相关组件。 如有必要，您可以稍后重新激活这些组件。

* *[!UICONTROL None]：*&#x200B;不更改相关组件的状态。

**[!UICONTROL Missing line items in a manually uploaded feed]：**&#x200B;当现有项目未包含在手动上传的新信息源文件中时，或者当它们未按照模板中的“仅映射”设置映射到现有促销活动或广告组时，如何处理这些现有项目：

* *[!UICONTROL Delete]：*&#x200B;删除现有组件。

* *[!UICONTROL Pause]：*&#x200B;暂停现有组件。 如果新的信息源文件包含任何相同的行项目，则它们将被重新激活，并且会保留其历史记录和质量分数。 **注意：**&#x200B;如果父产品组的所有子产品组缺失，则父产品组将被删除，因为您无法暂停产品组。

* *[!UICONTROL None]* （默认）：不更改现有组件。

**[!UICONTROL Missing line items in an FTP feed/GMC account]：**&#x200B;如何处理现有项目，条件是：1)这些项目不包括a)在上传到FTP目录的新信息源文件中；b)下次搜索、社交和Commerce与其同步时，商户中心帐户中；或2)它们未按照模板中的[!UICONTROL Map Only]设置映射到现有促销活动或广告组。

* *[!UICONTROL Delete]：*&#x200B;删除现有组件。

* *[!UICONTROL Pause]：*&#x200B;暂停现有组件。 如果新数据包含任何相同的行项目，则它们将重新激活，并且它们会保留其历史记录和质量分数。 **注意：**&#x200B;如果父产品组的所有子产品组缺失，则父产品组将被删除，因为您无法暂停产品组。

* *[!UICONTROL None]* （默认）：不更改现有组件。

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']：**&#x200B;在下列情况下，如何处理包含库存级别的行项目：

* （对于指定列中仅包含数字库存值的馈送）库存级别等于或低于指定数量。 默认数量为零(0)。

* （对于指定列中带有文本值的馈送）[!UICONTROL Availability]的值为“[!UICONTROL out of stock]”；该值不区分大小写。 **注意：** **在馈送模板中，使用“[!UICONTROL This column has non-numeric values]”的复选框表示基于文本的Stock级别列。

为两种情况选择操作：

* *[!UICONTROL Delete]*（默认）删除组件。

* *[!UICONTROL Pause]：*&#x200B;暂停组件。 更新数据时，如果数字库存值超过指定的数量，或者[!UICONTROL Availability]为“[!UICONTROL in stock]”或“[!UICONTROL preorder]”，则将重新激活组件。 组件将保留其历史记录和质量分数。

每个行项目的库存水平都来自信息源文件中的列，如每个模板的“[!UICONTROL Stock Level]”字段中所指定。

>[!TIP]
>
>* 对于您预期要重新库存或增加可用性的产品或服务，您应暂停广告组、关键词和广告，而不是删除并重新创建它们。 暂停可让他们保留其质量分数。
>* 如果为广告组启用过时的自动处理，并且新数据包括广告组的库存级别，则仅当指定的库存级别位于类别级别而不是品牌/项目级别时，删除或暂停广告组才有意义。 例如，如果您有一个广告组“可转换”，则该广告组的库存水平应为广告组中表示的所有单个可转换模型的总计。

**[!UICONTROL Propagate feed data through all applicable templates]：** （通过FTP或商户中心帐户上载数据文件的广告商）通过适用的模板自动传播新数据。 默认情况下会选中该选项。 如果禁用选项，则仍可以手动传播任何馈送文件或帐户或任何模板的数据。

>[!NOTE]
>
>* 对于FTP文件，信息源服务每两小时在FTP目录中检查一次更新（PST时区中的小时数偶数）。 此选项处理自上次检查以来上载的所有文件。
>* 对于商户中心帐户，Search、Social和Commerce每天在广告商所在时区的约06:00与帐户同步。 此选项处理自上次同步以来更新的所有数据。
>* 传播的数据可以从[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]选项卡使用，直到数据被发布到广告网络或[!UICONTROL Bulksheets]视图。

**[!UICONTROL Post to the SE]：** （通过FTP或商户中心帐户上传数据文件的广告商）在通过适用的模板传播新数据后，自动为相关广告网络以正确格式创建批量处理工作表文件。 此选项还会从[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]选项卡中删除数据，除非任何子组件都有错误。

此选项默认处于禁用状态。 要启用此选项，请选中该复选框，然后指定是否将批量处理工作表文件发布到广告网络：

* *[!UICONTROL Immediately]* （默认）：在通过模板传播数据之后，将批量工作表文件发布到相关广告网络。 批量工作表文件在[!UICONTROL Bulksheets]视图中保持可用30天。

* *[!UICONTROL Preview in Bulksheet Management area only, post later]：**不将批量处理工作表文件发布到相关广告网络，而是将其列在[!UICONTROL Bulksheets]视图中，以便您以后可以从中发布它们。 批量工作表文件在[!UICONTROL Bulksheets]视图中保持可用30天。 当批量处理工作表文件大于10 MB但小于2 GB时，该文件为ZIP格式；您无需解压缩文件即可发布该文件。 &#x200B;** 提示：**&#x200B;如果您之前未验证登陆页面，请使用此选项，以便您可以先从[!UICONTROL Bulksheets]视图验证这些登陆页面，然后再将数据发布到广告网络。

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]：**&#x200B;排除将超过指定字数的关键字短语发布到广告网络。 选择此选项时，会传播超过最大字数的关键字短语并将其列在[!UICONTROL Keywords]选项卡中，但当您尝试发布数据时，不会发布这些短语。

此选项默认处于禁用状态，因此无论短语包含多少个单词，都会发布所有关键词。 如果选择此选项，则选择要张贴的最大字数（从3-10）。

>[!MORELIKETHIS]
>
>* [关于清单信息源](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [通过模板传播馈送数据](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [从馈送生成的促销活动数据发布到广告网络](propagated-data-post.md)
