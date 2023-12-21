---
title: 受众源设置
description: 了解受众源的设置。
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# 受众源设置

**[!UICONTROL Data Visibility Level]：** 区段是否可供具有帐户访问权限的单个广告商使用(*[!UICONTROL Advertiser]*)，或所有有权访问该帐户的广告商 *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]：** （仅限广告商级别的可见性）可用于区段的广告商。 从具有帐户访问权限的广告商列表中选择一个。

**[!UICONTROL Enter IMS Org Id]：** ([!DNL Real-Time CDP] 源)的Adobe Experience Cloud组织ID [!DNL Adobe Experience Platform] 帐户。

**[!UICONTROL Convert PII to the following IDs]：** ([!DNL ActionIQ] 和 [!DNL Tealium] 源)要将个人身份信息(PII)转换为的ID类型。 数据收费也相应地计算。

* *[!DNL RampID]：* 将PII转换为RampID。 如果您选择 *[!DNL RampID]*，则您的区段将转换为 [!DNL RampIDs] 自动。

* *[!DNL Unified ID2.0]：* ([!DNL ActionIQ] （仅限源）要将PII转换为 [统一的ID 2.0](https://unifiedid.com/).

**[!UICONTROL Source Key]：** （只读；自动生成）可用于在客户数据平台中创建目标连接，以将受众推送到Advertising DSP的源密钥。 您可以将值复制到剪贴板以粘贴到目标连接设置或文件中。

>[!MORELIKETHIS]
>
>* [创建受众源以激活第一方受众](source-create.md)
>* [关于从受众源激活经过身份验证的区段](source-about.md)
>* [从通用ID合作伙伴激活经过身份验证的区段](source-universal-id.md)
>* [Adobe Advertising DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
