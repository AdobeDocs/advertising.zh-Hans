---
title: 将广告附加到投放位置
description: 了解如何将广告附加到投放位置。
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
source-git-commit: 86acfaecdf761adc7c6585a49dbcdf4490290a8c
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# 将广告附加到投放位置

使用[!UICONTROL Ad Tools]视图可将广告附加到投放位置，将第三方跟踪像素附加到广告，并将现有的第三方跟踪像素与广告分离。

>[!NOTE]
>
>通用视频广告只能附加到通用视频投放位置。

## 打开[!UICONTROL Ad Tools]视图 {#ad-tools-open}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击营销活动的名称。

1. 通过以下任一方式打开[!UICONTROL Ad Tools]视图：

   * （从[!UICONTROL Packages] 、 [!UICONTROL Placements]或[!UICONTROL Ads]视图）在右上角，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Ad Tools]**。

   * （从[!UICONTROL Placements]视图中）在投放位置名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Attach Ads]。**

   * （从[!UICONTROL Ads]视图中）在广告名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Add to Placements]**。

   默认情况下选择[!UICONTROL Attach Ads]选项卡。

## 将广告附加到投放位置 {#attach-ads-campaign}

1. [打开[!UICONTROL Ad Tools]视图](#ad-tools-open)。

1. 在[!UICONTROL Edit]子视图中，对要附加到投放位置的每个广告组执行以下操作：

   1. （可选）通过以下任意方式查找特定投放位置和广告：

      * 在左表上方单击![筛选器](/help/dsp/assets/filter.png)，并按包、版面类型、版面状态、广告类型或广告状态筛选列表。

      * 在右表和左表的上方，搜索版面和广告名称中的特定文本字符串。

   1. 在左表中，选中每个要向其附加广告的版面旁边的复选框。

   1. 在右侧表格中，选中要附加到所选投放位置的每个广告旁边的复选框。

      只有适用于投放类型且尚未附加到所选投放位置的广告才可选择。

   1. 单击右下角的&#x200B;**[!UICONTROL Attach]**。

1. （可选）要返回到营销活动详细信息视图，请单击![返回到文件夹](/help/dsp/assets/breadcrumb-return.png "返回到文件夹[!UICONTROL Ad Tools]左侧的文件夹")，然后选择营销活动名称。

## 查看附加到投放位置的广告 {#view-ads-campaign}

<!-- should be a separate page, combined with "List the Placements Associated with an Ad" (although that pertains to a single ad only), or maybe just rename this topic -->

1. [打开[!UICONTROL Ad Tools]视图](#ad-tools-open)。

1. 切换到右上角的&#x200B;**[!UICONTROL View]**&#x200B;选项。

1. （可选）根据需要查找特定投放位置和广告：

   * 在左表上方单击![筛选器](/help/dsp/assets/filter.png)，并按包、版面类型、版面状态、广告类型或广告状态筛选列表。

   * 在右侧和左侧表格中，搜索版面或广告名称中的特定文本字符串。

1. 单击左侧表中的任意版面行可查看右侧表中的附加广告。

1. （可选）要将更多广告附加到营销活动的投放位置，请切换到右上角的&#x200B;**[!UICONTROL Edit]**&#x200B;视图。 有关说明，请参阅上一过程中的步骤2“[将广告附加到投放位置](#attach-ads-campaign)”。

## 将第三方跟踪像素附加到投放位置中的广告 {#attach-pixels-ads}

1. [打开[!UICONTROL Ad Tools]视图](#ad-tools-open)。

1. 单击&#x200B;**[!UICONTROL Attach Pixels]**&#x200B;选项卡。

1. 在[!UICONTROL Edit]子视图中：

   1. （可选）通过以下任意方式查找广告和第三方像素：

      * 在左表上方，单击![过滤器](/help/dsp/assets/filter.png)并按广告状态、广告类型、像素集成事件或像素类型过滤列表。

      * 在右表和左表的上方，搜索广告名称和像素名称中的特定文本字符串。

   1. （如果营销活动不存在第三方跟踪像素）创建像素：

      1. 在右表中，单击&#x200B;**[!UICONTROL Create pixel]**。

      1. 指定设置：

         **[!UICONTROL Integration Event]：**&#x200B;触发像素触发的事件，如&#x200B;*[!UICONTROL Impression]*&#x200B;或&#x200B;*[!UICONTROL Click-through]*。

         **[!UICONTROL Pixel Type]：**&#x200B;像素是&#x200B;*[!UICONTROL IMG URL]* （1x1像素图像文件）、*[!UICONTROL HTML]*&#x200B;还是&#x200B;*[!UICONTROL JavaScript URL]*。

         **[!UICONTROL Pixel URL or Code]：**&#x200B;像素图像的URL，采用指定像素类型的相应格式。

         **[!UICONTROL Pixel Name]：**&#x200B;像素名称。 使用有助于您轻松识别像素的名称。

         **[!UICONTROL Pixel Provider]：**&#x200B;像素提供程序： *[!UICONTROL None]*、*[!UICONTROL Comscore]*、*[!UICONTROL WhiteOps]*&#x200B;或&#x200B;*[!UICONTROL IAS]*。

      1. 单击&#x200B;**[!UICONTROL Save]**。

   1. 在左表中，选中要附加第三方跟踪像素的每个广告旁边的复选框。

   1. 在右侧表格中，选中要附加到所选广告的每个第三方跟踪像素旁边的复选框。

      只有尚未附加到选定广告的像素才是可选的。

   1. 单击右下角的&#x200B;**[!UICONTROL Attach]**。

1. （可选）要返回到营销活动详细信息视图，请单击![返回到文件夹](/help/dsp/assets/breadcrumb-return.png "返回到文件夹[!UICONTROL Ad Tools]左侧的文件夹")，然后选择营销活动名称。

## 将第三方跟踪像素与投放位置中的广告分离 {#detach-pixels-ads}

1. [打开[!UICONTROL Ad Tools]视图](#ad-tools-open)。

1. 单击&#x200B;**[!UICONTROL Attach Pixels]**&#x200B;选项卡。

1. 在[!UICONTROL Edit]子视图中：

   1. （可选）通过以下任意方式查找广告和第三方像素：

      * 在左表上方，单击![过滤器](/help/dsp/assets/filter.png)并按广告状态、广告类型、像素集成事件或像素类型过滤列表。

      * 在右表和左表的上方，搜索广告名称和像素名称中的特定文本字符串。

   1. 在左侧表格中，选中要从中分离第三方跟踪像素的每个广告旁边的复选框。

   1. 在右侧表格中，选中要与所选广告分离的每个第三方跟踪像素旁边的复选框。

      只有附加到所有选定广告的像素才是可选的。

   1. 单击右下角的&#x200B;**[!UICONTROL Detach]**。

1. （可选）要返回到营销活动详细信息视图，请单击![返回到文件夹](/help/dsp/assets/breadcrumb-return.png "返回到文件夹[!UICONTROL Ad Tools]左侧的文件夹")，然后选择营销活动名称。

## 查看附加到广告的像素 {#view-pixels-ads}

1. [打开[!UICONTROL Ad Tools]视图](#ad-tools-open)。

1. 单击&#x200B;**[!UICONTROL Attach Pixels]**&#x200B;选项卡。

1. 切换到右上角的&#x200B;**[!UICONTROL View]**&#x200B;选项。

1. （可选）根据需要查找广告和第三方像素：

   * 在左表上方，单击![过滤器](/help/dsp/assets/filter.png)并按广告状态、广告类型、像素集成事件或像素类型过滤列表。

   * 在右表和左表的上方，搜索广告名称和像素名称中的特定文本字符串。

1. 单击左侧表中的任意广告行可查看右侧表中的附加像素。

1. （可选）要将更多像素附加到广告，请切换到右上角的&#x200B;**[!UICONTROL Edit]**&#x200B;视图。 有关说明，请参阅上一过程中的步骤3“[将第三方跟踪像素附加到投放位置](#attach-pixels-ads)中的广告”。

>[!MORELIKETHIS]
>
>* [关于广告管理](ad-about.md)
>* [创建单个Ad](ad-create.md)
>* [创建多个第三方广告](ad-create-multiple.md)
>* [编辑广告](ad-edit.md)
>* [列出与广告关联的版面](ad-list-placements.md)
>* [编辑投放位置的广告计划](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* 有关通用视频的[常见问题解答](/help/dsp/campaign-management/faq-universal-video.md)
