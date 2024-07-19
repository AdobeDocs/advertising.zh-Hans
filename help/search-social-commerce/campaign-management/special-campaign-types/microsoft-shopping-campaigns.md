---
title: 实施 [!DNL Microsoft Advertising] 购物营销活动
description: 了解用于设置 [!DNL Microsoft Advertising] 购物营销活动的工作流。
exl-id: fd10237b-864d-4808-8644-3fcb18edebde
feature: Search Campaign Management
source-git-commit: d5d4dee4356d941ea9cae74b9385add00e0480c3
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 实施[!DNL Microsoft Advertising]购物营销活动

购物营销活动中的广告使用有关您现有[!DNL Microsoft Merchant Center]产品信息源中的产品的数据（而不是关键字）来确定显示广告的方式和位置。

[!DNL Microsoft]购物营销活动以[!DNL Microsoft Advertising Shopping Network]为目标。 购物营销活动的设置包括销售产品的指定国家/地区和优先级（[!DNL High]、[!DNL Medium]或[!DNL Low]）。 您可以选择筛选库存以通告具有特定属性的产品，以及定位或排除特定位置和设备类型。

通过在广告组级别设置多级&#x200B;*[产品组](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)*，您可以控制哪些产品与购物广告一起显示。 产品组基于任何产品属性（类别、产品类型、品牌、条件、产品ID和自定义标签），您最多可以创建七个级别的产品组来包含或从竞价中排除，不包括“[!DNL Add Products]”。 您可以在最低级别的产品组中设置竞价，对所有匹配产品使用相同的竞价。 当同一产品包含在多个促销活动中时，[!DNL Microsoft Advertising]将首先使用促销活动级别的优先级来确定哪个促销活动（及相关竞价）符合广告竞价的条件。 如果所有促销活动具有相同的优先级，则具有最高竞价的促销活动符合条件。

## 设置[!DNL Microsoft Advertising]购物营销活动的步骤

您可以使用针对[!DNL Microsoft Advertising]的[库存馈送模板](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)、使用[批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)或单独使用来设置购物营销活动。 以下说明包含创建单个实体的链接。

1. 设置您的[!DNL Microsoft Merchant Center]帐户并使用产品数据填充该帐户。

1. [允许搜索、社交和Commerce从 [!DNL Microsoft Merchant Center] 帐户](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)下载数据。

1. [在购物网络上创建一个营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)。

1. [在促销活动中创建一个广告组](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)，并设置所有广告的默认出价。

   您可以覆盖单个产品组的默认出价。

1. 为广告组创建产品组：

   1. [创建“所有产品”产品组](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)。

   1. （可选） [创建子产品组](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md)。

   1. 创建包含[促销行的[产品广告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)以可能包含在广告组中的每个购物广告](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md)中。

      Microsoft Advertising会为每个广告动态生成广告副本和登陆页面URL。

      >[!NOTE]
      >
      >即使广告组不包含广告实体，[!DNL Microsoft Advertising]仍会显示产品的广告。

1. （可选）要跟踪广告上的点击次数，[使用跟踪URL工具](/help/search-social-commerce/tools/click-tracking-url-generate.md)生成跟踪URL。 最佳做法是将跟踪URL添加到帐户、营销活动或产品组设置中的[!UICONTROL Tracking Template]字段。 为便于维护，请尽可能将其添加到最高级别。

   或者，您也可以将跟踪URL添加到[!DNL Microsoft Merchant Center]帐户内的产品数据中。 为此，请在产品信息源的自定义列“[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)”中包含跟踪URL以及相应的“link”或“mobile_link”字段中的值。 “bingads_redirect”字段中的值将替换“link”和“mobile_link”字段中的值。 使用此方法生成的URL不包括“搜索”、“Social”和“Commerce”帐户或营销活动设置中指定的任何跟踪参数。

1. 通过[生成[!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)来监视性能。

1. 根据需要：

   1. [编辑营销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)以调整营销活动预算。

      如果促销活动属于某个项目组合，则项目组合设置“[!UICONTROL Auto adjust campaign budget limits]”允许Search、Social和Commerce优化该项目组合中所有促销活动的预算。

   1. 调整现有产品组的最高出价，删除您不再想为其创建广告的产品组，或者添加新的“所有产品”产品组或新的子产品组以便为其他产品创建广告。

>[!NOTE]
>
>* 查看使用[批量处理工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)和[库存馈送模板](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md)管理[!DNL Microsoft Shopping]营销活动和产品组的必填字段。
>* 有关[!DNL Microsoft Shopping]营销活动的详细信息，请参阅[[!DNL Microsoft Advertising] 文档](https://help.ads.microsoft.com/#apex/3/en/50903)。
