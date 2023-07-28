---
title: 实施 [!DNL Microsoft® Advertising] 购物营销活动
description: 了解用于设置的工作流 [!DNL Microsoft® Advertising] 购物营销活动。
exl-id: 3fb19b92-5bc0-414e-9234-68310082d0ed
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# 实施 [!DNL Microsoft® Advertising] 购物营销活动

购物营销活动中的广告使用有关您现有产品的数据 [!DNL Microsoft® Merchant Center] 由产品信息源（而不是关键字）决定显示广告的方式和位置。

[!DNL Microsoft®] 购物营销活动目标 [!DNL Microsoft® Advertising Shopping Network]. 购物营销活动的设置包括销售产品的指定国家/地区和优先级([!DNL High]， [!DNL Medium]，或 [!DNL Low])。 您可以选择筛选库存以通告具有特定属性的产品，以及定位或排除特定位置和设备类型。

您可以通过设置多级来控制哪些产品与您的购物广告一起显示 *[产品组](/help/search-social-commerce/campaign-management/campaigns/product-group-about.md)* 在广告组级别。 产品组基于任何产品属性（类别、产品类型、品牌、条件、产品ID和自定义标签），您最多可以创建七个级别的产品组来包含或从竞价中排除，不包括»[!DNL Add Products]“ 您可以在最低级别的产品组中设置竞价，对所有匹配产品使用相同的竞价。 当同一产品包含在多个营销活动中时， [!DNL Microsoft® Advertising] 首先使用促销活动级别优先级来确定哪个促销活动（及相关竞价）符合广告竞价的条件。 如果所有促销活动具有相同的优先级，则具有最高竞价的促销活动符合条件。

## 要设置的步骤 [!DNL Microsoft® Advertising] 购物营销活动

您可以使用设置购物营销活动 [库存馈送模板](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) 对象 [!DNL Microsoft® Advertising]，通过使用 [批量工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)，或者单独使用。 以下说明包含创建单个实体的链接。

1. 设置您的 [!DNL Microsoft® Merchant Center] 并使用产品数据填充该帐户。

1. [允许Search、Social和Commerce从下载数据 [!DNL Microsoft® Merchant Center] 帐户](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

1. [创建营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) 在购物网上。

1. [创建广告组](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) ，并为所有广告设置默认竞价。

您可以覆盖单个产品组的默认出价。

1. 为广告组创建产品组：

   1. [创建“所有产品”产品组](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. （可选） [创建子产品组](/help/search-social-commerce/campaign-management/campaigns/product-group-manage.md).

   1. 创建 [产品广告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) 替换为 [可能包含在每个购物广告中的促销行](/help/search-social-commerce/campaign-management/campaigns/product-group-settings-microsoft.md) 在广告组内。

      Microsoft® Advertising会为每个广告动态生成广告副本和登陆页面URL。

      >[!NOTE]
      >
      >即使广告组不包含广告实体， [!DNL Microsoft® Advertising] 仍会显示产品的广告。

1. （可选）要跟踪广告的点击量， [使用跟踪URL工具生成跟踪URL](/help/search-social-commerce/tools/click-tracking-url-generate.md). 最佳实践是将跟踪URL添加到 [!UICONTROL Tracking Template] “帐户”、“促销活动”或“产品组”设置中的字段。 为便于维护，请尽可能将其添加到最高级别。

   或者，您可以将跟踪URL添加到中的产品数据 [!DNL Microsoft® Merchant Center] 帐户。 为此，请将跟踪URL以及字段“link”或“mobile_link”中的值（如果适用）包含在自定义列中»[bingads_redirect](https://help.ads.microsoft.com/#apex/3/en/51084)”在产品信息源中。 “bingads_redirect”字段中的值将替换“link”和“mobile_link”字段中的值。 使用此方法生成的URL不包含在“搜索”、“Social”和“Commerce”帐户或营销活动设置中指定的任何跟踪参数。

1. 监控性能依据 [生成 [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md).

1. 根据需要：

   1. [编辑营销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) 以调整促销活动预算。

      如果营销活动属于项目组合，则项目组合设置»[!UICONTROL Auto adjust campaign budget limits]”允许搜索、社交和商务优化项目组合中所有促销活动的预算。

   1. 调整现有产品组的最高出价，删除您不再想为其创建广告的产品组，或者添加新的“所有产品”产品组或新的子产品组以便为其他产品创建广告。

>[!NOTE]
>
>* 查看用于管理的必填字段 [!DNL Microsoft® Shopping] 使用的促销活动和产品组 [批量工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md) 和 [库存馈送模板](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md).
>* 有关详情 [!DNL Microsoft® Shopping] 营销活动，请参见 [[!DNL Microsoft® Advertising] 文档](https://help.ads.microsoft.com/#apex/3/en/50903).
