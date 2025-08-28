---
source-git-commit: 91610ee5e1741f19dde5567b806e05f1034397c0
workflow-type: tm+mt
source-wordcount: '988'
ht-degree: 0%

---
# ADOBE ADVERTISING AMO ID {#amo-id}

AMO ID在较低的粒度级别跟踪每个唯一的广告组合，用于[!DNL Analytics]和Customer Journey Analytics数据分类以及从Adobe Advertising引入广告量度（例如展示次数、点击量和成本）。

对于[!DNL Analytics]，AMO ID存储在[eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)或rVar维度(AMO ID)中。

对于Customer Journey Analytics，AMO ID存储在`trackingCode`对象的`conversionDetails`属性中，该对象是[!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]的一部分。

AMO ID也称为`s_kwcid`，有时发音为“[!DNL squid]”。

### （[!DNL Analytics]用户）实施AMO ID的方法 {#amo-id-implement}

<!-- Add info about implementing in CJA -->

参数可通过以下方式之一添加到您的跟踪URL中：

* （推荐）实施服务器端插入功能时。

   * DSP客户：当最终用户查看带有Adobe Advertising像素的显示广告时，像素服务器会自动将s_kwcid参数附加到您的登陆页后缀。

   * 搜索、社交和Commerce客户：

      * 对于已为帐户或营销活动启用[!DNL Google Ads]设置的[!DNL Microsoft Advertising]和[!UICONTROL Auto Upload]帐户，当最终用户单击带有Adobe Advertising像素的广告时，像素服务器会自动将s_kwcid参数附加到您的登陆页后缀。

      * 对于其他广告网络，或禁用了[!DNL Google Ads]设置的[!DNL Microsoft Advertising]和[!UICONTROL Auto Upload]帐户，请手动将该参数添加到您的[帐户级别的附加参数](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}，这些参数会将其附加到您的基本URL。

* 未实施服务器端插入功能时：

   * DSP客户： [JavaScript代码](javascript.md)会自动记录点进和显示点进。 当浏览器不支持第三方Cookie时，您仍然可以跟踪以下广告类型的基于点击的转化：

      * 对于[!DNL Flashtalking]广告标记，请手动插入每个“[将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Flashtalking] 广告标记](/help/integrations/analytics/macros-flashtalking.md)”的其他宏。 **注意：**&#x200B;如果您的组织与[!DNL Flashtalking]直接合作，并且您根据`s_kwcid`支持文档(位于`ef_id`https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros[!DNL Flashtalking])使用数据传递宏跟踪[和](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros)跟踪参数，则不需要执行此过程。

      * 对于[!DNL Google Campaign Manager 360]广告标记，请手动插入每个“[将 [!DNL Analytics for Advertising] 宏附加到 [!DNL Google Campaign Manager 360] 广告标记](/help/integrations/analytics/macros-google-campaign-manager.md)”的其他宏。

   * 搜索、社交和Commerce客户：

      * 对于（[!DNL Google Ads]和[!DNL Microsoft Advertising]）广告，请手动将AMO ID参数添加到登陆页面后缀，最好在[帐户级别](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}添加，除非需要对各个帐户组件进行不同的跟踪。

      * 对于所有其他广告网络上的广告，请手动将AMO ID参数添加到您的[帐户级别的附加参数](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}，这会将其附加到您的基本URL。

要实施服务器端插入功能或确定最适合您的企业的选项，请联系您的Adobe客户团队。

### AMO ID格式 {#amo-id-formats}

#### [!DNL DSP]的AMO ID格式

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

其中：

* `AC`指示显示渠道。

* `{TM_AD_ID}`是Adobe Advertising生成的字母数字广告键。 它使用广告的唯一标识符，并用作将Adobe Advertising实体元数据转换为可读[!DNL Analytics]和Customer Journey Analytics维度的键。

* `{TM_PLACEMENT_ID}`是Adobe Advertising生成的字母数字放置键。 它使用了投放的唯一标识符，并用作将Adobe Advertising实体元数据转换为可读[!DNL Analytics]和Customer Journey Analytics维度的键。

示例AMO ID： AC！iIMvXqlOa6Nia2lDvtgw！GrVv6o2oV2qQLjQiXLC7

#### 搜索、社交和Commerce广告的AMO ID格式 {#amo-id-format-search}

这些参数因广告网络而异，但以下参数是所有参数共有的：

