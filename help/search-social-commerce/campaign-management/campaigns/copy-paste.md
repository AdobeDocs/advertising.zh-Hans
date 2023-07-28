---
title: 使用复制并粘贴功能批量创建和编辑营销活动数据
description: 了解如何使用复制并粘贴功能批量管理Campaign数据。
exl-id: 09454f19-221b-43bb-ac74-f2c121329422
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# 使用复制并粘贴功能批量创建和编辑营销活动数据

*[!DNL Baidu]， [!DNL Google Ads]， [!DNL Microsoft Advertising]， [!DNL Yahoo! Japan Ads]、和 [!DNL Yandex] 仅限帐户*

*[!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 查看次数*

您可以从以下位置复制多达10,000行： [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]， [!UICONTROL Keywords]、和 [!UICONTROL Ads] 视图，并将它们粘贴到 [!DNL Microsoft Excel] 或其他编辑器以编辑任何非ID字段。 然后，您可以复制 [!DNL Excel] 行，并将它们作为制表符分隔的数据粘贴回视图以进行更改。 该功能使用计算机的剪贴板。

您可以使用此功能编辑现有促销活动对象（包含ID字段），并创建不包含ID字段的新促销活动对象。

## 复制数据行

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**.

1. 选中要复制的每一行旁边的复选框。

   您最多可以复制10,000行。

1. 在数据表上方的工具栏中，单击 ![更多](/help/search-social-commerce/assets/more.png "更多")，然后单击 **[!UICONTROL Copy]**.

   或者，您可以使用操作系统的“复制”键盘命令，例如 **[!DNL Ctrl+C]** 对象 [!DNL Microsoft Windows] 或 **[!DNL Command-C]** 对象 [!DNL Apple Mac].

1. 在 [!UICONTROL Copy to Clipboard] 对话框，请单击 **[!UICONTROL Continue]**. 当数据准备复制时，单击 **[!UICONTROL Copy]**.

1. 将行粘贴到 [!DNL Excel] 或者另一位编辑者。

## 编辑和创建数据行

1. 根据以下要求编辑数据：

   * 粘贴的数据必须包含标题行和必要的营销活动对象值；请参阅 [百度](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)， [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)， [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)， [导航](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)， [雅虎！ 显示网络](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)， [雅虎！ 日本](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)、和 [扬代克斯](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). 列顺序无关紧要。

      * 对于要编辑的现有对象，必须包括所有相关的ID列、实体名称和要编辑的属性。 请勿编辑对象的数字ID。

      * 对于新的促销活动对象，请包括所有相关的实体名称和属性，但不包括对象ID（自动生成）。 例如，如果您创建新的广告，则将 [!UICONTROL Ad ID] 字段为空。 发布对象后，广告网络会自动创建一个ID。

   * 任何非必需列中的值都可以为null （空白），但每一行必须具有相同数量的制表符分隔值。

1. 将数据另存为制表符分隔的值。

## 将数据行粘贴到营销活动管理视图中

>[!NOTE]
>
>如果粘贴的行包含与现有实体中的数据相同或复制现有实体的任何数据，则会忽略重复的数据。

1. 在 [!DNL Excel] 或其他编辑器，复制相关的以制表符分隔的行。

1. 在搜索、社交和商务主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 打开要在其中粘贴数据的视图(**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**)。

1. 在数据表上方的工具栏中，单击 ![更多](/help/search-social-commerce/assets/more.png "更多")，然后单击 **[!UICONTROL Paste]**.

   或者，您可以使用操作系统的“粘贴”键盘命令，例如 **[!DNL Ctrl+V]** 对象 [!DNL Microsoft Windows] 或 **[!DNL Command-V]** 对象 [!DNL Apple Mac].

1. 将数据粘贴到输入框中，然后单击 **[!UICONTROL Process]**.

1. （可选）输入其他详细信息：

   * (如果 **[!UICONTROL Additional Details]** 已压缩)单击 ![打开](/help/search-social-commerce/assets/chevron-up.png "打开") 以展开详细信息。

   * 输入可选内容 **[!UICONTROL Job Name]** 和/或可选 **[!UICONTROL Job Description]**.

1. 单击 **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [关于使用批量处理工作表管理营销活动数据](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [直接在行中编辑设置](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [管理营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [管理广告组](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [管理关键字](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [管理广告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
