---
title: 导入Adobe Audience Manager区段以进行广告定位
description: 了解如何将 [!DNL Adobe] 受众导入Advertising DSP并使用Adobe Audience Manager搜索
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# 导入Adobe Audience Manager区段以进行广告定位

Advertising DSP和[!DNL Advertising Search, Social, & Commerce]可以各自为广告商或机构的所有受众[!DNL Adobe]拉入元数据、层次结构数据和唯一受众数据<!-- segments or audiences? Standardize terms per AAM's docs -->，包括：

* Adobe Audience Manager区段

* 发布到Adobe Experience Cloud的Adobe Analytics区段

* 使用Adobe Experience Cloud [!DNL Audience Library]创建的区段

* 在Adobe Experience Platform中创建并通过Audience Manager发送到Adobe Advertising的区段

要在DSP或[!DNL Creative]中访问[!DNL Adobe]受众，必须将受众导入DSP。 要访问[!DNL Search, Social, & Commerce]中的[!DNL Adobe]受众，必须将受众导入到[!DNL Search, Social, & Commerce]中。

## 先决条件

* 广告商必须实施[the [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview)版本2.0或更高版本。 [!DNL Identity Service]提供了一个通用的永久性ID，用于在Experience Cloud的所有解决方案中标识您的访客。

  实施包括将[!DNL Identity service]代码添加到广告商网站上的每个网页。

* 组织必须为Experience Cloud服务[&#128279;](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview)启用，并且具有Experience Cloud [!DNL Organization ID]（以前称为[!DNL IMS org ID]）。

  [!UICONTROL Organization ID]允许拥有多个Adobe Experience Cloud产品的组织在某些产品之间共享数据。

* （使用[!DNL Analytics]的广告商）该广告商必须[使用`appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview)版本1.6.4或更高版本实施 [!DNL Analytics] 。

* 广告商的网站访客不包括大量的[!DNL Apple Safari]用户。

* (当广告商同时使用Audience Manager和[!DNL Analytics]时推荐)要减少对每个网页的调用，请删除用于数据收集的现有Audience Manager [!DNL Data Integration Library]代码，并为每个[!DNL Analytics]报表包启用服务器端转发。 有关详细信息，请参阅[服务器端转发概述](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf)。

* （推荐）为了获得更高的匹配率，请仅将第一方网站数据发送到Adobe Advertising。 如果广告商捆绑来自客户关系管理系统的第三方数据或离线数据，则数据泄露可能会降低匹配率。

## 将Audience Manager受众导入DSP

### 将受众导入到DSP的步骤

[!DNL Adobe]帐户和数据操作团队执行以下步骤。

1. Adobe客户团队应配置广告商级别设置“[!UICONTROL Adobe Analytics Cloud]”。

1. Adobe客户团队应向数据运营团队提交请求，以使用Advertising DSP本机API集成导入组织的Audience Manager区段。

### Audience Manager做出了哪些更改？

API会自动执行以下操作：

* 在Audience Manager中创建两个DSP目标：

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* 将两个目标映射到所有Audience Manager区段，从而允许Audience Manager与DSP广告商帐户(该帐户与用于Audience Manager的相同Experience Cloud [!DNL Organization ID]关联)共享这些区段。

  该企业可以选择从Audience Manager中的目标删除不需要的区段。

* 将以下Exchange Cookie同步像素添加到组织的Audience Manager容器中，以提高客户促销活动的覆盖率：

   * Adobe AdCloud： 411(此像素是标准像素，自动作为[!DNL Identity Service]版本2.0的一部分。[!DNL Identity Service]版本低于2.0的组织应将此像素添加到其Audience Manager容器。

## 将Audience Manager受众导入[!DNL Search, Social, & Commerce]

### 将受众导入到[!DNL Search, Social, & Commerce]的步骤

[!DNL Adobe]人员执行以下大部分或全部步骤。

1. Adobe客户团队应向数据运营团队提交请求，以设置[!DNL Search, Social, & Commerce]与Audience Manager之间的集成。 包含要导出到[!DNL Search, Social, & Commerce]的Audience Manager区段名称。

1. 在Audience Manager中，为[!DNL Search, Social, & Commerce]配置目标：

   1. 创建两个新目标： `[!UICONTROL Adobe Media Optimizer (HTTP)]`和`[!UICONTROL Adobe Media Optimizer Batch Destination]`。

      [!DNL Media Optimizer]是以前的[!DNL Search, Social, & Commerce]名称。

   1. 指定每个目标的区段。

      使用[!UICONTROL Automatically map all current and future segments]选项，所有区段每天都会映射并同步。

      [!UICONTROL Manually map segments]选项允许您手动映射区段以与批处理目标(`[!UICONTROL Adobe Media Optimizer Batch Destination]`)同步。 无需将任何区段手动映射到HTTP目标。

1. 在[!DNL Search, Social, & Commerce]内，[!DNL Search, Social, & Commerce]实施团队或具有直接访问客户端管理器角色的用户应从[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup]启动导入。

   需要组织的Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID])。 ID必须与用于组织的Audience Manager帐户的ID相同。

### Audience Manager做出了哪些更改？

在Audience Manager中，组织可以使用两个[!DNL Search, Social, & Commerce]目标：

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## 数据同步

初次导入大约需要24小时。 初始导入后，数据会实时同步，延迟为1到2秒。

区段成员资格数据仅在发生以下任一事件后发送：

* (使用DSP的广告商)：

   * 该区段在Adobe Advertising展示广告中定位。

   * 该区段将添加到Audience Manager用户界面的[!DNL Adobe AdCloud Cross-Channel]批次和实时目标。

* （具有[!DNL Search, Social, & Commerce]的广告商）：

   * 在Adobe Advertising搜索广告中定位该区段。

   * 该区段将添加到Audience Manager用户界面的[!DNL Adobe Media Optimizer]批次和HTTP目标。

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### DSP如何同步数据

DSP使用[!DNL Adobe Experience Cloud Identity (ECID) Service]自动同步数据。 在同步过程中，[!DNL ECID Service]在[!DNL cm.everesttech.net]处调用Adobe Advertising。 由于Adobe Advertising是一个受信任的域，因此ID同步会从父页面中进行，而不是在目标发布iframe中进行，就像与大多数第三方激活合作伙伴进行同步一样。 Audience Manager使用[Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam)（也称为[!DNL Device ID]）按设备ID识别独特用户。

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### 搜索、社交和Commerce如何同步数据

Search、Social和Commerce使用[!DNL Adobe Experience Cloud Identity (ECID) Service]自动同步数据。 在同步过程中，[!DNL ECID Service]在[!DNL cm.everesttech.net]处调用Adobe Advertising，这是属于Adobe Advertising的受信任域。 Audience Manager使用[Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam)（也称为[!DNL Device ID]）按设备ID识别独特用户。

## 在何处查找同步的区段

### 在DSP中

DSP按Audience Manager分类组织区段名称，并在以下项中包含相应的区段成员资格计数：

* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting)：在[!UICONTROL Audience Targeting]分区的[!UICONTROL Adobe Segments]选项卡上。

* 在[受众设置](/help/dsp/audiences/audience-settings.md)中：在[!UICONTROL Adobe Segments]选项卡上。

### 在Advertising Creative中

在[!DNL Creative]中，区段在目标节点的体验设置中可用。

### 在[!DNL Advertising Search, Social, & Commerce]

在[!DNL Search, Social, & Commerce]中，当您从[!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library]使用[!UICONTROL Data Source]“[!UICONTROL Adobe Audience]”创建[!DNL Google]受众时，区段可用。

对于您创建的每个[!DNL Google]受众，[!DNL Google]提供受众大小。

>[!MORELIKETHIS]
>
>* [Adobe Advertising与Adobe Audience Manager的集成](/help/integrations/audience-manager/overview.md)
