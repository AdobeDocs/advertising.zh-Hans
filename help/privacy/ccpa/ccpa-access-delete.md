---
title: Adobe Advertising支持《加州消费者隐私法案》(&#58)；消费者数据访问和删除支持
description: 了解支持的数据请求类型、所需的设置和字段值，以及使用旧版产品ID和返回的数据字段的API访问请求示例。
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: a3e39ca4fa89f84ddc2669662c34bccb4425a2bb
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Adobe Advertising对《加州消费者隐私法案》的支持：消费者数据访问和删除支持

*适用于[!DNL Adobe Advertising Search, Social, & Commerce]、Adobe Advertising DSP、Adobe Advertising Creative和Adobe Advertising DCO*

>[!IMPORTANT]
>
>本文档的内容不是法律建议，也不会代替法律建议。 请咨询您的法律顾问，以获取有关《加州消费者隐私法案》的建议。

《加州消费者隐私法案》(CCPA)是加利福尼亚州的新隐私法，于2020年1月1日生效。 CCPA为加利福尼亚州居民提供了有关其个人信息的新权利，并对在加利福尼亚州开展业务的某些实体强加了数据保护责任。 CCPA为消费者提供访问和删除其个人信息的权利，以及选择退出某些有资格将个人信息“出售”给第三方的活动的权利。

作为企业，您可以决定Adobe Experience Cloud代表您处理和存储的个人数据。

作为您的服务提供商，Adobe Advertising将为您的企业提供支持，使其履行CCPA规定且适用于Adobe Advertising产品和服务使用的义务，包括管理访问和删除个人信息的请求，以及管理选择退出个人信息销售的请求。

本文档介绍[!DNL Advertising Search, Social, & Commerce]、Advertising Creative、Advertising DSP (Demand Side Platform)和[!DNL Advertising DCO]（作为服务提供商）如何支持消费者使用Adobe [!DNL Experience Platform Privacy Service API]和[!DNL Privacy Service UI]访问和删除个人信息的权限。

有关Advertising DSP如何支持消费者选择退出个人信息销售的权利的信息，请参阅[Adobe Advertising对《加州消费者隐私法案》的支持：消费者选择退出支持](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)。

有关适用于CCPA的Adobe隐私服务的更多信息，请参阅[Adobe隐私中心](https://www.adobe.com/privacy/ccpa.html)。

## Adobe Advertising支持的数据请求类型

Adobe Experience Platform使企业能够完成以下任务：

* 在[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]或[!DNL DCO]内访问消费者的Cookie级别数据或设备ID级别数据（适用于移动设备应用程序中的广告）。
* 对于使用浏览器的消费者，删除存储在[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]或[!DNL DCO]中的Cookie级别数据；对于使用移动设备上的应用的消费者，删除存储在[!DNL DSP]中的ID级别数据。
* 检查一个或所有现有请求的状态。

## 发送Adobe Advertising请求所需的设置

要请求从Adobe Advertising访问和删除消费者个人信息，您必须：

1. 部署JavaScript库以检索和删除客户的Cookie。 所有Adobe Experience Cloud解决方案都使用相同的库`AdobePrivacy.js`。

   >[!IMPORTANT]
   >
   >对某些Experience Cloud解决方案的请求不需要JavaScript库，但对Adobe Advertising的请求需要它。

   您应在客户可以从其中提交访问和删除请求的网页上部署库，例如公司的隐私门户。 库可帮助您检索Adobe Cookie（命名空间ID： `gsurferID`），以便您可以作为访问和删除请求的一部分通过[!DNL Adobe Experience Platform Privacy Service API]提交这些标识。

   当客户请求删除个人数据时，库还会从客户的浏览器中删除客户的Cookie。

   >[!NOTE]
   >
   >删除个人数据与选择退出不同，后者会停止使用受众区段定位最终用户。 但是，当使用者请求从[!DNL Creative]、[!DNL DSP]或[!DNL DCO]中删除个人数据时，库还会向Adobe Advertising发送请求，以选择退出客户区段定位。 对于具有[!DNL Search, Social, & Commerce]的广告商，我们建议您向客户提供指向[https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse)的链接，其中介绍了如何选择退出受众区段定位。

1. 识别您的Experience Cloud组织ID，并确保它已关联到您的Adobe Advertising帐户。

   Experience Cloud组织ID是由24个字符组成的字母数字字符串，其后附加有“@AdobeOrg”。 已经为大多数Experience Cloud客户分配了一个组织ID。 如果您的营销团队或内部[!DNL Adobe]系统管理员不知道您的组织ID，或不确定它是否已配置，请联系您的Adobe客户团队。 您将需要组织ID才能使用`imsOrgID`命名空间向隐私API提交请求。

   >[!IMPORTANT]
   >
   >请联系贵公司的Adobe Advertising代表，以确认贵公司的所有Adobe Advertising帐户（包括[!DNL DSP]帐户或广告商、[!DNL Search, Social, & Commerce]帐户以及[!DNL Creative]或[!DNL DCO]帐户）均关联到您的Experience Cloud组织ID。

1. 使用[Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html?lang=zh-Hans)（对于自动请求）或[Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hans#)（对于临时请求）将代表消费者访问和删除个人信息的请求提交到Adobe Advertising，并检查现有请求的状态。

   对于拥有可与客户交互以及通过[!DNL DSP]启动促销活动的移动应用程序的广告商，您必须下载适用于Experience Cloud的隐私就绪移动SDK。 Mobile SDK允许企业设置选择退出状态标记、检索消费者的设备ID（命名空间ID： `deviceID`），并将请求提交到Privacy Service API。 您的移动应用程序需要安装SDK版本4.15.0或更高版本。

   在提交消费者访问请求时，Privacy Service API会根据指定的Cookie或设备ID返回消费者的信息，然后您必须将此信息返回给消费者。

   在提交消费者删除请求时，Cookie ID或设备ID以及所有成本、点击和与Cookie关联的收入数据将从服务器中删除。

   >[!NOTE]
   >
   >如果您的企业有多个Experience Cloud组织ID，则必须为每个组织发送单独的API请求。 但是，您可以向多个Adobe Advertising子解决方案（[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]和[!DNL DCO]）发出一个API请求，每个子解决方案使用一个帐户。

要获得Adobe Advertising的支持，必须执行所有步骤。 有关使用Adobe Experience Platform Privacy Service需要执行的这些任务和其他相关任务以及在何处查找所需项目的更多信息，请参阅[https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hans](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hans)。

## Adobe Advertising JSON请求中的必填字段值

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*您的Experience Cloud组织ID*>

&quot;users&quot;：

* `"key":` &lt;*通常是客户的名称*>

* `"action":` `**access**`或`**delete**`

* `"user IDs":`

   * `"namespace": **411**` （表示[[!DNL AdCloud] Cookie空间](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/privacy/api/appendix)）

   * `"value":` &lt;*从`AdobePrivacy.js`*&#x200B;检索到的实际客户的Cookie ID值>

* `"include": **adCloud**` （适用于该请求的[[!DNL Adobe] 产品](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/privacy/api/appendix)）

* `"regulation": **ccpa**` （适用于该请求的隐私法规）

## 使用从AdobePrivacy.js检索到的Adobe Advertising用户ID提交的请求示例

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
    "regulation":"ccpa"
}
```

## 针对访问请求返回的数据字段

以下是Adobe Advertising的个人信息访问响应示例。

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
