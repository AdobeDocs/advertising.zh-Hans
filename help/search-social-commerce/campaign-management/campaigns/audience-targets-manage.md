---
title: 管理营销活动和广告组的受众目标
description: 了解如何为 [!DNL Google Ads] 和 [!DNL Microsoft Advertising] 营销活动和广告组配置和管理受众目标。
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# 管理[!DNL Google Ads]和[!DNL Microsoft Advertising]营销活动和广告组的受众目标

仅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]*

[!DNL Google Ads]个营销活动和广告组以及[!DNL Microsoft Advertising]个广告组可以定位来自同一广告网络的特定受众。 广告网络决定了受众必须有多大才能成为目标。

>[!NOTE]
>
>排除项始终会覆盖包含项/目标。

您可以配置受众目标、编辑受众目标的竞价修饰符以及更改受众目标的状态。

## 配置受众目标

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**。

1. 在数据表上方的工具栏中，单击![创建](/help/search-social-commerce/assets/add.png "创建")。

1. 选择广告网络和帐户名称，然后单击&#x200B;**[!UICONTROL Continue]**。

1. 为特定营销活动和广告组配置受众目标：

   1. 为指定的广告网络选择适用的受众。

      您可以选择搜索包含至少三个字符的特定文本字符串的受众。 对于任何匹配的受众，单击&#x200B;**[!UICONTROL Include]**&#x200B;以将其选定。

      [!DNL Google Ads]客户匹配受众仅适用于搜索和购物营销活动。

   1. 指定目标：

      1. （可选）要展开促销活动及其子广告组，请单击促销活动名称。

      1. （可选）要按名称中包含的文本字符串筛选促销活动列表或广告组列表，请单击![筛选](/help/search-social-commerce/assets/filter.png "筛选")，在输入字段中输入或粘贴该文本字符串，然后按&#x200B;**[!UICONTROL Enter]**&#x200B;键。

      1. 通过单击相邻的空圆圈，为指定的广告网络指定每个促销活动和广告组目标，以便显示一个蓝色复选标记（![选择](/help/search-social-commerce/assets/include.png "选择")）。

      您不能同时为父营销活动和子广告组（自动使用目标）配置目标。

1. 单击&#x200B;**[!UICONTROL Post]**。

1. （可选）从[!UICONTROL Targets]视图中，通过下列方式之一设置目标的竞价调整：

   * 单击&#x200B;**[!UICONTROL Bid Adjustment]**&#x200B;列并输入值。

   * 选中目标行旁边的复选框。 在工具栏中，单击![编辑](/help/search-social-commerce/assets/edit.png "编辑")，输入竞价修饰符，然后单击&#x200B;**[!UICONTROL Post]**。

   值可以包括：

   * *0%：*&#x200B;不调整此受众的广告竞价。

   * /[*从–90%到900%的其他值*/]：增加或减少此受众的广告竞价。 例如，如果关键词级别的竞价为1美元，而特定受众目标的竞价调整为50%，则该受众的竞价将增加到1.50美元。

## 编辑受众目标的竞价修饰符

您可以更改所有受众类型（市场内受众除外）的竞价修改量和受众目标状态。

>[!NOTE]
>
>当父营销活动使用CPC竞价策略并且在配置为自动优化受众目标竞价调整值的项目组合中时，Search、Social和Commerce会自动优化竞价修饰符。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**。

1. 执行以下任一操作：

   * 要编辑一个目标的竞价修饰符，请单击&#x200B;**[!UICONTROL Bid Adjustment]**&#x200B;列并编辑竞价调整。

   * 要编辑一个或多个目标的竞价修饰符，请执行以下操作：

      1. 选中要编辑的每个目标旁边的复选框。

         有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

      1. 在数据表上方的工具栏中，单击![编辑](/help/search-social-commerce/assets/edit.png "编辑")。

      1. 编辑&#x200B;**[!UICONTROL Bid Modifier]**&#x200B;和/或&#x200B;**[!UICONTROL Status]**&#x200B;字段。

         对于[!UICONTROL Bid Modifier]字段，您可以选择将现有值更改为指定值，或者增加或减少金额指定百分比或货币金额，但有限制。

         对于设置的值，该值可以包括：

         * *0%：*&#x200B;不调整此受众的广告竞价。

         * /[*从–90%到900%的其他值*/]：增加或减少此受众的广告竞价。 例如，如果关键词级别的竞价为1美元，而特定受众目标的竞价调整为50%，则该受众的竞价将增加到1.50美元。

         对于多个目标，您的更改将应用于所有选定的目标。

      1. （可选）单击&#x200B;**[!UICONTROL Additional Details]**，并选择性地输入项目名称和描述。

      1. 单击&#x200B;**[!UICONTROL Post]**。

## 更改受众目标的状态

您可以暂停活动受众目标以禁止对其进行竞价。 您稍后可以通过将状态更改回“活动”来恢复竞价。

您还可以删除活动或暂停的搜索受众目标。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**。

1. （可选）筛选列表以包含特定的受众目标。

1. 选中要更改其状态的每个受众目标旁边的复选框。

   有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

1. 在工具栏中，单击状态按钮：

   * 要激活行，请单击![激活](/help/search-social-commerce/assets/activate.png "激活")。

   * 要暂停行，请单击![暂停](/help/search-social-commerce/assets/pause.png "暂停")。

   * 要删除这些行，请单击![更多操作](/help/search-social-commerce/assets/more.png "更多操作")，然后选择&#x200B;**[!UICONTROL Delete]**。 在确认消息中，单击&#x200B;**[!UICONTROL Delete]**。

>[!MORELIKETHIS]
>
>* [关于受众](audience-about.md)
>* [管理营销活动和广告组的受众排除](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
