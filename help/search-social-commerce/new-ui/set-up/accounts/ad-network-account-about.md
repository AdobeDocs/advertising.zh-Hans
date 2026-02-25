---
title: （新UI）关于广告网络帐户
description: 在新的Search、Social和Commerce UI中了解广告网络帐户。
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# （新UI）关于广告网络帐户

搜索、社交和Commerce可以在支持的广告网络上跟踪广告商的任何帐户。 要启用帐户跟踪，您必须创建相应的帐户记录。 您必须为任何类型的帐户设置帐户详细信息，无论Search、Social和Commerce是否与其同步，还是优化其广告的竞价和预算。

## 通过API同步的帐户

*[!DNL Google Ads]、[!DNL Microsoft Advertising]（以前为[!DNL Bing Ads]）、[!DNL Yahoo! Display Network]、[!DNL Yahoo! Japan Ads]、[!DNL Yandex]和现有[!DNL Baidu]帐户*

搜索、Social和Commerce与受支持的广告网络帐户同步（*同步*），以便您可以跟踪、报告和可视化广告性能。 对于[!DNL Yahoo! Display Network]以外的所有广告网络，您可以选择在Search、Social和Commerce中管理您帐户的营销活动；[!DNL Yahoo! Display Network]营销活动为只读。 对于所有广告网络，您可以通过将促销活动添加到项目组合，利用优化功能来优化受管帐户中促销活动的出价、促销活动预算和促销活动竞价策略目标。

要启用帐户同步，帐户记录必须包含帐户访问凭据并启用（活动）。

在同步过程中，Search、Social和Commerce可提取广告商的营销活动结构和支持的营销活动实体，包括其在Search、Social和Commerce中管理或报告的大多数属性。 它不包括点击数据，也不包括在搜索、社交和Commerce之外输入的竞价和竞价修饰符，这些数据是单独收集的。 Search、Social和Commerce每天与您的广告网络帐户自动同步一次，每次检测到您的某个广告网络上有新的促销活动时，也会自动同步。 此外，它还会立即将从Search、Social和Commerce内对促销活动数据所做的所有更改发送到广告网络。 您可以选择在必要时请求手动同步。

有关创建和编辑同步营销活动的更多信息，请参阅“营销活动管理”一章。

## 手动上传数据的帐户

对于Search、Social和Commerce不提供API支持的在线广告网络，您可以上传促销活动内容和离线成本、点击次数和转化数据，以便帐户用于报表和性能模拟。 搜索、Social和Commerce不会将数据与广告网络同步、提供自动竞价，也不会提供任何类型的优化，但它允许您简化跨渠道分析并识别手动优化的机会。

## 基于模板的仅跟踪帐户

*仅可用于现有[!DNL Naver]帐户*

利用跟踪促销活动，您可以跟踪、报告和可视化直接从广告网络购买的广告的表现。 搜索、Social和Commerce不会将数据与广告网络同步、提供自动竞价，也不会提供任何类型的优化或模拟。

要允许Search、Social和Commerce将转化归因于点击，请在帐户记录中设置跟踪选项并启用帐户记录。 然后，您可以使用批量工作表生成广告和关键字的跟踪URL，并在[!DNL Naver]广告管理器中手动添加跟踪URL。

无法在Search、Social和Commerce中设置新的[!DNL Naver]帐户。 查看有关[!DNL Naver]仅跟踪营销活动的更多信息，请参阅“[实施 [!DNL Naver] 仅跟踪帐户](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)”。

>[!MORELIKETHIS]
>
>* [通过API连接管理广告网络帐户](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
>* [管理用于数据上载的广告网络帐户](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md)
>* [仅管理 [!DNL Naver] 帐户以进行跟踪](/help/search-social-commerce/new-ui/set-up/accounts/template-account-manage.md)
>* [实施 [!DNL Naver] 仅跟踪帐户](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [管理商家中心帐户](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
