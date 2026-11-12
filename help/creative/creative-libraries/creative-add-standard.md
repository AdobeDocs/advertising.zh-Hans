---
title: 将标准创意添加到创意库
description: 了解如何将标准（非动态）创意添加到创意库。
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
TQID: 'https://experienceleague.adobe.com/mgUcE-E6LAIFFU8S5WrUceCQ6ZMSGF9tFkqEfnuKKSQ'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d06c1576-7039-4934-b256-7366e138fbb6
    internal-label: Creative Standard Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: a2a6d94329df17c332a140de428bb44fb892c97a
workflow-type: tm+mt
source-wordcount: '2018'
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

您可以使用上传到帐户的任何灵活的创意模板来构建预定义大小的广告。 选择要使用的模板后，您将编辑点击标记和属性。

<!--
Replace last sentence with this if we add the template download feature back:  You can either a\) select a template to use, and then edit the click tags and attributes; or b\) [download a template as a ZIP file](#download-flexible-creative-template), edit the contents offline to build your own creative, and then [upload the edited file as a new creative](flexible-creative-upload).
-->

<!--
 Not currently an option:
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

<!--
 Add in when we add this feature back:
You can optionally download a sample HTML5 creative as a ZIP file, edit the contents to build your own creative, and then add the edited file as a new creative.
-->

>[!NOTE]
>
>您还可以[添加灵活的HTML5创意](#flexible-creative-add)，这些创意是HTML5创意，具有作为标准HTML标记的所有属性，您可以直接在[!DNL Creative]中编辑这些标记。

### 通过新的UI

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （可选） [自定义视图](/help/creative/introduction/customize-data-views.md)以包含特定库。

1. 通过以下任一方式打开库：

   * 单击库名称。

   * 在库名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Open]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Upload]** > **[!UICONTROL Display]**。

