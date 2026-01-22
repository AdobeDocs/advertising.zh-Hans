---
title: 将标准创意添加到创意库
description: 了解如何将标准（非动态）创意添加到创意库。
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
source-git-commit: a1ca7815334b35de8f9ab5781e53e6b6aa5f4770
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 0%

---

# 将标准创意添加到创意库

将标准创意添加到您的[创意库](creative-library-manage.md)中以用于标准[广告体验](/help/creative/experiences/experience-about.md)。

>[!NOTE]
>
> 您可以直接在广告体验中包含没有定义用户目标的单个创意人员。 您还可以将创意分组到[包](bundle-manage.md)中，这可以包含在定向广告体验中。

## 将灵活的HTML广告添加到创意库 {#flexible-creative-add}

您可以执行以下任一操作：

* 将您自己的灵活创意上传到ZIP文件中。

* 使用任何上传到您帐户的预定义灵活创意模板作为您自己的灵活创意的起点。

### 上传您自己的灵活创意 {#flexible-creative-upload}

您可以上传多个灵活的创意单位。 灵活的创意必须采用ZIP格式，并且最大可以为2 MB。 有关文件要求，请参阅[HTML5创作规范](html5-creative-specification.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击库名称。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Flexible]**。

1. 单击&#x200B;**[!UICONTROL Upload New]**。

1. 通过以下任一方式指定ZIP文件：

   * 将设备或网络上的文件拖放到框中。

   * 单击&#x200B;**[!UICONTROL Select a file]**&#x200B;在您的设备或网络上查找文件。

   查看[灵活的广告规范](#flexible-ad-spec)。

1. 添加或删除灵活的创意文件：

   * 要添加文件，请单击左上角的![添加](/help/creative/assets/create.png "添加")，然后在您的设备或网络上找到该文件。

   * 要删除文件，请取消选中该文件旁边的复选框。

1. （可选）要预览创意，请单击图像上方的![预览](/help/creative/assets/preview.png "预览")。

1. 指定[灵活的HTML5广告设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5)。

   默认情况下，将选择您刚刚上传的所有创意内容。 任何只有一个值的设置均适用于所有选定的创意；对于某些设置，您可以指定单个值。 要输入特定创意的设置，请取消选中每个不适用的创意旁边的复选框。

1. 单击&#x200B;**[!UICONTROL Create]**

### 使用模板添加灵活的创意 {#flexible-creative-use-template}

您可以使用上传到帐户的任何灵活的创意模板来构建预定义大小的广告。 选择要使用的模板后，您将编辑点击标记和属性。&lt;！ — 如果将模板下载功能添加回来，请将此替换最后一句：您可以a\)选择要使用的模板，然后编辑点击标记和属性；或b\) [以ZIP文件格式下载模板](#download-flexible-creative-template)，脱机编辑内容以构建您自己的创意，然后[将编辑后的文件上传为新的创意](flexible-creative-upload)。>

<!-- Not currently an option:
You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads.

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."
-->

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击库名称。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Flexible]**。

1. 单击&#x200B;**[!UICONTROL Browse System Flexible Templates]**。

1. （可选）要预览模板，请单击模板名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Preview]**。

   您可以选择下载模板：单击模板名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Download]**。

1. 单击模板名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Use Selected]**。

1. 编辑[灵活的HTML5创作设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5)以指定语言并包含您自己的点击标记、图像和其他属性。

   创意文件压缩后的最大文件大小为2 MB。<!-- Still true? -->

1. 添加或删除您自己的灵活创意文件：

   * 若要从设备或网络添加文件，请单击左上角的![添加](/help/creative/assets/create.png "添加")，然后找到该文件。 选中创意旁边的复选框，取消选中其他创意旁边的复选框，然后编辑[灵活的HTML5创意设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5)以指定语言并包含您自己的点击标记、图像和其他属性。

   * 要删除文件，请取消选中该文件旁边的复选框。

1. （可选）要预览创意，请单击图像上方的![预览](/help/creative/assets/preview.png "预览")。

1. 单击&#x200B;**[!UICONTROL Create]**。

## 将标准显示创意添加到创意库

标准显示创意包括图像和HTML5创意内容，其中包括从Adobe Experience Manager和Adobe GenStudio for Performance Marketing导入的创意内容。

* 图像创意内容可以是GIF、JPEG、JPG或PNG格式。 最大文件大小为两(2) MB。 查看[支持的创意大小](/help/creative/creative-libraries/creative-sizes.md)。

* 您可以一次添加多个Experience Manager资源、多个GenStudio体验或单个类型（简单或静态）的多个本地HTML5创意。 有关HTML5的创意，请参阅[HTML5广告规范](/help/creative/creative-libraries/html5-creative-specification.md)。

