---
title: 在Creative Studio中管理广告模板
description: 了解如何在Adobe Advertising Creative的Creative Studio“模板”选项卡中创建、导入、组织和管理广告模板。
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d4a041529615006a79093dccb8690f3b9f5e8cba
workflow-type: tm+mt
source-wordcount: 2512
ht-degree: 2%

---

# 在[!UICONTROL Creative Studio]中管理广告模板

*Beta功能*

创建、导入和管理显示和视频广告模板，以便在广告生成会话中使用。

## [!UICONTROL Creative Studio] > [!UICONTROL Templates]视图

**[!UICONTROL Templates]**&#x200B;选项卡提供创建或导入新广告模板的快速操作。

该选项卡还会将您现有的广告模板列在页面<!-- Only in the Templates tab -->的底部，作为[个单独的卡片（默认）或表格/列表](/help/creative/introduction/customize-data-views.md)列出。 广告模板列表包括[!UICONTROL All]、[!UICONTROL System Templates]（由您的Adobe客户团队上传到您的帐户）和[!UICONTROL User Templates]的选项卡。 默认情况下，将显示所有广告商的广告模板。 要仅查看特定广告商的广告模板，请从页面顶部的广告商列表中选择。

<!-- 
Probably not necessary:

* **[!UICONTROL Card view]** &mdash; Displays templates as cards. Each card shows a preview thumbnail and the ad dimensions. Hovering a card reveals action controls.

* **[!UICONTROL Table view]** &mdash; Displays templates in a table with columns for **[!UICONTROL Name]**, **[!UICONTROL Type]**, **[!UICONTROL Status]**, **[!UICONTROL Size/Duration]**, **[!UICONTROL Advertiser]**, and **[!UICONTROL Updated]**. Click the **[!UICONTROL Name]** or **[!UICONTROL Updated]** column header to sort ascending or descending. Pagination controls appear at the bottom of the list.
-->

### 可用操作

