---
title: 支持激活通用ID
description: 了解在以下支持方面的支持：导入通用ID区段，创建自定义区段以跟踪通用ID，以及将第一方区段中的其他用户标识符转换为通用ID以实现无痕定位。
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 0%

---

# 支持激活通用ID

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta功能*

DSP支持基于人员的通用ID，以便跨DSP支持的数字格式进行无cookie、单设备（而非跨设备）定位。

* 您可以使用[!DNL LiveRamp] [!DNL Connect]仪表板手动将经过身份验证的[[!DNL LiveRamp] [!DNL RampIDs]]直接发送到DSP。 请参阅“[从 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)手动导入经过身份验证的区段”。

* DSP可以摄取您的第一方区段(由您在客户数据平台(CDP)中构建的经过哈希处理的电子邮件ID组成)，并将它们转换为[!DNL LiveRamp] [!DNL RampIDs]和[!DNL Unified ID 2.0 (UID2.0)] ID。 有关支持的客户数据平台、每个受支持的通用ID类型的可用功能以及相关工作流的详细信息，请参阅“[关于第一方受众源](/help/dsp/audiences/sources/source-about.md)”。

* 您可以创建自定义区段，以跟踪与从桌面和移动设备中展示广告以及访问特定网页的ID5通用ID关联的用户。 ID5使用概率模型来分配从各种用户信号和浏览器信号派生的ID。 有关说明，请参阅&quot;[创建和实施自定义区段](/help/dsp/audiences/custom-segment-create.md)&quot;。

* 除了由Cookie或设备ID跟踪的用户之外，某些供应商提供的第三方区段还可以自动包含通用ID。 例如，[!DNL Eyeota]中的区段可能自动包含ID5 ID，而[!DNL Lotame]中的区段可能包含UID2.0 ID。 区段详细信息包括每种类型的大小。 每个区段通常收取的使用费（在区段名称旁边列出）将适用；ID5 ID无需额外付费。

## 按通用ID类型报告

* **自定义报告：**&#x200B;自定义报告中提供了按通用ID类型划分的成本、展示次数、点击次数、转化次数和频率数据。

* **[!DNL Analytics]报告：**&#x200B;具有[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)并已实施所有所需步骤的广告商可以在[!DNL Analytics]中按通用ID类型查看直达转化。

  >[!IMPORTANT]
  >
  >要获得正确的转化归因，请确保广告的点进URL同时包括[EF ID和AMO ID](/help/integrations/analytics/ids.md)。

* **区段详细信息：**&#x200B;对于所有区段类型，区段详细信息包括按通用ID类型以及按Cookie或设备ID跟踪的设备类型划分的受众规模。

## 如何在投放位置中定位通用ID受众

>[!NOTE]
>
>您不能在实时投放位置中更改目标ID类型。 如有必要，您可以复制实时版面，并在新版面中更改目标ID类型。

在新的、计划的或暂停的投放位置中，执行以下操作：

1. 在[!UICONTROL Geo-Targeting]部分中，指定要定位的地理区域。 每个通用ID合作伙伴仅允许在特定的地理区域进行用户定位，并且[!UICONTROL Targeting]设置中仅提供符合条件的ID类型。

1. 在[!UICONTROL Audience Targeting]部分中，执行以下操作：

   1. 在[!UICONTROL Included Audiences]设置中，选择用户数据已转换为通用ID的区段。

      您可以根据需要包含其他区段。

   1. 在[!UICONTROL Targeting]设置中：

      1. 选择要定位的通用ID类型。

         该设置包括选项“[!UICONTROL Legacy IDs]”和“[!UICONTROL Universal ID]”，它们可能包括子选项“[!UICONTROL ID5]”、“[!UICONTROL RampID]”和“[!UICONTROL Unified ID2.0]”。 所选地理目标决定了可用的子选项。

         您可以同时选择“[!UICONTROL Legacy IDs]”和“[!UICONTROL Universal ID]”，但每个投放位置只能选择一个类型的通用ID。 当您同时选择旧版ID和通用ID时，会为通用ID提供竞价偏好设置。

      1. （如有必要）接受使用通用ID的服务协议条款。

         在将数据转换为新的ID类型之前，DSP帐户中的用户必须接受服务协议条款。 对于每个ID类型、每个帐户，这些条款只能接受一次。

请参阅“[位置设置](/help/dsp/campaign-management/placements/placement-settings.md)”。

## 测试和数据验证的最佳实践

对于可用Adobe Analytics测量的基于[!DNL RampID]的区段和基于ID5的区段，请使用以下最佳实践。

