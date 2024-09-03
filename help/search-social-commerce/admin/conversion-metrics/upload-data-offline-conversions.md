---
title: 上载离线转化数据以增强转化
description: 了解如何上传第一方离线转化数据以映射到潜在客户的 [!DNL Google Ads] 增强型转化。
feature: Conversions
source-git-commit: c3cb1549adeb7b621c1b426c53da9bb09eddcbdc
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# 上载离线转化数据以增强转化

仅&#x200B;*[!DNL Google Ads]个帐户*

<!-- Tweak metadata title/description and heading -->

您可以上传第一方离线转化数据（包括经过哈希处理的电子邮件地址和电话号码），以映射到潜在客户的现有[[!DNL Google Ads] 增强型转化](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)。 所有上传的数据已实时同步到[!DNL Google Ads]。

## 为潜在客户上传[!DNL Google Ads]增强型转化数据

1. 在主菜单中，单击&#x200B;**[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**，然后单击&#x200B;**[!UICONTROL Upload]**&#x200B;选项卡。

1. 选择广告网络，然后选择帐户。

1. （可选）若要下载包含[!DNL Microsoft Excel]格式的所有[必需数据字段](#enhanced-conversions-leads-data)的模板，请单击&#x200B;**[!UICONTROL View Template]**，然后按照浏览器的正常程序下载该文件。

   您可以编辑文件以包含数据并保存更改，然后在下一步中上传文件。

1. 单击&#x200B;**[!UICONTROL Choose File]**，然后选择要从设备或网络上传的文件。

## 已上传文件的必需数据 {#enhanced-conversions-leads-data}

### 该表上方的数据

`Parameters:TimeZone=insert_timezone`

在此位置或在每行的“[!UICONTROL Conversion Time]”列中输入帐户的时区。 使用a) [支持的时区ID格式](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids)或b) GMT偏移(如+或 — 和4位数的时间差（如–0500表示纽约）。

### 表列和值

| 列 | 描述 |
| ------ | ----------- |
| 电子邮件 | 用户的电子邮件地址，必须使用SHA-256算法进行哈希处理。 每一行必须包含电子邮件值或电话号码值。 |
| 电话号码 | 用户的电话号码，必须使用SHA-256算法进行哈希处理。 它必须包含国家/地区代码，并且可能包含破折号和其他符号。 每一行必须包含电子邮件值或电话号码值。 |
| 转化名称 | （必需）转换操作的名称。 |
| 转化时间 | （必需）转换事件发生的时间采用[支持的时间格式](https://support.google.com/google-ads/answer/7014069#prepare_data)。 如果您在数据表上方的`Parameters:TimeZone=insert_timezone`行中未包含帐户的时区ID，则请使用a) [支持的时区ID格式](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids)或b) GMT偏移量（如+或 — 所示）和4位数的时间差（例如，纽约为–0500）来包含每行的时区。 |
| 转化值 | （必需）数字转换值。 |
| 转换货币 | 兑换事件的货币代码。 |
| 广告用户数据 | (适用于与欧洲经济区(EEA)或英国(UK)中的用户相关的数据)指示是否同意将用户数据发送到[!DNL Google]以进行广告个性化。 值可以包括`Granted`、`Denied`或\[null\]（作为`Unspecified`发送到[!DNL Google Ads]）。 **注意：** [!DNL Google Ads]当前不强制潜在客户同意增强型转化，但将来可能会强制同意。 |
| 广告Personalization | (适用于欧洲经济区(EEA)或英国(UK)中与用户相关的数据)指示是否同意将用户数据发送到[!DNL Google]以进行广告。 值可以包括`Granted`、`Denied`或\[null\]（作为`Unspecified`发送到[!DNL Google Ads]）。 **注意：** [!DNL Google Ads]当前不强制潜在客户同意增强型转化，但将来可能会强制同意。 |

>[!MORELIKETHIS]
>
>* [为潜在客户的 [!DNL Google Ads] 增强型转化创建转化操作](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [为潜在客户实施 [!DNL Google Ads] 增强的转化](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [将搜索、社交和Commerce跟踪的转化量度上传到 [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
