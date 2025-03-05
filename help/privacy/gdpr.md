---
title: Adobe Advertising对《通用数据保护条例》的支持
description: 了解支持的数据请求类型、所需的设置和字段值，以及使用旧版产品ID和返回的数据字段的API访问请求示例
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Adobe Advertising对《通用数据保护条例》的支持

*适用于[!DNL Adobe Advertising Search, Social, & Commerce]、Adobe Advertising DSP、Adobe Advertising Creative和Adobe Advertising DCO*

>[!IMPORTANT]
>
>本文档的内容不是法律建议，也不会代替法律建议。 请咨询您的法律顾问，以获得有关《通用数据保护条例》的建议。

《通用数据保护条例》(GDPR)法规于2018年5月25日生效，旨在赋予欧盟(EU)境内所有个人（数据主体）对其个人数据的控制权，并简化国际业务的监管环境。 该法规适用于向欧盟境内的个人提供商品或服务、监控个人行为或从其收集个人数据的所有企业（数据控制者）对个人数据进行处理的情况，而不论数据控制者的业务位置如何。

Adobe Experience Cloud充当数据处理者，可处理其代表客户接收并存储的任何个人数据。 作为数据控制者，您可以决定Adobe Experience Cloud代表您处理和存储的个人数据。

本文档介绍了[!DNL Advertising Search, Social, & Commerce]、Advertising Creative、Advertising DSP (Demand Side Platform)和[!DNL Advertising DCO]如何使用Adobe Experience Platform Privacy Service API和Privacy Service UI支持数据主体的GDPR数据访问和删除权限。

有关GDPR对您业务的意义的更多信息，请参阅[GDPR与您的业务](https://www.adobe.com/privacy/general-data-protection-regulation.html)。

## Adobe Advertising支持的数据请求类型

Adobe Experience Platform使企业能够完成以下任务：

* 在[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]或[!DNL DCO]内访问数据主体的Cookie级数据或设备ID级数据（适用于移动设备应用程序中的广告）。
* 对于使用浏览器的数据主体，删除存储在[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]或[!DNL DCO]中的Cookie级别数据；对于使用移动设备上的应用程序的数据主体，删除[!DNL DSP]中存储的ID级别数据。
* 检查一个或所有现有请求的状态。

## 发送Adobe Advertising请求所需的设置

要提出访问和删除Adobe Advertising数据的请求，您必须：

1. 部署JavaScript库以检索和删除数据主体Cookie。 所有Adobe Experience Cloud解决方案都使用相同的库`AdobePrivacy.js`。

   >[!IMPORTANT]
   >
   >对某些Experience Cloud解决方案的请求不需要JavaScript库，但对Adobe Advertising的请求需要它。

   您应该将库部署在数据主体可以提交访问和删除请求的网页上，例如您公司的隐私门户。 库可帮助您检索[!DNL Adobe] Cookie（命名空间ID： `gsurferID`），以使您可作为Adobe Experience Platform Privacy Service API访问和删除请求的一部分提交这些标识。

   当数据主体请求删除个人数据时，库还会从数据主体的浏览器中删除数据主体的Cookie。

   >[!NOTE]
   >
   >删除个人数据与选择退出不同，后者会停止使用受众区段定位最终用户。 但是，当数据主体请求从[!DNL Creative]、[!DNL DSP]或[!DNL DCO]中删除个人数据时，库还会向Adobe Advertising发送请求，以将该数据主体从区段定位中退出。 对于具有[!DNL Search, Social, & Commerce]的广告商，我们建议您向数据主体提供指向[https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html)的链接，其中介绍了如何选择退出受众区段定位。

1. 识别您的Experience Cloud组织ID，并确保它已关联到您的Adobe Advertising帐户。

   Experience Cloud组织ID是由24个字符组成的字母数字字符串，其后附加有“@AdobeOrg”。 已经为大多数Experience Cloud客户分配了一个组织ID。 如果您的营销团队或内部[!DNL Adobe]系统管理员不知道您的组织ID，或不确定它是否已配置，请通过gdprsupport@adobe.com联系Adobe客户关怀团队。 您将需要组织ID才能使用`imsOrgID`命名空间向隐私API提交请求。

   >[!IMPORTANT]
   >
   >请联系贵公司的Adobe Advertising代表，以确认贵公司的所有Adobe Advertising帐户（包括[!DNL DSP]帐户或广告商、[!DNL Search, Social, & Commerce]帐户以及[!DNL Creative]或[!DNL DCO]帐户）均关联到您的Experience Cloud组织ID。

1. 使用[Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html)（对于自动请求）或[Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html#)（对于临时请求）代表数据主体向Adobe Advertising提交访问和删除请求，并检查现有请求的状态。

   对于拥有移动应用程序以与数据主体进行交互并与DSP启动促销活动的广告商，您必须下载适用于Experience Cloud的隐私就绪移动SDK。 Mobile SDK允许数据控制者设置选择退出状态标记、检索数据主体的设备ID（命名空间ID： `deviceID`），并将请求提交到Privacy Service API。 您的移动应用程序需要安装SDK版本4.15.0或更高版本。

   当您提交数据主体的访问请求时，Privacy Service API会根据指定的Cookie或设备ID返回数据主体的信息，然后您必须将这些信息返回到数据主体。

   当您提交数据主体的删除请求时，Cookie ID或设备ID以及与Cookie关联的所有成本、点击和收入数据将从服务器中删除。

   >[!NOTE]
   >
   >如果贵公司拥有多个Experience Cloud组织ID，则必须为每个组织发送单独的API请求。 但是，您可以向多个Adobe Advertising子解决方案（[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]和[!DNL DCO]）发出一个API请求，每个子解决方案使用一个帐户。

Adobe Advertising需要执行所有步骤。 有关使用Adobe Experience Platform Privacy Service需要执行的这些任务和其他相关任务以及在何处查找所需项目的更多信息，请参阅“[Privacy Service概述](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)”。

## Adobe Advertising JSON请求中的必填字段值

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*您的Experience Cloud组织ID*>

`"users":`

* `"key":` &lt;*通常是数据主体的名称*>

* `"action":` `**access**`或`**delete**`

* `"user IDs":`

   * `"namespace": **411**` （表示[!DNL adcloud] Cookie空间）

   * `"value":` &lt;*从`AdobePrivacy.js`*&#x200B;检索的实际数据主体的Cookie ID值>

* `"include": **adCloud**` （适用于该请求的[!DNL Adobe]产品）

* `"regulation": **gdpr**` （适用于该请求的隐私法规）

## 数据主体使用检索自`AdobePrivacy.js`的Adobe Advertising用户ID提交的请求示例

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
```

## 针对访问请求返回的数据字段

以下是Adobe Advertising访问响应的示例。

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
                    "segmentName":"eXelate Australia Demographic - Jobs & Education - Job Seekers",
                    "segmentID":"2213789",
                    "serviceProvider":"exelate"
                }
            ]
        }
    }
}
```
