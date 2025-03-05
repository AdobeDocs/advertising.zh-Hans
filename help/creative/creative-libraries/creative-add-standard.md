---
title: 将标准创意添加到创意库
description: 了解如何将标准（非动态）创意添加到创意库。
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# 将标准创意添加到创意库

*已关闭的测试版*

将创意内容添加到您的[创意库](creative-library-manage.md)中以用于[广告体验](/help/creative/experiences/experience-about.md)。

>[!NOTE]
>
> 您可以直接在广告体验中包含没有定义用户目标的单个创意人员。 您还可以将创意分组到[包](bundle-manage.md)中，这可以包含在定向广告体验中。

## 将灵活的HTML广告添加到创意库 {#flexible-creative-add}

<!-- Later:
You can do either of the following: 

* Upload your own flexible creatives in ZIP files.

* Use any of the predefined flexible creative templates as a starting point for your own flexible creative.

### Upload your own flexible creatives {#flexible-creative-upload}

-->

您可以上传多个灵活的创意单位。 灵活的创意必须采用ZIP格式，并且最大可以为2 MB。 有关文件要求，请参阅[HTML5创作规范](html5-creative-specification.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击库名称。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Standard Ads]**&#x200B;子选项卡。

1. 单击&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Flexible]**。

1. 单击&#x200B;**[!UICONTROL Upload New]**。

1. 通过以下任一方式指定ZIP文件：

   * 将设备或网络上的文件拖放到框中。

   * 单击&#x200B;**[!UICONTROL select a file]**&#x200B;在您的设备或网络上查找文件。

   查看[灵活的广告规范](#flexible-ad-spec)。

1. 添加或删除灵活的创意文件：

   * 要添加文件，请单击左上角的![添加](/help/creative/assets/create.png "添加")，然后在您的设备或网络上找到该文件。

   * 要删除文件，请取消选中该文件旁边的复选框。

1. 指定[灵活的HTML5广告设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5)。

   默认情况下，将选择您刚刚上传的所有创意内容。 任何只有一个值的设置均适用于所有选定的创意；对于某些设置，您可以指定单个值。 要输入特定创意的设置，请取消选中每个不适用的创意旁边的复选框。

1. 单击&#x200B;**[!UICONTROL Create]**

<!-- In a later phase:

### Add flexible creatives using a template {#flexible-creative-use-template}

You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads. Once you select a template to use, you'll edit the click tags and attributes.<!-- Replace last sentence with this if we add the template download feature back:  You can either a\) select a template to use, and then edit the click tags and attributes; or b\) [download a template as a ZIP file](#download-flexible-creative-template), edit the contents offline to build your own creative, and then [upload the edited file as a new creative](flexible-creative-upload).>

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click the **[!UICONTROL Standard Ads]** subtab.

1. Click **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Flexible]**.

1. Click **[!UICONTROL Browse System Flexible Templates]**.



[The following are old instructions; see how this works in the new UI]


1. In the left panel, select the creative size to see all available templates for that size.

1. Under the template name, click **[!UICONTROL Use This Creative]**.

1. Edit the [flexible HTML5 creative settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) to include your own click tags, images, and other attributes.

   The maximum file size of the creative, once it's zipped, is 2 MB.[Will saving the creative zip it??]

1. (Optional) Once you've made your changes, click []()[add image] to preview the new creative. 

1. Click **[!UICONTROL Save]**.

-->

## 将HTML5创意添加到创意库

您可以一次添加多个属于单一类型（简单或静态）的HTML5创意。

<!-- Add in when we add this feature back:
You can optionally download a sample HTML5 creative as a ZIP file, edit the contents to build your own creative, and then add the edited file as a new creative.
-->

>[!NOTE]
>
>您还可以[添加灵活的HTML5创意](#flexible-creative-add)，这些创意是HTML5创意，具有作为标准HTML标记的所有属性，您可以直接在[!DNL Creative]中编辑这些标记。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击库名称。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Standard Ads]**&#x200B;子选项卡。

1. 单击&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL HTML5]**。

<!-- Not an option as of 3/4:

1. (Optional) To download a sample HTML5 creative as a ZIP file, click **Sample HTML5 Creatives**.

   The ZIP file is downloaded according to your browser's normal procedure, usually to the folder that is specified for downloads. 
   
   To create your own HTML5 creative using the sample, unzip the file and edit the contents to include your own ad images and attributes. Then, rename the folder and zip it, and continue below.

-->

1. 通过以下任一方式指定文件：

   * 将设备或网络上的文件拖放到框中。

   * 单击&#x200B;**[!UICONTROL select a file]**&#x200B;在您的设备或网络上查找该文件。

   请参阅[HTML5广告规范](/help/creative/creative-libraries/html5-creative-specification.md)。

1. 指定[HTML5广告设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5)。

默认情况下，将选择您刚刚上传的所有创意内容。 任何只有一个值的设置均适用于所有选定的创意；对于某些设置，您可以指定单个值。 要输入特定创意的设置，请取消选中每个不适用的创意旁边的复选框。

1. 单击&#x200B;**[!UICONTROL Create]**

## 将创意图像添加到创意库

图像创意内容可以是GIF、JPEG、JPG或PNG格式。 最大文件大小为两(2) MB。 查看[支持的创意大小](/help/creative/creative-libraries/creative-sizes.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击库名称。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Standard Ads]**&#x200B;子选项卡。

1. 单击&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Image]**。

1. 通过以下任一方式指定文件：

   * 将设备或网络上的文件拖放到框中。

   * 单击&#x200B;**[!UICONTROL select a file]**&#x200B;在您的设备或网络上查找该文件。

1. 添加或删除图像：

   * 要添加图像，请单击左上角的![添加](/help/creative/assets/create.png "添加")，然后在您的设备或网络上找到该文件。

   * 要删除图像，请取消选中图像旁边的复选框。

1. 指定[图像创作设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image)。

   默认情况下，将选择您刚刚上传的所有创意，并且您指定的任何设置将应用于所有选定的创意。 任何只有一个值的设置均适用于所有选定的创意。 要输入特定创意的设置，请取消选择每个不适用的创意内容。

1. 单击&#x200B;**[!UICONTROL Create]**

## 向创意库添加第三方创意内容 {#creative-add-third-party}

[!DNL Creative]支持大多数第三方广告服务器上托管的创意内容的JavaScript跟踪标记。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击库名称。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Standard Ads]**&#x200B;子选项卡。

1. 单击&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL 3rd Party]**。

1. 在[第三方创意设置](#creative-settings-third-party)中指定创意的JavaScript标记和其他设置。

   您可以将[可用宏](/help/creative/creative-macros.md)中的任意宏复制并粘贴到JavaScript标记中。

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
