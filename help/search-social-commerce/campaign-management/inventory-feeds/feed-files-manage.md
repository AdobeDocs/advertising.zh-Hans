---
title: 管理清单数据馈送文件
description: 了解如何配置用于控制如何处理馈送数据的设置。
exl-id: 7d19ecc0-c939-4996-b22b-970ce8644b09
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 0%

---

# 管理清单数据馈送文件

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （仅删除操作）和仅[!DNL Yandex]帐户*

如果您提交自己的信息源数据，则必须上传包含产品数据的文件，以根据产品数据动态创建促销活动结构、广告和关键词。 然后，您可以将它们与广告网络特定的广告模板相关联，并通过模板处理数据，最终将数据发布到相关广告网络。 您可以将多个模板与一个信息源文件关联，但每个模板只能与一个信息源文件关联。

>[!NOTE]
>
>如果您直接使用商户中心帐户的数据，请勿上传文件。

您可以通过以下任一方式上传和处理数据馈送文件：

* **自动使用FTP：**&#x200B;您可以直接将文件上传到FTP目录；馈送服务每两小时检查一次新文件。 首次上传文件后，您可以将其与特定于广告网络的模板关联。 之后，您上传的所有同名文件都会自动与同一模板关联。 根据您[配置信息源数据设置](feed-settings-manage.md)的方式，Search、Social和Commerce可能会通过所有适用的模板自动传播信息源数据，并可以选择将生成的营销活动和广告数据发布到相关广告网络。

  要设置用于存放和自动处理数据文件的FTP目录，请联系您的Adobe客户团队。

* **手动处理：**&#x200B;您可以从[!UICONTROL Advanced] (ACM)视图中手动[上载源文件](#feed-file-upload)。 在将信息源文件与一个或多个特定于广告网络的[模板](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)关联后，您可以通过[根据[信息源数据设置](feed-settings-manage.md)通过模板](feed-data-propagate.md)传播信息源数据来生成营销活动和广告数据。 您可以选择在促销活动层次结构视图中预览生成的数据，生成批量处理工作表文件以供审阅，或生成批量处理工作表文件以立即发布到广告网络。 如果不立即发布数据，则可以[预览数据](propagated-data-view.md)并在稍后[发布数据](propagated-data-post.md)。 您可以稍后[用新文件](#feed-file-replace)替换现有信息源文件，而不会丢失任何现有的模板关联。

## 信息源文件要求

单个文件中不需要特定数据字段，但每个文件都需要以下内容：

* 文件中的第一行必须包含与关联模板中的动态参数对应的列名称（也称为&#x200B;*标头*）。 其余行必须包含与列名对应的数据。 每个数据行（行）必须只与一个帐户组件相关，例如一个营销活动或一个广告。 所有行上的值必须以制表符或逗号分隔。 请参阅下面的[CSV示例文件](#example-csv-feed-file)和[TSV示例文件](#example-tsv-feed-file)。

* 文件大小不限，但必须具有以下文件扩展名之一： `.tsv` （用于制表符分隔的值）、`.txt` （用于符合[!DNL Unicode]的ASCII文本）、`.csv` （用于逗号分隔的值）或`.zip` （用于压缩ZIP格式的单个文件，该文件将解压缩为TSV文件）。

* 文件名区分大小写，不能包含以下字符： `# % & * | \ : " < > . ? /`

* 如果将文件存储在FTP目录中，则必须对文件的每个版本使用相同的文件名。

* （仅限[!DNL Google Ads]个模板）如果您的模板在文本广告中使用Param2或Param2广告参数，则馈送文件中的相应数据字段必须包含数字数据，且不含货币符号。

* 要更新现有帐户组件，请包含现有营销活动的名称（及其组件，如果相关）。 如果未指定现有结构，则会创建新组件。

### 逗号分隔的馈送文件示例 {#example-csv-feed-file}

```
Product Category,Product Name,Discount Percentage
electronics,iPods,10
apparel,Shirts,15
shoes,Clarks,20
```

### 制表符分隔的信息源文件示例 {#example-tsv-feed-file}

```
Product Category<TAB>Product Name<TAB>Discount Percentage
electronics<TAB>iPods<TAB>10
apparel<TAB>Shirts<TAB>15
shoes<TAB>Clarks<TAB>20
```