<!-- Add in when we add this feature back:
You can optionally download a sample HTML5 creative as a ZIP file, edit the contents to build your own creative, and then add the edited file as a new creative.
-->

>[!NOTE]
>
>您还可以[添加灵活的HTML5创意](#flexible-creative-add)，这些创意是HTML5创意，具有作为标准HTML标记的所有属性，您可以直接在[!DNL Creative]中编辑这些标记。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击库名称。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Standard Display]**。

1. 指定创意：

   * 对于本地图像或HTML5资源，请执行下列任一操作：

      * 将设备或网络上的文件拖放到框中。

      * 单击&#x200B;**[!UICONTROL Select a file]**&#x200B;在您的设备或网络上查找文件。

   * 对于连接到您的DSP帐户[的](/help/creative/creative-libraries/aem-assets-configure.md)Experience Manager库中已批准的图像，请执行以下操作：

      1. 单击&#x200B;**[!UICONTROL AEM Asset Library]**。

      1. (如果您尚未登录到您的Experience Manager帐户)请登录到您的Experience Manager帐户。

      1. 在[!UICONTROL Assets]或[!UICONTROL Collections]视图中查找并选择文件，然后单击右上角的&#x200B;**[!UICONTROL Select]**。

         <!-- If the existing asset has multiple quality options, [!DNL Creative] downloads the primary asset, or the asset with the highest resolution within some upper limit [verify what it is and how this works]. [If an asset is part of an image set, ... primary asset in the image set. -->

   * 对于GenStudio体验，请执行以下操作：

      1. 单击&#x200B;**[!UICONTROL GenStudio Library]**。

      1. (如果您尚未登录到您的GenStudio帐户)请登录到您的GenStudio帐户。

         默认情况下，会显示您的显示广告体验。 （可选）根据需要按营销活动或其他属性过滤体验。

      1. 找到并选择显示广告体验，然后单击右上角的&#x200B;**[!UICONTROL Select]**。

     选定体验中的每个创意变体都将作为单独的HTML5创意内容导入。

1. 添加或删除创意：

   * 要添加图像，请单击左上角的![添加](/help/creative/assets/create.png "添加")，然后在您的设备或网络上找到该文件。

   * 要删除图像，请取消选中图像旁边的复选框。

1. 指定[HTML5创意设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5)或[图像创意设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image)。

   默认情况下，将选中您刚刚上传的所有创意内容或GenStudio体验，而您指定的任何设置将应用于所有选定项目。 任何只有一个值的设置都适用于所有选定项目。 要输入特定创意或GenStudio体验的设置，请取消选择每个不适用的创意或体验。

1. 单击&#x200B;**[!UICONTROL Create]**。

## 向创意库添加第三方创意内容 {#creative-add-third-party}

[!DNL Creative]支持大多数第三方广告服务器上托管的创意内容的JavaScript跟踪标记。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击库名称。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL 3rd Party]**。

1. 在[第三方创意设置](#creative-settings-third-party)中指定创意的JavaScript标记和其他设置。

   您可以将[可用宏](/help/creative/creative-macros.md)中的任意宏复制并粘贴到JavaScript标记中。

1. 单击&#x200B;**[!UICONTROL Create]**

## 将视频创意添加到创意库

查看[视频创作规范](/help/creative/creative-libraries/creative-libraries-about.md#creative-video-specs)和[支持的创作大小](/help/creative/creative-libraries/creative-sizes.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击库名称。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Video]**。

1. 通过以下任一方式指定视频文件：

   * 将设备或网络上的文件拖放到框中。

   * 单击&#x200B;**[!UICONTROL Select a file]**&#x200B;在您的设备或网络上查找文件。

1. 指定[视频创作设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-video)。

   默认情况下，您刚刚上传的创意处于选中状态，您指定的任何设置都适用于所选的创意内容。<!-- By default, all creatives you just uploaded are selected, and any settings you specify apply to all selected creatives. Any settings with only one value apply to all selected creatives. To enter settings for specific creatives, deselect each inapplicable creative. -->

1. 单击&#x200B;**[!UICONTROL Create]**

>[!MORELIKETHIS]
>
>* [编辑标准创意](/help/creative/creative-libraries/creative-edit-standard.md)
>* [标准创意设置](/help/creative/creative-libraries/creative-settings-standard.md)
>* [可用于跟踪URL的宏](/help/creative/creative-macros.md)
>* [支持的创意大小](/help/creative/creative-libraries/creative-sizes.md)
>* [预览创意](/help/creative/creative-libraries/creative-preview.md)
>* [从包中附加和分离创意](/help/creative/creative-libraries/creative-attach-detach-bundles.md)
>* [关于您的创意库](/help/creative/creative-libraries/creative-libraries-about.md)
>* [管理创意库](/help/creative/creative-libraries/creative-library-manage.md)
