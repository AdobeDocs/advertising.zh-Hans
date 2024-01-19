---
title: 关于广告网络帐户
description: 了解Search、Social和Commerce中的广告网络帐户。
exl-id: cb3e650d-721f-48ec-ada3-50bdd7c0375b
feature: Search Campaign Management
source-git-commit: b2d578d0e15e647a57353dbfbde666b5e72d79f2
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# 关于广告网络帐户

*仅限代理客户经理、Adobe客户经理和管理员用户角色*

搜索、Social和Commerce可以在支持的广告网络上跟踪广告商的任何帐户。 要启用帐户跟踪，您必须创建相应的帐户记录。 您必须为任何类型的帐户设置帐户详细信息，无论Search、Social和Commerce是否与其同步，还是优化其广告的竞价和预算。

## 通过API同步的帐户

*[!DNL Google Ads]， [!DNL Microsoft Advertising] (以前称为 [!DNL Bing Ads])， [!DNL Yahoo! Display Network]， [!DNL Yahoo! Japan Ads]， [!DNL Yandex]，并且现有 [!DNL Baidu] 帐户*

搜索、社交和商务同步(*同步*)，以便您可以跟踪、报告和可视化广告效果。 对于所有广告网络，除 [!DNL Yahoo! Display Network]，您可以选择在Search、Social和Commerce中管理帐户的营销活动； [!DNL Yahoo! Display Network]，营销活动为只读。 对于所有广告网络，您可以允许优化功能，通过将受管帐户中的广告竞价添加到项目组合来优化这些广告。

要启用帐户同步，帐户记录必须包含帐户访问凭据并启用（活动）。

在同步过程中，搜索、社交和商务可提取广告商的促销活动结构和支持的促销活动实体，包括其在“搜索”、“社交”和“商务”中管理或报告的大多数属性。 它不包括点击数据，也不包括在Search、Social和Commerce之外输入的竞价和竞价修饰符，这些数据是单独收集的。 搜索、Social和Commerce每天与您的广告网络帐户自动同步一次，每次检测到您的某个广告网络上有新促销活动时也是如此。 此外，它会立即将从“搜索”、“社交和商务”内部对促销活动数据所做的所有更改发送到广告网络。 您可以选择在必要时请求手动同步。

有关创建和编辑同步营销活动的更多信息，请参阅“Campaign Management”一章。

## 仅跟踪帐户

*[!DNL Naver]帐户*

利用跟踪促销活动，您可以跟踪、报告和可视化直接从广告网络购买的广告的表现。 搜索、Social和Commerce不会将数据与广告网络同步、对帐户投标，也不会提供任何类型的优化或模拟。

要允许搜索、社交和商务将转化归因于点击，请在帐户记录中设置跟踪选项并启用帐户记录。 然后，您可以使用批量工作表为广告和关键词生成跟踪URL，并在中手动添加跟踪URL [!DNL Naver] 广告经理。

查看有关 [!DNL Naver] 仅限跟踪的营销活动，请参阅&quot;[实施 [!DNL Naver] 仅跟踪帐户](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)“

>[!MORELIKETHIS]
>
>* [管理广告网络帐户](ad-network-account-manage.md)
>* [管理商户中心帐户](merchant-account-manage.md)
>* [更新的AMO ID跟踪代码 [!DNL Google Ads] 帐户](update-amo-id-google.md)
