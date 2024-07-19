---
title: 管理 [!DNL Google Ads] 动态搜索目标
description: 了解如何创建和管理 [!DNL Google Ads] 动态搜索目标。
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# 管理[!DNL Google Ads]动态搜索目标

仅&#x200B;*[!DNL Google Ads]个帐户*

您可以为使用搜索网络的营销活动创建、编辑和更改动态搜索目标的状态。

>[!NOTE]
>
>您可以通过上传[批量工作表文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)并将它们发布到广告网络，同时创建和编辑大量目标数据。

## 创建[!DNL Google Ads]动态搜索目标

您可以创建动态搜索目标来定义网站中的页面（即广告显示URL中使用的域），这些页面的内容用于定位同一广告组中的动态搜索广告。

您可以定位所有标准或最多三个单独的标准。

>[!NOTE]
>
>要最佳跟踪性能，请为每个营销活动仅创建一个广告组的&quot;[!UICONTROL All Targets]&quot;目标。

>[!TIP]
>
>若要同时创建多个帐户组件，请使用[营销活动批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]>[!UICONTROL Auto Targets]**。

1. 在数据表上方的工具栏中，单击![创建](/help/search-social-commerce/assets/add.png "创建")。

1. 选择广告网络、帐户、营销活动和广告组，然后单击&#x200B;**[!UICONTROL Continue]**。

1. 指定[动态搜索目标设置](#dynamic-search-target-settings)。

1. 单击&#x200B;**[!UICONTROL Post]**。

## 编辑[!DNL Google Ads]动态搜索目标设置

您可以编辑[!DNL Google Ads]动态搜索目标的状态或最高出价。 您无法更改已定位的标准。

>[!TIP]
>
>若要同时编辑大量数据，请使用[营销活动批量工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]>[!UICONTROL Auto Targets]**。

1. 选中要编辑的每一行旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在数据表上方的工具栏中，单击![编辑](/help/search-social-commerce/assets/edit.png "编辑")。

1. 指定[动态搜索目标设置](#dynamic-search-target-settings)。

   对于多个目标，您的更改将应用于所有选定的目标。 对于[!UICONTROL Bid field]，您可以选择将现有值更改为指定的值，或者按指定的百分比或货币金额增加或减少金额，但有限制。

1. 保存数据：

   * （单个目标）单击&#x200B;**[!UICONTROL Post]**。

   * （多个广告组）单击&#x200B;**[!UICONTROL Post Now]**。

## 更改[!DNL Google Ads]动态搜索目标的状态

您可以暂停受支持营销活动类型中的任何活动动态搜索目标，以停止将它们用于同一广告组中的动态搜索广告。 您稍后可以将广告状态重新更改为“活动”，以将其用作目标。

您还可以删除任何动态目标。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]>[!UICONTROL Auto Targets]**。

1. （可选）筛选列表以包含特定的动态目标。

1. 执行以下任一操作：

   * 要更改某个动态目标的状态，请单击&#x200B;**[!UICONTROL Status]**&#x200B;列并更改状态。

   * 要删除一个或多个动态目标，请执行以下操作：

      1. 选中要删除的每个动态目标旁边的复选框。

     有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

      1. 在工具栏中，单击![更多](/help/search-social-commerce/assets/more.png "更多")并选择&#x200B;**[!UICONTROL Delete]**。

      1. 在确认消息中，单击&#x200B;**[!UICONTROL Delete]**。

## [!DNL Google Ads]动态搜索目标设置 {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]：** （未在营销活动的[!UICONTROL DSA Options]部分中指定网站域和语言时需要；现有目标为只读）广告组的动态搜索目标：

* *[!UICONTROL All Targets]* （默认）：定位所有索引页。

* *\[Specific Targets\]：*&#x200B;针对索引页最多定位三个条件。 选择此选项时，您必须通过指定信息类别和目标广告的特定值来指定标准（例如，“URL包含shoes.example.com”）。 若要指定多个条件，请单击&#x200B;**[!UICONTROL + And]**。 目标条件包括：

   * *[!UICONTROL Category]：*&#x200B;显示具有特定[!DNL Google Ads]内容类别的索引页面的广告。

   * *[!UICONTROL URL]：*&#x200B;为具有特定URL的索引页面显示广告，其中值可能包含在URL中的任何位置。

   * *[!UICONTROL Page Title]：*&#x200B;显示索引页面的广告，这些页面在页面标题中具有特定文本。

   * *[!UICONTROL Page Content]：*&#x200B;为具有特定内容的索引页面显示广告。

**状态：**&#x200B;目标设置的状态：

* *[!UICONTROL Active]* （默认）：启用竞价。

* *[!UICONTROL Paused]：*&#x200B;禁用竞价。

* *[!UICONTROL Deleted]* （仅限现有目标）：删除目标设置。

### [!UICONTROL Bids]

**[!UICONTROL Bid]：**&#x200B;广告的最大每次点击成本(CPC)或广告的每1000次展示成本(CPM)，适用于广告网络和促销活动定价模型。 此值覆盖广告组级别值。

>[!NOTE]
>
>如果目标在优化的产品组合中，则应用指定的CPC竞价一天。 之后，优化功能根据自己的计算来设置投标。

>[!MORELIKETHIS]
>
>* [关于 [!DNL Google Ads] 动态搜索目标](dynamic-search-target-about.md)
