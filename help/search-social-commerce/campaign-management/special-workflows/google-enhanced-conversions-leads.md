---
title: 为潜在客户实施 [!DNL Google Ads] 增强型转化
description: 了解用于为潜在客户设置 [!DNL Google Ads] 增强型转换的工作流。
feature: Search Campaign Management, Conversions
exl-id: b708c9f2-2962-45d9-8780-4e96ef2ae8f7
source-git-commit: 56161ece4ba9c01cddb86e16796150c391f1a811
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# 为潜在客户实施[!DNL Google Ads]增强型转化

仅&#x200B;*[!DNL Google Ads]个帐户*

[[!DNL Google Ads] 潜在客户的增强型转化](https://support.google.com/google-ads/answer/9888656)允许您使用第一方转化数据将用户映射到离线转化。 在点击ID不可用的环境中对潜在客户使用增强型转化，例如跟踪由网站潜在客户产生的电话或电子邮件销售。

在Search、Social和Commerce中，您可以：

* 查看潜在客户的现有增强型转化。

  搜索、社交和Commerce每天在广告商所在时区的05:00同步您现有的潜在客户增强转化。

* 为潜在客户创建增强型转化。

* 上传第一方离线转化数据以映射到潜在客户的增强转化。

* 将潜在客户的增强转化作为指标包含在报表中，并将加权指标包含在优化目标中。

要使用此功能，请完成以下步骤。 您可以选择撤消创建转化跟踪标记和创建转化操作的步骤。

1. 在[!DNL Google Ads]内，选择启用潜在客户的增强型转化：

   1. 打开帐户的转换设置。

   1. 选择潜在客户的增强转化选项，并接受服务条款。

   1. 选择使用[!DNL Google]标记还是[!DNL Google Tag Manager]创建转化标记。


1. 为转换操作配置并实施[!DNL Google]标记。

   有关说明，请参阅[!DNL Google Ads]帮助以使用 [!DNL Google] 标记](https://support.google.com/google-ads/answer/11021502)为潜在客户[创建增强型转化标记，或使用 [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11347292)为[创建标记。

1. 为[搜索、社交和Commerce](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)或[Google广告](https://support.google.com/google-ads/answer/12216226)中的潜在客户创建增强型转化操作。

   对于&#x200B;**转换类型，**&#x200B;选择&#x200B;*导入转换*&#x200B;或&#x200B;*导入。*

1. 根据需要，经常上传第一方数据（包括经过哈希处理的电子邮件地址或电话号码）以归因于指定帐户的转化。 您可以从[搜索、社交和Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)中或使用[!DNL Google Data Manager]完成此步骤。

   * 在Search、Social和Commerce中，您可以下载[!DNL Microsoft Excel]格式的模板，输入转化数据并将文件保存在本地，然后上传编辑后的文件。 该模板包含列，用于指示是否征得用户同意将数据上传到[!DNL Google]以用于广告和广告个性化。

     所有上传的数据已实时同步到[!DNL Google Ads]。

   * 有关使用[!DNL Google Data Manager]上载数据的详细信息，请参阅“[关于数据管理器](https://support.google.com/google-ads/answer/14639041)”。

>[!MORELIKETHIS]
>
>* [为潜在客户的 [!DNL Google Ads] 增强型转化创建转化操作](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [上载离线转化数据以进行增强型转化](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
