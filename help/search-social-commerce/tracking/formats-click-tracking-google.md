---
title: 的点击跟踪格式 [!DNL Google Ads]
description: 了解的点击跟踪格式 [!DNL Google Ads] 帐户。
exl-id: 68f6da43-3430-4c0a-9369-937fa52c071a
feature: Search Tracking
source-git-commit: 0c2603303dd9401b2d6fad2893f5a84cb457ed3a
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# 的点击跟踪格式 [!DNL Google Ads]

以下是Search、Social和Commerce所需的基本跟踪模板和登陆页面后缀（最终URL后缀）格式 [!DNL Google Ads].

## 跟踪模板格式

### 搜索/显示网络，包括站点链接

以下格式适用于搜索和显示网络以及站点链接上的所有可跟踪广告类型。

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

示例：

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe Advertising中广告商唯一ID的变量。
>
>* 此格式表示为营销活动启用令牌传递（默认）。 如果禁用令牌传递，则替换 `cq?` 之后 `<advertiser_ID>` 替换为 `c?`.
>
>* 此 [!DNL ValueTrack] 跟踪模板中用于指示最终URL的参数必须为 `{lpurl}` 或 `!{unescapedurl}`.
>
>* （文本广告）按关键字竞价时，参数 `ev_pl` （适用于投放位置）没有值。 当按投放位置竞价时， `ev_ln` （对于关键字）没有值。 当您按广告组或任何其他维度竞价时，两者 `ev_ln` 和 `ev_pl` 没有值。
>
>* （动态搜索广告） `{keyword}` 指示动态搜索目标表达式，例如 `_cat:[VALUE]` 或 `_url:[VALUE]`.
>
>* （动态搜索广告） [!DNL Google Ads] 可动态确定最终URL，因此您无需输入URL。
>
>* （站点链接）您可以通过生成 [!UICONTROL Transaction Report]. 此 [!UICONTROL Link Type] sitelink的列值为 `sl:<Sitelink text>`，例如 `sl:See Current Offers`.

### 购物网络

以下格式适用于购物网络中的购物广告和产品组。 您可以在帐户、营销策划、广告组或产品组级别指定跟踪模板。

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

示例：

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe Advertising中广告商唯一ID的变量。
>
>* 此格式表示为营销活动启用令牌传递（默认）。 如果禁用令牌传递，则替换 `cq?` 之后 `<advertiser_ID>` 替换为 `c?`.
>
>* 此 [!DNL ValueTrack] 跟踪模板中用于指示最终URL的参数必须为 `{lpurl}` 或 `!{unescapedurl}`.
>
>* [!DNL Google Ads] 会使用Google商家中心信息源中的产品URL作为最终URL，因此您无需为产品数据或产品组输入最终URL。
>
>* 您可以通过生成转化来查看点击购物广告产生了哪些转化 [!UICONTROL Transaction Report]. 此 [!UICONTROL Link Type] 产品广告的列值为pla：`<product ID>`，例如 `pla:8525822`.

## 登陆页面后缀（最终URL后缀）格式

使用Adobe Advertising转化跟踪的帐户必须包含广告网络的点击标识符(`gclid` 对象 [!DNL Google Ads])进行标记：

* 当广告商具有Adobe Analytics集成时，后缀必须包括以下任一项：

   * [!DNL Google Ads] 使用最新版本的帐户 [AMO ID格式](/help/integrations/analytics/ids.md#amo-id-formats) (开始于 `s_kwcid`)，支持针对效果最佳的营销活动、草稿和实验营销活动的营销活动和广告组级别报表：

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     如果帐户具有服务器端AMO ID实施以及帐户或营销活动设置»[!UICONTROL Auto Upload]”已启用，则会自动添加参数。 否则，您需要手动添加它。 请参阅中的“实施AMO ID的方法”[使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id-implement)“

   * 所有其他 [!DNL Google Ads] 帐户：

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* 当广告商没有Adobe Analytics集成时，后缀必须包括以下内容：

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* 较低级别的登陆页面后缀将覆盖帐户级别的后缀。 为便于维护，除非需要对各个帐户组件进行不同的跟踪，否则请仅使用帐户级别的后缀。 要在广告组级别或更低级别配置后缀，请使用广告网络的编辑器。
>
>* (动态搜索广告；具有Adobe Analytics但不具有服务器端跟踪的广告商)如果您希望包含对从Adobe Advertising到Analytics的反向馈送的跟踪，请将AMO ID跟踪代码附加到帐户级别的登陆页面后缀的末尾。

>[!MORELIKETHIS]
>
>* [关于Adobe Advertising转化跟踪服务的点击跟踪URL格式](formats-click-tracking-about.md)
>* [AMO ID格式](/help/integrations/analytics/ids.md#amo-id-formats)
