---
title: 管理动态广告模板
description: 了解xxxx。
feature: Creative Templates
source-git-commit: ed0fe4849c1db933f1c68a49fc848acd7c74af5b
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# 管理动态广告模板

通过上传具有所需广告格式的压缩HTML5文件，为广告类型(静态HTML5或动态HTML5)和广告大小的每个组合创建单独的广告模板。 对于动态HTML5广告，您还可以上传包含广告属性<!-- more clarification? -->的文件。

<!-- add this where/how?: You can use the same feed template for multiple ad templates. -->

<!-- EXPLAIN MORE:  Is this like repropagating a feed file through a template, or can you just change some things? Is generating an ad template a one-time thing, using the existing feed file, but you might later update the file and re-propagation doesn't happen automatically? Clarify the use cases for each.-->

## 创建动态广告模板

>[!NOTE]
>
>当您[将动态创意添加到创意库](/help/creative/creative-libraries/creative-add-dynamic.md)时，您还可以上传动态广告模板。 您在此处创建的任何广告模板均可在[!UICONTROL Ad Templates]视图中供将来使用。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**。

1. 单击右上角的&#x200B;**[!UICONTROL Create Ad Template]**

1. 指定[广告模板设置](#ad-template-settings)

1. 单击&#x200B;**[!UICONTROL Create]**。

## 编辑动态广告模板

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**。

1. 将光标悬停在广告模板行上并单击&#x200B;**[!UICONTROL Edit]**。

1. 编辑[广告模板设置](#ad-template-settings)。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 下载动态广告模板

<!-- Explain more about what this contains and the format:  Downloaded ad templates are compressed (zipped) files that include XXX as TDF files and the uploaded HTML5 (and attributes?) data. You can open the TDF file in a text editor. -->

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**。

1. 将光标悬停在广告模板行上并单击&#x200B;**[!UICONTROL Download]**。

   将按照浏览器的正常过程下载文件。

## 删除动态广告模板

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**。

1. 将光标悬停在广告模板行上并单击&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Delete]**.<!-- Confirm -->

## 从广告模板创建动态广告

>[!NOTE]
>
>您还可以在创意库中[将动态创意添加到创意库](/help/creative/creative-libraries/creative-add-dynamic.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**。

1. 将光标悬停在广告模板行上并单击&#x200B;**[!UICONTROL Create Dynamic Ad]**。

   在[!UICONTROL New Dynamic Ad]屏幕中，[!UICONTROL Ad Template Size]、[!UICONTROL Ad Template Type]和[!UICONTROL Ad Template]字段是自动选择的只读字段。

1. 指定动态广告设置以[创建动态广告](/help/creative/creative-libraries/creative-add-dynamic.md)。

## 广告模板设置 {#ad-template-settings}

### 广告模板详细信息

**[!UICONTROL Advertiser]**： （现有模板为只读）将为其生成广告的广告商。

**[!UICONTROL Ad Template Name]**：广告商的唯一广告模板名称。

**[!UICONTROL Ad Template Type]**： （现有模板为只读）广告模板格式： *静态HTML5*&#x200B;或&#x200B;*动态HTML5*。

**[!UICONTROL Ad Template Size]**： （现有模板为只读）模板创建的广告的维度。

**[!UICONTROL Description]**： （可选）对使用广告模板的任何人都有用的信息。

<!-- I don't see this on 9/24:

### (Static HTML5 ad templates) Click Tags

**\[Click Tag Parameter\]**: The click tag parameters to allow click-tracking redirects from ads created using the ad template. To add a parameter, click **[!UICONTROL + Add More]** and enter an additional parameter. You can include up to five parameters.

-->

### HTML5 zip

具有所需广告格式的压缩HTML5文件。 如果已上载文件，则会列出文件名。

请参阅[HTML5创作规范](/help/creative/creative-libraries/html5-creative-specification.md)。

要上传文件，请执行以下操作：

1. 单击&#x200B;**[!UICONTROL Upload HTML5 zip]**。

1. 在您的设备或网络上找到文件。

### (Dynamic HTML5广告模板)属性文件

<!-- EXPLAIN -->包含广告模板属性的文件。 如果已上载文件，则会列出文件名。

<!-- Add specs for this file type -->

要上传文件，请执行以下操作：

1. 单击&#x200B;**[!UICONTROL Upload Attributes File]**。

1. 在您的设备或网络上找到文件。

>[!MORELIKETHIS]
>
>* [动态广告的工作流](/help/creative/introduction/workflow-dynamic-ads.md)
>* [管理资源文件](/help/creative/feeds/asset-manage.md)
>* [管理馈送模板](/help/creative/feeds/feed-template-manage.md)
>* [管理目录](/help/creative/feeds/catalog-manage.md)
>* [将动态创意添加到创意库](/help/creative/creative-libraries/creative-add-dynamic.md)

