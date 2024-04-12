---
title: 点击跟踪URL的可选跟踪参数
description: 了解可选的搜索、社交和商务跟踪参数以及可添加到点击跟踪URL的广告网络特定的跟踪参数。
exl-id: df53bb8c-63ad-47f9-af44-57bd4bd58d71
feature: Search Tracking
source-git-commit: c743e0dec75578d739a704ef94f96dd7be4f982e
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# 点击跟踪URL的可选跟踪参数

*[!DNL Google Ads]， [!DNL Microsoft® Advertising]， [!DNL Yahoo! Japan]、和 [!DNL Yandex] 仅限帐户*

您可以添加更多参数来跟踪广告网络帐户的特定数据，而不是只使用最终URL或目标URL的标准跟踪参数。 您可以在帐户设置或营销活动设置中添加以下参数的任意组合：

* 您可以将任何静态文本字符串作为参数附加到帐户/营销策划的基本URL中。

* 您可以在客户/促销活动的基本URL中附加特定于Adobe Advertising和广告网络的参数，以跟踪更多数据：

   * Adobe Advertising参数是半静态的。 Adobe Advertising在将基本URL上传到广告网络时插入数据值。 例如，当您在 `campaign={ef_campaign}` 对于基本URL，Adobe Advertising会替换 `{ef_campaign}` 上传URL时使用实际的促销活动名称（例如“返校促销活动”）。

     **注意：** 插入值后，它们将保持静态。 如果您将关键词或广告移动到其他广告组，或将广告组移动到其他营销活动，则  {ef_adgroup} 或 {ef_campaign} 参数不会自动更新，因此您必须手动生成新的目标URL或基本（最终）URL。

   * 广告网络特定的参数是动态的，搜索引擎会在用户单击广告时插入数据值。 例如，当您在 `{param1}` 对于基本URL，广告网络会将其替换为实际URL {param1} 值。

>[!NOTE]
>
>* 用逗号或&amp;符号(`&`)。
>* 以下参数不区分大小写。
>* 附加参数中的特殊字符在生成的目标URL或基本（最终）URL中按以下方式替换：
>  * `=` 替换为 `%3D`
>  * `?` 替换为 `%26`
>  * 空格被替换为 `%2B`
>  例如，在附加参数时 `campaign={ef_campaign}` 到关键字的基本URL http://www.example.com ，则该关键字的基本URL将生成为 `http://www.example.com/campaign%3D{ef_campaign}`.

## 搜索、社交和商务静态跟踪参数

您可以为任何广告网络上的帐户使用以下参数，并可以根据需要将其与特定广告网络的参数组合。 当帐户的跟踪方法为“”时，其中一些参数会复制为特定广告网络自动添加的参数[!UICONTROL EF Direct]“

