---
title: 从通用ID合作伙伴激活经过身份验证的区段
description: 了解如何通过通用ID解决方案激活经过身份验证的受众。
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: e9ff454428d0256402a2ef2fa74f8bd45bd7592f
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# 从通用ID合作伙伴激活经过身份验证的区段

要通过Advertising DSP中的通用ID解决方案激活经过身份验证的受众，必须将您的区段转换为 [!DNL RampIDs]，这些资源可在竞价环境中识别。 您可以通过以下任一方式实现此目标：

* 利用DSP与 [!DNL Adobe Real-Time Customer Data Platform (CDP)] 和 [!DNL Adobe-LiveRamp Retrieval API].

* DSP手动将经过身份验证的区段从 [!DNL LiveRamp] [!DNL Connect] 仪表板。

## 任务

1. 对于任一选项，请联系 `adcloud-support@adobe.com` 在DSP中启用以下设置，以便在DSP促销活动中定位一次经过身份验证的区段 [激活工作流中的所有步骤均已完成](source-adobe-rtcdp.md)：

   1. [!DNL LiveRamp] [!DNL RampID] 从共享区段之前的营销活动配置 [!DNL Real-Time CDP].

   1. 帐户级别&#39;&#39;[!UICONTROL LiveRamp segments]”选项。

1. (用户从手动共享经过身份验证的区段 [!DNL LiveRamp])完成以下步骤： [!DNL LiveRamp] [!DNL Connect] 仪表板：

   1. 激活目标拼贴 **[!DNL AAC API 1P Onboarding]**.

   1. 设置 [!DNL Identifier Settings] 到 **[!DNL Ramp ID]** 仅限。

      ![标识符设置](/help/dsp/assets/liveramp-tile-settings.png)

   1. （可选）如果您仍要接收基于Cookie的标识符，请创建第二个 [!DNL AAC API 1P Onboarding] 目标拼贴，带有&quot;[!DNL Cookies]，&quot; &quot;[!DNL IDFA]，”和“[!DNL AAID]已选择“”。

## 测试和数据验证的最佳实践

* **Target [!DNL RampID]在单独的营销活动中基于的区段和基于Cookie的区段。**

   * Campaign设置仅允许对一个标识符进行优先级排序。

   * 目前， [!DNL RampIDs] 在现场活动期间不可检索。 这意味着某些自定义目标（如最低CPA和ROAS）在使用经过身份验证的区段时不可用。 仅在您具有限制性的性能KPI时才使用基于Cookie的区段。

* **在两个页面中创建一个版面 [!DNL RampID] 和基于Cookie的营销活动。**

   * 定位共享自的区段 [!DNL LiveRamp] 使用标准区段激活流程。

   * 与您的Adobe Advertising支持团队合作，验证正确的数据分发。

要了解有关DSP与集成的更多信息，请执行以下操作 [!DNL LiveRamp]，联系人 `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [关于从受众源激活经过身份验证的区段](source-about.md)
>* [创建受众源以激活第一方受众](source-create.md)
>* [受众源设置](source-settings.md)
>* [Adobe Advertising DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
