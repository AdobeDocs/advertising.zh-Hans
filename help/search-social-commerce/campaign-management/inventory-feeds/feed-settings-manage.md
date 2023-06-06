---
title: 配置馈送数据设置
description: 了解如何配置用于控制如何处理馈送数据的设置。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 0%

---

# 配置馈送数据设置

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan Ads] （仅删除操作），以及 [!DNL Yandex] 仅限帐户*

您可以配置如何处理馈送数据文件中的广告组、关键字和广告，以及如何通过馈送设置专门处理FTP文件中的数据。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. 在数据表上方的工具栏中，单击 **[!UICONTROL Settings]**.

1. 指定 [馈送数据设置](#feed-data-settings)：

   1. 在 [!UICONTROL Obsolete Item Auto-Processing] 部分，选择字段中的信息。

   1. （广告商通过FTP或通过直接链接指向商户中心帐户上传数据）在 [!UICONTROL FTP/GMC Account Auto-Processing] 部分，选择字段中的信息。

   1. 在 [!UICONTROL Miscellaneous Auto-Processing] 部分，选择字段中的信息。

1. 单击 **[!UICONTROL Save]**.

## 馈送数据设置 {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]：** 应用所有 [!UICONTROL Obsolete Item Auto-processing] 设置到：

* *[!UICONTROL Ad Groups Only]：* 仅限过时的广告组。

* *[!UICONTROL Keywords Only]：* 仅过时关键词和产品组。

* *[!UICONTROL Ad Variations Only]* （默认）：仅限过时的广告。

* *[!UICONTROL Keywords and Ad Variations]：* 过时的关键字/产品目标/产品组和过时的广告。

>[!NOTE]
>
>* 对象 [!DNL Google Ads] 购物广告时，只有最低级别的产品组会受到影响。
>* 对象 [!DNL Yandex] 无论此设置如何，始终对广告变体执行过时的物料自动处理任务。


**[!UICONTROL When the Scheduled End Date is reached]：** （仅限手动发布的数据）当到达结束时间后，如何处理在指定结束日期和时间发布的信息源文件中的行项目：

* *[!UICONTROL Delete]* （默认）：到达指定的结束时间时，删除所有相关组件。 无法撤消此操作。

* *[!UICONTROL Pause]：* 到达指定的结束时间时，暂停所有相关组件。 如有必要，您可以稍后重新激活这些组件。

* *[!UICONTROL None]：* 请勿更改相关组件的状态。

**[!UICONTROL Missing line items in a manually uploaded feed]：** 如果现有项目未包含在手动上传的新信息源文件中，或者未按照模板中的仅映射设置映射到现有促销活动或广告组，如何处理现有项目：

* *[!UICONTROL Delete]：* 删除现有组件。

* *[!UICONTROL Pause]：* 暂停现有组件。 如果新的信息源文件包含任何相同的行项目，则它们将重新激活，并且它们会保留其历史记录和质量分数。 **注意：** 如果父产品组的所有子产品组缺失，则会删除父产品组，因为您无法暂停产品组。

* *[!UICONTROL None]* （默认）：不更改现有组件。

**[!UICONTROL Missing line items in an FTP feed/GMC account]：** 如何处理现有项目，条件是：1)这些项目未包括a)上传到FTP目录的新馈送文件中未包括a)，或者b)下次搜索、社交和商务与其同步时商户中心帐户未包括，或者2)这些项目未按照以下规则映射到现有促销活动或广告组： [!UICONTROL Map Only] 模板中的设置。

* *[!UICONTROL Delete]：* 删除现有组件。

* *[!UICONTROL Pause]：* 暂停现有组件。 如果新数据包含任何相同的行项目，则它们将重新激活，并且它们会保留其历史记录和质量分数。 **注意：** 如果父产品组的所有子产品组缺失，则会删除父产品组，因为您无法暂停产品组。

* *[!UICONTROL None]* （默认）：不更改现有组件。

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']：** 在以下情况下，如何处理包含库存水平的行项目：