以下所有参数都必须指定为键值对；您可以为一个值对包括多个参数。 例如，要插入促销活动名称，请使用 `<your_parameter_name>={ef_campaign}`，例如 `campaign={ef_campaign}`. 要使用指定的匹配类型名称插入匹配类型，请使用 `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`，例如 `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. 不适用的匹配类型不会出现在生成的URL中。

| 参数 | 描述 |
| ---- | ---- |
| <code>{custom_code}</code> | 将上传批量工作表文件中“自定义URL参数”列的数据插入跟踪URL。 {custom_code} 只能在跟踪URL中的一个或多个键值对的值末尾使用。 示例：  <code>a={custom_code}</code>； <code>a={ef_campaignid}{custom_code}</code>； <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>注意：</b> 要将批量处理工作表文件中的自定义值插入到跟踪URL中，请使用“生成跟踪URL”选项上载批量处理工作表文件。 有关使用批量处理工作表文件的更多信息，请参阅“[关于使用批量处理工作表管理营销活动数据](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)“ |
| <code>{ef_uniqueid}</code> | 插入由Adobe Advertising创建的唯一ID。 当跟踪方法为“EF重定向”时自动添加。 |
| <code>{ef_userid}</code> | 插入Adobe Advertising分配给广告商的唯一用户ID。 |
| <code>{ef_sid}</code> | 要插入Search、Social &amp; Commerce分配给广告网络的数字ID，请执行以下操作： <i>[!UICONTROL 3]</i> 对象 [!DNL Google Ads]， <i>[!UICONTROL 10]</i> 对象 [!DNL Microsoft®® Advertising]， <i>[!UICONTROL 45]</i> 对象 [!DNL Meta]， <i>[!UICONTROL 86]</i> 对象 [!DNL Yahoo! Display Network]， <i>[!UICONTROL 87]</i> 对象 [!DNL Naver]， <i>[!UICONTROL 88]</i> 对象 [!DNL Baidu]， <i>[!UICONTROL 90]</i> 对象 [!DNL Yandex]， <i>[!UICONTROL 94]</i> 对象 [!DNL Yahoo! Japan Ads]， <i>[!UICONTROL 105]</i> 对象 [!DNL Yahoo Native] （已弃用），或 <i>[!UICONTROL 106]</i> 对象 [!DNL Pinterest] （已弃用）。 |
| <code>{ef_searchengine}</code> | 插入广告网络名称。 |
| <code>{ef_campaign}</code> | 插入促销活动名称。 |
| <code>{ef_campaignid}</code> | 插入促销活动ID。 <b>注意：</b> 只有在营销活动发布到广告网络后，才会创建新营销活动ID。 如果帐户使用&quot;[!UICONTROL EF Redirect]”和“自动上传”选项，然后Adobe Advertising会在第二天自动将促销活动ID插入到相关的目标URL或最终URL中。 如果帐户不使用&quot;[!UICONTROL EF Redirect]”和 [!UICONTROL Auto Upload]选项，并且要将促销活动ID插入到相关的目标URL或最终URL，则必须创建促销活动；使用“生成跟踪URL”选项下载新促销活动的批量工作表文件；然后将文件发布到广告网络。 |
| <code>{ef_adgroup}</code> | 插入广告组名称。 |
| <code>{ef_adgroupid}</code> | 插入广告组ID。 <b>注意：</b> 在将广告组发布到广告网络之前，不会创建新广告组的ID。 如果帐户使用&quot;[!UICONTROL EF Redirect]”和“自动上传”选项，然后Adobe Advertising会在第二天自动将广告组ID插入到相关的目标URL或最终URL中。 如果帐户不使用[!UICONTROL EF Redirect]”和 [!UICONTROL Auto Upload]选项，并且您要将广告组ID插入到相关的目标URL或最终URL，则必须创建广告组；使用“生成跟踪URL”选项下载适用于新广告组的批量处理工作表文件，然后将文件发布到广告网络。 |
| <code>{ef_keyword}</code> | 插入关键字。 |
| <code>{ef_keywordid}</code> | 插入关键字ID。 <b>注意：</b> 只有在将新关键字发布到广告网络后，才会创建该关键字的ID。 如果帐户使用&quot;[!UICONTROL EF Redirect]”和 [!UICONTROL Auto Upload]”选项，然后Adobe Advertising会在第二天自动将关键字ID插入到相关的目标URL或最终URL中。 如果帐户不使用&quot;[!UICONTROL EF Redirect]”和 [!UICONTROL Auto Upload]”选项，并且您要将关键字ID插入到相关的目标URL或最终URL，则必须创建关键字；使用“生成跟踪URL”选项下载新关键字的批量工作表文件；然后将文件发布到广告网络。 |
| <code>{ef_matchtype}</code> | 将关键词匹配类型插入为“广泛”、“精确”或“短语”。 自动包括用于 [!DNL Google Ads] 和 [!DNL Microsoft® Advertising] 带有&quot;[!UICONTROL EF Redirect]”跟踪方法。 |
| <code>{ef_adid}</code> | 插入广告ID。 <b>注意：</b> 只有在将新广告发布到广告网络后，才会创建该广告的ID。 如果帐户使用&quot;[!UICONTROL EF Redirect]”和 [!UICONTROL Auto Upload]”选项，则Adobe Advertising会在第二天自动将广告ID插入到相关的目标URL或最终URL中。 如果帐户不使用&quot;[!UICONTROL EF Redirect]”和 [!UICONTROL Auto Upload]选项，并且要将广告ID插入相关的目标URL或最终URL，则必须创建广告；使用“生成跟踪URL”选项下载新广告的批量处理工作表文件；然后将文件发布到广告网络。 |

## [!DNL Google Ads] 动态跟踪参数

请参阅 [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## [!DNL Microsoft® Advertising] 动态跟踪参数

请参阅 [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## 雅虎！ 日本Ads动态跟踪参数

请参阅 [https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## [!DNL Yandex] 动态跟踪参数

请参阅 [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [关于Adobe Advertising转化跟踪服务的点击跟踪URL格式](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
