---
title: '"更新的s\_kwcid跟踪代码 [!DNL Google Ads] account”'
description: 了解如何切换到的最新s\_kwcid跟踪代码 [!DNL Google Ads] 帐户。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# 更新的s\_kwcid跟踪代码 [!DNL Google Ads] 帐户

*仅具有AdobeAdvertising-Adobe Analytics集成的广告商*

*[!DNL Google Ads]仅限帐户*

现有跟踪代码的s\_kwcid旧格式 [!DNL Google Ads] 帐户不支持Analytics中的某些功能，例如营销活动和广告组级别的报告 [!DNL Google Ads] 效果最佳营销活动、草稿和实验营销活动，以及其他在多个营销活动中存在相同“广告+关键字+匹配”类型组合的使用案例。

最新格式包括促销活动ID和广告组ID的参数：

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

您可以单独更改任何或所有现有帐户的新格式。 如果您没有效果最佳的促销活动或草稿和实验促销活动，则可以选择迁移到新格式。

所有新 [!DNL Google Ads] 帐户会自动使用新的s\_kwcid格式。

>[!NOTE]
>
>迁移帐户后，在更改后会正确报告所有点击、成本和展示数据，但在迁移前发生的任何点进次数仍会根据旧的s\_kwcid格式归因于转化数据。

1. 在主菜单中，单击 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. 在子菜单中，单击 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.
1. 将光标悬停在帐户名称上，单击 ![箭头下拉图标](/help/search-social-commerce/assets/arrow-dropdown-menu.png)，然后选择 **[!UICONTROL Edit]**.
1. 单击 **[!UICONTROL Set Account Tracking]**.
1. 开始迁移：

   1. 旁边 **[!UICONTROL S_KWCID FORMAT]** ，单击 **[!UICONTROL LEGACY S_KWCID FORMAT]**.
   1. 单击 **[!UICONTROL Migrate to new s_kwcid format]**.
   1. 在确认消息中，选中复选框，然后单击 **[!UICONTROL Continue]**.
   1. 在帐户设置中，单击 **[!UICONTROL Post]**.

   营销活动的元数据会在几天内在Analytics中更新。 跟踪会持续进行，不会中断，因此不会丢失任何数据，但在Analytics收到所有元数据之前，报表可能不会反映新的跟踪代码。

   >[!NOTE]
   >
   >迁移前发生的所有点进仍将基于旧格式报告转换数据。

1. 开始迁移后，请根据需要更新登陆页面后缀设置（在某些广告网络中称为“最终URL后缀”）：

   * 在跟踪设置中启用“自动上传”功能后，Search、Social和Commerce会自动更新此帐户及其促销活动在登陆页面后缀中的跟踪代码。 你什么都不用做。
   * 如果未启用“自动上传”功能，并且您未使用服务器端s-kwcid，则必须手动更新“登陆页面后缀”设置中的s\_kwcid参数。 您可以在帐户和营销活动设置中手动更改帐户级别和营销活动级别的后缀，也可以通过在批量处理工作表中上载更改来更改后缀。 要在广告组级别或更低级别配置后缀，请使用 [!DNL Google Ads] 编辑者。
   * 如果您将s\_kwcid包含在任何促销活动组件的基本URL设置中，请将其移动到相关的登陆页面后缀设置。

1. （推荐）在迁移其他帐户之前，请在Analytics中验证此帐户的数据。

>[!MORELIKETHIS]
>
>* [管理广告网络帐户](ad-network-account-manage.md)
>* [s_kwcid跟踪参数](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md)
>* [概述 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html)

