---
title: 使用人工智能从图像生成广告模板
description: 了解如何在Creative Studio中使用AI将现有的静态显示广告图像转换为可编辑的广告模板。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: adc2fdc93f06b5459c19b08306d1e30ce00e7028
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%
---
# 使用人工智能从图像生成广告模板

*Beta功能*

在[!UICONTROL Creative Studio]中使用AI将现有的静态显示广告图像转换为可编辑的显示广告模板。 查看生成的模板，使用自然语言请求更改，然后打开模板编辑器以进行手动更改并保存模板。

## 开始之前

您需要在Creative库中包含一个现有的静态图像广告。 此工作流从库中选择广告；它不会直接在“生成”对话框中上传新图像。

## 生成并查看模板 {#template-generate}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Creative Studio]**。

1. 单击&#x200B;**[!UICONTROL Templates]**&#x200B;选项卡。

1. （可选）从页面顶部的广告商列表中选择一个广告商，以查看该广告商的库。

1. 在&#x200B;**[!UICONTROL Use AI to Generate a New Display Ad Template]**&#x200B;框中，单击&#x200B;**[!UICONTROL Generate]**。

1. 在&#x200B;**[!UICONTROL Generate New Ad Template]**&#x200B;对话框中，选择&#x200B;**[!UICONTROL Generate from Existing Standard Ad Image]**（如果尚未选择）。

1. 从&#x200B;**[!UICONTROL Ad Library]**&#x200B;列表中选择包含图像广告的库。

1. 将光标悬停在图像广告卡上并单击&#x200B;**[!UICONTROL Use this Standard Ad]**。

   使用选定广告的宽度和高度，自动开始生成。

1. 等待生成完成，然后查看模板预览和&#x200B;**[!UICONTROL Layers]**&#x200B;面板（如果可用）。

   在使用模板之前，请检查文本、图像和布局。 此处显示的层供审阅；请在模板编辑器中手动进行更改。

1. （可选）请求对生成的模板进行更改：

   1. 在&#x200B;**[!UICONTROL Ask the AI for any changes]**&#x200B;字段中，描述所需的更改。 例如，输入`Change the headline to "Limited Time Offer" and the button text to "Shop Now"`。

   1. 单击&#x200B;**[!UICONTROL Regenerate]**。

   1. 查看更新的预览。 根据需要重复执行上述步骤。

1. 准备好继续时，单击&#x200B;**[!UICONTROL Use this Ad Template]**。

   生成的模板将在显示模板编辑器中打开。

## 编辑并保存模板 {#template-save}

1. 在模板编辑器中，查看生成的元素，并使用[模板编辑器控件](creative-studio-manage-templates.md#template-controls)进行任何剩余的更改。

1. 单击&#x200B;**[!UICONTROL Save]**。

1. 在&#x200B;**[!UICONTROL Update Template]**&#x200B;对话框中，输入或更新&#x200B;**[!UICONTROL Template name]**，选择&#x200B;**[!UICONTROL Advertiser]**，并选择性地添加标记。

1. 单击&#x200B;**[!UICONTROL Update]**&#x200B;保存模板并返回&#x200B;**[!UICONTROL Templates]**&#x200B;视图。

   若要改为保存单独的副本，请单击&#x200B;**[!UICONTROL Save As New]**。

然后，您可以使用该模板[生成广告变体](creative-studio-manage-templates.md#ad-variations-generate)。

## 如果您无法生成模板 {#troubleshooting}

* **未列出任何库或图像广告：**&#x200B;请检查所选的广告商和&#x200B;**[!UICONTROL Ad Library]**。 如果库没有标准广告图像，请选择另一个包含现有静态图像广告的库。

* **生成失败或无法转换图像：**&#x200B;请检查显示的消息，单击&#x200B;**[!UICONTROL Back to library]**，然后选择一个图像广告重试。

>[!MORELIKETHIS]
>
>* [在Creative Studio中管理广告模板](creative-studio-manage-templates.md)
>* [在Creative Studio中管理标准广告](creative-studio-manage-standard-ads.md)