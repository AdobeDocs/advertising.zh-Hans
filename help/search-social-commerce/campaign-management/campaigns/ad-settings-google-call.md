---
title: ’[!DNL Google Ads] 仅限呼叫的广告设置
description: 引用设置 [!DNL Google Ads] 仅限呼叫的广告。
exl-id: 1f810c2b-9c30-43c6-bda6-07609423ef79
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# [!DNL Google Ads] 仅限呼叫的广告设置

您可以为使用搜索网络的营销活动创建仅限呼叫的文本广告。

搜索、Social和Commerce使用帐户级别的登陆页面后缀和跟踪模板跟踪仅限呼叫的广告，但您可以选择在中覆盖帐户级别的跟踪 [!DNL Google Ads] 经理。

请参阅 [!DNL Google Ads] 帮助 [每个帐户的广告限制](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]：** 企业的名称。 最大长度为25个字符或12个双字节字符。

**[!UICONTROL Country]：** （可选）企业所在的国家/地区。

**[!UICONTROL Phone Number]：** 公司的电话号码。 示例：(124) 123-4567、12345678901、+441234567890。

**[!UICONTROL Description 1]， [!UICONTROL Description 2]：** 广告主体的第一和第二行。 每行的最大长度为35个字符或17个双字节字符。

关键字替换语法不计入最大长度。 例如，“`{Description1: Free Account Analysis!}`“ ”将被视为22个字符（仅限“免费帐户分析\！”部分）。

>[!NOTE]
>
>描述字段不能包含电话号码。

**[!UICONTROL Display URL]：** 广告中显示的URL。 显示URL必须与与您的业务关联的域匹配，但广告不会将用户发送到登陆页面。

最大长度为35个单字节字符或17个双字节字符。 关键字替换语法不计入最大长度。 例如，“`{DisplayURL: example.com}`“”被视为11个字符（仅部分“example.com”）。

**[!UICONTROL Verification URL]：** （可选）广告电话号码以文本形式显示的网页，以便 [!DNL Google Ads] 可以验证电话号码是否有效。 它必须与广告的显示URL具有相同的域。

**[!UICONTROL Is Tracked]：** 启用呼叫跟踪和仅限呼叫的转换。

**[!UICONTROL Count calls as phone call conversions]：** (当&quot;[!UICONTROL Is Tracked]”处于选中状态；可选)如果指定了电话转换类型，则将广告产生的所有呼叫归因于这种类型。 否则， [!DNL Google Ads] 创建一个名为“”的默认转化操作[!UICONTROL Calls from ads]&quot;一旦它记录到您的转发号码中的至少一个转化，然后将呼叫归因于它。

**[!UICONTROL Count Action]：** (当&quot;[!UICONTROL Count calls as phone call conversions]”处于选中状态；可选)将调用归因到的现有转化操作。

您可以在中创建和管理转化操作 [!DNL Google Ads].

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [关于广告](ad-about.md)
>* [管理广告](ad-manage.md)
>* [[!DNL Google Ads] 扩展的动态搜索广告设置](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] 响应式搜索广告设置](ad-settings-google-rsa.md)
