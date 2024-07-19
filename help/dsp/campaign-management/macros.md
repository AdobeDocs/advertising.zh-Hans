---
title: Advertising DSP宏
description: 引用可用于常规跟踪和跟踪第三方显示广告点击量的宏。
feature: DSP Ads
exl-id: 7058c988-c544-4a61-84dd-eec4ce88ceba
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Advertising DSP宏

宏是指令的简短命令或简称，通常遵循格式`${MACRO_NAME}`。 创意代码或点进URL中包含的宏可展开为广告服务器可以理解的较长代码字符串。 DSP广告服务器在投放或单击广告时执行宏。

广告服务器宏可用于将重要信息传递到DSP或第三方广告服务器。 宏最常在第三方和自定义创意代码或元数据（如第三方像素）贩运期间使用。

您可以在任意位置手动插入宏，例如在VAST标记中、在任何URL中，或者在DSP或第三方事件像素中。 但是，每个DSP客户端和合作伙伴具有不同的广告标记格式，因此应将宏相应地插入标记中的不同位置。 每次与新客户或合作伙伴合作时，请向他们索取相关文档，了解如何在其广告标记中插入DSP流量的宏。

## 常规跟踪宏

根据需要，对所有广告和标记类型使用常规跟踪宏以传递特定数据。

| 宏 | 替代描述 | 类型 |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | 帐户ID。 | 整数 |
| `${TM_AD_ID}` | 广告键(adKey)。 | 字符串 |
| `${TM_AD_ID_NUM}` | 广告ID。 | 整数 |
| `${TM_ADVERTISER_ID}` | 广告商ID。 | 整数 |
| `${TM_CAMPAIGN_ID}` | 营销活动密钥。 | 字符串 |
| `${TM_CAMPAIGN_ID_NUM}` | 营销活动ID。 | 整数 |
| ` ${TM_CLICK_URL}` | 重定向URL，允许广告服务器跟踪和计数广告点击量。 当投放广告时，如果用户单击该广告，则会激活宏，并且会记录单击次数并计入报表中。 | 字符串 |
| ` ${TM_CLICK_URL_URLENC}` | 经过编码的重定向URL，允许广告服务器跟踪和计数广告点击量。 当投放广告时，如果用户单击该广告，则会激活宏，并且会记录单击次数并计入报表中。 除非您正在创建第三方广告，并且您的供应商需要URL编码，否则请勿使用此宏。 | 字符串 |
| `${TM_FEED_ID}` | 媒体投放的键(feedKey)。 | 字符串 |
| `${TM_FEED_ID_NUM}` | 媒体投放的ID。 | 整数 |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | 投放位置的站点键。 [!DNL AppsFlyer]点击跟踪器对于移动设备应用程序安装广告是必需的。<!-- should map to placement_site_key column of placement_site table --> | 字符串 |
| `${TM_PLACEMENT_ID}` | 放置键(cpKey)。 | 字符串 |
| `${TM_PLACEMENT_ID_NUM}` | 版面ID。 | 整数 |
| `${TM_RANDOM}` | Cachebuster：介于1和1000000之间的随机数。 | 长 |
| `${TM_SESSION_ID}` | 会话的ID，对应于对广告标记的单次检索。 | 字符串 |
| `${TM_SITE_DOMAIN_URLENC}` | 从竞价请求中的URL解析的页面子域；URL编码。 不支持在横幅中点击播放的广告。 | 字符串 |
| ` ${TM_SITE_NAME}` | 投放位置的站点名称。 | 字符串 |
| `${TM_SITE_URL_URLENC}` | 在竞价请求中传递的URL；URL编码。 不支持在横幅中点击播放的广告。 | 字符串 |
| `${TM_SITE_ID_NUM}` | 投放的网站ID。 | 整数 |
| `${TM_TIMESTAMP}` | Unix时间戳表示自1970年1月1日午夜(00:00 UTC)以来经过的秒数。 | 长 |
| ` ${TM_VIDEO_DURATION}` | 广告视频的持续时间（以秒为单位）。 | 整数 |