1. 指定创意：

   * 对于本地图像或HTML5资源，请执行下列任一操作：

     * 将设备或网络上的文件拖放到框中。

     * 单击&#x200B;**[!UICONTROL Select a file]**&#x200B;在您的设备或网络上查找文件。

   * 对于连接到您的DSP帐户](/help/creative/creative-libraries/aem-assets-configure.md)的[Experience Manager库中已批准的图像，请执行以下操作：

     1. 单击&#x200B;**[!UICONTROL AEM Asset Library]**。

     1. （如果您尚未登录到您的Experience Manager帐户）请登录到您的Experience Manager帐户。

     1. 在[!UICONTROL Assets]或[!UICONTROL Collections]视图中查找并选择文件，然后单击右上角的&#x200B;**[!UICONTROL Select]**。

        <!-- If the existing asset has multiple quality options, [!DNL Creative] downloads the primary asset, or the asset with the highest resolution within some upper limit [verify what it is and how this works]. [If an asset is part of an image set, ... primary asset in the image set. -->

   * 对于GenStudio体验，请执行以下操作：

     1. 单击&#x200B;**[!UICONTROL GenStudio Library]**。

     1. （如果您尚未登录到您的GenStudio帐户）请登录到您的GenStudio帐户。

        默认情况下，会显示您的显示广告体验。 （可选）根据需要按营销活动或其他属性过滤体验。

     1. 找到并选择显示广告体验，然后单击右上角的&#x200B;**[!UICONTROL Select]**。

     选定体验中的每个创意变体都会作为单独的HTML5创意内容导入。

1. 添加或删除创意：

   * 要添加图像，请单击左上角的![添加](/help/creative/assets/create.png "添加")，然后在您的设备或网络上找到该文件。

   * 要删除图像，请取消选中图像旁边的复选框。

1. 指定[HTML5创意设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5)或[图像创意设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image)。

   默认情况下，将选中您刚刚上传的所有创意内容或GenStudio体验，而您指定的任何设置将应用于所有选定项目。 任何只有一个值的设置都适用于所有选定项目。 要输入特定创意或GenStudio体验的设置，请取消选择每个不适用的创意或体验。

1. 单击&#x200B;**[!UICONTROL Save Creative]**。

### 从旧版UI

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击&#x200B;**[!UICONTROL Switch to classic UI]**。

1. 单击库名称。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Standard Display]**。

1. 指定创意：

   * 对于本地图像或HTML5资源，请执行下列任一操作：

     * 将设备或网络上的文件拖放到框中。

     * 单击&#x200B;**[!UICONTROL Select a file]**&#x200B;在您的设备或网络上查找文件。

   * 对于连接到您的DSP帐户](/help/creative/creative-libraries/aem-assets-configure.md)的[Experience Manager库中已批准的图像，请执行以下操作：

     1. 单击&#x200B;**[!UICONTROL AEM Asset Library]**。

     1. （如果您尚未登录到您的Experience Manager帐户）请登录到您的Experience Manager帐户。

     1. 在[!UICONTROL Assets]或[!UICONTROL Collections]视图中查找并选择文件，然后单击右上角的&#x200B;**[!UICONTROL Select]**。

        <!-- If the existing asset has multiple quality options, [!DNL Creative] downloads the primary asset, or the asset with the highest resolution within some upper limit [verify what it is and how this works]. [If an asset is part of an image set, ... primary asset in the image set. -->

   * 对于GenStudio体验，请执行以下操作：

     1. 单击&#x200B;**[!UICONTROL GenStudio Library]**。

     1. （如果您尚未登录到您的GenStudio帐户）请登录到您的GenStudio帐户。

        默认情况下，会显示您的显示广告体验。 （可选）根据需要按营销活动或其他属性过滤体验。

     1. 找到并选择显示广告体验，然后单击右上角的&#x200B;**[!UICONTROL Select]**。

     选定体验中的每个创意变体都会作为单独的HTML5创意内容导入。

1. 添加或删除创意：

   * 要添加图像，请单击左上角的![添加](/help/creative/assets/create.png "添加")，然后在您的设备或网络上找到该文件。

   * 要删除图像，请取消选中图像旁边的复选框。

1. 指定[HTML5创意设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5)或[图像创意设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image)。

   默认情况下，将选中您刚刚上传的所有创意内容或GenStudio体验，而您指定的任何设置将应用于所有选定项目。 任何只有一个值的设置都适用于所有选定项目。 要输入特定创意或GenStudio体验的设置，请取消选择每个不适用的创意或体验。

1. 单击&#x200B;**[!UICONTROL Create]**。

## 将第三方创意人员添加到创意库 {#creative-add-third-party}

[!DNL Creative]支持在第三方广告服务器上托管的显示创意的广告标记。 在新UI中，您可以从贩运页面导入一个或多个创意。 旧版UI支持为单个创意内容输入标记。

### 通过新的UI

#### 准备您的贩运单 {#third-party-sheet-requirements}

* 使用创意不超过500个的Excel （`.xlsx`或`.xls`）、CSV或TSV文件（不超过10 MB）。

* 对于Excel文件，将创意内容放在第一个工作表上。 仅导入第一个工作表。 不支持受密码保护的文件。

* 使用[!DNL Flashtalking]或[!DNL Google Campaign Manager 360]导出，或准备常规工作表。 工作表必须与上传时选择的广告服务器布局匹配。

* 包括每个创意内容的创意名称、大小和广告标签。 名称最多可包含255个字符。 在供应商导出的单个大小列（如`300x250`）中或单独的宽度和高度列中指定维度。 使用[支持的创意大小](creative-sizes.md)。

* 对于通用工作表，请使用列标题`Creative Name`、`Size`和`Ad Tag`。 您可以从上传对话框下载CSV模板。 将其示例行替换为您自己的创意数据。

>[!IMPORTANT]
>
>* 批量上传仅支持显示标记。 不支持视频和VAST标记。
>* 批量上传会存储所提供的广告标记；它不会在导入期间插入跟踪宏或重写跟踪URL。 在上载工作表之前，在标记中包含任何必需的[跟踪宏](/help/creative/creative-macros.md)。

#### 上传并查看创意内容 {#third-party-bulk-upload}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 通过以下任一方式打开库：

   * 单击库名称。

   * 在库名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Open]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Add new]** > **[!UICONTROL Upload]** > **[!UICONTROL 3rd Party]**。

   将打开&#x200B;**[!UICONTROL Bulk upload third-party tags]**&#x200B;对话框。

1. 选择与您的工作表匹配的&#x200B;**[!UICONTROL Ad server]**：

   * **[!UICONTROL Flashtalking]**

   * **[!UICONTROL Google CM360]**

   * **[!UICONTROL Generic]**

   在上传文件之前，必须选择广告服务器。 选定的广告服务器应用于工作表中的每个创意；它不会从单个标记中检测到。

1. （可选）要准备常规工作表，请单击&#x200B;**[!UICONTROL Download CSV template]**，使用您自己的创意替换示例数据，然后保存该文件。

