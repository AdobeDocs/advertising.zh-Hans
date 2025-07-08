---
title: 更新 [!DNL Google Ads] 帐户的AMO ID (s_kwcid)跟踪代码
description: 了解如何切换到 [!DNL Google Ads] 帐户的最新AMO ID跟踪代码。
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# 更新[!DNL Google Ads]帐户的AMO ID (s_kwcid)跟踪代码

*仅集成Adobe Advertising-Adobe Analytics的广告商*

仅&#x200B;*[!DNL Google Ads]个帐户*

现有[帐户的](/help/integrations/analytics/ids.md#amo-id-formats)AMO ID跟踪代码[!DNL Google Ads]的旧版（2019年10月之前）格式不支持Analytics中的某些功能，例如[!DNL Google Ads]效果最佳促销活动、草稿和实验促销活动的促销活动和广告组级别的报告，以及其他在多个促销活动中存在相同广告+关键字+匹配类型组合的使用案例。

当前格式包括促销活动ID和广告组ID的参数：

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

对于使用旧版格式的现有帐户，可更改为当前格式。 如果您没有效果最佳的促销活动或草稿和实验促销活动，则可以选择迁移到新格式。

所有新[!DNL Google Ads]帐户都会自动使用当前的AMO ID格式。

>[!NOTE]
>
>此选项仅适用于未使用当前格式的帐户。
>
>迁移帐户后，更改后会正确报告所有点击、成本和展示数据，但在迁移前发生的任何点进次数仍会根据旧AMO ID格式归因于转化数据。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**。 在子菜单中，单击&#x200B;**[!UICONTROL Live]** \> **[!UICONTROL Accounts]**。

1. 将光标悬停在帐户名称上，单击![箭头下拉图标](/help/search-social-commerce/assets/arrow-dropdown-menu.png)，然后选择&#x200B;**[!UICONTROL Edit]**。

1. 单击&#x200B;**[!UICONTROL Set Account Tracking]**。

1. 开始迁移：

   1. 在&#x200B;**[!UICONTROL S_KWCID FORMAT]**&#x200B;设置中的[!UICONTROL Account Tracking]旁边，单击&#x200B;**[!UICONTROL LEGACY S_KWCID FORMAT]**。

   1. 单击&#x200B;**[!UICONTROL Migrate to new s_kwcid format]**。

   1. 在确认消息中，选中复选框，然后单击&#x200B;**[!UICONTROL Continue]**。

   1. 在帐户设置中，单击&#x200B;**[!UICONTROL Post]**。

   营销活动的元数据在几天内于[!DNL Analytics]中更新。 跟踪继续进行，不会中断，因此不会丢失任何数据，但是在[!DNL Analytics]收到所有元数据之前，报表可能不会反映新的跟踪代码。

   >[!NOTE]
   >
   >迁移前发生的所有点进仍会根据旧格式报告转换数据。

1. 开始迁移后，请根据需要更新登陆页面后缀设置（在某些广告网络中称为“最终URL后缀”）：

   * 在跟踪设置中启用“[!UICONTROL Auto Upload]”功能后，Search、Social和Commerce会自动更新此帐户及其促销活动登陆页面后缀中的跟踪代码。 你不必做任何事。

   * 如果未启用“[!UICONTROL Auto Upload]”功能，并且您未使用[服务器端AMO ID功能](/help/integrations/analytics/ids.md#amo-id-formats)，则必须手动更新登陆页面后缀设置中的AMO ID参数。 您可以在[帐户设置](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)和[营销活动设置](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)中手动更改帐户级和营销活动级后缀，也可以通过[在批量处理工作表中上载更改](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md)来手动更改帐户级和营销活动级后缀。 要在广告组级别或更低级别配置后缀，请使用[!DNL Google Ads]编辑器。

   * 如果您将AMO ID包含在任何促销活动组件的基本URL设置中，请将其移至相关的登陆页面后缀设置。

1. （建议）在迁移其他帐户之前，请在[!DNL Analytics]中验证此帐户的数据。

>[!MORELIKETHIS]
>
>* [管理广告网络帐户](ad-network-account-manage.md)
>* [使用的 [!DNL Analytics]](/help/integrations/analytics/ids.md)Adobe Advertising ID
>* [概述 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html?lang=zh-Hans){target="_blank"}
