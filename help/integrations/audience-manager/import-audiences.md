---
title: 导入Adobe Audience Manager区段以进行广告定位
description: 了解如何导入您的 [!DNL Adobe] Advertising DSP中的受众和使用Adobe Audience Manager进行搜索
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: e6635abdb34444bc40d833a3c6a5eaf07f9f1789
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# 导入Adobe Audience Manager区段以进行广告定位

Advertising DSP和 [!DNL Advertising Search, Social, & Commerce] 每个报表可以拉入所有广告商或代理的元数据、层次结构数据和独特受众数据 [!DNL Adobe] 受众<!-- segments or audiences? Standardize terms per AAM's docs -->，包括：

* Adobe Audience Manager区段

* 发布到Adobe Experience Cloud的Adobe Analytics区段

* 使用Adobe Experience Cloud创建的区段 [!DNL Audience Library]

* 在Adobe Experience Platform中创建并通过Audience Manager发送到Adobe Advertising的区段

要访问 [!DNL Adobe] DSP中的受众或 [!DNL Creative]，必须将受众导入DSP。 要访问 [!DNL Adobe] 中的受众 [!DNL Search, Social, & Commerce]，则必须将受众导入 [!DNL Search, Social, & Commerce].

## 先决条件

* 广告商必须实施 [该 [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview) 版本2.0或更高版本。 此 [!DNL Identity Service] 提供了一个通用的永久性ID，用于在Experience Cloud的所有解决方案中标识您的访客。

  实施包括添加 [!DNL Identity service] 广告商网站上每个网页的代码。

* 组织必须为 [已启用Experience Cloud服务](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview) 并拥有Experience Cloud [!DNL Organization ID] (以前称为 [!DNL IMS org ID])。

  此 [!UICONTROL Organization ID] 允许拥有多个Adobe Experience Cloud产品的组织在某些产品之间共享数据。

* (广告商使用 [!DNL Analytics])广告商必须 [实施 [!DNL Analytics] 使用 `appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) 版本1.6.4或更高版本。

* 广告商的网站访客不包括大量的 [!DNL Apple Safari] 用户。

* (建议广告商同时使用Audience Manager和 [!DNL Analytics])要减少对每个网页的调用，请删除现有Audience Manager [!DNL Data Integration Library] 用于数据收集的代码，并为每个代码启用服务器端转发 [!DNL Analytics] 报表包中使用的错误。 有关更多信息，请参阅&quot;[服务器端转发概述](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* （推荐）为了获得更高的匹配率，请仅将第一方网站数据发送到Adobe Advertising。 如果广告商捆绑来自客户关系管理系统的第三方数据或离线数据，则数据泄露可能会降低匹配率。

## 将Audience Manager受众导入DSP

### 将受众导入到DSP的步骤

此 [!DNL Adobe] 帐户和数据操作团队执行以下步骤。

1. Adobe客户团队应配置广告商级别设置»[!UICONTROL Adobe Analytics Cloud]“

1. Adobe客户团队应向数据运营团队提交请求，以使用Advertising DSP本机API集成导入组织的Audience Manager区段。

### 哪些更改会导致Audience Manager？

API会自动执行以下操作：

* 在Audience Manager中创建两个DSP目标：

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* 将两个目标映射到所有Audience Manager区段，从而允许Audience Manager与同一Experience Cloud关联的DSP广告商帐户共享这些区段 [!DNL Organization ID] 用于Audience Manager。

  企业可以选择从Audience Manager中的目标删除不需要的区段。

* 将以下Exchange Cookie同步像素添加到组织的Audience Manager容器，以扩大客户促销活动的范围：

   * AdobeAdCloud： 411（此像素是标准像素，自动作为的一部分） [!DNL Identity Service] 版本2.0。组织具有 [!DNL Identity Service] 低于2.0的版本应将此像素添加到其Audience Manager容器。

## 将Audience Manager受众导入 [!DNL Search, Social, & Commerce]

### 将受众导入到的步骤 [!DNL Search, Social, & Commerce]

[!DNL Adobe] 人员执行以下大部分或全部步骤。

1. Adobe客户团队应向数据运营团队提交请求，以设置数据运营团队与 [!DNL Search, Social, & Commerce] 和Audience Manager。 包含要导出到的Audience Manager段的名称 [!DNL Search, Social, & Commerce].

1. 在Audience Manager中，配置目标 [!DNL Search, Social, & Commerce]：

   1. 创建两个新目标： `[!UICONTROL Adobe Media Optimizer (HTTP)]` 和 `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] 是以前的名称 [!DNL Search, Social, & Commerce].

   1. 指定每个目标的区段。

      使用 [!UICONTROL Automatically map all current and future segments] 选项，所有区段每天都会映射和同步。

      此 [!UICONTROL Manually map segments] 选项允许您手动映射区段以与批处理目标同步(`[!UICONTROL Adobe Media Optimizer Batch Destination]`)。 无需将任何区段手动映射到HTTP目标。

1. 范围 [!DNL Search, Social, & Commerce]，或者使用 [!DNL Search, Social, & Commerce] 实施团队或具有直接访问客户端管理员角色的用户应该从启动导入 [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   组织的Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID])为必填项。 ID必须与用于组织Audience Manager帐户的ID相同。

