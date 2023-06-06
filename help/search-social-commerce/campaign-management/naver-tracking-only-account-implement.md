---
title: 实施 [!DNL Naver] 仅跟踪帐户
description: 了解如何为您的设置跟踪活动 [!DNL Naver] 帐户，以便您可以跟踪、报告和可视化直接从广告网络购买的广告的表现。
source-git-commit: c4848da6c5489a5128a0424eef6a12f2c51caa12
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# 实施 [!DNL Naver] 仅跟踪帐户

*[!DNL Naver]仅限帐户*

您可以为创建跟踪营销活动 [!DNL Naver] 帐户，以便您可以跟踪、报告和可视化直接从广告网络购买的广告的表现。 搜索、Social和Commerce不会与广告网络同步数据，自动上传跟踪，也不会对帐户投标。

跟踪营销活动会复制您现有的营销活动、广告组和关键词。 在Search、Social和Commerce中创建帐户结构并向广告网络内的原始促销活动添加跟踪后，即可上传关键字或广告的每日网络流量量度。 然后，搜索、Social和Commerce可以将您的转化归因于广告和关键词。

您可以跟踪所有促销活动以及任何单个促销活动、广告组或关键词/广告的绩效指标。 您还可以在最基本、最高级和辅助报表中包含关于广告网络的信息，以及其他广告网络的数据。 不支持将量度导出到Adobe Analytics，但是Search、Social和Commerce可以同步 [您正在跟踪的指标 [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) 进入搜索、社交和商务。

>[!NOTE]
>
>您无法将跟踪营销活动添加到项目组合以进行优化。

1. 在Search、Social和Commerce中创建跟踪活动：

   1. 创建 [虚拟网络帐户详细信息](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). 如果您在单个广告网络中有多个帐户，则请在中将它们整合到一个帐户中 [!UICONTROL Accounts] 视图。

      [!DNL Naver] 不提供将跟踪参数上传到广告网络的API支持。 但是，您可以使用批量工作表生成跟踪参数，并在广告网络中手动添加这些参数（根据步骤2）。 要生成跟踪参数，您必须使用&quot;[!UICONTROL EF Redirect]”跟踪方法。 您可以选择添加任何所需的附加参数。

      搜索、社交和商务自动包含参数 `ev_cl={ef_uniqueid}` 在帐户批量工作表中生成的任何跟踪URL中。 此唯一ID用于将促销活动数据与任何成本进行匹配，然后单击您上传的数据。

   1. 设置要跟踪的营销活动：

      1. 在广告网络内，创建一个批量工作表文件，其中包含您希望Search、Social和Commerce跟踪帐户的所有实体及其所需的父实体。

         您可以包含有关关键字的数据，包括父营销活动和广告组。

      1. 编辑批量工作表文件（如有必要），使其遵循“搜索”、“社交”和“商务”规则 [批量处理工作表格式需要 [!DNL Naver] 帐户](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. 在搜索、社交和商务中， [上载批量工作表文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >注意：搜索、社交和商务不会将数据发布到广告网络帐户。

1. 为营销活动设置跟踪：

   1. 在搜索、社交和商务中， [下载新的批量处理工作表文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) 将选项用于&quot;[!UICONTROL Generate Tracking URLs].”
   使用&quot;[!UICONTROL Generate Tracking URLs]”选项填充 [!UICONTROL Destination URL] 每个关键字的字段，其中搜索、社交和商务跟踪代码的前缀为 [!UICONTROL Base URL] 值。

   以下是带有跟踪的目标URL的示例：

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. 复制 [!UICONTROL Destination URL] 下载批量工作表文件中的值到网络上的相关关键字设置。

      您可以通过将文件上传到广告网络编辑器中的网络，将URL添加到相关实体。 在这种情况下，您可能需要根据网络的数据要求删除某些列。 否则，必须在网络上手动输入URL。


1. 定期下载每天从广告网络累计的关键字或广告组级别品牌广告的点击和成本数据，然后 [上传点击和成本数据](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) 在中搜索、社交和商务 [所需格式](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   包括完整的帐户层次结构和要包括的任何指标。 搜索、Social和Commerce会将上传数据与现有营销活动中的数据匹配。

1. （可选）如果您在网页中使用Adobe广告转化跟踪服务标记来跟踪未在广告网络上跟踪的转化，则发送包含每日汇总转化数据的馈送文件以添加到跟踪促销活动。

   有关更多信息，请与您的Adobe客户团队联系。

所有上传的跟踪数据均可从以下位置获取： [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 在 [!UICONTROL Accounts]， [!UICONTROL Campaigns]， [!UICONTROL Ad Groups]、和 [!UICONTROL Keywords] 视图。 它还可以用于中的报告 [!UICONTROL Insights & Reports] 视图。

>[!MORELIKETHIS]
>
>* [附录 — 必需的批量工作表数据 [!DNL Naver] 帐户](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [上传流量和转化量度 [!DNL Naver] 仅跟踪帐户](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [的量度数据要求 [!DNL Naver] 仅跟踪帐户](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [的点击跟踪格式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)

