---
title: Adobe Advertising对《加州消费者隐私法案》的支持：消费者数据访问和删除支持
description: 了解支持的数据请求类型、所需的设置和字段值，以及使用旧版产品ID和返回的数据字段的API访问请求示例。
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: df19f47971e97727c85bce99ce80b677fbdb1a49
workflow-type: tm+mt
source-wordcount: '1075'
ht-degree: 0%

---

# Adobe Advertising对《加州消费者隐私法案》的支持：消费者数据访问和删除支持

*对象 [!DNL Adobe Advertising Search, Social, & Commerce]；Adobe Advertising DSP；Adobe Advertising Creative；Adobe AdvertisingDCO*

>[!IMPORTANT]
>
>本文档的内容不是法律建议，也不会代替法律建议。 请咨询您的法律顾问，以获取有关《加州消费者隐私法案》的建议。

《加州消费者隐私法案》(CCPA)是加利福尼亚州的新隐私法，自2020年1月1日起生效。 CCPA为加利福尼亚州居民提供了有关其个人信息的新权利，并对在加利福尼亚州开展业务的某些实体施加了数据保护责任。 CCPA为消费者提供访问和删除其个人信息的权利，以及选择退出某些有资格将个人信息“出售”给第三方的活动的权利。

作为企业，您将决定Adobe Experience Cloud代表您处理和存储的个人数据。

作为您的服务提供商，Adobe Advertising将为您的企业提供支持，使其履行CCPA中适用于Adobe Advertising产品和服务使用的义务，包括管理访问和删除个人信息的请求，以及管理选择退出个人信息销售的请求。

本文档介绍如何 [!DNL Advertising Search, Social, & Commerce]；Advertising Creative；Advertising DSP(Demand Side Platform)；和 [!DNL Advertising DCO]  — 作为服务提供商 — 支持消费者使用Adobe访问和删除个人信息的权利 [!DNL Experience Platform Privacy Service API] 和 [!DNL Privacy Service UI].

有关Advertising DSP如何支持消费者选择退出出售个人信息的权利的信息，请参阅 [Adobe Advertising对《加州消费者隐私法案》的支持：消费者选择退出支持](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

有关CCPAAdobe隐私服务的更多信息，请参阅 [Adobe隐私中心](https://www.adobe.com/privacy/ccpa.html).

## Adobe Advertising支持的数据请求类型

Adobe Experience Platform使企业能够完成以下任务：

* 在中访问消费者的Cookie级别数据或设备ID级别数据（适用于移动设备应用程序中的广告） [!DNL Search, Social, & Commerce]， [!DNL Creative]， [!DNL DSP]，或 [!DNL DCO].
* 删除中存储的Cookie级别数据 [!DNL Search, Social, & Commerce]， [!DNL Creative]， [!DNL DSP]，或 [!DNL DCO] 适用于使用浏览器的消费者；或删除存储在中的ID级别数据 [!DNL DSP] 适用于在移动设备上使用应用程序的消费者。
* 检查一个或所有现有请求的状态。

## 发送Adobe Advertising请求所需的设置

要申请访问和删除Adobe Advertising中的消费者个人信息，您需要：

1. 部署JavaScript库以检索和删除客户的Cookie。 同一个图书馆， `AdobePrivacy.js`，用于所有Adobe Experience Cloud解决方案。

   >[!IMPORTANT]
   >
   >对某些Experience Cloud解决方案的请求不需要JavaScript库，但对Adobe Advertising的请求需要它。

   您应将库部署在客户可以从其中提交访问和删除请求的网页上，例如您公司的隐私门户。 库可帮助您检索AdobeCookie(命名空间ID： `gsurferID`)，以便您可以将这些身份作为访问和删除请求的一部分通过 [!DNL Adobe Experience Platform Privacy Service API].

   当客户请求删除个人数据时，库还会从客户的浏览器中删除客户的Cookie。

   >[!NOTE]
   >
   >删除个人数据与选择退出不同，后者会停止定位具有受众区段的最终用户。 但是，当消费者请求从中删除个人数据时 [!DNL Creative]， [!DNL DSP]，或 [!DNL DCO]，则库还会向Adobe Advertising发送请求，以选择退出客户区段定位。 对于广告商，使用 [!DNL Search, Social, & Commerce]，我们建议您向客户提供以下链接： [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse)，其中介绍了如何选择退出受众区段定位。

1. 识别您的Experience Cloud组织ID，并确保它已链接到您的Adobe Advertising帐户。

   Experience Cloud的组织ID是由24个字符组成的字母数字字符串，其后附加有“@AdobeOrg”。 已为大多数Experience Cloud客户分配了组织ID。 如果您的营销团队或内部Adobe系统管理员不知道您的组织ID，或不确定它是否已配置，请通过gdprsupport@adobe.com联系Adobe客户关怀团队。 您将需要组织ID才能使用向隐私API提交请求 `imsOrgID` 命名空间。

   >[!IMPORTANT]
   >
   >请联系贵公司的Adobe Advertising代表，以确认贵组织的所有Adobe Advertising帐户，包括 [!DNL DSP] 客户或广告商， [!DNL Search, Social, & Commerce] 帐户，以及 [!DNL Creative] 或 [!DNL DCO] 帐户 — 链接到您的Experience Cloud组织ID。

1. 使用 [ADOBE EXPERIENCE PLATFORM PRIVACY SERVICE API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （适用于自动请求）或 [PRIVACY SERVICEUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=zh-Hans) （对于临时请求）将访问和删除个人信息的请求提交给Adobe Advertising以代表消费者，并检查现有请求的状态。

   对于拥有可与客户交互并启动促销活动的移动应用程序的广告商 [!DNL DSP]，您将需要下载适用于隐私的Mobile SDK以进行Experience Cloud。 Mobile SDK允许企业设置选择退出状态标记，检索消费者的设备ID(命名空间ID： `deviceID`)，并将请求提交到Privacy ServiceAPI。 您的移动应用程序将需要SDK版本4.15.0或更高版本。

   当您提交消费者访问请求时，Privacy ServiceAPI会根据指定的Cookie或设备ID返回消费者的信息，然后您必须将此信息返回到消费者。

   当您提交使用者删除请求时，Cookie ID或设备ID以及所有成本、点击和与Cookie关联的收入数据都会从服务器中删除。

   >[!NOTE]
   >
   如果您的企业有多个Experience Cloud组织ID，则必须为每个组织发送单独的API请求。 但是，您可以向多个Adobe Advertising子解决方案发出一个API请求([!DNL Search, Social, & Commerce]， [!DNL Creative]， [!DNL DSP]、和 [!DNL DCO])，每个子解决方案具有一个帐户。

要获得Adobe Advertising的支持，所有这些步骤都是必需的。 有关您需要使用Adobe Experience Platform Privacy Service执行的这些任务和其他相关任务，以及在何处查找所需项目的更多信息，请参阅 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Adobe AdvertisingJSON请求中的必填字段值

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*您的Experience Cloud组织ID*>

&quot;users&quot;：

* `"key":` &lt;*通常是客户的名称*>

* `"action":` 任一 `**access**` 或 `**delete**`

* `"user IDs":`

   * `"namespace": **411**` （表示adcloud Cookie空间）

   * `"value":` &lt;*从中检索的实际客户的Cookie ID值`AdobePrivacy.js`*>

* `"include": **adCloud**` (适用于该请求的Adobe产品)

* `"regulation": **ccpa**` （即适用于请求的隐私法规）

## 使用检索自AdobePrivacy.js的Adobe Advertising用户ID的消费者提交的请求示例

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
}
```

## 为访问请求返回的数据字段

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
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
