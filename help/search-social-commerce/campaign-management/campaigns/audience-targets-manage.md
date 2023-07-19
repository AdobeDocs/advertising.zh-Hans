---
title: 管理营销活动和广告组的受众目标
description: 了解如何为您的配置和管理受众目标 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 营销活动和广告组。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 0%

---

# 管理受众目标 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 营销活动和广告组

*[!DNL Google Ads]和 [!DNL Microsoft® Advertising] 仅限*

[!DNL Google Ads] 营销活动和广告组，以及 [!DNL Microsoft® Advertising] 广告组可以定位来自同一广告网络的特定受众。 广告网络确定受众必须有多大才能成为目标。

>[!NOTE]
>
>排除项始终会覆盖包含项/目标。

您可以配置受众目标、编辑受众目标的竞价修饰符以及更改受众目标的状态。

## 配置受众目标

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. 在数据表上方的工具栏中，单击 ![创建](/help/search-social-commerce/assets/add.png "创建").

1. 选择广告网络和帐户名称，然后单击 **[!UICONTROL Continue]**.

1. 为特定营销活动和广告组配置受众目标：

   1. 为指定的广告网络选择适用的受众。

      您可以选择搜索包含至少三个字符的特定文本字符串的受众。 对于任何匹配的受众，单击 **[!UICONTROL Include]** 以选择它。

      [!DNL Google Ads] 客户匹配受众仅适用于搜索和购物营销活动。

   1. 指定目标：

      1. （可选）要展开促销活动及其子广告组，请单击促销活动名称。

      1. （可选）要按名称中包含的文本字符串筛选营销活动列表或广告组列表，请单击 ![筛选条件](/help/search-social-commerce/assets/filter.png "筛选条件") ，输入文本字符串或将文本字符串粘贴到输入字段中，然后按 **[!UICONTROL Enter]** 键。

      1. 通过单击指定广告网络旁边的空圆圈，为指定的广告网络指定每个营销活动和广告组目标，以便显示一个蓝色复选标记(![选择](/help/search-social-commerce/assets/include.png "选择"))。

      您不能同时为父营销活动和子广告组（自动使用目标）配置目标。


1. 单击 **[!UICONTROL Post]**.

1. （可选）通过以下方式之一为目标设置竞价调整： [!UICONTROL Targets] 视图：

   * 单击 **[!UICONTROL Bid Adjustment]** 列并输入一个值。

   * 选中目标行旁边的复选框。 在工具栏中，单击 ![编辑](/help/search-social-commerce/assets/edit.png "编辑")，输入竞价修饰符，然后单击 **[!UICONTROL Post]**.

   值可以包括：

   * *0%：* 不调整此受众的广告投标。

   * /[*从–90%到900%的其他值*/]：提高或降低此受众的广告竞价。 例如，如果关键词级别的竞价为1美元，而特定受众目标的竞价调整为50%，则该受众的竞价将增至1.50美元。


## 编辑受众目标的竞价修饰符

您可以更改所有受众类型（市场内受众除外）的竞价修饰符和受众目标的状态。

>[!NOTE]
>
>当父营销活动使用CPC竞价策略，并且在配置为自动优化受众目标的竞价调整值的项目组合中时，“搜索”、“Social”和“Commerce”会自动优化竞价修饰符。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. 执行以下任一操作：

   * 要编辑一个目标的竞价修饰符，请单击 **[!UICONTROL Bid Adjustment]** 列并编辑竞价调整。

   * 要编辑一个或多个目标的竞价修饰符，请执行以下操作：

      1. 选中要编辑的每个目标旁边的复选框。

         有关选择多行的提示，请参阅&quot;[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).”

      1. 在数据表上方的工具栏中，单击 ![编辑](/help/search-social-commerce/assets/edit.png "编辑").

      1. 编辑 **[!UICONTROL Bid Modifier]** 和/或 **[!UICONTROL Status]** 字段。

         对于 [!UICONTROL Bid Modifier] 字段，则可选择将现有值更改为指定值，或者增加或减少金额指定百分比或货币金额（具有限制）。

         对于设置值，该值可以包括：

         * *0%：* 不调整此受众的广告投标。

         * /[*从–90%到900%的其他值*/]：提高或降低此受众的广告竞价。 例如，如果关键词级别的竞价为1美元，而特定受众目标的竞价调整为50%，则该受众的竞价将增至1.50美元。

         对于多个目标，您的更改将应用于所有选定的目标。

      1. （可选）单击 **[!UICONTROL Additional Details]** （可选）输入项目名称和说明。

      1. 单击 **[!UICONTROL Post]**.


## 更改受众目标的状态

您可以暂停活动的受众目标以禁用对其的竞价。 您稍后可以通过将状态改回活动来恢复竞价。

您还可以删除活动或暂停的搜索受众目标。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. （可选）筛选列表以包含特定的受众目标。

1. 选中要更改其状态的每个受众目标旁边的复选框。

   有关选择多行的提示，请参阅&quot;[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).”

1. 在工具栏中，单击状态按钮：

   * 要激活行，请单击 ![激活](/help/search-social-commerce/assets/activate.png "激活").

   * 要暂停行，请单击 ![暂停](/help/search-social-commerce/assets/pause.png "暂停").

   * 要删除行，请单击 ![更多操作](/help/search-social-commerce/assets/more.png "更多操作") 并选择 **[!UICONTROL Delete]**. 在确认消息中，单击 **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [关于受众](audience-about.md)
>* [管理营销活动和广告组的受众排除](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
