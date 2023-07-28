---
title: 将转化量度上传到 [!DNL Google Ads]
description: 了解如何将搜索、社交和商务跟踪的转化量度上传到 [!DNL Google Ads].
exl-id: 88db66c2-12db-41cf-b6c4-ed821cb3b8ea
feature: Search Tools
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# 将转化量度上传到 [!DNL Google Ads]

*广告商使用 [!DNL Google Ads] 仅限帐户*

搜索、社交和商务可以选择上传至 [!DNL Google Ads] 它跟踪的所有转化量度 [!DNL Google Ads] 使用从Adobe Analytics同步的Adobe Advertising转化跟踪服务和转化量度的营销活动。 此选项不使转换可用于混合优化。 如果要将Adobe转化用于混合优化，请参阅&quot;[允许将目标上传到广告网络](objective-upload-to-networks.md)“

每日上传包括跟踪的 `gclid` 值、使用广告商级别归因模型定义的转化值和时间戳。 如果更新了归因模型，则下次上传时将使用新模型，但不会更新过去的数据以使用新模型。

>[!NOTE]
>
>上传内容不包括从馈送文件上传到Adobe Advertising的转化量度。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. 选中旁边的复选框 **[!UICONTROL Upload Conversions to Google Ads]**.

1. 单击 **[!UICONTROL Save]**.

1. （如果在经理帐户级别跟踪您的转化） [为您的经理帐户添加凭据](/help/search-social-commerce/admin/manager-accounts.md) 在 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [允许将目标上传到广告网络](objective-upload-to-networks.md)
