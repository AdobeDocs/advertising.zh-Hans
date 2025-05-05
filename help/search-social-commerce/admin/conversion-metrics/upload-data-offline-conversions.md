---
title: 上载离线转化数据以增强转化
description: 了解如何上传第一方离线转化数据以映射到潜在客户的 [!DNL Google Ads] 增强型转化和 [!DNL Microsoft Advertising] 增强型转化。
feature: Conversions
exl-id: 5c5dfbb8-3b17-4973-8012-fc7f0e97e33b
source-git-commit: eb7320fdddce4895a689c32ec6fb1e44cb8f2705
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# 上载离线转化数据以增强转化

仅&#x200B;*[!DNL Google Ads]和[!DNL Microsoft Advertising]帐户*

您可以上传第一方离线转化数据（包括经过哈希处理的电子邮件地址和电话号码），以映射到潜在客户的现有[[!DNL Google Ads] 增强转化](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)和[[!DNL Microsoft Advertising] 增强转化](https://help.ads.microsoft.com/#apex/ads/en/60178)。 所有上传的数据都会实时同步到广告网络。

## 上传数据以增强转化

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**，然后单击&#x200B;**[!UICONTROL Upload]**&#x200B;选项卡。

1. 选择广告网络，然后选择帐户。

1. （可选）若要下载包含[!DNL Microsoft Excel]格式的所有[必需数据字段](#enhanced-conversions-leads-data)的模板，请单击&#x200B;**[!UICONTROL View Template]**，然后按照浏览器的正常程序下载该文件。

   您可以编辑文件以包含数据并保存更改，然后在下一步中上传文件。

1. 单击&#x200B;**[!UICONTROL Choose File]**，然后选择要从设备或网络上传的文件。

## 已上传文件的必需数据 {#enhanced-conversions-leads-data}

### 该表上方的数据

`Parameters:TimeZone=insert_timezone`

在此位置或在每行的“[!UICONTROL Conversion Time]”列中输入帐户的时区。 使用a\) ([!DNL Google Ads only]) [支持的时区ID格式](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids)或b\)GMT偏移，如+或 — 和4位数的时间差（例如，纽约为–0500，柏林为+0100，格林尼治标准时间为+0000）。

### [!DNL Google Ads]的表列和值

| 列 | 描述 |
| ------ | ----------- |
| 电子邮件 | 用户的电子邮件地址，必须使用SHA-256算法进行哈希处理。 每一行必须包含电子邮件值或电话号码值。 |
| 电话号码 | 用户的电话号码，必须使用SHA-256算法进行哈希处理。 它必须包含国家/地区代码，并且可能包含破折号和其他符号。 每一行必须包含电子邮件值或电话号码值。 |
| 转化名称 | （必需）转换操作的名称。 |
| 转化时间 | （必需）转换事件发生的时间采用[支持的时间格式](https://support.google.com/google-ads/answer/7014069#prepare_data)。 如果您在数据表上方的`Parameters:TimeZone=insert_timezone`行中未包含帐户的时区ID，请使用a\) [支持的时区ID格式](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids)或b\)GMT偏移量和4位数的时间差（例如，纽约为–0500，柏林为+0100，格林威治标准时间为+000）包含每行的时区。 |
| 转化值 | （必需）数字转换值。 |
| 转换货币 | 兑换事件的货币代码。 |
| 广告用户数据 | (适用于与欧洲经济区(EEA)或英国(UK)中的用户相关的数据)指示是否同意将用户数据发送到[!DNL Google]以进行广告个性化。 值可以包括`Granted`、`Denied`或\[null\]（作为`Unspecified`发送到[!DNL Google Ads]）。 **注意：** [!DNL Google Ads]当前不强制潜在客户同意增强型转化，但将来可能会强制同意。 |
| 广告Personalization | (适用于欧洲经济区(EEA)或英国(UK)中与用户相关的数据)指示是否同意将用户数据发送到[!DNL Google]以进行广告。 值可以包括`Granted`、`Denied`或\[null\]（作为`Unspecified`发送到[!DNL Google Ads]）。 **注意：** [!DNL Google Ads]当前不强制潜在客户同意增强型转化，但将来可能会强制同意。 |

### [!DNL Microsoft Advertising]的表列和值

有关使用该模板的更多说明，请参阅[https://help.ads.microsoft.com/#apex/3/56852](https://help.ads.microsoft.com/#apex/3/56852)。

| 列 | 描述 |
| ------ | ----------- |
| 转化名称 | （必需）转化目标的名称。 |
| 转化时间 | （必需）发生转化事件的时间。 如果不在数据表上方的`Parameters:TimeZone=insert_timezone`行中包括帐户的时区ID，则使用GMT偏移量包括每行的时区，如+或 — 和4位数的时间差（例如，纽约为–0500，柏林为+0100，格林威治标准时间为+000）。 有关各个城市的时区列表，请参阅[https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones)，但请确保使用此处指定的格式而不是时区列表中的格式。 |
| 转化值 | （必需）数字转换值。 |
| 转换货币 | 兑换事件的货币代码。 |
| Microsoft点击ID | 关联的唯一[!DNL Microsoft]点击标识符(MSCLKID)。 对于增强的离线转化，此字段可能为空。 |
| 经过哈希处理的电子邮件地址 | 用户的电子邮件地址，必须使用SHA-256算法进行哈希处理。 对于增强的离线转化，每一行必须包含“哈希电子邮件地址”值或“哈希电话号码”值。 |
| 散列电话号码 | 用户的电话号码，必须使用SHA-256算法进行哈希处理。 它必须包含国家/地区代码，并且可能包含破折号和其他符号。 对于增强的离线转化，每一行必须包含“哈希电子邮件地址”值或“哈希电话号码”值。 |

>[!MORELIKETHIS]
>
>* [为潜在客户实施 [!DNL Google Ads] 增强的转化](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [实施 [!DNL Microsoft Advertising] 增强的脱机转换](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* ([!DNL Google Ads only]) [为潜在客户的 [!DNL Google Ads] 增强型转化创建转化操作](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [将搜索、社交和Commerce跟踪的转化量度上传到 [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
