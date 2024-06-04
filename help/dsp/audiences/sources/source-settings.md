---
title: 受众源设置
description: 了解受众源的设置。
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 16a796e02150b00c77c825d7f54c6e390c85214a
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# 受众源设置

*Beta版功能*

**[!UICONTROL Data Visibility Level]：** 区段是否可供具有帐户访问权限的单个广告商使用(*[!UICONTROL Advertiser]*)，或所有有权访问该帐户的广告商 *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]：** （仅限广告商级别的可见性）可用于区段的广告商。 从具有帐户访问权限的广告商列表中选择一个。

**[!UICONTROL Enter IMS Org Id]：** ([!DNL Real-Time CDP] 源)的Adobe Experience Cloud组织ID [!DNL Adobe Experience Platform] 帐户。

**[!UICONTROL Convert PII to the following IDs]：** 要将个人身份信息(PII)转换为的ID类型。 如果选择多种类型，则生成的区段将填充每个选定ID类型的值(例如 [!DNL RampID] 和 [!DNL Unified ID2.0] （每个电子邮件地址）。 数据收费也相应地计算。

对象 [!DNL RampID] 和 [!DNL Unified ID2.0]，供应商会查找每个电子邮件地址，以查看该ID是否已存在，并在有匹配的ID可用时将其转换为匹配的ID。 如果地址不存在ID，则会创建新的ID。

>[!NOTE]
>
>在单个投放位置中只能定位一种类型的ID。 要按ID类型测试性能， [创建单独的投放位置](/help/dsp/campaign-management/placements/placement-create.md) 区段中的每个ID类型。

* *[!DNL RampID]：* 要将PII转换为 [!DNL RampID]. 您可以使用 [!DNL RampIDs] 用于重新定位登录用户和 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) 测量。

* *[!DNL Unified ID2.0](Beta)：* 要将PII转换为 [统一的ID 2.0](https://unifiedid.com) 用于重新定位登录用户的ID。

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]：** 用于将PII转换为通用ID的服务协议条款。 您或DSP帐户中的其他用户必须接受一次这些条款，然后才能将数据转换为新的ID类型。 对于签订托管服务合同的客户，您的Adobe客户团队将代表贵组织获得您的同意并接受相关条款。 要阅读术语，请单击 **>**. 要接受条款，请滚动到条款的底部并单击 **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]：** （只读；自动生成）可用于在客户数据平台中创建目标连接，以将受众推送到Advertising DSP的源密钥。 您可以将值复制到剪贴板以粘贴到目标连接设置或文件中。

>[!MORELIKETHIS]
>
>* [创建受众源以激活通用ID受众](source-create.md)
>* [关于第一方受众源](source-about.md)
>* [从手动导入经过身份验证的区段 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Adobe Advertising DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
