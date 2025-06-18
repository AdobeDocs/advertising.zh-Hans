---
title: 为实时体验导出和实施广告体验标记
description: 了解如何导出广告体验标记并（可选）将其上传到Advertising DSP营销活动。
feature: Creative Experiences
exl-id: 4ae05142-8319-4329-96d7-f87d77f02745
source-git-commit: 41763b21bda47e8bd45f48c18a674cd694df68d1
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# 为实时体验导出和实施广告体验标记

*已关闭的测试版*

特定创意大小的广告标记可用于[实时](experience-about.md#experience-statuses)体验后，您便可以生成并复制JavaScript和iframe格式的标记，以便在Advertising DSP或其他DSP上实施。 DSP的标记包括DSP所需的所有宏。

使用Advertising DSP的广告商可以选择将标记作为广告直接上传到Advertising DSP促销活动。

>[!NOTE]
>
>* 当您使用决策树定位创建体验时，[!DNL Creative]会自动为每个适用的创意大小创建广告标记。
>* 当您创建没有决策树定位的体验时，必须为每种适用的创意大小[手动创建广告标记](experience-tag-create-manually.md)。
>* 体验标记是动态的。 如果您编辑体验，则无需更新标记。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**。

1. 执行以下操作之一：<!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * 在卡片视图中，单击体验名称旁边的&#x200B;**[!UICONTROL ...]**，然后单击&#x200B;**[!UICONTROL Tag Manager]**。

   * 在表格视图中，将光标悬停在行上，单击&#x200B;**[!UICONTROL More]**，然后单击&#x200B;**[!UICONTROL Tag Manager]**

1. 将光标悬停在适用的广告标记的行上，然后单击![导出广告标记](/help/creative/assets/export.png "导出广告标记") **[!UICONTROL Export ad tags]**&#x200B;或&#x200B;**[!UICONTROL ... More] > &#x200B;** [!UICONTROL Export ad tags]**。

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. （可选）在[!UICONTROL Macros]选项卡上，指定最多五个要包含在标记中的自定义宏。 对于要包含的每个宏：

   1. 选中复选框。<!-- Explain more -->

   1. 输入自定义宏。<!-- Explain more -->

1. 单击右上角的&#x200B;**[!UICONTROL Next]**&#x200B;或单击左侧菜单中的&#x200B;**[!UICONTROL Generate ad tags]**。

1. 选择标记类型： ** *JavaScript<!-- sic -->* **或** *IFRAME* ** <!-- sic -->。

1. 在[!UICONTROL Destinations]列表中，选择要为体验创建广告的位置。

   * *通用：*&#x200B;对于您将在其他DSP中创建的广告。 **注意：**&#x200B;您可能需要根据需要手动包含[其他宏](/help/creative/creative-macros.md)。

   * *Adobe AdCloud：*&#x200B;对于您将在Advertising DSP中创建的广告。

   * *Google CM360：*&#x200B;对于您将在[!DNL Google Campaign Manager 360]中创建的广告。 **注意：**&#x200B;您可能需要根据需要手动包含[其他宏](/help/creative/creative-macros.md)。

1. 单击&#x200B;**[!UICONTROL Generate tags]**。

1. 复制或下载标记：

   * 若要复制单个广告大小的标记，请展开标记行，将光标悬停在该行上，然后单击![复制](/help/creative/assets/copy.png "复制") **[!UICONTROL Copy]**。<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->

   * 要将所有生成的标记作为文件下载到浏览器的默认下载位置，请单击![下载标记](/help/creative/assets/download.png "下载标记")。

   您可以在文本编辑器中打开文件以复制每个标记。 对于JavaScript标记，该标记包含在`<script></script>`和`<noscript></noscript>`标记中。 对于iframe标记，该标记包含在`<iframe></iframe>`标记中。

1. 实施相关DSP的标记：

   * 对于Advertising DSP以外的DSP，将标记提供给将在DSP中创建广告的用户。

   * 对于Advertising DSP：

      1. 单击右上角的&#x200B;**[!UICONTROL Next]**&#x200B;或单击左侧菜单中的&#x200B;**[!UICONTROL DSP link]**。

      1. 选择要将广告标记上传到的营销策划。

      1. 单击&#x200B;**[!UICONTROL Assign Tags]**。

         DSP将打开以显示选定营销活动的[!UICONTROL Ads]视图。

      1. 在[!UICONTROL Create ads]视图中，查看广告标记，选择要为其创建广告的每个标记，然后单击&#x200B;**[!UICONTROL Create]**。

         [!UICONTROL Ads]视图现在包含与[!DNL Creative]中的广告标记具有相同名称的新广告。 您可以[将广告附加到营销活动中的任何投放位置](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)。

<!-- no way to get back to the Creative Tag Manager -- you have to click back through the main menu -->

<!-- Add this info, with descriptions:

## Ad tag formats

### JavaScript

### Iframe

-->

>[!MORELIKETHIS]
>
>* [为适用的创意大小手动创建广告标签](experience-tag-create-manually.md)
>* [将创意内容分配给无定位体验的广告标记](experience-tag-assign-creatives.md)
>* [重命名广告标记](experience-tag-rename.md)