## 最佳实践

* 对于包含国际字符的数据，请使用TSV或TXT格式的文件。

* 要通过有限的手动审查或编辑实现可重复的过程，请按照以下方式设置信息源文件及其帐户结构数据：

   * 包含足以创建帐户结构或映射到现有帐户结构的数据的列和行。 理想情况下，使用与产品分类密切相关并且信息源数据可以轻松映射到其中的现有帐户结构。

   * 包括短到可在广告副本中使用的描述。

   * 跨产品行使用一致的数据模式和命名约定。

   * 删除所有前导空格和尾随空格。

   * 删除所有乱码字符。

## 查看或下载信息源文件

您可以打开或下载手动或使用FTP上传的任何信息源文件。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，这将打开到[!UICONTROL Templates]选项卡。

1. 找到信息源文件：

1. 在模板列表中，找到使用信息源文件的模板。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Feeds]**&#x200B;以打开所有馈送文件的列表。

1. 单击馈送文件名。

1. 按照浏览器的正常过程打开或保存文件。

有关详细信息，请参阅浏览器的联机帮助。

## 手动上传信息源文件 {#feed-file-upload}

>[!NOTE]
> 如果将模板与手动上传的文件关联，然后通过FTP上传另一个具有相同名称、文件扩展名和语法大小写的文件，则在通过模板传播数据时将使用FTP文件。 例如，myfile.csv将取代myfile.csv，但Myfile.CSV则不取代。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，这将打开到[!UICONTROL Templates]选项卡。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Feeds]**。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Upload]**。

1. 通过输入完整路径和文件名或单击&#x200B;**[!UICONTROL Browse]**&#x200B;在设备或网络上查找文件来指定要上传的文件。

1. 单击**[!UICONTROL Upload]。

将验证文件中的所有字段。 在更正值之前，您不能稍后发布字段长度无效的项目。 文件中的所有列名在模板中作为动态参数变为可用。

## 替换信息源文件 {#feed-file-replace}

替换馈送文件时，即使新文件具有不同的文件名或扩展名，所有现有的模板关联仍会保留。 当您通过最初与上一个文件相关联的所有模板传播数据时，将使用新文件。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，这将打开到[!UICONTROL Templates]选项卡。

1. 执行以下任一操作：

   * 在任何适用模板的[!UICONTROL Feed]列中，单击![更多选项](/help/search-social-commerce/assets/options.png "更多选项")并选择&#x200B;**[!UICONTROL Re-upload]**。

   * 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Feeds]**。 在馈送文件列表中，选中现有文件名旁边的复选框。 在数据表上方，单击&#x200B;**[!UICONTROL Upload]**。

   >[!NOTE]
   >
   >信息源文件的源（“[!UICONTROL FTP]”或手动上传文件的“&amp;mdash”）包含在[!UICONTROL Source]列中。

1. 通过输入完整路径和文件名或单击&#x200B;**[!UICONTROL Browse]**&#x200B;在设备或网络上查找文件来指定要上传的文件。

即使新文件具有不同的文件名或扩展名，现有文件也会被新文件覆盖。

1. 单击&#x200B;**[!UICONTROL Re-Upload]**。

将验证文件中的所有字段。 在更正值之前，您不能稍后发布字段长度无效的项目。 文件中的所有列名在模板中作为动态参数变为可用。

## 删除馈送文件

您可以删除手动或通过FTP上传的任何信息源文件。 当您删除信息源文件时，它将不再与任何模板关联。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**，这将打开到[!UICONTROL Templates]选项卡。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Feeds]**。

1. 选中要删除的每个文件旁边的复选框。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Yes]**。

>[!MORELIKETHIS]
>
>* [关于清单信息源](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [通过模板传播馈送数据](feed-data-propagate.md)
>* [查看从馈送生成的数据](propagated-data-view.md)
>* [编辑从馈送生成的数据](propagated-data-edit.md)
>* [从馈送生成的促销活动数据发布到广告网络](propagated-data-post.md)
>* [停止库存馈送数据的发布作业](stop-job.md)
>* [从馈送生成的数据的状态](propagated-data-status.md)
