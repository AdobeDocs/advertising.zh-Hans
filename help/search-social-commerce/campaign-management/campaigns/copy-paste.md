---
title: 使用复制并粘贴功能批量创建和编辑营销活动数据
description: 了解如何使用复制并粘贴功能批量管理Campaign数据。
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# 使用复制并粘贴功能批量创建和编辑营销活动数据

仅&#x200B;*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads]、[!DNL Yandex]和现有[!DNL Baidu]帐户*

*[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]次查看*

您可以从[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]和[!UICONTROL Ads]视图中复制多达10,000行，并将其粘贴到[!DNL Microsoft Excel]或其他编辑器中，以编辑任何非ID字段。 然后，您可以复制[!DNL Excel]行并将它们作为制表符分隔的数据粘贴回视图以进行更改。 该功能使用计算机的剪贴板。

您可以使用此功能编辑现有促销活动对象（包含ID字段），并创建不包含ID字段的新促销活动对象。

## 复制数据行

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**。

1. 选中要复制的每一行旁边的复选框。

   您最多可以复制10,000行。

1. 在数据表上方的工具栏中，单击![更多](/help/search-social-commerce/assets/more.png "更多")，然后单击&#x200B;**[!UICONTROL Copy]**。

   或者，您可以使用操作系统的“复制”键盘命令，如[!DNL Microsoft Windows]的&#x200B;**[!DNL Ctrl+C]**&#x200B;或[!DNL Apple Mac]的&#x200B;**[!DNL Command-C]**。

1. 在[!UICONTROL Copy to Clipboard]对话框中，单击&#x200B;**[!UICONTROL Continue]**。 当数据准备复制时，单击&#x200B;**[!UICONTROL Copy]**。

1. 将行粘贴到[!DNL Excel]或其他编辑器中。

## 编辑和创建数据行

1. 根据以下要求编辑数据：

   * 粘贴的数据必须包含标题行和必要的营销活动对象值；请查看[百度](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)、[Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)、[Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)、[Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)、[Yahoo！所需的批量工作表列 显示网络](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)，[Yahoo！ 日本](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)和[Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md)。 列顺序无关紧要。

      * 对于要编辑的现有对象，必须包括所有相关的ID列、实体名称和要编辑的属性。 请勿编辑对象的数字ID。

      * 对于新的促销活动对象，请包括所有相关的实体名称和属性，但不包括对象ID（自动生成）。 例如，如果您创建新广告，请将[!UICONTROL Ad ID]字段留空。 发布对象后，广告网络会自动创建一个ID。

   * 任何非必需列中的值都可以为null （空白），但每一行必须具有相同数量的制表符分隔值。

1. 将数据另存为制表符分隔的值。

## 将数据行粘贴到营销活动管理视图中

>[!NOTE]
>
>如果粘贴的行包含与现有实体中的数据相同或复制现有实体的任何数据，则会忽略重复的数据。

1. 在[!DNL Excel]或其他编辑器中，复制相关的制表符分隔行。

1. 在“搜索、社交和Commerce”主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 打开粘贴数据的视图(**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**)。

1. 在数据表上方的工具栏中，单击![更多](/help/search-social-commerce/assets/more.png "更多")，然后单击&#x200B;**[!UICONTROL Paste]**。

   或者，您可以使用操作系统的“粘贴”键盘命令，例如[!DNL Microsoft Windows]的&#x200B;**[!DNL Ctrl+V]**&#x200B;或[!DNL Apple Mac]的&#x200B;**[!DNL Command-V]**。

1. 将数据粘贴到输入框中，然后单击&#x200B;**[!UICONTROL Process]**。

1. （可选）输入其他详细信息：

   * （如果&#x200B;**[!UICONTROL Additional Details]**&#x200B;已压缩）单击![打开](/help/search-social-commerce/assets/chevron-up.png "打开")以展开详细信息。

   * 输入可选的&#x200B;**[!UICONTROL Job Name]**&#x200B;和/或可选的&#x200B;**[!UICONTROL Job Description]**。

1. 单击&#x200B;**[!UICONTROL Post Now]**。


>[!MORELIKETHIS]
>
>* [关于使用批量处理工作表管理营销活动数据](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [直接在行中编辑设置](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [管理营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [管理广告组](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [管理关键字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [管理广告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