* 在激活区段大约24小时后，在[!UICONTROL Audiences] > [!UICONTROL All Audiences]内检查该区段的转换ID计数。 如果ID计数异常，请联系您的Adobe客户团队。

  有关区段计数如何变化的更多信息，请参阅&quot;[电子邮件ID和通用ID之间的数据差异](#universal-ids-data-variances)&quot;。

* 请勿更改现有包和投放位置。 但是，如果您没有任何用于测试通用ID的增量预算，请减少原始预算以资助测试。

* 复制原始包和投放位置，根据测试的大小调整预算，将受众更改为使用基于[!DNL RampID]的区段（对于经过身份验证的用户）或基于ID5的区段（对于未经身份验证的用户），并验证新包和投放位置是否花费了其完整预算。

   * 要将基于ID的通用区段的效果与定位其他受众标识符（如Cookie或移动广告ID）的投放效果进行比较，请创建一个活动，其中包含一个单独的基于ID的通用投放和基于ID的旧版投放。

     要进行完整的重定位测试，请同时定位经过身份验证的用户的RampID和未经身份验证的用户的ID5。

     获得最佳性能不应作为主要比较。 相反，请确定哪些ID正在很好地缩放，这可能会稍后通知您的优化和预算分配。 长期目标是弥补在Cookie被弃用时损失的展示次数和网站流量。

   * 要比较浏览器总访问范围，请在相同位置定位基于ID的通用区段和基于ID的旧版区段。 使用与上一个用例相同的营销活动设置，只不过您不需要分摊营销活动预算。

     虽然为通用ID提供了竞价偏好设置，但旧版ID会在通用ID不可用时接收竞价。 确保比较不同浏览器(包括Chrome、Safari和Mozilla)中的范围。

     >[!NOTE]
     >
     >频率上限适用于单个ID。 当用户有多种ID类型时，您与该用户的联系可能会超出您的预期。

* 请记住，经过身份验证的受众区段的访问范围自然小于基于Cookie的区段的访问范围，使用其他定位选项会进一步减少您的访问范围。 谨慎使用粒度定位，尤其是使用AND语句连接多个目标。

## 电子邮件ID与通用ID之间的数据差异 {#universal-ids-data-variances}

### 可接受差异级别

经过哈希处理的电子邮件地址到通用ID的翻译率应大于90%；如果所有经过哈希处理的电子邮件地址都是唯一的，则[!DNL RampIDs]的翻译率尤其应为95%。 例如，如果您从客户数据平台发送了100个经过哈希处理的电子邮件地址，则应将其转换为至少95个[!DNL RampIDs]或超过90个其他类型的通用ID。 较低的翻译率可能表示存在问题。 有关可能的解释，请参阅&quot;[导致差异的原因](#universal-ids-data-variances-causes&quot;。

对于[!DNL RampIDs]，如果翻译率低于70%，请联系您的Adobe客户团队以进一步调查。

### 差异原因 {#universal-ids-data-variances-causes}

* 转换为ID5 ID的经过哈希处理的电子邮件ID：

  概率模型的误差方差为+/-5%。 这意味着它可能高估或低估受众数量5%。

* 已转换为[!DNL RampIDs]的经过哈希处理的电子邮件ID：

   * 如果多个用户档案使用相同的电子邮件ID，则DSP区段计数可能低于客户数据平台中的用户档案计数。 例如，在Adobe Photoshop中，您可以使用单个电子邮件ID创建公司帐户和个人帐户。 但是，如果两个配置文件属于同一个人，则配置文件将映射到同一个电子邮件ID，并相应地映射到一个[!DNL RampID]。

   * [!DNL RampID]可以升级到新值。 如果[!DNL LiveRamp]无法识别电子邮件ID或无法将其映射到其数据库中的现有[!DNL RampID]，则它将新[!DNL RampID]分配给电子邮件ID。 将来，当他们能够将电子邮件ID映射到另一个[!DNL RampID]或者能够收集有关同一电子邮件ID的详细信息时，他们就会将[!DNL RampID]升级到新值。 [!DNL LiveRamp]引用此操作为从“派生”[!DNL RampID]升级到“维护”[!DNL RampID]。 但是，DSP无法获取派生和维护[!DNL RampIDs]之间的映射，因此无法从DSP区段中移除以前版本的RampID。 在这种情况下，区段计数可以大于用户档案计数。

     示例：用户登录到[!DNL Adobe]网站并访问Photoshop页面。 如果[!DNL LiveRamp]没有任何关于电子邮件ID的现有信息，则他们将其分配给派生的[!DNL RampID]，例如D123。 15天后，用户访问同一页面，但[!DNL LiveRamp]在这15天内升级了[!DNL RampID]并将该[!DNL RampID]重新分配到M123。 即使客户数据平台的“Photoshop发烧友”区段仅有一个用户的电子邮件ID，DSP区段仍具有两个RampID：D123和M123。

## 故障排除

如果您没有看到用户计数，或者您的受众规模较低，请检查以下各项：

* 如果您使用[!DNL Flashtalking]或[!DNL Google Campaign Manager 360]广告，请确保广告的点进URL已附加正确的宏。 查看[[!DNL Flashtalking] 广告](/help/integrations/analytics/macros-flashtalking.md)和[[!DNL Google Campaign Manager 360] 广告](/help/integrations/analytics/macros-google-campaign-manager.md)的宏。

* 确保在您的网站上实施正确的、通用的ID合作伙伴特定代码，以匹配网站上的事件和广告曝光。 根据需要与您的[!DNL LiveRamp]或[!DNL ID5]代表合作。

* （对于[!DNL RampIDs]和[!DNL UID 2.0] ID）确保您的[DSP数据源配置正确](/help/dsp/audiences/sources/source-manage.md#source-settings)，并且为生成的受众区段填充用户计数。

* 如果您的覆盖范围小于预期，请检查受众区段逻辑是否不够细化。

* 确保您的营销活动、包和投放位置设置正确。<!-- wording-->

如果您无法解决问题，请联系您的Adobe客户团队。

>[!MORELIKETHIS]
>
>* [关于第一方受众源](/help/dsp/audiences/sources/source-about.md)
>* [管理受众源以激活通用ID受众](/help/dsp/audiences/sources/source-manage.md)
>* [创建和实施自定义区段](/help/dsp/audiences/custom-segment-create.md)
>* [从 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)手动导入经过身份验证的区段
>* [关于受众管理](/help/dsp/audiences/audience-about.md)
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
