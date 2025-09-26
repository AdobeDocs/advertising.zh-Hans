---
title: 动态创意设置
description: 引用动态创意的设置。
feature: Creative Dynamic Creatives
source-git-commit: 31651c4e30d22b4d1639ef3fc05d5ff9e02dd040
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# 动态创意设置

<!-- add a description -->

<!-- This looks the same for me for either HTML5 type as of 9/24:

## Dynamic ad settings for static HTML5 ads {#dynamic-ad-settings-static-html5}

### Basic Details

**[!UICONTROL Advertiser]:** The advertiser for which to create the ads.

**[!UICONTROL Library]:** The creative library in which to create the ads.

**[!UICONTROL Dynamic Ad Name]:** A unique name for the creative.

**[!UICONTROL Ad Template Size]:** The ad dimensions for the ad template from which to create the ad. If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template Type]:** The type of ad template from which to create the ad: *[!UICONTROL Static HTML5]* or *[!UICONTROL Dynamic HTML5]*.  If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template]:** The ad template from which to create the ad.

**[!UICONTROL clickURL]:** A valid landing page URL to which users are redirected when they click the ad.

### [!UICONTROL Attributes Details]

-->

## 动态广告设置<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### 基本详细信息

**[!UICONTROL Dynamic Ad Name]：**&#x200B;创意的唯一名称。

**[!UICONTROL Advertiser]：**&#x200B;要为其创建广告的广告商。

**[!UICONTROL Library]：**&#x200B;要在其中创建广告的创意库。 如果您是从[!UICONTROL Creatives] > [!UICONTROL Creative Libraries]中创建广告，则库名称已被选择且为只读。

**[!UICONTROL Ad Template Size]：**&#x200B;从中创建广告的广告模板的[广告维度](/help/creative/creative-libraries/creative-sizes.md)。 如果您首先选择特定的[!UICONTROL Ad Template]，则会自动选择此值。

## 广告模板

**[!UICONTROL Ad Template]：**&#x200B;从中创建广告的广告模板。 选择现有的广告模板，或上传新的广告模板并选择模板类型（*静态*&#x200B;或&#x200B;*动态*）。 上载的模板必须采用ZIP格式，并包含HTML5文件和模板定义文件(template.TDF)。<!-- Need to add more specs for that -->

**[!UICONTROL Number of offers (Max 50)]：**&#x200B;轮播中要显示的产品数。

## 目录

**[!UICONTROL Template]：**&#x200B;用于创建广告的信息源模板。

**\[目录\]**：要从中生成广告的一个或多个目录。 选择现有目录，或通过下载现有信息源模板并创建和上传新目录来创建新目录。

上传的目录必须采用ZIP格式并包含以下内容：

* CSV、TSV或Microsoft Excel电子表格(XLSX)格式的一个或多个信息源文件。<!-- Need to add more specs for that -->

* GIF、JPEG、JPG或PNG格式的图像资源

* （可选）MP4或WEBM格式的视频资产

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**： <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->馈送文件中必须存在值以创建广告的列的类型： *[!UICONTROL Profile data]*、*[!UICONTROL Geographic data]、*[!UICONTROL Data pass]、*[!UICONTROL Audience Segment]*。  **注意：**&#x200B;这些设置独立于广告体验设置中的高级设置工作。<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]：**

将指定广告模板中的每个属性（动态广告字段）映射到指定目录（目录标签）中的列或输入静态值。

>[!MORELIKETHIS]
>
>* [将动态创意添加到创意库](creative-add-dynamic.md)
>* [在创意库中编辑动态创意内容](creative-edit-dynamic.md)
>* [动态广告的工作流](/help/creative/introduction/workflow-dynamic-ads.md)
