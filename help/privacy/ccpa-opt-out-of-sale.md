---
title: Adobe对《加州消费者隐私法案》的广告支持：消费者选择退出销售支持
description: 了解对捕获消费者选择退出销售请求的支持。
feature: CCPA
exl-id: 2c0cd4f5-798f-479a-99cd-f555cd676766
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 0%

---

# Adobe对《加州消费者隐私法案》的广告支持：消费者选择退出销售支持

*对于Adobe广告Demand Side Platform(DSP)*

>[!IMPORTANT]
>
>本文档的内容不是法律建议，也不会代替法律建议。 请咨询您的法律顾问，以获取有关《加州消费者隐私法案》的建议。

《加州消费者隐私法案》(CCPA)是加利福尼亚州的新隐私法，于2020年1月1日生效。 CCPA为加利福尼亚州居民提供了有关其个人信息的新权利，并对在加利福尼亚州开展业务的某些实体强加了数据保护责任。 CCPA为消费者提供访问和删除其数据的权利，以及选择退出某些有资格“向第三方出售”个人信息的活动的权利。

作为企业，您将决定Adobe Experience Cloud代表您处理和存储的个人数据。

作为您的服务提供商，Adobe广告为您的企业提供支持，以履行CCPA规定的适用于Adobe广告产品和服务使用的义务，包括管理客户访问和删除个人信息的请求以及管理客户选择退出出售个人信息的请求。

本文档介绍Adobe广告Demand Side Platform(DSP)作为服务提供商，如何支持消费者选择退出“出售”“个人信息”的权利，因为CCPA定义了每个术语。 它包括有关如何传达选择退出销售请求以Adobe广告以及如何检索贵组织选择退出销售请求的报表的信息。

有关如何 [!DNL Advertising Search];广告创意；和 [!DNL Advertising DCO] 支持消费者的个人信息访问和删除权限，请参阅 [Adobe对《加州消费者隐私法案》的广告支持：消费者数据访问和删除支持](/help/privacy/ccpa-access-delete.md).

有关CCPA的Adobe隐私服务的更多信息，请参阅 [Adobe隐私中心](https://www.adobe.com/privacy/ccpa.html).

## 传达消费者选择退出销售的请求以Adobe广告

您可以使用以下任一方式传递消费者的选择退出销售请求：

* 在Advertising DSP中创建的CCPA选择退出销售区段
* Adobe Experience Platform Privacy Service API

### 方法1:使用 [!UICONTROL CCPA Opt-Out-of-Sale] 在Advertising DSP中划分区段

>[!NOTE]
>
>用户将无限期地保留在CCPA选择退出销售区段中。

1. 在Advertising DSP中登录广告商的帐户，网址为 [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [创建CCPA选择退出销售区段，并实施区段像素以捕获选择退出请求](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### 方法2:使用Adobe Experience Platform Privacy Service API传达CCPA选择退出销售请求

*广告商仅分配了Adobe Experience Cloud组织ID*

1. 部署JavaScript库以检索客户的Cookie。 同一个图书馆， `AdobePrivacy.js`，用于所有Adobe Experience Cloud解决方案。

   >[!IMPORTANT]
   >
   >对某些Adobe Experience Cloud解决方案的请求不需要JavaScript库，但Adobe广告的请求需要它。

   您应该在网页上部署库，客户可从该网页提交选择退出销售请求，如您公司的隐私门户。 库可帮助您检索AdobeCookie(命名空间ID: `gsurferID`)，以便您能够通过Adobe Experience Platform Privacy Service API将这些身份作为选择退出销售请求的一部分提交。

1. 识别您的Experience Cloud组织ID，并确保它已关联到您的Adobe广告帐户。

   Experience Cloud组织ID是由24个字符组成的字母数字字符串，其后附加有“@AdobeOrg”。 大多数Experience Cloud客户都分配了组织ID。 如果您的营销团队或内部Adobe系统管理员不知道您的组织ID，或者不确定是否已配置，请通过gdprsupport@adobe.com联系Adobe客户关怀团队。 您需要组织ID才能使用 `imsOrgID` 命名空间。

   >[!IMPORTANT]
   >
   >联系贵公司的Adobe广告代表，以确认贵组织的所有Adobe广告帐户(包括 [!DNL DSP] 帐户或广告商， [!DNL Search] 帐户和 [!DNL Creative] 或 [!DNL DCO] 帐户 — 已关联到您的Experience Cloud组织ID。

1. 使用Adobe Experience Platform Privacy Service API [提交选择退出销售请求](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) 代表消费者Adobe广告，并检查现有请求的状态。

   有关选择退出销售请求的示例，请参阅下面的附录。

   >[!NOTE]
   如果您的企业具有多个Experience Cloud组织ID，则必须为每个IP发送单独的API请求。 但是，您可以向多个Adobe广告子解决方案([!DNL Search], [!DNL Creative], [!DNL DSP]和 [!DNL DCO])，每个子解决方案具有一个帐户。

要从Adobe广告获得支持，所有这些步骤都是必需的。 有关使用Adobe Experience Platform Privacy Service执行这些任务和其他相关任务以及在何处查找所需项目的更多信息，请参阅 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## 检索提交选择退出销售请求的消费者的报表

Adobe广告会生成客户为帐户的选择退出销售请求提交的ID的月度报表。 每个报表都可作为以制表符分隔的文本文件进行压缩，格式为GZIP。 该数据整合了使用在Advertising DSP中创建的CCPA选择退出销售区段捕获的请求，以及通过Privacy ServiceAPI提交的任何内容。 在CCPA选择退出销售区段中捕获的用户ID由区段和广告商进行标识。 报表是在每月的第一个月生成，具体时间为上个月。 例如，6月份的每月用户列表在7月1日可用。

您可以从Advertising DSP中或使用Advertising DSP检索到在前三个月中创建的月度报表的链接 [!DNL Trafficking API]. 每个链接的有效期为7天，但客户每次尝试检索一个链接时都会刷新。

### 方法1:在Advertising DSP中检索消费者选择退出销售报表

1. 在Advertising DSP中登录广告商的帐户，网址为 [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [检索报表](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### 方法2:使用Advertising DSP检索消费者选择退出销售报表 [!DNL Trafficking API]

此功能适用于使用 [!DNL Trafficking API]. 请参阅 [!DNL Trafficking API] 以了解更多信息。

如果贵组织不使用 [!DNL Trafficking API] 但有兴趣了解更多信息，请联系 [!DNL Adobe] 客户团队。

## 附录：示例 [!UICONTROL CCPA Opt-Out-of-Sale] 请求Privacy ServiceAPI用户

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

* `"namespace": "AdCloud"` 表示 `AdCloud` Cookie空间，且相应的值是客户的Cookie ID，检索自 `AdobePrivacy.js`
* `"include": ["AdCloud"]` 指示请求适用于Adobe广告
