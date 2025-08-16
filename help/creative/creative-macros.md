---
title: 可用于跟踪URL的宏
description: 引用可添加到登陆页面URL、跟踪URL和第三方创意内容的宏。
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 可用于跟踪URL的宏

<!-- More feature metadata???  -->

您可以在第三方创意内容中、体验的第三方跟踪URL中以及登陆页面URL中包含以下任意宏，以供您自行使用。

一些可用的宏或其等效宏会自动包含在体验标记中。

<!-- Later: 

| Macro | Description | Automatically in experience tags for Advertising DSP? | Automatically in experience tags for [!DNL Google Campaign Manager 360]? |
| --- | --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Tracks and reports the campaign ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ebuy!` |
| `${TM_SITE_ID_NUM}` | Tracks and reports the site ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%esid!` |
| `${TM_PLACEMENT_ID_NUM}` | Tracks and reports the placement ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%epid!` |
| `${TM_AD_ID_NUM}` | Tracks and reports the ad ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%eaid!` |
| `${TM_CREATIVE_ID_NUM}` | Tracks and reports the creative ID from the DSP | N/A | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ecid!` |
| `${TM_SESSION_ID}` | Tracks and reports the impression ID from the DSP. If a value isn't returned, Advertising Creative generates one. | Yes | &mdash; |
| `${TM_ACC_EXPERIENCE_ID}` | Tracks and reports the Advertising Creative experience ID | &mdash; | &mdash; |
| `${TM_ACC_CREATIVE_ID}` | Tracks and reports the Advertising Creative creative ID | &mdash; | &mdash; |
| `${TM_RANDOM}` | A random number between 1 and 1000000 | &mdash; | &mdash; |
| `${TM_TIMESTAMP}` | The Unix Timestamp (in seconds) | &mdash; | &mdash; |
| `${TM_CLICK_URL_URLENC}` | (For third-party ads from vendors who require URL encoding) The encoded click redirect URL, which enables ad servers to track and count ad clicks. When the ad is served and the user clicks on it, the macro is activated, and the click is recorded and counted for reporting purposes. | Yes | &mdash; |

-->

| 宏 | 描述 | 是否自动在Advertising DSP的Experience Tags中启用？ |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | 从DSP跟踪和报告营销活动ID | 是 |
| `${TM_SITE_ID_NUM}` | 从DSP跟踪和报告网站ID | 是 |
| `${TM_PLACEMENT_ID_NUM}` | 从DSP跟踪和报告版面ID | 是 |
| `${TM_AD_ID_NUM}` | 从DSP跟踪和报告广告ID | 是 |
| `${TM_CREATIVE_ID_NUM}` | 从DSP跟踪和报告创意ID | 不适用 |
| `${TM_SESSION_ID}` | 跟踪并报告来自DSP的展示ID。 如果不返回值，Advertising Creative将生成一个值。 | 是 |
| `${TM_ACC_EXPERIENCE_ID}` | 跟踪和报告Advertising Creative体验ID | — |
| `${TM_ACC_CREATIVE_ID}` | 跟踪和报告Advertising Creative创意ID | — |
| `${TM_RANDOM}` | 介于1和1000000之间的随机数 | — |
| `${TM_TIMESTAMP}` | UNIX®时间戳（以秒为单位） | — |
| `${TM_CLICK_URL_URLENC}` | （适用于来自需要URL编码的供应商的第三方广告）经过编码的点击重定向URL，使广告服务器能够跟踪和计数广告点击次数。 当用户单击广告时，将激活宏，并且会记录该点击并计入报表中。 | 是 |

>[!MORELIKETHIS]
>
>* [将标准创意添加到创意库](/help/creative/creative-libraries/creative-add-standard.md#creative-add-third-party)
>* [标准创意设置](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party)
>* [目标体验设置](/help/creative/experiences/experience-settings-targeting.md)
>  >*[非目标体验设置](/help/creative/experiences/experience-settings-no-targeting.md)