* `AL`指示搜索渠道。<!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}`是分配给广告商的唯一用户ID。

* `{sid}`已被广告商广告网络帐户的数值ID替换：*的* 3[!DNL Google Ads]，*的* 10[!DNL Microsoft Advertising]，*的* 45[!DNL Meta]，*的* 86[!DNL Yahoo! Display Network]，*的* 87[!DNL Naver]，*的* 88[!DNL Baidu]，*的* 90[!DNL Yandex]，*94* [!DNL Yahoo! Japan Ads]的&#x200B;*、* 105[!DNL Yahoo Native]（已弃用）或&#x200B;*的* 106[!DNL Pinterest]（已弃用）。

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!88!{creative}!{placement}!{keywordid}`

其中：

* `{creative}`是广告网络的唯一创意数字ID。
* `{placement}`是点击了广告的网站。
* `{keywordid}`是触发广告的关键字的广告网络的唯一数值ID。

##### [!DNL Google Ads]

包括使用[!DNL Google Merchant Center]的购物营销活动。

* 使用最新AMO ID格式（支持营销活动和广告组级别报表以实现最佳效果营销活动以及草稿和实验营销活动）的帐户：

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* 所有其他帐户：

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

其中：

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}`是创意的[!DNL Google Ads]唯一数字ID。
* `{matchtype}`是触发广告的关键字的匹配类型：精确为`e`，短语为`p`，广泛为`b`。
* `{placement}`是广告被点击网站的域名。 值适用于以投放位置为目标的促销活动中的广告，以及内容网站上显示的以关键词为目标的促销活动中的广告。
* `{network}`指示发生点击的网络：`g`搜索的[!DNL Google]（仅关键词定向广告）、`s`搜索合作伙伴的（仅关键词定向广告）或显示网络的`d`（关键词定向或投放目标广告）。
* `{product_partition_id}`是与产品广告一起使用的产品组的广告网络的唯一数值ID。
* `{keyword}`是触发您的广告的特定关键词（在搜索网站上）或最佳匹配关键词（在内容网站上）。
* `{campaignid}`是广告网络的营销活动唯一数字ID。
* `{adgroupid}`是广告组的广告网络的唯一数字ID。

>[!NOTE]
>
>* 对于动态搜索广告，{keyword}填充了自动定位。
>* 当您为[!DNL Google]购物广告生成跟踪时，产品ID参数`{adwords_producttargetid}`将插入到关键词参数之前。 产品ID参数未出现在[!DNL Google Ads]帐户级别和营销活动级别的跟踪参数中。
>* 若要使用最新的AMO ID跟踪代码，请参阅“[更新 [!DNL Google Ads] 帐户](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)的AMO ID跟踪代码”<!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!45!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* 所有营销活动类型：

  `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

其中：

* `{AdId}`是广告网络的唯一创意数字ID。
* `{OrderItemId}`是关键词的广告网络的数字ID。
* `{CampaignId}`是广告网络的营销活动唯一数字ID。
* `{AdGroupId}`是广告组的广告网络的唯一数字ID。

>[!NOTE]
>
> 对于其营销活动没有[!UICONTROL Auto Upload]跟踪选项且尚未迁移到新格式的帐户，请手动更新每个登陆页面后缀以包含上述格式。
> >与此同时，旧版格式（如下所示）仍然有效：
>* 搜索促销活动：
>  >  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* 购物营销活动（使用[!DNL Microsoft Merchant Center]）：
>  >  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* 受众网络营销活动：
>  >  `s_kwcid=AL!{userid}!10!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!94!{creative}!{matchtype}!{network}!{keyword}`

其中：

* `{creative}`是广告网络的唯一创意数字ID。
* `{matchtype}`是触发广告的关键字的匹配类型：精确为`be`，短语为`bp`，广泛为`bb`。
* `{network}`指示发生点击的网络： `n`用于本机，或`s`用于搜索。
* `{keyword}`是触发广告的关键字。

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!90!{ad_id}!{source_type}!!!{phrase_id}`

其中：

* `{ad_id}`是广告网络的唯一创意数字ID。
* `{source_type}`是显示广告的网站类型：搜索为&#x200B;*b*，上下文（内容）为&#x200B;*c*，类别为&#x200B;*ct*。
* `{phrase_id}`是关键词的广告网络的数字ID。
