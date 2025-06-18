---
title: 管理URL
description: 了解如何创建和管理用于投放定位的URL列表。
feature: DSP Placements
source-git-commit: ea33d6fa7612f1c9631c223e5bf0ec80bb5f8d96
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---

# 管理URL

您可以创建和管理用于投放定位的网站和应用程序URL列表。 在投放设置中定位或排除特定URL列表。

## 查看URL列表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Resources]** > **[!UICONTROL URL Lists]**。

1. 单击列表名称。

1. （可选）要将所选列表导出为XLSX （[!DNL Microsoft Excel]电子表格）格式，请单击![导出](/help/dsp/assets/export.png "导出") **[!UICONTROL Export]**。

   将按照浏览器的正常过程下载文件。

## 创建URL列表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Resources]** > **[!UICONTROL URL Lists]**。

1. 单击右上角的&#x200B;**[!UICONTROL Create].**

1. 输入&#x200B;**[!UICONTROL List name]**，然后单击&#x200B;**[!UICONTROL Create].**

1. 执行以下任一操作：

   * 要手动输入或粘贴要添加的URL，请执行以下操作：

      1. 单击&#x200B;**[!UICONTROL Bulk Add URLs]** > **[!UICONTROL Copy/Paste URLs]**。

      1. 输入或粘贴最多10,000个URL，每个URL单独占一行。

      1. 单击&#x200B;**[!UICONTROL Validate]**&#x200B;以验证URL是否有效。

         已识别任何无效的URL。 如果继续，则仅添加有效的URL。

      1. 单击&#x200B;**[!UICONTROL Add to list]**。

   * 从文件添加URL：

      1. 单击&#x200B;**[!UICONTROL Bulk Add URLs]** > **[!UICONTROL Import File]**。

      1. 拖放一个包含URL的本地CSV文件，其中每个URL都位于单独的一行中。

         文件应仅包含一个数据列，不包含列标题行。 如果导出现有列表并编辑了行，请在重新导入文件之前删除标题行以及第二和第三列。 如果继续，将不会添加任何具有无效值的行。

      1. 单击&#x200B;**[!UICONTROL Add to list]**。

         通知消息指示任务何时完成。 刷新页面以查看更新的列表。

      1. 要查看任务状态（包括添加的URL数和失败值的数量），请执行以下操作：

         1. 单击顶部菜单栏右侧的![作业](/help/dsp/assets/downloads.png)。

         1. （如果未添加任何行）要下载包含失败值的错误文件，请单击作业旁边的&#x200B;**[!UICONTROL Download]**。

            该文件将保存到浏览器的“下载”文件夹中。

   * 要删除特定URL，请执行以下任一操作：

      * 选择要删除的URL：

         1. 选中要从列表中删除的每个交易旁边的复选框。

         1. 单击&#x200B;**[!UICONTROL Remove from List]**。

         1. 在确认消息中，单击&#x200B;**[!UICONTROL Remove]**。

      * 要输入或粘贴要删除的URL，请执行以下操作：

         1. 单击&#x200B;**[!UICONTROL Bulk Remove URLs]** > **[!UICONTROL Copy/Paste URLs]**。

         1. 输入或粘贴最多10,000个URL，每个URL单独占一行。

         1. 单击&#x200B;**[!UICONTROL Validate]**&#x200B;以验证URL是否有效以及当前是否包含在列表中。

         1. 单击&#x200B;**[!UICONTROL Remove from list]**。

   * 要删除所有URL，请执行以下操作：

      1. 单击&#x200B;**[!UICONTROL Bulk Remove URLs]** > **[!UICONTROL Copy/Paste URLs]**。

      1. 单击&#x200B;**[!UICONTROL Remove All URLs]**。

      1. 单击&#x200B;**[!UICONTROL Remove]**。

## 编辑URL列表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Resources]** > **[!UICONTROL URL Lists]**。

1. 单击列表名称。

1. 执行以下任一操作：

   * 要手动输入或粘贴要添加的URL，请执行以下操作：

      1. 单击&#x200B;**[!UICONTROL Bulk Add URLs]** > **[!UICONTROL Copy/Paste URLs]**。

      1. 输入或粘贴最多10,000个URL，每个URL单独占一行。

      1. 单击&#x200B;**[!UICONTROL Validate]**&#x200B;以验证URL是否有效。

         已识别任何无效的URL。 如果继续，则仅添加有效的URL。

      1. 单击&#x200B;**[!UICONTROL Add to list]**。

   * 从文件添加URL：

      1. 单击&#x200B;**[!UICONTROL Bulk Add URLs]** > **[!UICONTROL Import File]**。

      1. 拖放一个包含URL的本地CSV文件，其中每个URL都位于单独的一行中。

         文件应仅包含一个数据列，不包含列标题行。 如果导出现有列表并编辑了行，请在重新导入文件之前删除标题行以及第二和第三列。 如果继续，将不会添加任何具有无效值的行。

      1. 单击&#x200B;**[!UICONTROL Add to list]**。

         通知消息指示任务何时完成。

      1. 要查看任务状态（包括添加的URL数和失败值的数量），请执行以下操作：

         1. 单击顶部菜单栏右侧的![作业](/help/dsp/assets/downloads.png)。

         1. （如果未添加任何行）要下载包含失败值的错误文件，请单击作业旁边的&#x200B;**[!UICONTROL Download]**。

            该文件将保存到浏览器的“下载”文件夹中。

   * 要删除特定URL，请执行以下任一操作：

      * 选择要删除的URL：

         1. 选中要从列表中删除的每个交易旁边的复选框。

         1. 单击&#x200B;**[!UICONTROL Remove from List]**。

         1. 在确认消息中，单击&#x200B;**[!UICONTROL Remove]**。

      * 要输入或粘贴要删除的URL，请执行以下操作：

         1. 单击&#x200B;**[!UICONTROL Bulk Remove URLs]** > **[!UICONTROL Copy/Paste URLs]**。

         1. 输入或粘贴最多10,000个URL，每个URL单独占一行。

         1. 单击&#x200B;**[!UICONTROL Validate]**&#x200B;以验证URL是否有效以及当前是否包含在列表中。

         1. 单击&#x200B;**[!UICONTROL Remove from list]**。

   * 要删除所有URL，请执行以下操作：

      1. 单击&#x200B;**[!UICONTROL Bulk Remove URLs]** > **[!UICONTROL Copy/Paste URLs]**。

      1. 单击&#x200B;**[!UICONTROL Remove All URLs]**。

      1. 单击&#x200B;**[!UICONTROL Remove]**。

## 导出URL列表

1. 在主菜单中，单击&#x200B;**[!UICONTROL Resources]** > **[!UICONTROL URL Lists]**。

1. 单击列表名称。

1. 单击![导出](/help/dsp/assets/export.png "导出") **[!UICONTROL Export]**。

   根据浏览器的正常过程，以XLSX （[!DNL Microsoft Excel]电子表格）格式下载该文件。

>[!MORELIKETHIS]
>
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
>* [关于帐户级别和广告商级别的阻止网站列表](/help/dsp/admin/blocked-sites-list-about.md)
>* [编辑帐户级别或广告商级别的阻止站点列表](/help/dsp/admin/blocked-sites-list-edit.md)
