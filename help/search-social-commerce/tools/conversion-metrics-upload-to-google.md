---
title: 将转化量度上传到 [!DNL Google Ads]
description: 了解如何将搜索、社交和商务跟踪的转化量度上传到 [!DNL Google Ads].
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: e8eabf7e4aa7c9201cd8198aae32d325b2858f2b
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# 将转化量度上传到 [!DNL Google Ads]

*广告商使用 [!DNL Google Ads] 仅限帐户*

搜索、社交和商务可以选择上传至 [!DNL Google Ads] 它跟踪的所有转化量度 [!DNL Google Ads] 使用Adobe Advertising转化跟踪服务的营销活动。 此选项不使转换可用于混合优化。 如果要将Adobe转化用于混合优化，请参阅&quot;[允许将目标上传到广告网络](objective-upload-to-networks.md)“

每日上传包括跟踪的 `gclid` 值、使用广告商级别归因模型定义的转化值和时间戳。 如果更新了归因模型，则下次上传时将使用新模型，但不会更新过去的数据以使用新模型。

>[!NOTE]
>
>上传内容不包括从馈送文件上传到Adobe Advertising的转化量度。

1. 在主菜单中，单击 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. 选中旁边的复选框 **[!UICONTROL Upload Conversions to Google Ads]**.

1. (在欧洲经济区(EEA)或英国(UK)开展业务的广告商；可选)如果您已向EEA和英国用户收集同意以上传其数据用于广告，请选中 **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. 单击 **[!UICONTROL Save]**.

1. （如果在经理帐户级别跟踪您的转化） [为您的经理帐户添加凭据](/help/search-social-commerce/admin/manager-accounts.md) 在 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [允许将目标上传到广告网络](objective-upload-to-networks.md)
