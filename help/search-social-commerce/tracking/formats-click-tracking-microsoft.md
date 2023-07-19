---
title: 的点击跟踪格式 [!DNL Microsoft Advertising]
description: 了解的点击跟踪格式 [!DNL Microsoft Advertising] 帐户。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# 的点击跟踪格式 [!DNL Microsoft Advertising]

以下是Search、Social和Commerce所需的基本跟踪模板和登陆页面后缀（最终URL后缀）格式 [!DNL Microsoft Advertising].

## 跟踪模板格式

### 搜索和受众网络（站点链接除外）

以下格式适用于搜索和受众网络上的所有可跟踪广告类型。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

示例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe广告中广告商唯一ID的变量。
>
>* 此格式表示已为营销活动启用令牌传递（默认）。 如果禁用令牌传递，请替换 `cq?` 之后 `<advertiser_ID>` 替换为 `c?`.
>
>* `{TargetId}` 表示a)关键字或b)触发广告的关键字和再营销列表（受众）（例如，对于关键字和再营销列表，“kwd-123：aud-456”，或仅对于关键字，“kwd-123”）的ID。


### 站点链接

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

示例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe广告中广告商唯一ID的变量。
>
>* 此格式表示已为营销活动启用令牌传递（默认）。 如果禁用令牌传递，请替换 `cq?` 之后 `<advertiser_ID>` 替换为 `c?`.
>
>* `{TargetId}` 表示a)关键字或b)触发广告的关键字和再营销列表（受众）（例如，对于关键字和再营销列表，“kwd-123：aud-456”，或仅对于关键字，“kwd-123”）的ID。
>
>* `{adextensionid}` 未使用。
>
>* （站点链接）您可以通过生成 [!UICONTROL Transaction Report]. 此 [!UICONTROL Link Type] sitelink的列值为 `sl:<Sitelink text>`，例如 `sl:See Current Offers`.


### 购物网络

以下格式适用于购物网络中的购物广告。 您可以在帐户、营销策划、广告组或产品组级别指定跟踪模板。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

示例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` 是Adobe广告中广告商唯一ID的变量。
>
>* 此格式表示已为营销活动启用令牌传递（默认）。 如果禁用令牌传递，请替换 `cq?` 之后 `<advertiser_ID>` 替换为 `c?`.
>
>* `{TargetId}` 表示a)关键字或b)触发广告的关键字和再营销列表（受众）（例如，对于关键字和再营销列表，“kwd-123：aud-456”，或仅对于关键字，“kwd-123”）的ID。
>
>* （可选）您可以将跟踪URL添加到中的产品数据，而不是在帐户、营销活动、广告组或产品组级别输入跟踪模板。 [!DNL Microsoft Merchant Center] 帐户。 为此，请包含跟踪URL以及“”中的值`link`“或”`mobile_link`”字段（根据需要）[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)”在产品信息源中。 “”中的值`bingads_redirect`“ ”字段将替换“ ”中的值`link`“ ”和“ ”`mobile_link`”字段。 使用此方法生成的URL不包括在Search、Social和Commerce帐户或营销活动设置中指定的任何跟踪参数。


## 登陆页面后缀（最终URL后缀）格式

>[!NOTE]
>
>较低级别的登陆页面后缀将覆盖帐户级别的后缀。 为便于维护，除非需要对各个帐户组件进行不同的跟踪，否则请仅使用帐户级别的后缀。 要在广告组级别或更低级别配置后缀，请使用广告网络的编辑器。

### 搜索和受众网络

使用Adobe广告转化跟踪的帐户必须包含广告网络的点击标识符(`msclkid` 对象 [!DNL Microsoft Advertising])的句子中输入：

* 当广告商具有Adobe Analytics集成时，后缀必须包含以下内容：

   `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* 当广告商没有Adobe Analytics集成时，后缀必须包含以下内容：

   `&ev_efid={msclkid}:G:s`

### 购物网络

使用Adobe广告转化跟踪的帐户必须包含广告网络的点击标识符(`msclkid` 对象 [!DNL Microsoft Advertising])的句子中输入：

* 当广告商具有Adobe Analytics集成时，后缀必须包含以下内容：

   `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* 当广告商没有Adobe Analytics集成时，后缀必须包含以下内容：

   `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [关于Adobe广告转化跟踪服务的点击跟踪URL格式](formats-click-tracking-about.md)
>* [s\_kwcid跟踪代码的格式](skwcid-tracking-parameter.md)
