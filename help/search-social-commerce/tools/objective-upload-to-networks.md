---
title: 支持将目标上传到广告网络
description: 了解如何将混合投资组合 [!DNL Google Ads] 的目标上传到 和 [!DNL Microsoft Advertising]。
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 803f1ad2ad5be005b7dab467efbeb1c4ceaa7559
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# 支持将目标上传到广告网络

*Advertisers with [!DNL Google Ads] 和 [!DNL Microsoft Advertising] accounts only*

*Advertisers enabled for hybrid optimization only*

Search, Social, &amp; Commerce can upload the objectives for an advertiser account&#39;s portfolios to [!DNL Google Ads] 和 [!DNL Microsoft Advertising] so you can use them for hybrid optimization. Your uploaded objectives are available as conversion actions for account-level and campaign-level custom conversion goals.

Enabling this option automatically triggers an upload for objectives in portfolios that contain campaigns with smart bidding strategies. Search, Social, &amp; Commerce creates a conversion on the ad network for each applicable objective. The conversion represents all weighted conversion metrics in the objective. Each conversion has one of the following names:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  where `<network_ID>` is the numeric ID that Search, Social, &amp; Commerce uses for the ad network, `<objective_id>` is the numeric objective ID, and `<network_account_ID>` is the numeric ID for the ad network account or manager account.

* （将来将弃用的旧格式） `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  其中 `<portfolio_id>` ，是数字组合 ID， `<se_acctid/conversion_manager_se_acctid>` 是广告联盟帐户或经理帐户的数字 ID。

  您的 Adobe 帐户团队将与您合作，在弃用旧格式之前，在广告联盟中迁移现有的转化操作名称。 在迁移期间，新旧格式上传将并行运行。 模型估算和优化功能不受影响，因为新的转化操作最初显示为“次要”（未优化）状态，并包含 90 天的回填数据。

Uploads to [!DNL Google Ads] occur daily at 06:00 in the advertiser&#39;s time zone. Uploads to [!DNL Microsoft Advertising] occur daily at 09:00 in the advertiser&#39;s time zone.

>[!IMPORTANT]
>
>Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren&#39;t re-uploaded to the ad networks. If you include them within an objective, add them to the campaign goals within the ad network&#39;s editor.

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. In the main menu, click **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Select the check box next to **[!UICONTROL Enable Objective Upload]**.

1. (Advertisers with [!DNL Google Ads] accounts who do business in the European Economic Area (EEA) or United Kingdom (UK); optional) If you&#39;ve collected consent from EEA and UK users to upload their data for advertising purposes, then select the check box next to **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Click **[!UICONTROL Save]**.

1. （如果您的转化是在经理帐号一级跟踪的） [在 > [!UICONTROL Admin] > [!UICONTROL Manager Accounts]**上**[!UICONTROL Search]&#x200B;为您的经理帐号](/help/search-social-commerce/admin/manager-accounts.md)添加凭据。

1. 验证每个目标（已命名） `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` 是否在 2 天内在广告网络上展示。

   在编辑器中 [!DNL Google Ads] ，查找您的 [转化操作](https://support.google.com/google-ads/answer/11461796)。 在编辑器中 [!DNL Microsoft Advertising] ，查找您的 [转化目标](https://help.ads.microsoft.com/#apex/ads/en/56709)。

   If necessary, update the date range to include the upload date.

## Troubleshooting missing objectives

If the objective — named `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — for one of your portfolios doesn&#39;t appear on the ad network, then check the following:

* ([!DNL Google Ads]) Check if the conversions should be uploaded to the account or manager level. If they should be uploaded at the manager level:

   * Check if the credentials for the [!DNL Google Ads] manager account is provided at **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. If necessary, [add the credentials for the manager account](/help/search-social-commerce/admin/manager-accounts.md).

   * Check if the ad network account already includes the same metric name. 如果是，请重命名指标，以便创建正确的经理级媒体资源。

* 检查是否选择了投资组合的“混合”选项，以及目标是否具有有效的收入。

>[!MORELIKETHIS]
>
>* [管理广告客户的转化指标简介](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [将转化指标上传到 [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
