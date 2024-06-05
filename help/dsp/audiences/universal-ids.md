---
title: 支持激活通用ID
description: 了解在以下支持方面的支持：导入通用ID区段，创建自定义区段以跟踪通用ID，以及将第一方区段中的其他用户标识符转换为通用ID以实现无痕定位。
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 2d8edb7e5c32ba7077a7f4e6550ed22ec680b1fc
workflow-type: tm+mt
source-wordcount: '1366'
ht-degree: 0%

---

# 支持激活通用ID

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta版功能*

DSP支持基于人员的通用ID，以便跨DSP支持的数字格式进行无cookie、单设备（而非跨设备）定位。

* 您可以手动发送经过身份验证的[[!DNL LiveRamp] [!DNL RampIDs]]直接访问DSP，使用 [!DNL LiveRamp] [!DNL Connect] 仪表板。 请参阅&quot;[从手动导入经过身份验证的区段 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)“

* DSP可以摄取您的第一方区段(由在客户数据平台(CDP)中构建的经过哈希处理的电子邮件ID组成)，并将它们转换为 [!DNL LiveRamp] [!DNL RampIDs] 和 [!DNL Unified ID 2.0 (UID2.0)] ID。 有关受支持的客户数据平台、每种受支持的通用ID类型的可用功能以及相关工作流的更多信息，请参阅“[关于第一方受众源](/help/dsp/audiences/sources/source-about.md)“

* 您可以创建自定义区段，以跟踪与从桌面和移动设备中展示广告以及访问特定网页的ID5通用ID关联的用户。 ID5使用概率模型来分配从各种用户信号和浏览器信号派生的ID。 有关说明，请参阅&quot;[创建和实施自定义区段](/help/dsp/audiences/custom-segment-create.md)“

* 来自的第三方区段 [!DNL Eyeota] 除了Cookie或设备ID跟踪的用户之外，其他一些供应商可能会自动包含ID5 ID。 区段详细信息包括每种类型的大小。 每个区段通常收取的使用费（在区段名称旁边列出）将适用；ID5 ID无需额外付费。

<!-- Make above statement more generic when other ID types are available 

* Some third-party segment vendors have started including universal IDs in their segments, and you can use them in saved audiences and as placement targets without any extra steps or extra fees.
-->

## 按通用ID类型报告

* **自定义报表：** 在自定义报表中提供了按通用ID类型划分的成本、展示次数、点击次数、转化次数和频率数据。

* **[!DNL Analytics]报告：** 广告商使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) 已实施所有必需步骤的用户可以在以下位置查看按通用ID类型划分的显示到达转换： [!DNL Analytics].

  >[!IMPORTANT]
  >
  >要获得正确的转化归因，请确保广告的点进链接URL同时包括 [EF ID和AMO ID](/help/integrations/analytics/ids.md).

* **区段详细信息：** 对于所有区段类型，区段详细信息包括按通用ID类型以及按Cookie或设备ID跟踪的设备类型划分的受众规模。

## 如何在投放位置中定位通用ID受众

>[!NOTE]
>
>您不能在实时投放位置中更改目标ID类型。 如有必要，您可以复制实时版面，并在新版面中更改目标ID类型。

在新的、计划的或暂停的投放位置中，执行以下操作：

1. 在 [!UICONTROL Geo-Targeting] 部分，指定要定位的地理区域。 每个通用ID合作伙伴仅允许在特定地理区域中进行用户定位，并且中仅提供符合条件的ID类型 [!UICONTROL Targeting] 设置。

1. 在 [!UICONTROL Audience Targeting] 部分，执行以下操作：

   1. 在 [!UICONTROL Included Audiences] 设置，选择用户数据转换为通用ID的区段。

      您可以根据需要包含其他区段。

   1. 在 [!UICONTROL Targeting] 设置：

      1. 选择要定位的通用ID类型。

         该设置包括选项»[!UICONTROL Legacy IDs]”和“[!UICONTROL Universal ID]，其中可能包含子选项“[!UICONTROL ID5]，&quot; &quot;[!UICONTROL RampID]，”和“[!UICONTROL Unified ID2.0]“ 所选地理目标决定了可用的子选项。

         您可以选择两者[!UICONTROL Legacy IDs]”和“[!UICONTROL Universal ID]，”，但您只能为每个投放位置选择一种类型的通用ID。 当您同时选择旧版ID和通用ID时，会为通用ID提供竞价偏好设置。

      1. （如有必要）接受使用通用ID的服务协议条款。

         在将数据转换为新的ID类型之前，DSP帐户中的用户必须接受服务协议条款。 对于每个ID类型、每个帐户，这些条款只能接受一次。

请参阅&quot;[投放设置](/help/dsp/campaign-management/placements/placement-settings.md)“

## 测试和数据验证的最佳实践

使用以下最佳实践 [!DNL RampID]基于的区段和基于ID5的区段，对于它们，Adobe Analytics测量可用。

