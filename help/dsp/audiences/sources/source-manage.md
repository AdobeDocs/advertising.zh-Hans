---
title: 管理受众源以激活通用ID受众
description: 了解如何创建和管理源以从客户数据平台导入受众，并将它们转换为包含通用ID的区段。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: f24aec0588f0298c5a3aa63226bd05bd4fa95f92
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 0%

---

# 管理受众源以激活通用ID受众

*Beta版功能*

在DSP中为客户数据平台中的每个第一方受众创建一个源，您要将该受众转换为包含指定通用ID类型的区段。 您可以将区段导入到贵组织的DSP帐户或广告商帐户。 根据所选通用ID类型收取数据费用。 创建源后，需要执行其他步骤以从每个客户数据平台摄取受众。 请参阅过程末尾的注释以创建源。

您可以稍后更改源受众将翻译成的通用ID类型，并查看更改日志。

您还可以删除源。

## 创建受众源

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. 在主菜单中，单击 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. 单击 **[!UICONTROL Add Source]**.

1. 在 [!UICONTROL Select a Type] 菜单，选择您的 [客户数据平台](source-about.md)：

   * *[!UICONTROL RT-CDP]*：和 [!DNL Adobe Real-Time Customer Data Platform].

   * *[!UICONTROL ActionIQ]*：和 [!DNL ActionIQ] 客户数据平台。

   * *[!UICONTROL Tealium CDP]*：（仅限已配置的用户）和 [!DNL Tealium] 客户数据平台。

1. 指定 [!UICONTROL Data Visibility Level]： *[!UICONTROL Advertiser]* 或 *[!UICONTROL Account]*.

1. 输入其余的 [源设置](#source-settings).

   保留 [!UICONTROL Source Key] 即会生成。 稍后您需要该值。

1. 单击 **[!UICONTROL Save]**.

>[!NOTE]
>
>在为客户数据平台创建源后，您需要完成其他步骤。 请参阅 [用于从导入受众的工作流 [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> 和 [用于从导入受众的工作流 [!DNL Tealium]](source-tealium.md).

## 更改受众源的ID类型

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. 在主菜单中，单击 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. 将光标悬停在源行上并单击 **[!UICONTROL Edit]**.

1. 更改 [为源选择的ID](#source-settings).

1. 单击 **[!UICONTROL Save]**.

## 删除受众源

删除源将删除通过源翻译的区段。<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. 在主菜单中，单击 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. 将光标悬停在源行上并单击 **[!UICONTROL Delete]**.

1. 在确认消息中，单击 **[!UICONTROL Delete]**.

## 查看受众源的更改日志

您可以查看有关对受众源记录所做更改的详细信息，还可以选择将注释附加到日志。

1. 在主菜单中，单击 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. 将光标悬停在源行上并单击 **[!UICONTROL Change log]**.

1. （可选）要在更改日志中附加注释，请执行以下操作：

   1. 将光标悬停在源行上并单击 **[!UICONTROL Add Notes]**.

   1. 输入注释，然后单击 **[!UICONTROL Save]**.

      最大长度为256个字符。

1. （可选）要在更大的详细信息屏幕中打开日志，请将光标悬停在源行上，然后单击 **[!UICONTROL View Details]**.

## 受众源设置 {#source-settings}

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
>* [关于第一方受众源](source-about.md)
>* [从手动导入经过身份验证的区段 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Adobe Advertising DSP连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
