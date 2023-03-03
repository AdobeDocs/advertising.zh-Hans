---
title: 导入Adobe Audience Manager区段以进行广告定位
description: 了解如何导入 [!DNL Adobe] 受众进入Advertising DSP并使用Adobe Audience Manager搜索
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# 导入Adobe Audience Manager区段以进行广告定位

Advertising DSP和 [!DNL Advertising Search] 是否可以拉入所有广告商或代理的元数据、层次结构数据和独特受众数据 [!DNL Adobe] 受众<!-- segments or audiences? Standardize terms per AAM's docs -->. 其中包括以下项的数据：

* Adobe Audience Manager区段

* 发布到Adobe Experience Cloud的Adobe Analytics区段

* 使用Adobe Experience Cloud创建的区段 [!DNL Audience Library]

* 在Adobe Experience Platform中创建并通过Audience Manager发送到Adobe广告的区段

要访问 [!DNL Adobe] DSP中的受众或 [!DNL Creative]，必须将受众导入DSP。 要访问 [!DNL Adobe] 中的受众 [!DNL Search]，您必须将受众导入 [!DNL Search].

## 先决条件

* 广告商必须实施 [此 [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) 版本2.0或更高版本。 此 [!DNL Identity Service] 提供了一个通用的永久性ID，用于在Experience Cloud的所有解决方案中标识您的访客。

   实施包括添加 [!DNL Identity service] 广告商网站上每个网页的代码。

* 组织必须为 [已启用Experience Cloud服务](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) 并拥有Experience Cloud [!DNL Organization ID] (以前称为 [!DNL IMS org ID])。

   此 [!UICONTROL Organization ID] 允许拥有多个Adobe Experience Cloud产品的组织在某些产品之间共享数据。

* (广告商使用 [!DNL Analytics])广告商必须 [实施 [!DNL Analytics] 使用 `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) 版本1.6.4或更高版本。

* 广告商的网站访客不包括大量的 [!DNL Apple Safari] 用户。

* (当广告商同时使用Audience Manager和时，建议使用 [!DNL Analytics])要减少对每个网页的调用，请删除现有Audience Manager [!DNL Data Integration Library] 用于数据收集的代码，并为每个代码启用服务器端转发 [!DNL Analytics] 报表包进行替换。 有关更多信息，请参阅“[服务器端转发概述](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* （推荐）为了获得更高的匹配率，请仅将第一方网站数据发送到Adobe广告。 如果广告商捆绑来自客户关系管理系统的第三方数据或离线数据，则数据泄露可能会降低匹配率。

## 将Audience Manager受众导入DSP

### 将受众导入到DSP的步骤

此 [!DNL Adobe] 帐户和数据操作团队将执行以下步骤。

1. Adobe客户团队应配置广告商级别设置»[!UICONTROL Adobe Analytics Cloud].”

1. Adobe客户团队应提交申请<!-- Submit a request as a JIRA task? --> 至数据运营团队<!-- implementation team? --> 使用Advertising DSP本机API集成导入组织的Audience Manager区段。

### 哪些更改会导致Audience Manager？

API会自动执行以下操作：

* 在Audience Manager中创建两个DSP目标：

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* 将两个目标映射到所有Audience Manager区段，允许Audience Manager与同一Experience Cloud关联的DSP广告商帐户共享区段 [!DNL Organization ID] 用于Audience Manager。 <!-- Verify -->

   企业可以选择从Audience Manager中的目标删除不需要的区段。

* 将以下Exchange Cookie同步像素添加到组织的Audience Manager容器中，以提高客户促销活动的覆盖率：

   * AdobeAdCloud： 411（这是标准版本，并且作为的一部分自动提供） [!DNL Identity Service] 版本2.0。组织具有 [!DNL Identity Service] 低于2.0的版本应将此像素添加到其Audience Manager容器中。

## 将Audience Manager受众导入 [!DNL Search]

### 将受众导入到的步骤 [!DNL Search]

[!DNL Adobe] 人员将执行以下大部分或全部步骤。

1. Adobe客户团队应向数据运营团队提交请求，以设置两者之间的集成 [!DNL Search] 和Audience Manager。 包含要导出到的Audience Manager区段名称 [!DNL Search].

1. 在Audience Manager中，配置目标 [!DNL Search]：

   1. 创建两个新目标： `[!UICONTROL Adobe Media Optimizer (HTTP)]` 和 `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] 是以前的名称 [!DNL Search].

   1. 指定每个目标的区段。

      使用 [!UICONTROL Automatically map all current and future segments] 选项，则所有区段都将每天映射和同步。

      此 [!UICONTROL Manually map segments] 选项允许您手动映射区段以与批处理目标同步(`[!UICONTROL Adobe Media Optimizer Batch Destination]`)。 无需将任何区段手动映射到HTTP目标。

1. 范围 [!DNL Search]，可以 [!DNL Search] 实施团队或具有直接访问客户端管理员角色的用户应该从启动导入 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   您需要输入组织的Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID])。 ID必须与用于组织Audience Manager帐户的ID相同。

### 哪些更改会导致Audience Manager？

组织将看到两个 [!DNL Search] Audience Manager中的目标：

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## 数据同步

初次导入大约需要24小时。 初次导入后，数据会实时同步，延迟时间为一到两秒。

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.eversttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].

![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Adobe Advertising display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## 在何处查找同步的区段

### 在DSP中

在DSP中，区段名称按Audience Manager分类法组织，并可用于中的相应区段成员资格计数：

* [置入设置](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting)：在 [!UICONTROL Adobe Segments] 的选项卡 [!UICONTROL Audience Targeting] 部分。

* In [受众设置](/help/dsp/audiences/audience-settings.md)：在 [!UICONTROL Adobe Segments] 选项卡。

### Advertising Creative内容

In [!DNL Creative]中，这些区段在target节点的体验设置中可用。

### In [!DNL Advertising Search]

In [!DNL Search]，则这些区段在创建 [!DNL Google] 受众使用 [!UICONTROL Data Source] ”[!UICONTROL Adobe Audience]”自 [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

针对每个 [!DNL Google] 您创建的受众， [!DNL Google] 提供受众规模。

>[!MORELIKETHIS]
>
>* [Adobe广告与Adobe Audience Manager的集成](/help/integrations/audience-manager/overview.md)