* 在激活区段大约24小时后，检查内该区段的转换ID计数 [!UICONTROL Audiences] > [!UICONTROL All Audiences]. 如果ID计数异常，请联系您的Adobe客户团队。

  请参阅&quot;[电子邮件ID与通用ID之间的数据差异原因](#universal-ids-data-variances)”以了解有关区段计数如何变化的更多信息。

* 请勿更改现有包和投放位置。 但是，如果您没有任何用于测试通用ID的增量预算，请减少原始预算以资助测试。

* 复制原始包和投放位置，根据测试的大小调整预算，更改要使用的受众 [!DNL RampID]基于的区段（适用于经过身份验证的用户）或基于ID5的区段（适用于未经身份验证的用户），并验证新资源包和投放位置是否花费了其全部预算。

   * 要将基于ID的通用区段的效果与定位其他受众标识符（如Cookie或移动广告ID）的投放效果进行比较，请创建一个活动，其中包含一个单独的基于ID的通用投放和基于ID的旧版投放。

     要进行完整的重定位测试，请同时定位经过身份验证的用户的RampID和未经身份验证的用户的ID5。

     获得最佳性能不应作为主要比较。 相反，请确定哪些ID正在很好地缩放，这可能会稍后通知您的优化和预算分配。 长期目标是弥补在Cookie被弃用时损失的展示次数和网站流量。

   * 要比较浏览器总访问范围，请在相同位置定位基于ID的通用区段和基于ID的旧版区段。 使用与上一个用例相同的营销活动设置，只不过您不需要分摊营销活动预算。

     虽然为通用ID提供了竞价偏好设置，但旧版ID会在通用ID不可用时接收竞价。 确保比较不同浏览器（包括Chrome、Safari和Mozilla）中的范围。

     >[!NOTE]
     >
     >频率上限适用于单个ID。 当用户有多种ID类型时，您与该用户的联系可能会超出您的预期。

* 请记住，经过身份验证的受众区段的访问范围自然小于基于Cookie的区段的访问范围，使用其他定位选项会进一步减少您的访问范围。 谨慎使用粒度定位，尤其是使用AND语句连接多个目标。

## 电子邮件ID与通用ID之间的数据差异原因 {#universal-ids-data-variances}

转换为的经过哈希处理的电子邮件ID之所以存在差异，原因有二 [!DNL RampIDs]：

* 如果多个用户档案使用相同的电子邮件ID，则DSP区段计数可能低于客户数据平台中的用户档案计数。 例如，在Adobe Photoshop中，您可以使用单个电子邮件ID创建公司帐户和个人帐户。 但是，如果两个用户档案都属于同一区段，则用户档案将映射到同一个电子邮件ID，并相应地映射到一个ID [!DNL RampID].

* A [!DNL RampID] 可以升级到新值。 如果 [!DNL LiveRamp] 无法识别电子邮件ID或无法将其映射到现有的电子邮件ID [!DNL RampID] 在其数据库中，它分配一个新的 [!DNL RampID] 到电子邮件ID。 将来，他们何时可以将电子邮件ID映射到另一个 [!DNL RampID] 或者可以收集有关同一电子邮件ID的更多信息，则会升级 [!DNL RampID] 转换为新值。 [!DNL LiveRamp] 将此操作称为从“派生”升级 [!DNL RampID] 到“维护的” [!DNL RampID]. 但是，DSP不会获得派生与维护之间的映射 [!DNL RampIDs] 因此，无法从DSP区段中移除先前版本的RampID。 在这种情况下，区段计数可以大于用户档案计数。

  示例：用户登录到 [!DNL Adobe] 网站和访问Photoshop页面。 如果 [!DNL LiveRamp] 没有任何关于电子邮件ID的现有信息，则他们会将其分配给派生 [!DNL RampID]例如D123。 15天后，用户访问同一页面，但 [!DNL LiveRamp] 已升级 [!DNL RampID] 于该15天内，并已重新 [!DNL RampID] 到M123。 即使客户数据平台的“Photoshop发烧友”区段仅有一个用户的电子邮件ID，DSP区段仍具有两个RampID：D123和M123。

## 故障排除

如果您没有看到用户数，或者您的受众规模较低，请检查以下各项：

* 如果您使用 [!DNL Flashtalking] 或 [!DNL Google Campaign Manager 360] 然后，确保广告的点进URL已附加正确的宏。 查看宏 [[!DNL Flashtalking] 广告](/help/integrations/analytics/macros-flashtalking.md) 和 [[!DNL Google Campaign Manager 360] 广告](/help/integrations/analytics/macros-google-campaign-manager.md).

* 确保在您的网站上实施正确的、通用的ID合作伙伴特定代码，以匹配网站上的事件和广告曝光。 使用您的 [!DNL LiveRamp] 或 [!DNL ID5] 代表性。

* (用于 [!DNL RampIDs] 和 [!DNL UID 2.0] ID)确保您的 [DSP数据源配置正确](/help/dsp/audiences/sources/source-settings.md)，并为生成的受众区段填充用户计数。

* 如果您的覆盖范围小于预期，请检查受众区段逻辑是否不够细化。

如果您无法解决问题，请联系您的Adobe客户团队。

>[!MORELIKETHIS]
>
>* [创建受众源以激活通用ID受众](/help/dsp/audiences/sources/source-create.md)
>* [转换用户ID [!DNL Adobe Real-Time CDP] 到通用ID](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [转换用户ID [!DNL Tealium] 到通用ID](/help/dsp/audiences/sources/source-tealium.md)
>* [创建和实施自定义区段](/help/dsp/audiences/custom-segment-create.md)
>* [从手动导入经过身份验证的区段 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
>* [投放设置](/help/dsp/campaign-management/placements/placement-settings.md)

<!--
>* [Convert User IDs from [!DNL Optimizely] to Universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
-->
