---
title: “[!DNL Google Ads]仅调用广告设置”
description: 引用 [!DNL Google Ads] 纯呼叫广告的设置。
exl-id: 10672771-53fd-4ce9-9d67-6b1f8f5a41b8
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# [!DNL Google Ads]仅限呼叫的广告设置

您可以为使用搜索网络的营销活动创建仅限呼叫的文本广告。

Search、Social和Commerce使用帐户级别的登陆页面后缀和跟踪模板跟踪仅限呼叫的广告，但您可以选择在[!DNL Google Ads]管理器内的广告级别覆盖帐户级别的跟踪。

有关每个帐户](https://support.google.com/google-ads/answer/6372658?hl=en)的[广告限制，请参阅[!DNL Google Ads]帮助。

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]：**&#x200B;业务的名称。 最大长度为25个字符或12个双字节字符。

**[!UICONTROL Country]：**（可选）业务所在的国家/地区。

**[!UICONTROL Phone Number]：**&#x200B;公司的电话号码。 示例：(124) 123-4567、12345678901、+441234567890。

**[!UICONTROL Description 1]，[!UICONTROL Description 2]：**&#x200B;广告正文的第一行和第二行。 每行的最大长度为35个字符或17个双字节字符。

关键字替换语法不计入最大长度。 例如，“`{Description1: Free Account Analysis!}`”被视为22个字符（只有“免费帐户分析\！”部分）。

>[!NOTE]
>
>描述字段不能包含电话号码。

**[!UICONTROL Display URL]：**&#x200B;广告中显示的URL。 显示URL必须与与您的业务关联的域匹配，但广告不会将用户发送到登陆页面。

最大长度为35个单字节字符或17个双字节字符。 关键字替换语法不计入最大长度。 例如，“`{DisplayURL: example.com}`”被视为11个字符（只有“example.com”部分）。

**[!UICONTROL Verification URL]：**（可选）广告电话号码以文本形式显示的网页，以便[!DNL Google Ads]可以验证电话号码是否有效。 它必须与广告的显示URL具有相同的域。

**[!UICONTROL Is Tracked]：**&#x200B;启用呼叫跟踪和仅呼叫转换。

**[!UICONTROL Count calls as phone call conversions]：** （当选择“[!UICONTROL Is Tracked]”时；可选）将广告产生的所有呼叫归因于特定类型的电话转换（当指定一种类型的电话转换时）。 否则，[!DNL Google Ads]在记录来自您的转发号码的至少一次转化后，会创建一个名为“[!UICONTROL Calls from ads]”的默认转化操作，然后将其调用归因于它。

**[!UICONTROL Count Action]：** （选择“[!UICONTROL Count calls as phone call conversions]”时；可选）调用所归因的现有转换操作。

您可以在[!DNL Google Ads]中创建和管理转化操作。

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [关于广告](ad-about.md)
>* [管理广告](ad-manage.md)
>* [[!DNL Google Ads] 扩展的动态搜索广告设置](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] 响应式搜索广告设置](ad-settings-google-rsa.md)
