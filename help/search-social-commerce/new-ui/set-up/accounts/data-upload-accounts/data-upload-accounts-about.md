---
title: null
description: null
source-git-commit: f2b29c2f3a38cadc31a9b3110aa82feadd62e5cc
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# 关于上传用于报告和模拟的帐户数据

<!-- Move all related files into one page? -->

如果您使用搜索、社交和Commerce不提供API支持的在线广告网络，则可以上传促销活动内容和离线成本、点击次数和转化数据，以便帐户进行报表和性能模拟。 具有[[!DNL Adobe Analytics for Advertising] 集成](/help/integrations/analytics/overview.md)的广告商还可以在Adobe Analytics中查看其帐户的数据。

此功能适用于遵循标准三层营销活动结构(营销活动、广告组或广告集以及竞价单位（广告或关键词）)的广告网络。 对于Adobe DSP，该功能适用于分配给包的包和投放位置，但不适用于具有投放位置级别步调的营销活动或投放位置。

对以下网络提供开箱即用支持：<!-- But what if you want to use something else? Is that possible currently? -->

<!-- * Adobe Demand Side Platform (Advertising DSP) [Is any data upload required, or just an initial setup of an S3 bucket and/or something else, and then DSP sends the data automatically? If so, then I may need to reframe this whole chapter accordingly.] -->
<!-- * [!DNL Reddit Ads] -->

* [!DNL Apple Search Ads]
* [!DNL LinkedIn Ads]
* [!DNL TikTok Ads]

此功能不支持搜索、社交和Commerce点击跟踪以及Adobe Advertising转化跟踪。

## 搜索、社交和Commerce中可用的功能

* 跟踪和报告：

   * 在营销活动管理视图中，将只读营销活动组件细化到竞价单位级别。

   * 在营销活动管理视图和自定义报表中，将性能数据降至广告组级别<!-- verify the entity level -->。 此外，在为该广告商指定的Adobe Analytics报表包中，具有[!DNL Adobe Analytics for Advertising]的广告商将获取低至广告组级别<!-- verify the entity level -->的业绩数据。&lt;！ — 验证数据类型是否受限 — 成本、点击量、显示展示次数、收入？—>

* 将营销活动添加到项目组合时的性能模拟。<!-- How does this even work? Do they need to be in standard or hybrid portfolios, with active or optimized status, and can you mix these campaigns with API-synced campaigns? If so, do we just ignore these campaigns and optimize the others? -->

  搜索、Social和Commerce不会优化产品组合中此类促销活动的任何内容，甚至不会投标。

## 用于设置脱机帐户的工作流

<!-- subtitle wording? -->

1. [设置虚拟帐户记录](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md)。

1. 为单个帐户<!--  in what file format? -->创建数据文件，包括促销活动、广告组和广告在天级别的状态。

数据必须遵循广告网络的数据要求，因此每个实体的数据字段可能因广告网络而异。

1. <!-- For all ad networks (excluding DSP), -->通过以下任一方式上传单个帐户的初始数据：

* 从设备或网络手动上传文件。

* 将数据上传到[!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3])存储段中的Search、Social和Commerce分配的文件夹。

  >[!PREREQUISITES]
  >
  >* 请联系您的Adobe客户团队，为您的Search、Social和Commerce广告商帐户启用帐户数据上传。 团队将协助在[!DNL S3]存储桶中创建特定于组织的文件夹，并在完成时通知您。<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
  >* 检索您帐户的[!DNL S3]云存储路径、访问密钥ID和访问密钥。 组织的所有数据上传<!-- naming convention?-->帐户均使用相同的访问密钥ID和秘密访问密钥。

1. 继续每天上传新数据文件。

1. 上传30天的数据后，您可以选择将营销活动添加到<!--what type? how should we refer to them? -->项目组合并生成模拟。

您可以[查看每个数据上载的日志](upload-log.md)以查看其状态。 此外，如果您启动上载操作，但上载未完全成功，则根据通知设置，您会通过[通知中心](/help/search-social-commerce/notifications/notification-about.md)收到错误通知。

<!-- Data validation, and any troubleshooting? -->

>[!MORELIKETHIS]
>
>* [关于上载用于报告和模拟的帐户数据](data-upload-accounts-about.md)
>* [将帐户数据上传到 [!DNL Amazon] [!DNL S3]存储段](upload-data-from-s3-bucket.md)
>* [手动上载帐户数据](upload-data-manually.md)
>* [查看已上载帐户数据文件的日志](upload-log.md)
>* [管理用于数据上载的广告网络帐户](/help/search-social-commerce/campaign-management/accounts/data-upload-account-manage.md)
