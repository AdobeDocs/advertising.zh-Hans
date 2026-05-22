---
title: 管理受众源以激活通用ID受众
description: 了解如何创建和管理源以从客户数据平台导入受众，并将它们转换为包含通用ID的区段。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
TQID: https://experienceleague.adobe.com/us8NC8BEngb240MAW8hEo-DHGoW7MRDWvu0HedMsnFs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 14a4d5b0bbe27697668b4a1a8eb3a7f74a18cc04
workflow-type: tm+mt
source-wordcount: 881
ht-degree: 0%

---

# 管理受众源以激活通用ID受众

在DSP中为客户数据平台中的每个第一方受众创建一个源，您要将该受众导入或转换为包含指定通用ID类型的区段。 您可以将区段导入到贵组织的DSP帐户或广告商帐户。 将受众转换为通用ID时，会根据所选的通用ID类型收费。 创建源后，需要执行其他步骤以从每个客户数据平台流式传输源受众。 请参阅过程末尾的注释以创建源。

对于除[!DNL AdFixus]之外的所有客户数据平台，您以后可以更改源受众所转换到的通用ID类型，并查看更改日志。

您还可以删除源。

## 创建受众源

您可以为通用ID合作伙伴和帐户或单个广告商的每个组合创建一个源。 例如，您可以为帐户有一个[!UICONTROL RT-CDP]源，为广告商1有一个[!UICONTROL RT-CDP]源，为广告商2有一个[!UICONTROL RT-CDP]源。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL Sources]**。

1. 单击&#x200B;**[!UICONTROL Add Source]**。

1. 在[!UICONTROL Select a Type]菜单中，选择您的[客户数据平台](source-about.md)：

   * *[!UICONTROL RT-CDP]*： [!DNL Adobe Real-Time CDP]。

   * *[!UICONTROL AdFixus ID]*： [!DNL AdFixus]客户数据平台。 仅适用于澳大利亚的广告商。

   * *[!UICONTROL ActionIQ]*： [!DNL ActionIQ]客户数据平台。

   * *[!UICONTROL Amperity]*： [!DNL Amperity]客户数据平台。

   * *[!UICONTROL Optimizely]*： [!DNL Optimizely]客户数据平台。

   * *[!UICONTROL Tealium CDP]*： （仅配置用户） [!DNL Tealium]客户数据平台。

1. 指定[!UICONTROL Data Visibility Level]： *[!UICONTROL Advertiser]*&#x200B;或&#x200B;*[!UICONTROL Account]*。

1. 输入其余的[源设置](#source-settings)。

   保留生成的[!UICONTROL Source Key]的副本。 稍后您需要该值。

1. 单击&#x200B;**[!UICONTROL Save]**。

>[!NOTE]
>
>为客户数据平台创建源后，必须完成其他步骤以导入受众：
>* 对于[!DNL ActionIQ]源，请与您的Adobe客户团队合作。
>* 对于其他源类型，请参阅<!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), -->  [!DNL AdFixus][&#128279;](source-adfixus.md), the [workflow for [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)的[工作流、 [!DNL Amperity]](source-amperity.md)的[工作流、 [!DNL Optimizely]](source-optimizely.md)的[工作流和 [!DNL Tealium]](source-tealium.md)的工作流。

## 更改受众源的ID类型

*适用于除[!DNL AdFixus]*&#x200B;之外的所有受支持的客户数据平台

<!-- 
Clarify this:

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses that you shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we don't delete any historical IDs of that type from the segments shared through the source.

-->

1. 在主菜单中，单击&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL Sources]**。

1. 将光标悬停在源行上并单击&#x200B;**[!UICONTROL Edit]**。

1. 更改为源[&#128279;](#source-settings)选择的ID。

1. 单击&#x200B;**[!UICONTROL Save]**。

## 删除受众源

删除源将删除通过源导入的区段，包括所有已翻译的ID。<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. 在主菜单中，单击&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL Sources]**。

1. 将光标悬停在源行上并单击&#x200B;**[!UICONTROL Delete]**。

1. 在确认消息中，单击&#x200B;**[!UICONTROL Delete]**。

