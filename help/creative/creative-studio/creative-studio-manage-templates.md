---
title: 在Creative Studio中管理广告模板
description: 了解如何在Adobe Advertising Creative中创建、导入、组织和管理广告模板。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: fcd97d29c5009d22100283970892d258043b2d90
workflow-type: tm+mt
source-wordcount: '3697'
ht-degree: 1%
---
# 在[!UICONTROL Creative Studio]中管理广告模板

创建、导入和管理显示和视频广告模板，以便在广告生成会话中使用。

## [!UICONTROL Creative Studio] > [!UICONTROL Templates]视图

**[!UICONTROL Templates]**&#x200B;选项卡提供创建或导入新广告模板的快速操作。

[!UICONTROL Templates]选项卡还会将您现有的广告模板列在页面<!-- Only in the Templates tab -->的底部，作为[个单独的卡片（默认）或表格/列表](/help/creative/introduction/customize-data-views.md)列出。 广告模板列表包括[!UICONTROL All]、[!UICONTROL System Templates]（您的Adobe帐户团队将上载到您的帐户）和[!UICONTROL User Templates]的选项卡。 默认情况下，将显示所有广告商的广告模板。 要仅查看特定广告商的广告模板，请从页面顶部的广告商列表中选择。

<!--
Probably not necessary:

* **[!UICONTROL Card view]** &mdash; Displays templates as cards. Each card shows a preview thumbnail and the ad dimensions. Hovering a card reveals action controls.

* **[!UICONTROL Table view]** &mdash; Displays templates in a table with columns for **[!UICONTROL Name]**, **[!UICONTROL Type]**, **[!UICONTROL Status]**, **[!UICONTROL Size/Duration]**, **[!UICONTROL Advertiser]**, and **[!UICONTROL Updated]**. Click the **[!UICONTROL Name]** or **[!UICONTROL Updated]** column header to sort ascending or descending. Pagination controls appear at the bottom of the list.
-->

### 可用操作

