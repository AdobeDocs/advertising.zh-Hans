---
title: 动态创意设置
description: 引用动态创意的设置。
feature: Creative Dynamic Creatives
exl-id: 9dcd7245-fa02-4082-9abb-8c0792322a68
source-git-commit: 164ee92f85c0e649dc2bd6c0224a531eb72d1962
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# 动态创意设置

<!-- add a description -->

## 动态广告设置<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### 基本详细信息

**[!UICONTROL Creative Type]：**&#x200B;创意内容是&#x200B;*[!UICONTROL Display]*&#x200B;广告(HTML5)还是&#x200B;*[!UICONTROL Video]*&#x200B;广告。

**[!UICONTROL Dynamic Display Ad Name]**&#x200B;或&#x200B;**[!UICONTROL Dynamic Video Ad Name]：**&#x200B;创意的唯一名称。

**[!UICONTROL Advertiser]：**&#x200B;要为其创建广告的广告商。 如果您是从[!UICONTROL Creatives] > [!UICONTROL Creative Libraries]内创建广告，则已选择该广告商且为只读。

**[!UICONTROL Library]：**&#x200B;要在其中创建广告的创意库。 如果您是从[!UICONTROL Creatives] > [!UICONTROL Creative Libraries]中创建广告，则库名称已被选择且为只读。

## 广告模板

**[!UICONTROL Ad Template]：**&#x200B;从中创建广告的广告模板。 选择现有的广告模板，或上传新的广告模板并选择模板类型（*静态*&#x200B;或&#x200B;*动态*）。 模板必须为ZIP格式并包含：<!-- Need to add more specs for templates -->

* 显示创意：具有所需广告格式的HTML5文件，以及具有广告属性(.tdf)的文件(仅限动态HTML5广告)

* 视频创意：具有所需广告格式的.scene文件。 ZIP文件最大可以为512 MB。

要继续，请单击&#x200B;**[!UICONTROL Select Ad Template]**。

**[!UICONTROL Size]：** （仅限动态显示广告；只读）用于创建广告的所选广告模板的[广告维度](/help/creative/creative-libraries/creative-sizes.md)。

**[!UICONTROL Card Count (Max 50)]：** （仅限显示广告）轮播中显示的产品数。

**[!UICONTROL Duration]：** （仅限视频广告；只读）从所选广告模板派生的视频持续时间。 每个视频的持续时间必须介于1至90秒之间。

## 目录

**\[目录\]**：要从中生成广告的一个或多个目录。 选择现有目录，或通过下载现有信息源模板并创建和上传新目录来创建新目录。 单击&#x200B;**[!UICONTROL Select Catalog]**。

上传的目录必须采用ZIP格式并包含以下内容：

* （动态显示和视频广告）CSV、TSV或Microsoft Excel电子表格(XLSX)格式的一个或多个馈送文件。 最大文件大小为512 MB。<!-- Need to add more specs for the feed files -->

* （显示广告）GIF、JPEG、JPG或PNG格式的图像资源

* （视频广告）MP4、MOV或WEBM格式的视频资产。 支持的广告模板包括开始卡、结束卡、顶部叠加、底部叠加或L形。 每个视频的持续时间必须介于1至90秒之间。

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**： <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->馈送文件中必须存在值以创建广告的列的类型： *[!UICONTROL Profile data]*、*[!UICONTROL Geographic data]、*[!UICONTROL Data pass]、*[!UICONTROL Audience Segment]*。  **注意：**&#x200B;这些设置独立于广告体验设置中的高级设置工作。<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]：**

将指定广告模板中的每个属性（动态广告字段）映射到指定目录（目录标签）中的列或输入静态值。

>[!MORELIKETHIS]
>
>* [将动态创意添加到创意库](creative-add-dynamic.md)
>* [在创意库中编辑动态创意内容](creative-edit-dynamic.md)
>* [动态广告的工作流](/help/creative/introduction/workflow-dynamic-ads.md)