<!--  Figure out how to handle these, which relate to the template list at the bottom of the page: * [Browse and search templates](#browse-search) -->

创建：

* [导入HTML5广告模板](#templates-import)

* [手动创建广告模板](#template-create)

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

## 模板编辑器控件 {#template-controls}

显示模板编辑器和视频模板编辑器在编辑画布和右侧[!UICONTROL Layers]面板上方共享相同的常规操作工具栏。 左侧面板、广告模板编辑控件和时间轴在显示模板和视频模板之间有所不同。

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

### 常规操作工具栏

常规操作工具栏位于广告模板编辑器的编辑画布上方，并分为两部分（左和右）。

#### 显示广告模板

| 控件 | 描述 |
| --- | --- |
| **[!UICONTROL Undo]** | 撤消上一个操作。 |
| ![重做](/help/creative/assets/cs-icon-redo.png) **[!UICONTROL Redo]** | 重新执行上一个撤消的操作。 |
| **[!UICONTROL Links]** | 打开一个面板以管理附加到模板中元素的点进URL。 |
| 缩放控件 | 单击&#x200B;**[!UICONTROL Zoom out]**&#x200B;或&#x200B;**[!UICONTROL Zoom in]**&#x200B;可调整画布放大率（10%-150%，以10%为增量）。 单击缩放级别标签（在画布自动调整时显示&#x200B;**[!UICONTROL Auto]**，在手动设置时显示百分比）以打开包含选项&#x200B;**[!UICONTROL Auto-Fit Page]**、**[!UICONTROL 100% Zoom]**、**[!UICONTROL 50% Zoom]**、**[!UICONTROL Zoom In]**&#x200B;和&#x200B;**[!UICONTROL Zoom Out]**&#x200B;的菜单。 |
| 广告大小 | 显示当前的广告维度（例如，300 × 250）。 单击以打开大小选择器，选择器提供6种常用的IAB标准大小作为卡片，以及包含所有19个标准IAB显示广告大小的下拉列表。 新模板的默认大小为300 × 250 （Medium矩形）。 |
| ![打开图层面板](/help/creative/assets/layers-panel-open.png "打开图层面板") | 打开[!UICONTROL Layers]面板。 仅在[!UICONTROL Layers]面板关闭时显示。 |

#### 视频广告模板

| 控件 | 描述 |
| --- | --- |
| **[!UICONTROL Undo]** / ![重做](/help/creative/assets/cs-icon-redo.png) **[!UICONTROL Redo]** | 撤消或重新执行上一个操作。 |
| 缩放控件 | 单击&#x200B;**[!UICONTROL Zoom out]**&#x200B;或&#x200B;**[!UICONTROL Zoom in]**&#x200B;调整画布放大率。 单击缩放级别以打开包含下列选项的菜单： **[!UICONTROL Auto-Fit Page]**、**[!UICONTROL 100% Zoom]**、**[!UICONTROL 50% Zoom]**、**[!UICONTROL Zoom In]**&#x200B;和&#x200B;**[!UICONTROL Zoom Out]**。 |
| ![打开图层面板](/help/creative/assets/layers-panel-open.png "打开图层面板") | 打开[!UICONTROL Layers]面板。 仅在[!UICONTROL Layers]面板关闭时显示。 |

<!-- Not there as of 7/10:  | **[!UICONTROL Preview]** | Opens a preview of the video template. | -->

### 左侧面板

左侧面板包含一列图标。 单击图标以打开其内容面板；再次单击同一图标以将其关闭。

#### 显示广告模板

| 图标 | 描述 |
| --- | --- |
| **[!UICONTROL Search]** | 在库中的所有资产类型中进行搜索。 |
| **[!UICONTROL Upload]** | 将图像或字体文件上载到编辑器以在当前模板中使用。 您一次最多可以上传20个文件。 |
| **[!UICONTROL Templates]** | 从Creative Studio库中浏览广告模板，以用作基础层或引用元素。 |
| **[!UICONTROL My Assets]** | 浏览您在Creative Studio Assets选项卡中上传的所有资源。 |
| **[!UICONTROL Images]** | 仅浏览您在Creative Studio Assets选项卡中上传的图像资源。 |
| **[!UICONTROL Text]** | 向画布中添加文本元素，包括您上传的任何自定义字体。 |
| **[!UICONTROL Elements]** | 添加形状和布局元素，如按钮和矩形。 |

您可以将项目从任何面板直接拖到画布上，也可以单击该项目以将其置于默认位置。

#### 视频广告模板

| 图标 | 描述 |
| --- | --- |
| **[!UICONTROL Search]** | 在库中的所有资产类型中进行搜索。 |
| **[!UICONTROL Upload]** | 将图像、视频、音频或字体文件(TTF、OTF、WOFF、WOFF2)上载到编辑器以便在当前模板中使用。 您一次最多可以上传20个文件。 |
| **[!UICONTROL Templates]** | 从Creative Studio库中浏览广告模板。 |
| **[!UICONTROL My Assets]** | 浏览您在Creative Studio Assets选项卡中上传的所有资源。 |
| **[!UICONTROL Images]** | 仅浏览您在Creative Studio Assets选项卡中上传的图像资源。 |
| **[!UICONTROL Video]** | 仅浏览您在Creative Studio Assets选项卡中上传的视频资源。 |
| **[!UICONTROL Audio]** | 仅浏览您在Creative Studio Assets选项卡中上传的音频资源。 |
| **[!UICONTROL Text]** | 向画布中添加文本元素，包括您上传的任何自定义字体。 |
| **[!UICONTROL Elements]** | 添加形状和矢量元素。 |

您可以将项目从任何面板直接拖到画布上，也可以单击该项目以将其置于默认位置。

### 广告模板编辑控件

单击编辑画布上的元素以将其选定。 根据模板类型，将显示一个或多个包含该元素控件的工具栏。

#### 检查器工具栏和面板

控件因元素类型而异。

<!-- From inspectorbar.ts -->

##### 显示广告模板

| 控件 | 元素类型 | 描述 |
| --- | --- | --- |
| **[!UICONTROL Properties]** | 全部 | 打开面板以编辑图层名称；将图层标记为动态（在广告生成期间可交换）；并设置点进URL（仅限链接）。 在其下方，选择&#x200B;**[!UICONTROL Default]**、**[!UICONTROL Hover]**、**[!UICONTROL Click]**&#x200B;或&#x200B;**[!UICONTROL Focus]**&#x200B;状态以设置该交互状态的元素样式，然后根据元素类型调整样式 — 排版规则（仅限文本和链接）、装饰（填充、边框、圆角半径）、维度、位置。 |
| **[!UICONTROL Effects]** | 全部 | 打开一个面板，从中可选择要将效果应用于该交互状态的&#x200B;**[!UICONTROL Default]**、**[!UICONTROL Hover]**、**[!UICONTROL Click]**&#x200B;或&#x200B;**[!UICONTROL Focus]**&#x200B;状态，然后调整&#x200B;**[!UICONTROL Transform]**、**[!UICONTROL Transition]**、**[!UICONTROL Box Shadow]**、**[!UICONTROL Filter]**、**[!UICONTROL Blend Mode]**&#x200B;和&#x200B;**[!UICONTROL Cursor]**&#x200B;分区。 文本元素还包含&#x200B;**[!UICONTROL Text Shadow]**&#x200B;节。 |
| **[!UICONTROL Animations]** | 全部 | 打开一个面板，以设置图层在时间轴上的进入和退出时间，并通过持续时间和经济缓动配置&#x200B;**[!UICONTROL Entrance Animation]**、**[!UICONTROL Loop Animation]**&#x200B;和&#x200B;**[!UICONTROL Exit Animation]**&#x200B;预设。 包括&#x200B;**[!UICONTROL Copy]**、**[!UICONTROL Paste]**&#x200B;和&#x200B;**[!UICONTROL Reset]**&#x200B;操作。 |
| **[!UICONTROL Crop]** | 图像 | 打开工具栏以裁切图像。 选择&#x200B;**[!UICONTROL Aspect Ratio]**&#x200B;预设（或&#x200B;**[!UICONTROL Free]**），然后单击&#x200B;**[!UICONTROL Apply]**&#x200B;或&#x200B;**[!UICONTROL Cancel]**。 |
| **[!UICONTROL Position]** | 全部 | 打开包含&#x200B;**[!UICONTROL Move]**&#x200B;选项(**[!UICONTROL Forward]**、**[!UICONTROL Backward]**、**[!UICONTROL To front]**、**[!UICONTROL To back]**)、**[!UICONTROL Align to Page]**&#x200B;选项(**[!UICONTROL Top]**、**[!UICONTROL Left]**、**[!UICONTROL Middle]**、**[!UICONTROL Center]**、**[!UICONTROL Bottom]**、**[!UICONTROL Right]**、**[!UICONTROL Fit Vertically]**、**[!UICONTROL Fit Horizontally]**、**[!UICONTROL Fit to Page]**)的菜单，对于非图像元素，打开&#x200B;**[!UICONTROL Layer Level Alignment]**&#x200B;选项（相同的六个对齐选项，加上&#x200B;**[!UICONTROL Fit to Content]**）。 |

##### 视频广告模板

| 控件 | 元素类型 | 描述 |
| --- | --- | --- |
| **[!UICONTROL Shape]** | 形状 | 设置特定于形状的选项。 |
| **[!UICONTROL Group]** / **[!UICONTROL Ungroup]** | 多个选定的元素或组 | 将所选元素组合在一起，或取消选定组的组合。 |
| **[!UICONTROL Combine]** | 兼容的形状 | 将选定的形状组合为单个形状。 |
| **[!UICONTROL Audio replace]** | 音频和视频 | 将音轨替换为资产库中的文件。 |
| **[!UICONTROL Typeface]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, **[!UICONTROL Font size]**, **[!UICONTROL Align horizontal]**, **[!UICONTROL Advanced]** | 文本 | 调整字体系列、粗细、大小、水平对齐和其他高级排版设置。 |
| **[!UICONTROL Image]** / **[!UICONTROL Video]** | 图像和视频 | 设置元素的填充图像或视频源。 |
| **[!UICONTROL Trim]** | 视频和音频 | 打开修剪模式以设置剪辑的起点和终点。 |
| ![卷](/help/creative/assets/volume.png "卷") ([!UICONTROL Volume]) | 视频和音频 | 调整音频级别。 |
| ![播放速度](/help/creative/assets/speed.png "播放速度") ([!UICONTROL Playback speed]) | 视频和音频 | 调整播放速率。 |
| ![裁切](/help/creative/assets/crop.png "裁切") ([!UICONTROL Crop]) | 全部 | 将元素裁剪为自定义区域。 |
| ![笔触](/help/creative/assets/stroke.png "笔触") ([!UICONTROL Stroke]) | 全部 | 设置边框颜色和宽度。 |
| **[!UICONTROL Text Background]** | 文本 | 在文本后面添加背景颜色。 |
| **[!UICONTROL Animations]** | 全部 | 添加或编辑输入、退出或循环动画。 |
| **[!UICONTROL Style]** | 全部 | 打开包含&#x200B;**[!UICONTROL Adjustments]**、**[!UICONTROL Filter]**、**[!UICONTROL Effect]**&#x200B;和&#x200B;**[!UICONTROL Blur]**&#x200B;选项的菜单。 |
| **[!UICONTROL Shadow]** | 全部 | 添加或编辑投影。 |
| **[!UICONTROL Opacity]** | 全部 | 设置元素的透明度级别。 |
| **[!UICONTROL Position]** | 全部 | 按数值调整元素的大小、位置和旋转。 |

#### 常规编辑控件

##### 显示广告模板

| 操作 | 描述 |
| --- | --- |
| **[!UICONTROL Replace]** | （仅限图像元素）打开“图像”面板，以便您可以将图像替换为资源库中的图像。 |
| ![前进](/help/creative/assets/cs-icon-move-forward.png) **[!UICONTROL Move forward]** | 按栈叠顺序将元素向前移动一步（向前移动）。 |
| ![向后移动](/help/creative/assets/cs-icon-move-backward.png) **[!UICONTROL Move backward]** | 按栈叠顺序向后移动元素一步（向后）。 |
| ![重复](/help/creative/assets/cs-icon-duplicate.png) **[!UICONTROL Duplicate]** | 创建元素的副本。 |
| ![删除](/help/creative/assets/cs-icon-delete.png) **[!UICONTROL Delete]** | 从画布中删除元素。 |

您还可以拖动选定元素来重新定位它，并拖动其周围的手柄来调整其大小。

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

您还可以拖动选定元素来重新定位它，并拖动其周围的手柄来调整其大小。

### 时间线

显示和视频编辑器都在画布底部显示一个时间轴面板。

#### 显示广告模板

时间轴显示画布上每个图层的跟踪，该跟踪跨越了根据图层进入和退出动画时间而使其可见的时间范围。 拖动轨道的开始或结束手柄以调整其进入或退出时间，或者拖动轨道以重新排序图层。 单击标尺或拖动播放头以移动到时间点。

时间线工具栏包括&#x200B;**[!UICONTROL Duration]**&#x200B;字段（0-60秒）、**[!UICONTROL Play]**/**[!UICONTROL Pause]**、当前时间/总持续时间显示、循环切换、**[!UICONTROL Timeline Scale]**&#x200B;缩放控件、**[!UICONTROL Fit View]**&#x200B;按钮和折叠/展开切换。

#### 视频广告模板

时间轴显示模板中的所有视频和音频剪辑。 使用时间轴查看剪辑的及时排列方式，并通过拖动剪辑的开始和结束手柄来裁剪剪剪辑。 不能直接在时间轴上添加新剪辑；请改为从左侧面板或画布中添加它，然后它会在时间轴上显示为剪辑。

### [!UICONTROL Layers]面板

画布右侧的[!UICONTROL Layers]面板列出了模板中的所有元素，并允许您管理其顺序、可见性和属性。 对于显示模板，单击画布工具栏中的&#x200B;**[!UICONTROL Open Layers]**&#x200B;以将其打开。 对于视频模板，默认情况下将打开面板。

单击任意层以在画布上选择相应的元素。

**选项卡（仅限显示广告模板）**

显示模板在[!UICONTROL Layers]面板的顶部有两个选项卡：

* **[!UICONTROL Dynamic]** — 仅列出在广告生成期间可以交换的图层，例如AI代理可以替换的图像和文本。 这是生成广告变体的默认视图。
* **[!UICONTROL All]** — 显示模板的完整层层次结构，包括结构容器。 使用此视图可检查或重新组织元素的嵌套方式。

视频模板在一个不含选项卡的列表中显示所有图层。

**每层操作**

将光标悬停在图层上可查看以下操作：

| 操作 | 描述 |
| --- | --- |
| ![重命名图层](/help/creative/assets/edit.png) **[!UICONTROL Rename layer]** | 允许您在面板中输入新图层名称。 |
| ![锁定图层](/help/creative/assets/cs-icon-lock.png) **[!UICONTROL Lock layer]** / ![解锁图层](/help/creative/assets/cs-icon-unlock.png) **[!UICONTROL Unlock layer]** | 防止或允许移动、编辑或重新排序图层。 |
| ![隐藏图层](/help/creative/assets/cs-icon-hidden.png) **[!UICONTROL Hide layer]** / ![显示图层](/help/creative/assets/cs-icon-visible.png) **[!UICONTROL Show layer]** | 隐藏或显示画布上的图层。 隐藏的图层会保留在模板中，但不会在模板渲染时显示。 |
| ![拖动以重新排序](/help/creative/assets/cs-icon-drag.png)拖动以重新排序 | （仅限显示广告模板）拖动重新排序图标可更改图层在栈叠顺序中的位置。 必须解锁该图层才能对其进行重新排序。 |

**面板页脚**

| 操作 | 描述 |
| --- | --- |
| ![复制选定层](/help/creative/assets/cs-icon-duplicate.png) **[!UICONTROL Duplicate selected layer]** | 创建选定图层的副本。 |
| ![删除选定层](/help/creative/assets/cs-icon-delete.png) **[!UICONTROL Delete selected layer]** | 删除所选图层。 |
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

   * 要将模板添加为收藏，请单击![收藏](/help/creative/assets/favorite-null.png)。

   * 要删除作为收藏的模板，请单击![收藏夹](/help/creative/assets/favorite.png)。

## 删除广告模板 {#template-delete}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio].**

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. 将光标悬停在模板卡或表格行上，然后单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Delete]**。

>[!MORELIKETHIS]
>
>* [关于Advertising Creative中的Creative Studio](creative-studio-about.md)
>* [在Creative Studio中管理资源](creative-studio-manage-assets.md)
>* [在Creative Studio中管理标准广告](creative-studio-manage-standard-ads.md)
>* [在Creative Studio中管理动态创意](creative-studio-manage-dynamic-ads.md)