{style="table-layout:auto"}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## 特定于移动设备的宏

| 宏 | 替代描述 | 类型 |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore])与设备的操作系统对应的平台ID：<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>当平台不是上述任何平台时`other`</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore])设备型号名称，以URL编码。 | 字符串 |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore])投放广告的环境：<ul><li>`a` =移动应用程序</li><li>`b` =移动网站</li></ul> | 字符串（`a`或`b`） |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen])与设备的操作系统对应的平台ID：<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>当平台不是上述任何平台时`other`</li></ul> | 字符串 |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen])广告作为查看者的设备类型：<ul><li>`TAB` =平板电脑</li><li>`PHN` =移动设备</li><li>`computer` =计算机</li></ul> | 字符串 |
| `${UOO}` | ([!DNL Nielsen])用户是否已选择退出广告跟踪：<ul><li>`1` （DNT标志= 1） =用户已选择退出广告跟踪</li><li>`0` （DNT标志= 0） =用户已选择加入广告跟踪</li></ul> | 整数（`0`或`1`） |
| `${TM_BUNDLE}` | [!DNL iOS]或[!DNL Android]应用商店捆绑包标识。 示例： com.zynga.wwf2.free或id804379658 | 字符串 |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}`指示投标人是否确定投标请求来自欧盟来源并要求GDPR实施：<ul><li>`1` =应强制执行GDPR</li><li>`0` =不应强制GDPR</li></ul>`gdpr_consent=${GDPR_CONSENT}`是从入站竞价请求中的供应合作伙伴传递的同意值：<ul><li>在大多数情况下，这是base64url编码的同意字符串，或daisybit（示例：BN5lERiOMYEdiAKAWXEND1HoSBE6CAFApAMgBkIDIgM0AgOJxAnQA）</li><li>`0` =不同意</li><li>`1` =同意</li></ul> | Daisybit或整数 |

{style="table-layout:auto"}

## 单击第三方显示广告的宏

要使用第三方显示标记准确跟踪广告的点击量，DSP需要显示点击宏。 只需要宏的一个版本；相关的宏取决于标记类型。

| 宏 | 替代描述 | 类型 |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | 使广告服务器能够跟踪和计数平台中的广告点击的重定向URL。 | 字符串 |
| `${TM_CLICK_URL_URLENC}` | 重定向URL，允许需要URL编码的广告服务器跟踪和计数平台中的广告点击量。 | 字符串 |

{style="table-layout:auto"}

在以下情况下，DSP会在第三方显示标签中自动插入显示单击宏：

* 从广告服务器合作伙伴<!-- [Needs PM confirmation.] -->导出广告标记
* 直接在DSP中批量上传[!DNL Flashtalking]或[!DNL Google DoubleClick for Advertisers]广告标记

如果在构建显示广告时缺少单击宏，DSP将显示一条警告消息，提示您手动在标签的正确区域插入相应的显示单击宏。

## [!DNL Analytics for Advertising]宏

有关[[!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)客户专门可用的其他宏，请参阅“[将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Flashtalking] 广告标签](/help/integrations/analytics/macros-flashtalking.md)”和“[将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Google Campaign Manager 360] 广告标签](/help/integrations/analytics/macros-google-campaign-manager.md)”。

## 宏错误疑难解答

将宏添加到代码时，请确保使用宏的确切语法。 验证宏时，DSP会检查宏是否与有效宏之一完全匹配。

如果宏名称的开头或结尾缺少字符，则会生成错误。 例如，如果出现以下情况，则显示错误消息：

* 您忘记了宏名称开头的一个或多个字符，如`${`。 如果不包括完整语法，则无法将条目识别为有效的宏。
* 宏的结尾不是一组有效的字符，如`}`。

>[!MORELIKETHIS]
>
>* [音频广告设置](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [已连接电视广告设置](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [显示广告设置](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [移动广告设置](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [本机广告设置](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [前置广告设置](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [通用视频广告设置](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
