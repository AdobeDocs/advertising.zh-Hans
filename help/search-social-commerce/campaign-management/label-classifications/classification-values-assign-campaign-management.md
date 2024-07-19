---
title: 从营销活动管理视图将分类值分配给帐户组件
description: 了解如何将分类值分配给帐户组件。
exl-id: 5a3cb059-9cff-4a2e-b8aa-be8626774377
feature: Search Label Classifications
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# 从营销活动管理视图将分类值分配给帐户组件

您可以从营销活动管理视图中分配和移除以下搜索实体的分类值：营销活动、广告组、关键词、广告、投放位置、单位级别产品组和动态搜索目标。 如有必要，您可以在分配过程中创建分类和分类值。 每个标签分类最多可以具有2000个值。

每个实体在每个分类中可以有一个标签值。 例如，Shoes_Campaign的“颜色”值可以为“红色”，“地域”值可以为“洛杉矶”，但不能为“颜色”或“地域”具有多个值。

标签值由子实体继承，因此除非要覆盖继承的值，否则不要为子实体输入值。

>[!NOTE]
>
>您为某些广告网络和促销活动类型创建的关键字和广告副本的时间是[不可变的](/help/search-social-commerce/campaign-management/faqs-campaigns.md)，这意味着编辑它们会删除现有实体并创建一个新实体。 以这种方式删除现有实体时，标签分类不会分配给新实体。

1. 单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**，然后选择帐户组件视图。

1. 执行以下任一操作：

   * （要将值分配给单个实体）将光标悬停在实体名称上，单击![菜单按钮](/help/search-social-commerce/assets/arrow-dropdown-menu.png "菜单按钮")，然后选择&#x200B;**[!UICONTROL Classification]**。

   * （为一个或多个实体分配值）执行以下操作：

      * 选中每个相关行旁边的复选框。

        有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

      * 在数据表上方的工具栏中，单击![更多](/help/search-social-commerce/assets/more.png "更多")，然后单击&#x200B;**[!UICONTROL Classification]**。

1. 在[!UICONTROL Assignment Details]中，执行以下任一操作：

   * 要将任何现有分类值更改为新值，请选择&#x200B;**[!UICONTROL Set To]**。

     每个值的最大长度为100个字符，可包含ASCII和非ASCII字符。

   * 要分配指定的分类值而不删除现有值，请选择&#x200B;**[!UICONTROL Assign]**。

   * 要删除当前分配的特定分类值，请选择&#x200B;**[!UICONTROL Remove]**。

     删除分类值时，该值对应的报表数据不再可用于指定的帐户组件。

   * 要删除指定的分类值，请选择&#x200B;**[!UICONTROL Delete]**。

     删除分类值会使其在将来不可用，并且报表数据不再可用于该值。 将删除值与特定帐户组件之间的所有分配，但不会删除帐户组件。

1. 对于每个适用的分类值，执行以下操作：

   1. 在&#x200B;**[!UICONTROL Classification]**&#x200B;列中，指定分类名称：

      * 要使用现有分类，请单击分类名称以将其展开。

      * 要创建分类，请单击[!UICONTROL +]。 在输入字段中，输入分类名称，然后单击![保存](/help/search-social-commerce/assets/select.png "保存")以立即保存分类。

        名称必须包含[个32-126](https://www.asciitable.com/)的ASCII字符，最大长度为27个单字节字符。

   1. 在&#x200B;**[!UICONTROL Value Name]**&#x200B;列中，指定值的名称：

      * 要使用现有值，请单击值名称以将其选定。

      * 要创建值，请单击[!UICONTROL +]。 在输入字段中输入值，然后单击![保存](/help/search-social-commerce/assets/select.png "保存")以立即保存该值。

        最大长度为100个字符，可包含ASCII和非ASCII字符。

1. （可选）输入其他详细信息：

   1. 在&#x200B;**[!UICONTROL Additional Details]**&#x200B;旁边，单击![打开](/help/search-social-commerce/assets/chevron-up.png "打开")展开详细信息。

   1. 输入可选的&#x200B;**[!UICONTROL Project Name]**&#x200B;和/或可选的&#x200B;**[!UICONTROL Description]**。

1. 单击&#x200B;**[!UICONTROL Save]**。

>[!MORELIKETHIS]
>
>* [关于标签分类](classification-about.md)
>* [创建标签分类](classification-create.md)
>* [使用批量处理工作表将分类值分配给帐户组件](classification-values-assign-bulksheets.md)
>* [从帐户组件中删除标签分类值](classification-values-remove.md)
>* [删除标签分类值](classification-values-delete.md)
>* [删除标签分类](classification-delete.md)
