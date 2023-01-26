---
title: Adobe对《通用数据保护条例》的广告支持
description: 了解支持的数据请求类型、必需的设置和字段值，以及使用旧版产品ID和返回的数据字段的API访问请求示例
feature: GDPR
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# Adobe对《通用数据保护条例》的广告支持

*对于 [!DNL Adobe Advertising Search];Adobe广告DSP;Adobe广告创意；和Adobe广告DCO*

>[!IMPORTANT]
>
>本文档的内容不是法律建议，也不会代替法律建议。 请咨询您的法律顾问，以获取有关《通用数据保护条例》的建议。

2018年5月25日生效的《通用数据保护条例》(GDPR)法规赋予欧盟(EU)境内所有个人（数据主体）对其个人数据的控制权，并简化了国际业务的监管环境。 本法适用于在欧盟境内为个人提供商品或服务、监控其行为或从其个人收集个人数据的所有企业（数据控制者），无论数据控制者的业务位置如何。

Adobe Experience Cloud充当数据处理者，处理其代表客户接收和存储的任何个人数据。 作为数据控制者，您可以决定Adobe Experience Cloud代表您处理和存储的个人数据。

本文档介绍如何 [!DNL Advertising Search];广告创意；Advertising DSP(Demand Side Platform);和 [!DNL Advertising DCO] 使用Adobe Experience Platform Privacy Service API和Privacy ServiceUI支持数据主体的GDPR数据访问和删除权限。

有关GDPR对您业务的意义的更多信息，请参阅 [GDPR与您的业务](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## 支持的Adobe广告数据请求类型

Adobe Experience Platform为企业提供了完成以下任务的功能：

* 在 [!DNL Search], [!DNL Creative], [!DNL DSP]或 [!DNL DCO].
* 删除中存储的Cookie级数据 [!DNL Search], [!DNL Creative], [!DNL DSP]或 [!DNL DCO] 对于使用浏览器的数据主体；或删除存储在 [!DNL DSP] 适用于在移动设备上使用应用程序的数据主体。
* 检查一个或多个现有请求的状态。

## 发送Adobe广告请求所需的设置

要请求访问和删除Adobe广告的数据，您需要：

1. 部署JavaScript库以检索和删除数据主体Cookie。 同一个图书馆， `AdobePrivacy.js`，用于所有Adobe Experience Cloud解决方案。

   >[!IMPORTANT]
   >
   >对某些Adobe Experience Cloud解决方案的请求不需要JavaScript库，但Adobe广告的请求需要它。

   您应该在网页上部署库，数据主体可以从中提交访问和删除请求，例如您公司的隐私门户。 库可帮助您检索AdobeCookie(命名空间ID: `gsurferID`)，以便您能够在访问和删除请求中通过Adobe Experience Platform Privacy Service API提交这些身份。

   当数据主体要求删除个人数据时，库还会从数据主体的浏览器中删除数据主体的Cookie。

   >[!NOTE]
   >
   >删除个人数据与选择退出不同，选择退出会阻止使用受众区段的最终用户进行定位。 但是，当数据主体要求从 [!DNL Creative], [!DNL DSP]或 [!DNL DCO]，该库还会向Adobe广告发送请求，以从区段定位中选择禁用数据主体。 对于具有 [!DNL Search]，我们建议您向数据主体提供一个链接 [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html)，其中说明了如何选择退出受众区段定位。

1. 识别您的Experience Cloud组织ID，并确保它已关联到您的Adobe广告帐户。

   Experience Cloud组织ID是由24个字符组成的字母数字字符串，其后附加有“@AdobeOrg”。 大多数Experience Cloud客户都分配了组织ID。 如果您的营销团队或内部Adobe系统管理员不知道您的组织ID，或者不确定是否已配置，请通过gdprsupport@adobe.com联系Adobe客户关怀团队。 您需要组织ID才能使用 `imsOrgID` 命名空间。

   >[!IMPORTANT]
   >
   >联系贵公司的Adobe广告代表，以确认贵组织的所有Adobe广告帐户(包括 [!DNL DSP] 帐户或广告商， [!DNL Search] 帐户和 [!DNL Creative] 或 [!DNL DCO] 帐户 — 已关联到您的Experience Cloud组织ID。

1. 使用 [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （对于自动请求）或 [Privacy ServiceUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) （对于临时请求）代表数据主体向Adobe广告提交访问和删除请求，并检查现有请求的状态。

   对于拥有移动应用程序以与数据主体进行交互并使用DSP启动促销活动的广告商，您将需要下载隐私就绪的移动SDK以进行Experience Cloud。 Mobile SDK允许数据控制者设置选择退出状态标记，检索数据主体的设备ID(命名空间ID:设备ID)，并向Privacy ServiceAPI提交请求。 您的移动设备应用程序将需要SDK版本4.15.0或更高版本。

   在您提交数据主体的访问请求时，Privacy ServiceAPI会根据指定的Cookie或设备ID返回数据主体的信息，然后您必须将该信息返回到数据主体。

   在您提交数据主体的删除请求时，将从服务器中删除Cookie ID或设备ID以及与Cookie关联的所有成本、点击和收入数据。

   >[!NOTE]
   如果您的公司有多个Experience Cloud组织ID，则必须为每个IP发送单独的API请求。 但是，您可以向多个Adobe广告子解决方案([!DNL Search], [!DNL Creative], [!DNL DSP]和 [!DNL DCO])，每个子解决方案具有一个帐户。

所有这些步骤对于Adobe广告都是必需的。 有关使用Adobe Experience Platform Privacy Service执行这些任务和其他相关任务以及在何处查找所需项目的更多信息，请参阅 [www.adobe.io/apis/cloudplatform/gdpr.html](https://www.adobe.io/apis/experienceplatform/gdpr.html).

## Adobe广告JSON请求中的必填字段值

&quot;&quot;company context&quot;:

* `"namespace": **imsOrgID**`
* `"value":` &lt;*您的IMS组织ID值*>

`"users":`

* `"key":` &lt;*通常是数据主体的名称*>

* `"action":` e `**access**` 或 `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (表示 [!DNL adcloud] cookie空间)

   * `"value":` &lt;*实际数据主体的Cookie ID值，检索自`AdobePrivacy.js`*>

* `"include": **adCloud**` (即适用于请求的Adobe产品)

* `"regulation": **gdpr**` （即适用于该请求的隐私法规）

## 数据主体使用从中检索的Adobe广告用户ID提交的请求示例 `AdobePrivacy.js`

```
{
"companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
  "userIDs":[
      {
         "namespace":"411",
         "value":"Wqersioejr-wdg",
         "type":"namespaceId",
         "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"gdpr"
}
}
```

## 为访问请求返回的数据字段

以下是Adobe广告的访问响应示例。

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
