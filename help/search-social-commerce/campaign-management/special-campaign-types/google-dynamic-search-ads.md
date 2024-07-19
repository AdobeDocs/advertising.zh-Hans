---
title: 实施 [!DNL Google Ads] 动态搜索广告
description: 了解用于设置 [!DNL Google Ads] 动态搜索广告的工作流。
exl-id: 69e5069f-3f82-4ee3-841a-0c1292677223
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# 实施[!DNL Google Ads]动态搜索广告

*[!DNL Google Ads]仅搜索具有创意级别或关键词和创意级别跟踪的营销活动*

动态搜索广告使用网站中的内容而不是关键字来确定何时显示广告。 您可以定义网站中的页面，这些页面的内容将用于定位动态搜索广告，方法是为广告组设置单独的动态搜索目标，或者选择促销活动级别的设置，以使用网站内容定位您的广告。

您可以单独设置动态搜索广告，也可以使用批量工作表进行设置。 以下说明包含创建单个实体的链接。

## 设置[!DNL Google Ads]动态搜索广告的步骤

1. [为动态搜索广告创建营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)：

   1. 最初，将促销活动预算设置为每日搜索促销活动支出的10%。

      您可以在广告证明其价值后增加预算。

   1. （如果您希望[!DNL Google Ads]根据网站内容显示您的动态搜索广告）请在促销活动设置的[!UICONTROL DSA Options]部分中指定根域和域的语言。

      >[!NOTE]
      >
      >您的域必须按[!DNL Google Ads]有机搜索索引编制索引才能定位。 此外，如果域包含多种语言的页面，并且您希望定位所有语言，则请为每个语言创建单独的营销活动。

      如果您不使用网站域来定位广告，则请为每个广告组创建动态搜索目标（请参阅步骤4）。 您可以单独创建目标[](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md)或使用[批量工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)。

   1. 确保该营销活动以搜索渠道为目标，且仅以[!DNL Google Ads]搜索网络（而非显示网络）为目标。 这些设置可在[!UICONTROL Networks and Devices]选项卡中使用。

   1. （可选）在[!UICONTROL Negatives]选项卡上排除关键字。

   1. （可选）配置营销活动级别的跟踪模板，以覆盖帐户级别的跟踪模板，但可以在较低级别覆盖该模板。

      (使用Adobe Analytics且没有服务器端跟踪的广告商)如果您希望包含对Search、Social和Commerce到Analytics的反向馈送的跟踪，请将AMO ID跟踪代码添加到帐户级别的附加参数，这会将该代码添加到最终URL。 查看 [!DNL Analytics]](/help/integrations/analytics/ids.md)使用的[Adobe AdvertisingID。

1. [在营销活动中创建一个广告组](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)，包括以下步骤：

   1. 将[!UICONTROL Ad Group Type]设置为&#x200B;**[!UICONTROL Search Dynamic].**

   1. 设置所有广告的默认出价。

      您可以覆盖单个动态搜索目标的默认竞价（如果进行了配置）。

   1. （可选）配置广告组级别的跟踪模板，以覆盖更高级别的任何跟踪模板，但可以在广告级别覆盖。

      如果您在促销活动级别添加了Adobe Analytics跟踪，并且希望将其包含在广告组中，请在此处添加它。 请参阅步骤1e。

1. [在广告组内创建每个动态搜索广告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)。

   [!DNL Google Ads]动态生成每个广告的标题、显示URL和登陆页面URL。 您可以选择将重定向和跟踪添加到广告级别的跟踪模板，这会覆盖更高级别的跟踪模板。
如果要使用广告级别跟踪覆盖较高级别的任何Adobe Analytics跟踪，请在此处添加该跟踪。 请参阅步骤1e和2c。

1. （当您未将根域和域的语言包含在Campaign设置的DSA选项部分中时，此为必需字段；否则为可选字段）为广告组创建[动态搜索目标](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md)。 您可以选择使用目标级别竞价覆盖广告组级别竞价。

   目标定义广告网络使用网站中的所有页面还是部分页面来定位动态搜索广告。 要最佳跟踪性能，请为每个动态搜索目标配置一个广告组的营销活动，并包含定向所有标准的广告组。

1. 如有必要，[编辑营销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)以调整营销活动预算，并通过从营销活动中排除其他关键字来优化流量。
