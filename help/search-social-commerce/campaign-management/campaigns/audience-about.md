---
title: 关于受众
description: 了解用于跟踪、创建和管理数据的选项 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 受众。
exl-id: 34169650-9820-4b7d-9ae6-09ff8a8c6f2e
feature: Search Campaign Management
source-git-commit: 9f30518efbbe29f976298fe1fcd962182285679f
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---

# 关于管理 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 搜索、社交和商务中的受众

*[!DNL Google Ads]和 [!DNL Microsoft® Advertising] 仅限*

受众库列出了您的所有 [!DNL Google Ads] 基于客户数据、市场内和类似受众以及 [!DNL Microsoft® Advertising] 再营销和动态再营销、自定义、客户匹配、市场内和类似受众。 您可以使用任何 [!DNL Google Ads] 受众作为 [!DNL Google Ads] 营销活动级别和广告组级别的目标和排除项，您可以使用任意的 [!DNL Microsoft® Advertising] 受众作为 [!DNL Microsoft® Advertising] 营销活动级别和广告组级别的目标以及（仅限动态二次营销受众）排除项。 您可以添加或编辑任何受众目标的竞价调整。

您还可以使用现有Adobe Experience Cloud受众中的区段或电子邮件列表，以及客户关系管理(CRM)系统中的各种客户数据，来创建和管理受众：

* **Adobe受众区段：** 具有已选择启用的Adobe Audience Manager或Adobe Analytics帐户的广告商可以创建 [!DNL Google Ads] 客户匹配来自其受众 [!DNL Adobe] 区段：

   * (广告商使用 [!DNL Analytics] 没有Audience Manager的帐户)您可以创建 [!DNL Google Ads] 客户使用来自的用户ID匹配受众 [!DNL Analytics] 与Adobe Experience Cloud共享的区段。

   * (具有Audience Manager帐户的广告商)您可以创建 [!DNL Google Ads] 客户使用受众区段中的用户ID匹配受众，这些Audience Manager区段将Search、Social和Commerce作为目标。 这可能包括发布到Adobe Experience Cloud的Adobe Analytics区段和使用Adobe Experience Cloud受众库创建的区段。

  要创建符合客户要求的受众，广告商的 [!DNL Google Ads] 帐户必须 [符合自定义匹配条件](https://support.google.com/adspolicy/answer/6299717) 并选择加入 [用户标识区段](https://support.google.com/google-ads/answer/9199250). 此外，必须将Search、Social和Commerce中的广告商帐户配置为允许创建客户匹配受众。

  [!DNL Adobe] 基于客户数据的受众的区段数据和Cookie同步文件会同步到 [!DNL Google Ads] 每天。

* **Adobe Campaign电子邮件列表：** 您的Adobe客户团队可帮助您设置工作流以创建和更新 [!DNL Google Ads] 客户匹配来自电子邮件列表的受众，该列表位于 [!DNL Campaign].

* **客户数据列表：** 广告商使用 [!DNL Google Ads] 或 [!DNL Microsoft® Advertising] 符合客户匹配资格的客户可以创建和更新特定于广告网络的基于客户数据的受众 &lt;!> — 或动态再营销受众 — 包含在基于客户数据的受众中，至少对于 [!DNL Google Ads]？—>通过上载包含主标识符的CSV文件。

* **动态二次营销列表：** 广告商使用 [!DNL Microsoft® Advertising] 客户可以创建和管理动态二次营销受众，您可以使用这些受众通过多种方式重新定位最近通过某种方式与您的产品交互的潜在客户（如产品查看者或过去的购买者）。 动态二次营销受众要求您在网页上使用广告网络的JavaScript转化和受众跟踪标记。 将动态再营销列表与搜索和受众网络上的购物营销活动结合使用，通过产品广告重新定位受众，将动态再营销列表与搜索营销活动结合使用，通过文本广告和动态搜索广告重新定位受众。 <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >动态二次营销受众目标的竞价修饰符未在具有&quot;[!UICONTROL Auto-optimize Bid Adjustment Values]”设置。

>[!NOTE]
>
>Search、Social和Commerce不会存储您上传或来自的任何客户数据 [!DNL Adobe] 用于创建或编辑 [!DNL Google Ads] 或 [!DNL Microsoft® Advertising] 受众。

>[!MORELIKETHIS]
>
>* [创建 [!DNL Google Ads] 客户匹配受众来自 [!DNL Adobe] 受众](google-audience-from-adobe-audience.md)
>* [创建 [!DNL Google Ads] Adobe Campaign电子邮件列表中的客户匹配受众](google-audience-from-campaign-email-list.md)
>* [使用客户数据列表管理客户匹配受众](audience-from-customer-data-list.md)
>* [管理动态二次营销受众](audience-dynamic-remarketing-manage.md)
>* [管理营销活动和广告组的受众目标](audience-targets-manage.md)
>* [管理营销活动和广告组的受众排除](audience-exclusions-manage.md)
