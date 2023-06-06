---
title: 实施 [!DNL Google Ads] 效果最佳营销活动
description: 了解设置的工作流 [!DNL Google Ads] 效果最佳的营销活动。
source-git-commit: 333d32963b96d2add1d99b2e27d7725341b4cfdf
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# 实施 [!DNL Google Ads] 效果最佳营销活动

In [!DNL Google Ads] 效果最佳的营销活动，您无需设置广告组、广告或关键字。 相反，您可以在促销活动设置中指定一个或多个资产组，包括标题、描述以及上传的图像、徽标和 [!DNL YouTube videos]. [!DNL Google Ads] 自动组合资产以根据渠道提供广告(例如 [!DNL YouTube]， [!DNL Gmail]，或 [!DNL Search])。

您可以在中查看效果最佳的现有促销活动，以及采用表格和趋势图格式的效果数据。 [!DNL Campaigns] 视图；数据在较低级别不可用。 报告和Adobe Analytics中也提供了营销活动级别的效果数据(适用于具有 [Analytics集成](/help/integrations/analytics/overview.md). 要查看效果最佳促销活动的效果数据，请执行以下操作： [!DNL Analytics]，营销活动必须使用 [已升级s_kwcid跟踪代码](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md) （跟踪促销活动ID和广告组ID）。

>[!NOTE]
>
>* 您必须手动上传所有图像文件。 链接到 [!DNL Google Merchant Center] 不支持产品馈送。
>* 只有所需的设置可用。 对于可选设置，请登录 [!DNL Google Ads] 编辑者。
>* 不支持列出组。 要管理和查看列表组的数据，请登录 [!DNL Google Ads] 编辑者。


## 要设置的步骤 [!DNL Google Ads] 效果最佳营销活动

您可以从以下位置单独设置效果最佳的促销活动： [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 视图。

1. [创建营销活动](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) 具有营销活动类型 **[!UICONTROL Performance Max]**.

   指定 [!UICONTROL Campaign Details]， [!UICONTROL Budget Options]， [!UICONTROL Campaign Targeting]、和 [!UICONTROL URL Options]. （可选）输入 [!UICONTROL Negative Keywords]，输入 [!UICONTROL Negative Websites]，和/或覆盖 [!UICONTROL Campaign Tracking] 选项。

1. 为营销活动创建资源组并上传资源：

   1. 在Campaign设置的底部，单击 **[!UICONTROL Manage Asset Groups]**.

   1. 指定第一个资产组的设置，并上传该资产组的图像、徽标和可选视频。

      参见 [资源组设置的描述](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) 了解要求和规格。

   1. 根据需要添加其他资源组。

1. 单击 **[!UICONTROL Post]**.

1. （可选）将营销活动添加到混合项目组合以进行优化。
