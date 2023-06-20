---
title: Adobe Advertising对《通用数据保护条例》的支持
description: 了解支持的数据请求类型、所需的设置和字段值，以及使用旧版产品ID和返回的数据字段的API访问请求示例
feature: GDPR
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 071d0ae725c21aaea19072725ae99ca77ef1a410
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 0%

---

# Adobe Advertising对《通用数据保护条例》的支持

*对象 [!DNL Adobe Advertising Search, Social, & Commerce]；Adobe Advertising DSP；Adobe Advertising Creative；Adobe AdvertisingDCO*

>[!IMPORTANT]
>
>本文档的内容不是法律建议，也不会代替法律建议。 请咨询您的法律顾问，以获得有关《通用数据保护条例》的建议。

《通用数据保护条例》(GDPR)法规于2018年5月25日生效，旨在赋予欧盟(EU)境内所有个人（数据主体）对其个人数据的控制权，并简化针对国际业务的监管环境。 该法规适用于向欧盟境内的个人提供商品或服务、监控其行为或从其收集个人数据的所有企业（数据控制者），而不论数据控制者的业务位置如何。

Adobe Experience Cloud充当数据处理者，可处理其代表客户接收并存储的任何个人数据。 作为数据控制者，您可以决定Adobe Experience Cloud代表您处理和存储的个人数据。

本文档介绍如何 [!DNL Advertising Search, Social, & Commerce]；Advertising Creative；Advertising DSP(Demand Side Platform)；和 [!DNL Advertising DCO] 使用Adobe Experience Platform Privacy Service API和Privacy ServiceUI，支持数据主体的GDPR数据访问和删除权限。

有关GDPR对您业务的意义的更多信息，请参阅 [GDPR与您的业务](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Adobe Advertising支持的数据请求类型

Adobe Experience Platform使企业能够完成以下任务：

* 在中访问数据主体的Cookie级别数据或设备ID级别数据（适用于移动设备应用程序中的广告） [!DNL Search, Social, & Commerce]， [!DNL Creative]， [!DNL DSP]，或 [!DNL DCO].
* 删除中存储的Cookie级别数据 [!DNL Search, Social, & Commerce]， [!DNL Creative]， [!DNL DSP]，或 [!DNL DCO] 适用于使用浏览器的数据主体；或删除存储在中的ID级别数据 [!DNL DSP] 适用于在移动设备上使用应用程序的数据主体。
* 检查一个或所有现有请求的状态。

## 发送Adobe Advertising请求所需的设置

要请求访问和删除Adobe Advertising数据，您需要：

1. 部署JavaScript库以检索和删除数据主体Cookie。 同一个图书馆， `AdobePrivacy.js`，用于所有Adobe Experience Cloud解决方案。

   >[!IMPORTANT]
   >
   >对某些Adobe Experience Cloud解决方案的请求不需要JavaScript库，但对Adobe Advertising的请求需要它。

   您应该将库部署在数据主体可以提交访问和删除请求的网页上，例如您公司的隐私门户。 库可帮助您检索AdobeCookie(命名空间ID： `gsurferID`)，以便您可以将这些身份作为访问和删除请求的一部分通过Adobe Experience Platform Privacy Service API提交。

   当数据主体请求删除个人数据时，库还会从数据主体的浏览器中删除数据主体的Cookie。

   >[!NOTE]
   >
   >删除个人数据不同于选择退出，后者会停止使用受众区段定位最终用户。 但是，当数据主体请求从中删除个人数据时 [!DNL Creative]， [!DNL DSP]，或 [!DNL DCO]，则库还会向Adobe Advertising发送请求，以选择退出数据主体进行区段定位。 对于广告商，使用 [!DNL Search, Social, & Commerce]，我们建议您向数据主体提供一个链接， [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html)，其中介绍了如何选择退出受众区段定位。

1. 识别您的Experience Cloud组织ID并确保它已链接到您的Adobe Advertising帐户。

   Experience Cloud的组织ID是由24个字符组成的字母数字字符串，其后附加有“@AdobeOrg”。 已为大多数Experience Cloud客户分配了组织ID。 如果您的营销团队或内部Adobe系统管理员不知道您的组织ID，或不确定它是否已配置，请通过gdprsupport@adobe.com联系Adobe客户关怀团队。 您将需要组织ID才能使用向隐私API提交请求 `imsOrgID` 命名空间。

   >[!IMPORTANT]
   >
   >请联系贵公司的Adobe Advertising代表，以确认贵组织的所有Adobe Advertising帐户，包括 [!DNL DSP] 客户或广告商， [!DNL Search, Social, & Commerce] 帐户，以及 [!DNL Creative] 或 [!DNL DCO] 帐户 — 链接到您的Experience Cloud组织ID。

1. 使用 [ADOBE EXPERIENCE PLATFORM PRIVACY SERVICE API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （适用于自动请求）或 [PRIVACY SERVICEUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hans) （适用于临时请求）代表数据主体向Adobe Advertising提交访问和删除请求，并检查现有请求的状态。

   对于拥有移动应用程序以与数据主体交互并与DSP启动促销活动的广告商，您将需要下载适用于隐私的Mobile SDK以进行Experience Cloud。 Mobile SDK允许数据控制者设置选择退出状态标记、检索数据主体的设备ID（命名空间ID：设备ID），并将请求提交到Privacy ServiceAPI。 您的移动应用程序将需要SDK版本4.15.0或更高版本。

   当您提交数据主体的访问请求时，Privacy ServiceAPI会根据指定的Cookie或设备ID返回数据主体的信息，然后您必须将其返回到数据主体。

   当您提交数据主体的删除请求时，Cookie ID或设备ID以及与Cookie关联的所有成本、点击和收入数据都会从服务器中删除。

   >[!NOTE]
   >
   如果贵公司拥有多个Experience Cloud组织ID，则必须为每个组织发送单独的API请求。 但是，您可以向多个Adobe Advertising子解决方案发出一个API请求([!DNL Search, Social, & Commerce]， [!DNL Creative]， [!DNL DSP]、和 [!DNL DCO])，每个子解决方案具有一个帐户。

所有这些步骤都是进行Adobe Advertising所必需的。 有关您需要使用Adobe Experience Platform Privacy Service执行的这些任务和其他相关任务，以及在何处查找所需项目的更多信息，请参阅 [隐私和GDPR](https://developer.adobe.com/client-sdks/documentation/privacy-and-gdpr/).

## Adobe AdvertisingJSON请求中的必填字段值

&quot;company context&quot;：

* `"namespace": **imsOrgID**`
* `"value":` &lt;*您的IMS组织ID值*>

`"users":`

* `"key":` &lt;*通常为数据主体的名称*>

* `"action":` 任一 `**access**` 或 `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (表示 [!DNL adcloud] cookie space)

   * `"value":` &lt;*从中检索的实际数据主体的Cookie ID值`AdobePrivacy.js`*>

* `"include": **adCloud**` (适用于该请求的Adobe产品)

* `"regulation": **gdpr**` （即适用于请求的隐私法规）

## 数据主体使用从中检索的Adobe Advertising用户ID提交的请求示例 `AdobePrivacy.js`

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

以下是Adobe Advertising的访问响应示例。

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