### 哪些更改会导致Audience Manager？

两个 [!DNL Search, Social, & Commerce] 目标将可用于Audience Manager中的组织：

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## 数据同步

初次导入大约需要24小时。 初始导入后，数据会实时同步，延迟为1到2秒。

区段成员资格数据仅在发生以下任一事件后发送：

* (使用DSP的广告商)：

   * 该区段在Adobe Advertising展示广告中定位。

   * 该区段将添加到 [!DNL Adobe AdCloud Cross-Channel] Audience Manager用户界面中的批量目标和实时目标。

* (广告商使用 [!DNL Search, Social, & Commerce])：

   * 在Adobe Advertising搜索广告中定位该区段。

   * 该区段将添加到 [!DNL Adobe Media Optimizer] Audience Manager用户界面中的批处理和HTTP目标。

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### DSP如何同步数据

DSP使用自动同步数据 [!DNL Adobe Experience Cloud Identity (ECID) Service]. 在同步过程中， [!DNL ECID Service] 调用Adobe Advertising于 [!DNL cm.everesttech.net]. 由于Adobe Advertising是一个受信任的域，因此ID同步会从父页面中进行，而不是在目标发布iframe中进行，就像与大多数第三方激活合作伙伴进行同步一样。 Audience Manager使用设备ID识别独特用户 [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam)，也称为 [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### 搜索、社交和Commerce如何同步数据

Search、Social和Commerce使用自动同步数据 [!DNL Adobe Experience Cloud Identity (ECID) Service]. 在同步过程中， [!DNL ECID Service] 调用Adobe Advertising于 [!DNL cm.everesttech.net]，这是属于Adobe Advertising的受信任域。 Audience Manager使用设备ID识别独特用户 [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam)，也称为 [!DNL Device ID].

## 在何处查找同步的区段

### 在DSP中

DSP按Audience Manager分类组织区段名称，并在以下项中包含相应的区段成员资格计数：

* [投放设置](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting)：在 [!UICONTROL Adobe Segments] 选项卡 [!UICONTROL Audience Targeting] 部分。

* 在 [受众设置](/help/dsp/audiences/audience-settings.md)：在 [!UICONTROL Adobe Segments] 选项卡。

### 在Advertising Creative中

在 [!DNL Creative]中，这些区段在target节点的体验设置中可用。

### 在 [!DNL Advertising Search, Social, & Commerce]

在 [!DNL Search, Social, & Commerce]，则这些区段在创建 [!DNL Google] 受众使用 [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]”从 [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

对于每个 [!DNL Google] 您创建的受众， [!DNL Google] 提供受众规模。

>[!MORELIKETHIS]
>
>* [Adobe Advertising与Adobe Audience Manager的集成](/help/integrations/audience-manager/overview.md)
