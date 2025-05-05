---
title: 实施 [!DNL Naver] 仅跟踪帐户
description: 了解如何为您的 [!DNL Naver] 帐户设置跟踪营销活动，以便您可以跟踪、报告和可视化直接从广告网络购买的广告的表现。
exl-id: acbaf4f0-eb55-4788-bc84-c3181d635f1d
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# 实施[!DNL Naver]仅跟踪帐户

仅&#x200B;*[!DNL Naver]个帐户*

您可以为[!DNL Naver]帐户创建跟踪营销活动，以便能够跟踪、报告和可视化您直接从广告网络购买的广告的表现。 搜索、社交和Commerce不会将数据与广告网络同步、自动上传跟踪或对帐户投标。

跟踪营销活动可复制您现有的营销活动、广告组和关键词。 在Search、Social和Commerce中创建帐户结构并向广告网络内的原始促销活动添加跟踪后，即可上传关键词或广告的每日网络流量量度。 然后，搜索、Social和Commerce可以将您的转化归因于广告和关键词。

您可以跟踪所有促销活动以及任何单个促销活动、广告组或关键词/广告的绩效指标。 您还可以在最基本、高级和辅助报表中包含有关这些广告网络的信息，以及其他广告网络的数据。 不支持将量度导出到Adobe Analytics，但Search、Social和Commerce可以将您在 [!DNL Analytics][&#128279;](/help/integrations/analytics/analytics-data-in-advertising.md)中跟踪的量度同步到Search、Social和Commerce。

>[!NOTE]
>
>您无法将跟踪营销活动添加到项目组合以进行优化。

1. 在Search、Social和Commerce中创建跟踪活动：

   1. 创建[虚拟网络帐户详细信息](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)。 如果单个广告网络中有多个帐户，请在[!UICONTROL Accounts]视图中将其合并为一个帐户。

      [!DNL Naver]不提供将跟踪参数上传到广告网络的API支持。 但是，您可以使用批量工作表生成跟踪参数，并在广告网络中手动添加这些参数（根据步骤2）。 要生成跟踪参数，必须使用&quot;[!UICONTROL EF Redirect]&quot;跟踪方法。 您可以选择添加任何所需的附加参数。

      Search、Social和Commerce会自动将参数`ev_cl={ef_uniqueid}`包含在它在帐户的批量处理工作表内生成的任何跟踪URL中。 此唯一ID用于将促销活动数据与任何成本进行匹配，并单击您上传的数据。

   1. 设置要跟踪的营销活动：

      1. 在广告网络中，创建一个批量工作表文件，其中包含您希望Search、Social和Commerce跟踪帐户的所有实体及其所需的父实体。

         您可以包含有关关键字的数据，包括父营销活动和广告组。

      1. 如有必要，请编辑批量工作表文件，使其遵循 [!DNL Naver] 帐户[&#128279;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)所需的Search、Social和Commerce 批量工作表格式。

      1. 在Search、Social和Commerce中，[上传批量处理工作表文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md)。

         >[!NOTE]
         >
         >注意：搜索、社交和Commerce不会将数据发布到广告网络帐户。

1. 设置对营销活动的跟踪：

   1. 在Search、Social和Commerce中，[使用“[!UICONTROL Generate Tracking URLs]”选项下载新的批量处理工作表文件](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)。

   使用“[!UICONTROL Generate Tracking URLs]”选项会使用前缀为[!UICONTROL Base URL]值的Search、Social和Commerce跟踪代码填充每个关键字的[!UICONTROL Destination URL]字段。

   以下是带有跟踪的目标URL的示例：

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. 将下载的批量处理工作表文件中的[!UICONTROL Destination URL]值复制到网络上的相关关键字设置中。

      您可以通过将文件上传到广告网络编辑器中的网络，将URL添加到相关实体。 在这种情况下，您可能需要根据网络的数据要求删除某些列。 否则，必须在网络上手动输入URL。

1. 每天从广告网络定期下载您正在跟踪的关键字或广告组级别品牌广告的点击和成本数据，然后[&#128279;](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)按照[所需格式](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)将点击和成本数据上传到Search、Social和Commerce。

   包括完整的帐户层次结构和要包括的任何量度。 搜索、Social和Commerce会将上传的数据与现有营销活动中的数据匹配。

1. （可选）如果您在网页中使用Adobe Advertising转化跟踪服务标签来跟踪未在广告网络上跟踪的转化，则发送包含每日汇总转化数据的馈送文件，以添加到您的跟踪促销活动。

   有关更多信息，请与您的Adobe客户团队联系。

在[!UICONTROL Accounts]、[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]和[!UICONTROL Keywords]视图中，所有上传的跟踪数据均可从[!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]使用。 它还可用于[!UICONTROL Insights & Reports]视图中的报告。

>[!MORELIKETHIS]
>
>* [附录 —  [!DNL Naver] 帐户](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)的必需批量工作表数据
>* [上传 [!DNL Naver] 仅跟踪帐户的流量和转化量度](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [仅跟踪帐户 [!DNL Naver] 的量度数据要求](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>*  [!DNL Naver][&#128279;](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)的点击跟踪格式
