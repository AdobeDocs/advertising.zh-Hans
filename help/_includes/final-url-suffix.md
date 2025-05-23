---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# 最终URL后缀定义

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]：** （仅限[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户；可选）要附加到最终URL末尾以跟踪信息的所有参数；包括您的企业必须跟踪的所有参数。 示例：`param1=value1&param2=value2`

在使用Adobe Advertising转化跟踪的帐户中，后缀必须包含广告网络的点击标识符（[!DNL Microsoft Advertising]为`msclkid`；[!DNL Google Ads]为`gclid`）。

具有Adobe Analytics集成的帐户必须使用[AMO ID](/help/integrations/analytics/ids.md)参数。 如果该帐户具有服务器端AMO ID实施，则当用户单击广告时，参数会自动添加；否则，您必须在此处手动添加该参数。 查看 [!DNL Google Ads][&#128279;](/help/search-social-commerce/tracking/formats-click-tracking-google.md)的[必需后缀格式和 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)的必需后缀格式。

>[!NOTE]
>
>* [!UICONTROL Auto Upload]跟踪设置未更新此字段。
>* 较低级别的最终URL后缀将覆盖帐户级别的后缀。 为便于维护，除非需要对各个帐户组件进行不同的跟踪，否则请仅使用帐户级别的后缀。 要在广告组级别或更低级别配置后缀，请使用广告网络的编辑器。
