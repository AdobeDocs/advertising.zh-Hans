---
title: Adobe广告对《加州消费者隐私法案》的支持：消费者选择退出销售支持
description: 了解对捕获消费者选择退出销售请求的支持。
feature: CCPA
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 0%

---

# Adobe广告对《加州消费者隐私法案》的支持：消费者选择退出销售支持

*对于Adobe广告Demand Side Platform(DSP)*

>[!IMPORTANT]
>
>本文档的内容不是法律建议，也不会代替法律建议。 请咨询您的法律顾问，以获取有关《加州消费者隐私法案》的建议。

《加州消费者隐私法案》(CCPA)是加利福尼亚州的新隐私法，自2020年1月1日起生效。 CCPA为加利福尼亚州居民提供了有关其个人信息的新权利，并对在加利福尼亚州开展业务的某些实体施加了数据保护责任。 CCPA为消费者提供访问和删除其数据的权利，以及选择退出某些有资格将个人信息“出售”给第三方的活动的权利。

作为企业，您将决定Adobe Experience Cloud代表您处理和存储的个人数据。

作为您的服务提供商，Adobe广告支持您的企业履行CCPA中适用于使用Adobe广告产品和服务的义务，包括管理消费者访问和删除个人信息的请求，以及管理消费者选择退出个人信息销售的请求。

本文档介绍了Adobe广告Demand Side Platform(DSP)作为服务提供商，如何支持消费者选择退出“个人信息销售”的权利，因为CCPA定义了每个术语。 其中包括有关如何向Adobe广告传达选择退出销售请求以及如何检索贵组织的选择退出销售请求的报表的信息。

有关如何 [!DNL Advertising Search]；广告创意；以及 [!DNL Advertising DCO] 支持消费者的个人信息访问和删除权利，请参阅 [Adobe广告对《加州消费者隐私法案》的支持：消费者数据访问和删除支持](/help/privacy/ccpa/ccpa-access-delete.md).

有关CCPAAdobe隐私服务的更多信息，请参阅 [Adobe隐私中心](https://www.adobe.com/privacy/ccpa.html).

## 将消费者选择退出销售的请求传达给Adobe广告

您可以使用以下任一方式传达消费者选择退出销售的请求：

* 在Advertising DSP中创建的CCPA选择退出销售区段
* ADOBE EXPERIENCE PLATFORM PRIVACY SERVICE API

### 方法1：使用 [!UICONTROL CCPA Opt-Out-of-Sale] Advertising DSP中的区段

>[!NOTE]
>
>用户无限期地停留在CCPA选择退出销售区段中。

1. 登录Advertising DSP中的广告商帐户，网址为 [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [创建CCPA选择退出销售区段，并实施区段像素以捕获选择退出请求](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### 方法2：使用Adobe Experience Platform Privacy Service API传达CCPA选择退出销售请求

*广告商仅分配了Adobe Experience Cloud组织ID*

1. 部署JavaScript库以检索客户的Cookie。 同一个图书馆， `AdobePrivacy.js`，用于所有Adobe Experience Cloud解决方案。

   >[!IMPORTANT]
   >
   >对某些Adobe Experience Cloud解决方案的请求不需要JavaScript库，但对Adobe广告的请求则需要它。

   您应该将库部署在客户可以从其中提交选择退出销售请求的网页上，例如您公司的隐私门户。 库可帮助您检索AdobeCookie(命名空间ID： `gsurferID`)，以便您可以将这些身份作为选择退出销售请求的一部分通过Adobe Experience Platform Privacy Service API提交。

1. 识别您的Experience Cloud组织ID，并确保它已链接到您的Adobe广告帐户。

   Experience Cloud的组织ID是由24个字符组成的字母数字字符串，其后附加有“@AdobeOrg”。 已为大多数Experience Cloud客户分配了组织ID。 如果您的营销团队或内部Adobe系统管理员不知道您的组织ID，或不确定它是否已配置，请通过gdprsupport@adobe.com联系Adobe客户关怀团队。 您将需要组织ID才能使用向隐私API提交请求 `imsOrgID` 命名空间。

   >[!IMPORTANT]
   >
   >请联系贵公司的Adobe广告代表，以确认贵组织的所有Adobe广告帐户，包括 [!DNL DSP] 客户或广告商， [!DNL Search] 帐户，以及 [!DNL Creative] 或 [!DNL DCO] 帐户 — 链接到您的Experience Cloud组织ID。

1. 使用Adobe Experience Platform Privacy Service API可以 [提交选择退出销售请求](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) 代表消费者Adobe广告，并检查现有请求的状态。

   有关选择退出销售请求的示例，请参阅下面的附录。

   >[!NOTE]
   如果您的企业有多个Experience Cloud组织ID，则必须为每个组织发送单独的API请求。 但是，您可以向多个Adobe广告子解决方案发出一个API请求([!DNL Search]， [!DNL Creative]， [!DNL DSP]、和 [!DNL DCO])，每个子解决方案具有一个帐户。

所有这些步骤都是从Adobe广告获得支持所必需的。 有关您需要使用Adobe Experience Platform Privacy Service执行的这些任务和其他相关任务，以及在何处查找所需项目的更多信息，请参阅 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## 检索提交了选择退出销售请求的消费者的报表

Adobe广告每月生成客户针对帐户的选择退出销售请求提交的ID报表。 每个报表都以制表符分隔的文本文件形式提供，并压缩为GZIP格式。 数据整合了使用Advertising DSP中创建的CCPA选择退出销售区段捕获的请求和通过Privacy ServiceAPI提交的任何提交。 在CCPA选择退出销售区段中捕获的用户ID由区段和广告商标识。 报告是在每月的第一天生成的，显示在上个月。 例如，6月的每月用户列表可在7月1日提供。

您可以通过在Advertising DSP中或使用Advertising DSP，检索到在前三个月创建的每月报表的链接 [!DNL Trafficking API]. 每个链接的有效期为七天，但每次客户尝试检索一个链接时都会刷新。

### 方法1：在Advertising DSP中检索消费者选择退出销售报表

1. 登录Advertising DSP中的广告商帐户，网址为 [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [检索报告](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### 方法2：使用Advertising DSP检索消费者选择退出销售报表 [!DNL Trafficking API]

此功能适用于使用 [!DNL Trafficking API]. 请参阅以下内容的文档： [!DNL Trafficking API] 了解更多信息。

如果您的组织不使用 [!DNL Trafficking API] 但希望了解更多信息，请联系您的Adobe客户团队。

## 附录：示例 [!UICONTROL CCPA Opt-Out-of-Sale] Privacy ServiceAPI用户请求

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["AdCloud"],
    "regulation": "ccpa"
}'
```

其中：

* `"namespace": "AdCloud"` 表示 `AdCloud` Cookie空间，并且对应的值是从中检索的客户Cookie ID `AdobePrivacy.js`
* `"include": ["AdCloud"]` 指示该请求适用于Adobe广告
