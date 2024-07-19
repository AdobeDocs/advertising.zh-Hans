---
title: 管理修饰符
description: 了解如何为清单数据馈送配置和管理广告模板的修饰符。
exl-id: 74c9a7c7-0979-4f78-9225-43bc6c94acd7
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# 管理修饰符

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （仅删除操作）和仅[!DNL Yandex]帐户*

修饰符是可以添加到句子中或从句子中移除的形容词或副词，而无需改变基本句子结构。 您可以创建修改量组，以用作馈送数据模板中各种数据字段中的变量。 通过在帐户结构（营销活动和广告组）字段、关键字、基本URL和广告中包含修饰符，您可以为每个关联的修饰符值创建一个值。 例如，如果您在广告标题中使用修饰符组变量，并且该修饰符组包含三个修饰符（“便宜”、“折扣”和“可承受”），则将为数据馈送中的每个数据行创建三个单独的广告 — 每个修饰符各一个。 同样，如果您在广告组的基本URL中包含具有多个值的修饰符组，则会为每个生成的基本URL创建一组关键字。

每个修改量组均可包含所需数量的修改量。 每个模板只能使用一个修饰符组。

## 创建修改量组

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Modifiers]**。

1. 在修饰符组列表的上方，单击&#x200B;**[!UICONTROL Create]**。

1. 指定修饰符组设置：

   **[!UICONTROL Name]：**&#x200B;修饰符组的名称。

   **[!UICONTROL Modifiers]：**&#x200B;组的修饰符值（每行一个）。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 编辑修改者组

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Modifiers]**。

1. 在修改量组列表中，单击修改量组名称。

1. 编辑修饰符组设置：

   **[!UICONTROL Name]：**&#x200B;修饰符组的名称。

   **[!UICONTROL Modifiers]：**&#x200B;组的修饰符值（每行一个）。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 删除修饰符组

>[!IMPORTANT]
>
>当您删除修改量组时，请从现有模板的字段中移除该修改量组的所有变量（表示为`<modifier_group_name>`）。 如果尝试使用不存在修饰符的变量通过模板传播数据，则作业会失败1。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**。

1. 在数据表上方的工具栏中，单击&#x200B;**[!UICONTROL Modifiers]**。

1. 选中要删除的每个修改量组旁边的复选框。

1. 在修饰符组列表的上方，单击&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Yes]**。

1. （如有必要）[从所有适用的模板中删除对修饰符](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)的引用。

>[!MORELIKETHIS]
>
>* [关于清单信息源](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [管理广告模板](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