<!--  Figure out how to handle these, which relate to the template list at the bottom of the page: * [Browse and search templates](#browse-search) -->

创建：

* [使用AI生成广告模板](#template-generate)

* [手动创建广告模板](#template-create)

* [导入HTML5广告模板](#templates-import)

对现有模板执行的操作：

* [从显示广告模板生成广告变体](#ad-variations-generate)

* [编辑广告模板](#template-edit)

* [为广告模板添加或删除标签](#template-labels)

* [预览广告模板](#template-preview)

* [下载广告模板](#template-download)

* [添加或删除作为收藏的广告模板](#template-favorite)

* [删除广告模板](#template-delete)

<!--

Move to a Common Tasks chapter:

## Browse and search templates {#browse-search}

### Search

Type in the **[!UICONTROL Search templates]** field and press **[!UICONTROL Enter]** to find templates by name. Click the **[!UICONTROL Clear search]** button to reset.

### Filter by source

Use the filter pills in the toolbar to show a subset of templates:

* **[!UICONTROL All]** &mdash; Shows all templates.
* **[!UICONTROL System Templates]** &mdash; Shows Adobe-provided templates only.
* **[!UICONTROL User Templates]** &mdash; Shows templates you or your team have created or imported.

### Filter by status or format

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Click **[!UICONTROL Filter]** in the toolbar.

1. In the **[!UICONTROL Filters]** dialog, select a filter category:

   * **[!UICONTROL Status]:** Filter by **[!UICONTROL Live]** or **[!UICONTROL Draft]**.
   * **[!UICONTROL Ad Format]:** Filter by **[!UICONTROL Display]** or **[!UICONTROL Video]**.

1. Select one or more options in the category, then click **[!UICONTROL Apply]**.

Applied filters appear as chips below the toolbar. To refine or remove an active filter, click its chip to open a popover where you can toggle options, then click **[!UICONTROL Apply]** or **[!UICONTROL Delete]** to remove the filter. To remove all active filters at once, click **[!UICONTROL Clear All]**.

-->

## 使用AI生成广告模板 {#template-generate}

*Beta功能*

在[!UICONTROL Creative Studio]中使用AI将现有的静态显示广告图像转换为可编辑的显示广告模板。 三步向导可帮助您生成和查看模板、使用自然语言请求更改，以及打开模板编辑器以进行手动更改并保存模板。

### 先决条件

您需要在Creative库中包含静态图像广告。 此工作流从库中选择广告；它不会直接在“生成”对话框中上传新图像。

<!--

Publish this when prompt-based generation becomes available:

To generate a template from an existing image, you need a static image ad in a Creative Library. This option selects ads from your libraries; it doesn't upload a new image directly in the generation dialog. You don't need an existing ad image to generate a template from a prompt.

-->

### 步骤1：生成并查看模板

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. （可选）从页面顶部的广告商列表中选择一个广告商，以查看该广告商的库。

1. 在&#x200B;**[!UICONTROL Use AI to Generate a New Display Ad Template]**&#x200B;框中，单击&#x200B;**[!UICONTROL Generate]**。

1. 在&#x200B;**[!UICONTROL Generate New Ad Template]**&#x200B;对话框中，选择&#x200B;**[!UICONTROL Generate from Existing Standard Ad Image]**（如果尚未选择）。

1. 从&#x200B;**[!UICONTROL Ad Library]**&#x200B;列表中选择包含图像广告的库。

1. 将光标悬停在图像广告卡上并单击&#x200B;**[!UICONTROL Use this Standard Ad]**。

   使用选定广告的宽度和高度，自动开始生成。

<!--

Switch to this when prompt-based generation becomes available:

1. In the **[!UICONTROL Generate New Ad Template]** dialog, choose how to generate the template:

   * **[!UICONTROL Generate from Prompt]:** Describe the ad template you want to create using a text prompt.

   * **[!UICONTROL Generate from Existing Standard Ad Image]:** Convert an existing static image ad into an editable template.

1. Follow the steps for your selected option:

   * From a prompt:

      1. Enter a description of the template you want to create. Include details such as the layout, headline, call to action, and visual style.

      1. Follow the on-screen instructions to generate the template.

   * From an existing standard ad image:

      1. Select the library containing the image ad from the **[!UICONTROL Ad Library]** list.

      1. Hold the cursor over the image ad card and click **[!UICONTROL Use this Standard Ad]**.

         Generation begins automatically, using the selected ad's width and height.

-->

1. [审核并优化生成的模板](#template-review)。

### 第2步：查看和优化模板 {#template-review}

1. 等待生成完成，然后查看模板预览和&#x200B;**[!UICONTROL Layers]**&#x200B;面板（如果可用）。

   在使用模板之前，请检查文本、图像和布局。 此处显示的层供审阅；请在模板编辑器中手动进行更改。

1. （可选）请求对生成的模板进行更改：

   1. 在&#x200B;**[!UICONTROL Ask the AI for any changes]**&#x200B;字段中，描述所需的更改。 例如，输入`Change the headline to "Limited Time Offer" and the button text to "Shop Now"`。

   1. 单击&#x200B;**[!UICONTROL Regenerate]**。

   1. 查看更新的预览。 根据需要重复执行上述步骤。

1. 准备好继续时，单击&#x200B;**[!UICONTROL Use this Ad Template]**。

   生成的模板将在显示模板编辑器中打开。

### 步骤3：编辑并保存模板 {#template-save}

>[!TIP]
>
> AI Assistant使用开源字体库在广告中查找该字体的匹配项。 要使用您自己的字体，请将其上载到[!UICONTROL Assets]选项卡或从模板编辑器上载它，然后在编辑器中替换生成的字体。
>
> 为了获得最佳结果，请在模板编辑器中将AI生成的徽标替换为原始的像素完美徽标。

1. 在模板编辑器中，查看生成的元素，并使用[模板编辑器控件](#template-controls)进行任何剩余的更改。

1. 单击&#x200B;**[!UICONTROL Save]**。

1. 在&#x200B;**[!UICONTROL Update Template]**&#x200B;对话框中，输入或更新&#x200B;**[!UICONTROL Template name]**，选择&#x200B;**[!UICONTROL Advertiser]**，并选择性地添加标记。

1. 单击&#x200B;**[!UICONTROL Update]**&#x200B;保存模板并返回&#x200B;**[!UICONTROL Templates]**&#x200B;视图。

   若要改为保存单独的副本，请单击&#x200B;**[!UICONTROL Save As New]**。

然后，您可以使用该模板[生成广告变体](#ad-variations-generate)。

### 故障排除 {#troubleshooting}

| 问题 | 要做什么 |
| --- | --- |
| 从图像生成时，不会列出库或图像广告 | 检查所选的广告商和&#x200B;**[!UICONTROL Ad Library]**。 如果库没有标准广告图像，请选择另一个包含现有静态图像广告的库。 |
| 基于图像的生成失败或无法转换图像 | 查看显示的消息，单击&#x200B;**[!UICONTROL Back to library]**，然后选择一个图像广告重试。 |

<!--

Add when prompt-based generation is available:

| Prompt-based generation fails | Review the displayed message and revise your prompt before trying again. |

-->

## 手动创建广告模板 {#template-create}

使用模板编辑器创建空白显示或视频模板。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio].**

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 在&#x200B;**[!UICONTROL Create New Ad Template]**&#x200B;框中，单击&#x200B;**[!UICONTROL Create]**，然后选择&#x200B;**[!UICONTROL Display Ad Template]**&#x200B;或&#x200B;**[!UICONTROL Video Ad Template]**。

1. （显示广告）选择广告模板大小，然后单击&#x200B;**[!UICONTROL Continue]**。

1. 使用模板编辑器](#template-controls)中的[控件配置模板设置。

1. （可选）要下载所定义的模板副本，请单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download]**。

   将按照浏览器的正常过程下载文件。

1. 保存模板：

   1. 执行以下任一操作：

      * 单击&#x200B;**[!UICONTROL Save]**。

      * 要将模板另存为草稿，请单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**。

   1. 输入&#x200B;**[!UICONTROL Template name]**，选择&#x200B;**[!UICONTROL Advertiser]**，或者选择现有标记或向模板中添加新标记，然后单击&#x200B;**[!UICONTROL Save]**。

## 导入HTML5广告模板 {#templates-import}

上传一个或多个打包为ZIP文件的预建HTML5模板。 导入时会验证模板；如果HTML超过200,000个字符，CSS超过60,000个字符，模板包含超过5,000个DOM元素，或者模板包含不支持的脚本标记，则导入失败。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio].**

1. 选择页面顶部的广告商。

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 在&#x200B;**[!UICONTROL Upload HTML5 Templates]**&#x200B;框中，单击&#x200B;**[!UICONTROL Upload]**，然后选择&#x200B;**[!UICONTROL Display Ad Template]**&#x200B;或&#x200B;**[!UICONTROL Video Ad Template]**。

1. 从设备或网络中选择一个或多个ZIP文件。

1. 在&#x200B;**[!UICONTROL Import Templates]**&#x200B;对话框中：

   1. 选择&#x200B;**[!UICONTROL Advertiser]**。

      如果您已在页面顶部选择了特定广告商，则会预先选择该广告商。

   1. （可选）对于每个文件，编辑&#x200B;**[!UICONTROL Template Name]**。

      默认使用文件名。

   1. （可选）要添加更多文件，请单击&#x200B;**[!UICONTROL Add more]**&#x200B;并选择其他ZIP文件。 为每个附加文件指定&#x200B;**[!UICONTROL Template Name]**。

1. 单击&#x200B;**[!UICONTROL Import Templates]**。

>[!NOTE]
>
>如果导入失败，请简化模板或联系您的Adobe客户团队。

## 编辑广告模板 {#template-edit}

*仅显示广告模板。*

>[!IMPORTANT]
>
>AI代理无法更改模板布局、元素位置、间距或排版规则。 在生成内容之前，在模板编辑器中进行任何结构性更改。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio].**

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 将光标悬停在模板卡或表格行上，然后单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Template]**。

1. 在模板编辑器](#template-controls)中使用[控件编辑模板布局或元素。

1. （可选）要下载所定义的模板副本，请单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download]**。

   将按照浏览器的正常过程下载文件。

1. 保存模板：

   * 单击&#x200B;**[!UICONTROL Save]**。

   * 要将模板另存为草稿，请单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**。 输入&#x200B;**[!UICONTROL Template name]**，选择&#x200B;**[!UICONTROL Advertiser]**，或者选择现有标记或向模板中添加新标记，然后单击&#x200B;**[!UICONTROL Save]**。

<!--

I don't see this anywhere:

1. Click **[!UICONTROL Generate Ad Variations]** to proceed to content generation, or navigate away to save your changes.

-->

## 从显示广告模板生成广告变体 {#ad-variations-generate}

*仅显示广告模板。*

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio].**

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 将光标悬停在模板卡或表格行上，然后单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**。

   将打开[!UICONTROL Ad Variations Generator]并预加载模板。

1. 使用AI聊天界面生成和优化广告内容。 有关完整的工作流，请参阅[在Creative Studio中管理标准广告](creative-studio-manage-standard-ads.md)。

## 为广告模板添加或删除标签 {#template-labels}

*仅显示广告模板。*

标签可帮助您组织和筛选用户模板。 不能向系统模板添加标签。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio].**

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 将光标悬停在模板卡或表格行上，然后单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit Labels]**。

1. 在&#x200B;**[!UICONTROL Edit Labels]**&#x200B;对话框中：

   * 要添加标签，请选择现有标签或在输入字段中输入名称，然后单击&#x200B;**[!UICONTROL Add Tag]**。

   * 要删除标签，请单击标签标签旁边的&#x200B;**[!UICONTROL X]**。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 预览广告模板 {#template-preview}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio].**

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 将光标悬停在模板卡片上。

1. 执行以下任一操作：

   * （卡片视图）单击&#x200B;**[!UICONTROL Preview template]**&#x200B;图标，或单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Preview]**。

   * （表格视图）单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Preview]**。

1. 对于视频模板，请单击![播放](/help/creative/assets/play.png "播放")。

## 下载广告模板 {#template-download}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio].**

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 将光标悬停在模板卡或表格行上，然后单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Download]**。

   模板将按照浏览器的正常过程下载为ZIP文件。

## 添加或删除作为收藏的广告模板 {#template-favorite}

*仅卡片视图*

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio].**

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 将光标悬停在模板卡片上。

1. 执行以下任一操作：

   * 要将模板添加为收藏，请单击![收藏](/help/creative/assets/favorite-null.png "收藏")。

   * 要删除作为收藏的模板，请单击![收藏夹](/help/creative/assets/favorite.png "收藏夹")。

## 删除广告模板 {#template-delete}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio].**

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 将光标悬停在模板卡或表格行上，然后单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Delete]**。

## 模板编辑器控件 {#template-controls}

显示模板和视频模板编辑器在画布上方提供一个工具栏以撤消更改并调整视图，在左侧提供一个面板以添加资源和元素，在右侧提供一个面板[!UICONTROL Layers]以管理图层。 显示模板和视频模板之间用于编辑所选元素以及控制计时和播放的工具有所不同。

<!--

Removing -- these are actions that are used within specific procedures:

### Top toolbar

The top toolbar above the canvas is the same for both display and video templates.

| Control | Description |
| --- | --- |
| Template name | The current template name, shown at the top of the editor. Click the **[!UICONTROL Edit name]** icon next to the name to rename it inline. |
| **[!UICONTROL Save]** | Saves and publishes the template. |
| **[!UICONTROL ...]** > **[!UICONTROL Save As Draft]** | Saves the template as a draft without publishing. Enter or update the name, select the advertiser, optionally add tags, and click **[!UICONTROL Save]**. |
| **[!UICONTROL ...]** > **[!UICONTROL Download]** | Downloads the current template as a ZIP file. |
| **[!UICONTROL Cancel]** | Discards unsaved changes and returns to the Templates list. |

-->

### 撤消更改并调整画布视图

常规操作工具栏位于广告模板编辑器的编辑画布上方，并分为两部分（左和右）。

#### 显示广告模板

| 控件 | 描述 |
| --- | --- |
| **[!UICONTROL Undo]** | 撤消上一个操作。 |
| ![重做](/help/creative/assets/cs-icon-redo.png "重做") **[!UICONTROL Redo]** | 重新执行上一个撤消的操作。 |
| **[!UICONTROL Links]** | 打开一个面板以管理附加到模板中元素的点进URL。 |
| 缩放控件 | 单击&#x200B;**[!UICONTROL Zoom out]**&#x200B;或&#x200B;**[!UICONTROL Zoom in]**&#x200B;可调整画布放大率（10%-150%，以10%为增量）。 单击缩放级别标签（在画布自动调整时显示&#x200B;**[!UICONTROL Auto]**，在手动设置时显示百分比）以打开包含选项&#x200B;**[!UICONTROL Auto-Fit Page]**、**[!UICONTROL 100% Zoom]**、**[!UICONTROL 50% Zoom]**、**[!UICONTROL Zoom In]**&#x200B;和&#x200B;**[!UICONTROL Zoom Out]**&#x200B;的菜单。 |
| 广告大小 | 显示当前的广告维度（例如，300 × 250）。 单击以打开大小选择器，选择器提供6种常用的IAB标准大小作为卡片，以及包含所有19个标准IAB显示广告大小的下拉列表。 新模板的默认大小为300 × 250 （Medium矩形）。 |
| ![打开图层面板](/help/creative/assets/layers-panel-open.png "打开图层面板") | 打开[!UICONTROL Layers]面板。 仅在[!UICONTROL Layers]面板关闭时显示。 |

#### 视频广告模板

| 控件 | 描述 |
| --- | --- |
| **[!UICONTROL Undo]** / ![重做](/help/creative/assets/cs-icon-redo.png "重做") **[!UICONTROL Redo]** | 撤消或重新执行上一个操作。 |
| 缩放控件 | 单击&#x200B;**[!UICONTROL Zoom out]**&#x200B;或&#x200B;**[!UICONTROL Zoom in]**&#x200B;调整画布放大率。 单击缩放级别以打开包含下列选项的菜单： **[!UICONTROL Auto-Fit Page]**、**[!UICONTROL 100% Zoom]**、**[!UICONTROL 50% Zoom]**、**[!UICONTROL Zoom In]**&#x200B;和&#x200B;**[!UICONTROL Zoom Out]**。 |
| ![打开图层面板](/help/creative/assets/layers-panel-open.png "打开图层面板") | 打开[!UICONTROL Layers]面板。 仅在[!UICONTROL Layers]面板关闭时显示。 |

<!--

Not there as of 10/15:

| Page resize | Opens the page-size controls to change the video template dimensions. |
| **[!UICONTROL Preview]** | Opens a preview of the video template. |

   -->

### 添加资源和元素

左侧面板允许您向模板添加广告资源和元素。 单击图标以打开其内容面板；再次单击同一图标以将其关闭。

#### 显示广告模板

| 图标 | 描述 |
| --- | --- |
| **[!UICONTROL Search]** | 在库中的所有资产类型中进行搜索。 |
| **[!UICONTROL Upload]** | 将图像或字体文件上载到编辑器以在当前模板中使用。 您一次最多可以上传20个文件。 |
| **[!UICONTROL Templates]** | 从Creative Studio库中浏览广告模板，以用作基础层或引用元素。 |
| **[!UICONTROL My Assets]** | 浏览您在Creative Studio [!UICONTROL Assets]选项卡中上传的所有资源。 |
| **[!UICONTROL Images]** | 仅浏览您在Creative Studio [!UICONTROL Assets]选项卡中上传的图像资源。 |
| **[!UICONTROL Text]** | 向画布中添加文本元素，包括您上传的任何自定义字体。 |
| **[!UICONTROL Elements]** | 添加形状和布局元素，如按钮和矩形。 |

您可以将项目从任何面板直接拖到画布上，也可以单击该项目以将其置于默认位置。

#### 视频广告模板

| 图标 | 描述 |
| --- | --- |
| **[!UICONTROL Search]** | 在库中的所有资产类型中进行搜索。 |
| **[!UICONTROL Upload]** | 将图像、视频、音频或字体文件(TTF、OTF、WOFF、WOFF2)上载到编辑器以便在当前模板中使用。 您一次最多可以上传20个文件。 |
| **[!UICONTROL Templates]** | 从Creative Studio库中浏览广告模板。 |
| **[!UICONTROL My Assets]** | 浏览您在Creative Studio [!UICONTROL Assets]选项卡中上传的所有资源。 |
| **[!UICONTROL Images]** | 仅浏览您在Creative Studio [!UICONTROL Assets]选项卡中上传的图像资源。 |
| **[!UICONTROL Video]** | 仅浏览您在Creative Studio [!UICONTROL Assets]选项卡中上传的视频资源。 |
| **[!UICONTROL Audio]** | 仅浏览您在Creative Studio [!UICONTROL Assets]选项卡中上传的音频资源。 |
| **[!UICONTROL Text]** | 向画布中添加文本元素，包括您上传的任何自定义字体。 |
| **[!UICONTROL Elements]** | 添加形状和矢量元素。 |

您可以将项目从任何面板直接拖到画布上，也可以单击该项目以将其置于默认位置。

### 编辑所选元素

单击编辑画布上的元素以将其选定。 根据模板类型，将显示一个或多个包含该元素控件的工具栏。

控件因元素类型而异。

<!-- From inspectorbar.ts -->

#### 显示模板编辑工具栏

| 控件 | 元素类型 | 描述 |
| --- | --- | --- |
| **[!UICONTROL Properties]** | 全部 | 打开面板以编辑图层名称；将图层标记为动态（在广告生成期间可交换）；并设置点进URL（仅限链接）。 在其下方，选择&#x200B;**[!UICONTROL Default]**、**[!UICONTROL Hover]**、**[!UICONTROL Click]**&#x200B;或&#x200B;**[!UICONTROL Focus]**&#x200B;状态以设置该交互状态的元素样式，然后根据元素类型调整样式 — 排版规则（仅限文本和链接）、装饰（填充、边框、圆角半径）、维度、位置。 |
| **[!UICONTROL Effects]** | 全部 | 打开一个面板，从中可选择要将效果应用于该交互状态的&#x200B;**[!UICONTROL Default]**、**[!UICONTROL Hover]**、**[!UICONTROL Click]**&#x200B;或&#x200B;**[!UICONTROL Focus]**&#x200B;状态，然后调整&#x200B;**[!UICONTROL Transform]**、**[!UICONTROL Transition]**、**[!UICONTROL Box Shadow]**、**[!UICONTROL Filter]**、**[!UICONTROL Blend Mode]**&#x200B;和&#x200B;**[!UICONTROL Cursor]**&#x200B;分区。 文本元素还包含&#x200B;**[!UICONTROL Text Shadow]**&#x200B;节。 |
| **[!UICONTROL Animations]** | 全部 | 打开一个面板，以设置图层在时间轴上的进入和退出时间，并通过持续时间和经济缓动配置&#x200B;**[!UICONTROL Entrance Animation]**、**[!UICONTROL Loop Animation]**&#x200B;和&#x200B;**[!UICONTROL Exit Animation]**&#x200B;预设。 包括&#x200B;**[!UICONTROL Copy]**、**[!UICONTROL Paste]**&#x200B;和&#x200B;**[!UICONTROL Reset]**&#x200B;操作。 |
| **[!UICONTROL Crop]** | 图像 | 打开工具栏以裁切图像。 选择&#x200B;**[!UICONTROL Aspect Ratio]**&#x200B;预设（或&#x200B;**[!UICONTROL Free]**），然后单击&#x200B;**[!UICONTROL Apply]**&#x200B;或&#x200B;**[!UICONTROL Cancel]**。 |
| **[!UICONTROL Position]** | 全部 | 打开包含&#x200B;**[!UICONTROL Move]**&#x200B;选项(**[!UICONTROL Forward]**、**[!UICONTROL Backward]**、**[!UICONTROL To front]**、**[!UICONTROL To back]**)、**[!UICONTROL Align to Page]**&#x200B;选项(**[!UICONTROL Top]**、**[!UICONTROL Left]**、**[!UICONTROL Middle]**、**[!UICONTROL Center]**、**[!UICONTROL Bottom]**、**[!UICONTROL Right]**、**[!UICONTROL Fit Vertically]**、**[!UICONTROL Fit Horizontally]**、**[!UICONTROL Fit to Page]**)的菜单，对于非图像元素，打开&#x200B;**[!UICONTROL Layer Level Alignment]**&#x200B;选项（相同的六个对齐选项，加上&#x200B;**[!UICONTROL Fit to Content]**）。 |

#### 视频模板编辑工具栏

| 控件 | 元素类型 | 描述 |
| --- | --- | --- |
| **[!UICONTROL Shape]** | 形状 | 设置特定于形状的选项。 |
| 挖剪控件 | 图像 | 调整切口类型、偏移和平滑。 |
| **[!UICONTROL Group]** / **[!UICONTROL Ungroup]** | 多个选定的元素或组 | 将所选元素组合在一起，或取消选定组的组合。 |
| **[!UICONTROL Combine]** | 兼容的形状 | 将选定的形状组合为单个形状。 |
| **[!UICONTROL Audio replace]** | 音频和视频 | 将音轨替换为资产库中的文件。 |
| **[!UICONTROL Typeface]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, **[!UICONTROL Font size]**, **[!UICONTROL Align horizontal]**, **[!UICONTROL Advanced]** | 文本 | 调整字体系列、粗细、大小、水平对齐和其他高级排版设置。 |
| **[!UICONTROL Image]** / **[!UICONTROL Video]** | 图像和视频 | 设置元素的填充图像或视频源。 |
| **[!UICONTROL Trim]** | 视频和音频 | 打开修剪模式以设置剪辑的起点和终点。 |
| ![卷](/help/creative/assets/volume.png "卷") ([!UICONTROL Volume]) | 视频和音频 | 调整音频级别。 |
| ![播放速度](/help/creative/assets/speed.png "播放速度") ([!UICONTROL Playback speed]) | 视频和音频 | 调整播放速率。 |
| ![裁切](/help/creative/assets/crop.png "裁切") ([!UICONTROL Crop]) | 全部 | 将元素裁剪为自定义区域。 |
| 旋转和翻转控件 | 全部 | 旋转或翻转所选元素。 |
| ![笔触](/help/creative/assets/stroke.png "笔触") ([!UICONTROL Stroke]) | 全部 | 设置边框颜色和宽度。 |
| **[!UICONTROL Text Background]** | 文本 | 在文本后面添加背景颜色。 |
| **[!UICONTROL Animations]** | 全部 | 添加或编辑输入、退出或循环动画。 |
| **[!UICONTROL Style]** | 全部 | 打开包含&#x200B;**[!UICONTROL Adjustments]**、**[!UICONTROL Filter]**、**[!UICONTROL Effect]**&#x200B;和&#x200B;**[!UICONTROL Blur]**&#x200B;选项的菜单。 |
| **[!UICONTROL Shadow]** | 全部 | 添加或编辑投影。 |
| **[!UICONTROL Opacity]** | 全部 | 设置元素的透明度级别。 |
| **[!UICONTROL Position]** | 全部 | 按数值调整元素的大小、位置和旋转。 |
| ![正在编辑面板](/help/creative/assets/cs-template-video-editing-panel.png "正在编辑面板") | 全部 | 打开或关闭具有更多编辑功能的选定元素的[编辑面板](#detailed-element-properties-for-video-templates)。 |

#### 视频模板的详细元素属性

在视频模板编辑器中，单击工具栏中的![“编辑面板”](/help/creative/assets/cs-template-video-editing-panel.png "“编辑面板”")，为具有更多编辑功能的选定元素打开编辑面板。 编辑面板显示在画布的左侧，与列出模板中图层的[!UICONTROL Layers]面板不同。

##### 单个元素

选择单个图像、视频、形状或文本元素时，编辑面板会在下面显示适用的部分。

| 面板部分 | 工具 | 控件 |
| --- | --- | --- |
| [!UICONTROL Layer] | 对齐和图层定位 | 将选定图层与左对齐、水平居中对齐、右对齐、顶部对齐、垂直居中对齐或底部对齐。 排列菜单更改了其从前到后的栈叠顺序。 这些控件定位图层本身；它们不会两端对齐图层中的文本。 |
| | [!UICONTROL Rotate & Flip] | 输入旋转角度（以度为单位）。 使用![水平翻转](/help/creative/assets/cs-template-video-flip.png "水平翻转")可水平镜像图层，或者使用![垂直翻转](/help/creative/assets/cs-template-video-flip-vertical.png "垂直翻转")可垂直镜像图层。 |
| | ![不透明度](/help/creative/assets/cs-template-video-opacity.png "不透明度") [!UICONTROL Opacity] | 使所选图层或多或少透明。 |
| | ![混合模式](/help/creative/assets/cs-template-video-blend-mode.png "混合模式") [!UICONTROL Blend Mode] | 更改所选图层的颜色与其后面的图层的组合方式。 |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | 打开层位置和尺寸的附加控件。 可用性取决于所选层的转换权限。 |
| [!UICONTROL Shape] | ![形状选项](/help/creative/assets/cs-template-video-shape-options.png "形状选项") [!UICONTROL Shape]和特定于形状的属性 | 更改形状及其可用属性，如点、侧、内径、线宽或圆角半径。 控件取决于所选的形状。 |
| | [!UICONTROL Vector]: [!UICONTROL Edit Path] | 进入矢量编辑模式以编辑形状的路径（如果可用）。 |
| [!UICONTROL Character] | ![字体](/help/creative/assets/cs-template-video-typeface.png "字体")字体，![文本样式](/help/creative/assets/cs-template-video-text-style.png "文本样式")文本样式，![粗体](/help/creative/assets/cs-template-video-text-bold.png "粗体")粗体，![斜体](/help/creative/assets/cs-template-video-text-italic.png "斜体")斜体，以及![字体大小](/help/creative/assets/cs-template-video-font-size.png "字体大小")字体大小 | （文本图层）更改所选文本的字体系列、字体样式和大小。 |
| | ![左对齐](/help/creative/assets/cs-template-video-text-align-l.png "左对齐") / ![居中对齐](/help/creative/assets/cs-template-video-text-align-c.png "居中对齐") / ![右对齐](/help/creative/assets/cs-template-video-text-align-r.png "右对齐")文本对齐 | （文本图层）将框架中的文本与左对齐、居中对齐或右对齐，或者自动检测对齐方式。 |
| | ![高级文本设置](/help/creative/assets/cs-template-video-advanced-text.png "高级文本设置")高级文本设置 | （文本图层）打开其他排版设置。 |
| [!UICONTROL Fill] | ![填充](/help/creative/assets/cs-template-video-fill.png "填充")填充控件 | 更改所选图层的颜色、图像或视频填充。 控件反映当前的填充类型并打开其设置。 对于文本，更改文本颜色。 |
| [!UICONTROL Stroke] | ![笔触](/help/creative/assets/cs-template-video-stroke.png "笔触")笔触控件 | 启用或禁用轮廓，并更改其颜色、宽度、样式和位置。 启用笔触时，将显示其他控件。 |
| [!UICONTROL Text Background] | ![文本背景](/help/creative/assets/cs-template-video-text-bg.png "文本背景")背景控件 | （文本图层）添加或更改文本后面的背景。 |
| [!UICONTROL Animations] | ![动画](/help/creative/assets/cs-template-video-animation.png "动画") [!UICONTROL Presets] | 打开选定图层的动画预设，包括进入、退出和循环动画。 |
| [!UICONTROL Appearance] | ![调整](/help/creative/assets/cs-template-video-adjustments.png "调整") [!UICONTROL Adjustments] | 更改选定图层的视觉属性。 |
| | ![筛选器](/help/creative/assets/cs-template-video-filter.png "筛选器") [!UICONTROL Filter] | 将可视滤镜应用于选定图层。 |
| | ![效果](/help/creative/assets/cs-template-video-effects.png "效果") [!UICONTROL Effect] | 将效果应用于所选图层。 |
| | ![模糊](/help/creative/assets/cs-template-video-blur.png "模糊") [!UICONTROL Blur] | 将模糊应用于所选图层。 |
| | ![阴影](/help/creative/assets/cs-template-video-shadow.png "阴影") [!UICONTROL Shadow] | 添加或更改所选图层的阴影。 |

##### 多个选择和专用元素

选择多个元素、组、切除元素或音频剪辑时，编辑面板会在下面显示特定于选择的部分。 多个元素、组和切除也保留[!UICONTROL Layer]部分。

| 面板部分 | 工具 | 控件 |
| --- | --- | --- |
| [!UICONTROL Layer] | 对齐和图层定位 | 对齐多个选定的元素或组。 排列菜单会更改其从前到后的栈叠顺序。 |
| | [!UICONTROL Rotate & Flip] | 旋转或翻转选定的元素或组。 |
| | ![不透明度](/help/creative/assets/cs-template-video-opacity.png "不透明度") [!UICONTROL Opacity] | 使所选元素或组或多或少透明。 |
| | ![混合模式](/help/creative/assets/cs-template-video-blend-mode.png "混合模式") [!UICONTROL Blend Mode] | 更改所选元素或组的颜色与它们后面的图层的组合方式。 |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | 打开选定元素或组的位置和尺寸的控件。 可用的控件取决于所选的元素。 |
| [!UICONTROL Selection] | ![组](/help/creative/assets/cs-template-video-group.png "组")组/![取消组](/help/creative/assets/cs-template-video-ungroup.png "取消组")取消组 | 对于多个选定图层或选定组，显示在[!UICONTROL Layer]下方。 将所选图层编组，以便一起管理，或将组分成单独的图层。 |
| [!UICONTROL Settings] | ![挖剪辑](/help/creative/assets/cs-template-video-cutout-clip.png "挖剪辑") / ![挖剪重叠](/help/creative/assets/cs-template-video-cutout-overlay.png "挖剪重叠")挖剪控件 | （切口层）显示在[!UICONTROL Layer]下方。 选择切口类型并调整其偏移和边平滑。 |
| [!UICONTROL Audio Properties] | ![修剪](/help/creative/assets/cs-template-video-trim.png "修剪")修剪，![音量](/help/creative/assets/cs-template-video-volume.png "音量")音量，以及![播放速度](/help/creative/assets/cs-template-video-playback-speed.png "播放速度")播放速度 | （音频图层）设置剪辑的起点和终点、音频级别和播放速度。 |

#### 直接在画布上编辑元素

##### 显示广告模板

| 操作 | 描述 |
| --- | --- |
| **[!UICONTROL Replace]** | （仅限图像元素）打开“图像”面板，以便您可以将图像替换为资源库中的图像。 |
| ![前进](/help/creative/assets/cs-icon-move-forward.png "前进") **[!UICONTROL Move forward]** | 按栈叠顺序将元素向前移动一步（向前移动）。 |
| ![向后移动](/help/creative/assets/cs-icon-move-backward.png "向后移动") **[!UICONTROL Move backward]** | 按栈叠顺序向后移动元素一步（向后）。 |
| ![重复](/help/creative/assets/cs-icon-duplicate.png "重复") **[!UICONTROL Duplicate]** | 创建元素的副本。 |
| ![删除](/help/creative/assets/cs-icon-delete.png "删除") **[!UICONTROL Delete]** | 从画布中删除元素。 |
| 旋转手柄 | 单击并将手柄拖动到选定元素上方可旋转它。 拖动时按住&#x200B;**[!UICONTROL Shift]**&#x200B;以将旋转捕捉到15度增量。 |

也可以单击并拖动选定元素以将其重新定位，单击并拖动其周围的手柄以调整其大小。

##### 视频广告模板

| 操作 | 描述 |
| --- | --- |
| **[!UICONTROL Edit text]** | （仅限文本元素）切换到文本编辑模式，以便您可以直接在画布上键入文本并设置其格式。 在文本编辑模式下，辅助菜单提供&#x200B;**[!UICONTROL Text color]**、**[!UICONTROL Bold]**、**[!UICONTROL Italic]**&#x200B;和&#x200B;**[!UICONTROL Text variables]**（模板占位符）。 |
| **[!UICONTROL Replace]** | （仅限图像元素）打开资产库以便交换图像。 |
| **[!UICONTROL Bring forward]** | 按栈叠顺序将元素向前移动一步。 |
| **[!UICONTROL Send backward]** | 按栈叠顺序向后移动元素一步。 |
| **[!UICONTROL Duplicate]** | 创建元素的副本。 |
| **[!UICONTROL Delete]** | 从画布中删除元素。 |
| **... >[!UICONTROL Flip horizontal]** | 水平翻转元素180度。 |
| **... >[!UICONTROL Flip vertical]** | 将元素垂直翻转180度。 |
| **... >[!UICONTROL Copy Element]** | 将元素复制到画布剪贴板。 |
| **... >[!UICONTROL Pastes Element]** | 粘贴复制的元素。 |

也可以单击并拖动选定元素以将其重新定位，单击并拖动其周围的手柄以调整其大小。

### 控制定时和播放

显示和视频编辑器都在画布底部显示一个时间轴面板。

#### 显示广告模板

时间轴显示画布上每个图层的跟踪，该跟踪跨越了根据图层进入和退出动画时间而使其可见的时间范围。 拖动轨道的开始或结束手柄以调整其进入或退出时间，或者拖动轨道以重新排序图层。 单击标尺或拖动播放头以移动到时间点。

时间线工具栏包括&#x200B;**[!UICONTROL Duration]**&#x200B;字段（0-60秒）、**[!UICONTROL Play]**/**[!UICONTROL Pause]**、当前时间/总持续时间显示、循环切换、**[!UICONTROL Timeline Scale]**&#x200B;缩放控件、**[!UICONTROL Fit View]**&#x200B;按钮和折叠/展开切换。

#### 视频广告模板

时间轴显示模板中的所有视频和音频剪辑。 使用时间轴查看剪辑的及时排列方式，并通过拖动剪辑的开始和结束手柄来裁剪剪剪辑。 不能直接在时间轴上添加新剪辑；请改为从左侧面板或画布中添加它，然后它会在时间轴上显示为剪辑。

### 管理图层

画布右侧的[!UICONTROL Layers]面板列出了模板中的所有元素，并允许您管理其顺序、可见性和属性。 对于显示模板，单击画布工具栏中的&#x200B;**[!UICONTROL Open Layers]**&#x200B;以将其打开。 对于视频模板，默认情况下将打开面板。

单击任意层以在画布上选择相应的元素。

**选项卡（仅限显示广告模板）**

显示模板在[!UICONTROL Layers]面板的顶部有两个选项卡：

* **[!UICONTROL Dynamic]** — 仅列出在广告生成期间可以交换的图层，例如AI代理可以替换的图像和文本。 这是生成广告变体的默认视图。
* **[!UICONTROL All]** — 显示模板的完整层层次结构，包括结构容器。 使用此视图可检查或重新组织元素的嵌套方式。

视频模板在一个不含选项卡的列表中显示所有图层。

**每层操作**

将光标悬停在图层上可查看以下操作。

| 操作 | 描述 |
| --- | --- |
| ![重命名层](/help/creative/assets/edit.png "重命名层") **[!UICONTROL Rename layer]** | 允许您在面板中输入新图层名称。 |
| ![锁定图层](/help/creative/assets/cs-icon-lock.png "锁定图层") **[!UICONTROL Lock layer]** / ![解锁图层](/help/creative/assets/cs-icon-unlock.png "解锁图层") **[!UICONTROL Unlock layer]** | 防止或允许移动、编辑或重新排序图层。 |
| ![隐藏图层](/help/creative/assets/cs-icon-hidden.png "隐藏图层") **[!UICONTROL Hide layer]** / ![显示图层](/help/creative/assets/cs-icon-visible.png "显示图层") **[!UICONTROL Show layer]** | 隐藏或显示画布上的图层。 隐藏的图层会保留在模板中，但不会在模板渲染时显示。 |
| ![拖动以重新排序](/help/creative/assets/cs-icon-drag.png "拖动以重新排序")拖动以重新排序 | （仅限显示广告模板）拖动重新排序图标可更改图层在栈叠顺序中的位置。 必须解锁该图层才能对其进行重新排序。 |

**面板页脚**

| 操作 | 描述 |
| --- | --- |
| ![复制选定层](/help/creative/assets/cs-icon-duplicate.png "复制选定层") **[!UICONTROL Duplicate selected layer]** | 创建选定图层的副本。 |
| ![删除选定层](/help/creative/assets/cs-icon-delete.png "删除选定层") **[!UICONTROL Delete selected layer]** | 删除所选图层。 |
| **[!UICONTROL Group selected layers]** （仅限视频模板） | 将两个或多个选定图层组合为一个组。 仅在选定两个或多个层时显示。 您可以使用组行上的控件取消分组图层或从组中移除单个图层。 |

<!--

These are all saved with the template, but they aren't what you see, as-is, in the template settings per se. Rethink if I should include this, and how to frame it:

## Template settings {#template-settings}

### Display ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Type]** | (Required) The HTML5 template type: **[!UICONTROL Static HTML5]** or **[!UICONTROL Dynamic HTML]**. |
| **[!UICONTROL Size]** | (Required) The ad dimensions. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **[!UICONTROL Tags]** | (Optional) One or more labels. Click **[!UICONTROL Add More]** to add additional tags. |
| **ZIP file** | The HTML5 creative ZIP file. For **[!UICONTROL Dynamic HTML]** templates, also upload the template data file (TDF). |

### Video ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **ZIP file** | The video ad template ZIP file. |

-->

>[!MORELIKETHIS]
>
>* [关于Advertising Creative中的Creative Studio](creative-studio-about.md)
>* [在Creative Studio中管理资源](creative-studio-manage-assets.md)
>* [在Creative Studio中管理标准广告](creative-studio-manage-standard-ads.md)
>* [在Creative Studio中管理动态创意](creative-studio-manage-dynamic-ads.md)