* （对于指定列中仅包含数字库存值的馈送）库存级别等于或低于指定数量。 默认数量为零(0)。

* （对于指定列中带有文本值的馈送）的值 [!UICONTROL Availability] 为“[!UICONTROL out of stock]“”；值不区分大小写。 **注意：** **在馈送模板中，使用&quot;[!UICONTROL This column has non-numeric values].”

为两种情况选择操作：

* *[!UICONTROL Delete]* （默认）删除组件。

* *[!UICONTROL Pause]：* 暂停组件。 更新数据后，如果数字库存值高于指定数量或 [!UICONTROL Availability] 为“[!UICONTROL in stock]“或”[!UICONTROL preorder]“。 组件将保留其历史记录和质量分数。

每个行项目的库存水平都来自馈送文件中的列，如&quot;[!UICONTROL Stock Level]每个模板的“ ”字段。

>[!TIP]
>
>* 对于您预期要重新补充库存或增加可用性的产品或服务，您应暂停广告组、关键词和广告，而不是删除它们并重新创建它们。 暂停可让客户保留其质量分数。
>* 如果您为广告组启用了过时的自动处理，并且新数据包含广告组的库存级别，则仅当指定的库存级别位于类别级别而不是品牌/项目级别时，删除或暂停广告组才有意义。 例如，如果您有一个广告组“可转换债券”，则该广告组的库存水平应该是该广告组中表示的所有单个可转换模型的总计。


**[!UICONTROL Propagate feed data through all applicable templates]：** （广告商通过FTP或商户中心帐户上传数据文件）通过适用的模板自动传播新数据。 默认情况下会选中该选项。 如果禁用该选项，则仍可以手动传播任何信息源文件或帐户或任何模板的数据。

>[!NOTE]
>
>* 对于FTP文件，信息源服务每两小时检查FTP目录中的更新（在PST时区中为偶数小时）。 此选项处理自上次检查以来上载的所有文件。
>* 对于商户中心帐户，Search、Social和Commerce每天在广告商所在时区的大约06:00与帐户同步。 此选项处理自上次同步以来更新的所有数据。
>* 传播的数据可从 [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 选项卡，直到数据被发布到广告网络或 [!UICONTROL Bulksheets] 视图。


**[!UICONTROL Post to the SE]：** （通过FTP或商户中心帐户上传数据文件的广告商）在通过适用的模板传播新数据后，自动为相关广告网络以正确格式创建批量处理工作表文件。 此选项还会从以下位置删除数据： [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 选项卡，除非任何子组件出错。

此选项默认处于禁用状态。 要启用此选项，请选中该复选框，然后指定是否将批量处理工作表文件发布到广告网络：

* *[!UICONTROL Immediately]* （默认）：在通过模板传播数据后，将批量工作表文件发布到相关广告网络。 批量工作表文件在 [!UICONTROL Bulksheets] 查看30天。

* *[!UICONTROL Preview in Bulksheet Management area only, post later]：**不要将批量处理工作表文件发布到相关广告网络，而是将其列在 [!UICONTROL Bulksheets] 视图，稍后可从中发布它们。 批量工作表文件在 [!UICONTROL Bulksheets] 查看30天。 当批量工作表文件大于10 MB但小于2 GB时，该文件为ZIP格式；您无需解压缩文件即可发布该文件。 **提示：** 如果您之前未验证登陆页面，请使用此选项，以便您可以从 [!UICONTROL Bulksheets] 在将数据发布到广告网络之前查看。

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]：** 禁止向广告网络发布超过指定字数的关键字短语。 如果选择该选项，则会传播字数超过最大字数的关键字短语，并将其列在 [!UICONTROL Keywords] 选项卡，但当您尝试发布数据时，不会发布这些数据。

此选项默认处于禁用状态，因此无论短语包含多少个单词，都会发布所有关键词。 如果选择此选项，请选择要发布的最大字数（从3-10）。

>[!MORELIKETHIS]
>
>* [关于库存信息源](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [通过模板传播馈送数据](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [从馈送生成的促销活动数据发布到广告网络](propagated-data-post.md)

