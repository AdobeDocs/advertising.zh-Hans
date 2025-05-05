---
title: 将搜索、社交和Commerce跟踪的转化指标上传至 [!DNL Google Ads]
description: 了解如何将搜索、社交和Commerce跟踪的转化指标上传到 [!DNL Google Ads]。
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# 将搜索、社交和Commerce跟踪的转化指标上传至[!DNL Google Ads]

*仅包含[!DNL Google Ads]帐户和Adobe Advertising转化跟踪的广告商*

Search、Social和Commerce可以选择将其为使用Adobe Advertising转化跟踪服务的[!DNL Google Ads]营销活动跟踪的所有转化指标上传到[!DNL Google Ads]。 此选项不使转换可用于混合优化。 如果要使用Adobe转化进行混合优化，请参阅“启用将目标上传到广告网络[&#128279;](objective-upload-to-networks.md)”。

每日上传包括跟踪的`gclid`值、使用广告商级别归因模型定义的转化值以及时间戳。 如果更新了归因模型，则下次上传时将使用新模型，但不会更新过去的数据以使用新模型。

>[!NOTE]
>
>上传内容不包括从馈送文件上传到Adobe Advertising的转化量度。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**。

1. 选中&#x200B;**[!UICONTROL Upload Conversions to Google Ads]**&#x200B;旁边的复选框。

1. (在欧洲经济区(EEA)或英国(UK)开展业务的广告商；可选)如果您已向EEA和英国用户收集同意以将其数据上传用于广告，请选中&#x200B;**[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**&#x200B;旁边的复选框

1. 单击&#x200B;**[!UICONTROL Save]**。

1. （如果在经理帐户级别跟踪您的转化）[在&#x200B;**[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**&#x200B;为您的经理帐户添加凭据](/help/search-social-commerce/admin/manager-accounts.md)。

>[!MORELIKETHIS]
>
>* [启用将目标上传到广告网络](objective-upload-to-networks.md)