1. 通过以下任一方式指定工作表：

   * 将文件拖放到上传框中。

   * 单击&#x200B;**[!UICONTROL select a file]**&#x200B;在您的设备或网络上查找该文件。

   上传并分析工作表。 如果布局与所选广告服务器不匹配，请更正工作表或选择匹配的广告服务器，然后再次上传文件。

1. 在&#x200B;**[!UICONTROL Review third-party creatives]**&#x200B;中，查看每行的&#x200B;**[!UICONTROL Creative name]**、**[!UICONTROL Size]**、**[!UICONTROL Type]**、**[!UICONTROL Language]**&#x200B;和&#x200B;**[!UICONTROL Status]**。

   * 如果工作表包含多种标记格式，请为要导入的标记列选择选项卡。 所选的格式将应用于所有行，并且不会显示在该列中没有标记的行。 更改选项卡会将所选内容重置为该格式的所有可导入行。

   * 默认情况下，将选择所有可导入行。 取消选中任何您不想导入的创意旁边的复选框。

   * （可选）更改单个创意的&#x200B;**[!UICONTROL Language]**。 缺省为英语。

   * 无法选择或导入状态为&#x200B;**[!UICONTROL Error]**&#x200B;的行。 您可以导入有效行，或单击&#x200B;**[!UICONTROL Cancel]**，更正源工作表并重新上传。 更正缺少的名称、维度或标记，并删除视频标记或任何标记为不受支持的字符。

1. 单击&#x200B;**[!UICONTROL 导入 <N> 创意内容&#x200B;]**，其中`<N>`是所选创意内容的数量。 对于单个创意，请单击&#x200B;**[!UICONTROL Import 1 creative]**。

   该对话框将关闭，并且会显示一条通知，确认已开始导入。 处理完成后，创意会显示在库中。

要跟踪导入，请单击顶部菜单栏右侧的![作业管理器](/help/creative/assets/job-manager.png "作业管理器") (**[!UICONTROL Job Manager]**)。 如果处理过程中任何行失败，请单击导入作业的&#x200B;**[!UICONTROL Download failed rows]**，更正下载的工作表，然后再次上传。

### 从旧版UI

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击&#x200B;**[!UICONTROL Switch to classic UI]**。

1. （可选） [自定义视图](/help/creative/introduction/customize-data-views.md)以包含特定库。

1. 单击库名称。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL 3rd Party]**。

1. 在[第三方创意设置](#creative-settings-third-party)中指定创意的JavaScript标记和其他设置。

   您可以将[可用宏](/help/creative/creative-macros.md)中的任意宏复制并粘贴到JavaScript标记中。

1. 单击&#x200B;**[!UICONTROL Create]**。

## 将视频创意上传到创意库

查看[视频创作规范](/help/creative/creative-libraries/creative-libraries-about.md#creative-video-specs)和[支持的创作大小](/help/creative/creative-libraries/creative-sizes.md)。

### 通过新的UI

您可以一次上传一个视频。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. （可选） [自定义视图](/help/creative/introduction/customize-data-views.md)以包含特定库。

1. 通过以下任一方式打开库：

   * 单击库名称。

   * 在库名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Open]**。

1. 在&#x200B;**[!UICONTROL Creatives]**&#x200B;选项卡上，单击&#x200B;**[!UICONTROL Create]** > **[!UICONTROL Upload]** > **[!UICONTROL Video]**。

1. 通过以下任一方式指定视频文件：

   * 将文件拖放到设备或网络上的框中。

   * 单击&#x200B;**[!UICONTROL Select a file]**&#x200B;在您的设备或网络上查找文件。

1. 指定[视频创作设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-video)。

1. 单击&#x200B;**[!UICONTROL Save Creative]**。

### 从旧版UI

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**。

1. 单击&#x200B;**[!UICONTROL Switch to classic UI]**。

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
>* [查看创意内容的更改日志](/help/creative/creative-libraries/creative-view-change-log.md)
>* [可用于跟踪URL的宏](/help/creative/creative-macros.md)
>* [支持的创意大小](/help/creative/creative-libraries/creative-sizes.md)
>* [预览创意](/help/creative/creative-libraries/creative-preview.md)
>* [从包中附加和分离创意](/help/creative/creative-libraries/creative-attach-detach-bundles.md)
>* [关于您的创意库](/help/creative/creative-libraries/creative-libraries-about.md)
>* [管理创意库](/help/creative/creative-libraries/creative-library-manage.md)