## 查看受众源的更改日志

您可以查看有关对受众源记录所做更改的详细信息，还可以选择将注释附加到日志。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL Sources]**。

1. 将光标悬停在源行上并单击&#x200B;**[!UICONTROL Change log]**。

1. （可选）要在更改日志中附加注释，请执行以下操作：

   1. 将光标悬停在源行上并单击&#x200B;**[!UICONTROL Add Notes]**。

   1. 输入注释，然后单击&#x200B;**[!UICONTROL Save]**。

      最大长度为256个字符。

1. （可选）要在更大的详细信息屏幕中打开日志，请将光标悬停在源行上，然后单击&#x200B;**[!UICONTROL View Details]**。

## 受众源设置 {#source-settings}

**[!UICONTROL Data Visibility Level]：**&#x200B;区段是否可供具有帐户(*[!UICONTROL Advertiser]*)访问权限的单个广告商使用，或可供具有帐户&#x200B;*[!UICONTROL Account]*&#x200B;访问权限的所有广告商使用。

**[!UICONTROL Advertiser]：** （仅限广告商级别的可见性）区段可用的广告商。 从具有帐户访问权限的广告商列表中选择一个。

**[!UICONTROL Enter IMS Org Id]：** （仅限[!DNL Real-Time CDP]个源） [!DNL Adobe Experience Platform]帐户的Adobe CX Enterprise组织ID。

**[!UICONTROL Convert PII to the following IDs]：** （适用于除[!DNL AdFixus]之外的所有受支持的客户数据平台）要将个人身份信息(PII)转换为的ID类型。 如果选择多种类型，则生成的区段将填充每个选定ID类型的值（例如每个电子邮件地址的[!DNL RampID]和[!DNL Unified ID2.0]）。 数据收费也相应地计算。

对于[!DNL RampID]和[!DNL Unified ID2.0]，供应商会查找每个电子邮件地址，以查看该ID是否已存在，并在可用时将地址转换为匹配的ID。 如果地址不存在ID，则会创建新的ID。

>[!NOTE]
>
>在单个投放位置中只能定位一种类型的ID。 要按ID类型测试性能，请[为区段中的每个ID类型创建一个单独的版面](/help/dsp/campaign-management/placements/placement-create.md)。

* *[!DNL RampID]：*&#x200B;要将PII转换为[!DNL RampID]。 您可以使用[!DNL RampIDs]重新定位登录用户和[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)测量。

* *[!DNL Unified ID2.0]：*&#x200B;要将PII转换为[统一ID 2.0](https://unifiedid.com) ID以重新定位登录用户。

<!--
 Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]：**&#x200B;用于将PII转换为通用ID的服务条款协议。 您或DSP帐户中的其他用户必须接受一次条款，然后才能导入ID、将数据转换为新的ID类型或定位ID类型。对于具有托管服务合同的客户，您的Adobe帐户团队将获得您的同意，并代表贵组织接受条款。 若要阅读术语，请单击&#x200B;**>**。 要接受条款，请滚动到条款的底部并单击&#x200B;**[!UICONTROL Accept]**。

**[!UICONTROL Source Key]：**（只读；自动生成）可用于在客户数据平台中创建目标连接以将受众推送到Advertising DSP的源密钥。 您可以将值复制到剪贴板以粘贴到目标连接设置或文件中。 与将让受众流式传输到DSP的团队共享该值。

>[!MORELIKETHIS]
>
>* [关于第一方受众源](source-about.md)
>* [支持激活通用ID](/help/dsp/audiences/universal-ids.md)
>* [将用户ID从 [!DNL Adobe Real-Time CDP] 转换为通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [将用户ID从 [!DNL Amperity] 转换为通用ID](/help/dsp/audiences/sources/source-amperity.md)
>* [将用户ID从 [!DNL Optimizely] 转换为通用ID](/help/dsp/audiences/sources/source-optimizely.md)
>* [将用户ID从 [!DNL Tealium] 转换为通用ID](/help/dsp/audiences/sources/source-tealium.md)
>* [从 [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)导入第一方区段
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
