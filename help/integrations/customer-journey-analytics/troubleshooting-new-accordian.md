---
title: Customer Journey Analytics中的Adobe Advertising数据疑难解答
description: 了解如何对Customer Journey Analytics中的Adobe Advertising数据问题进行故障排除和解决。
feature: Integration with Adobe Customer Journey Analytics
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: b0f629e862e1008ca39b7f96901d47abbe595452
workflow-type: tm+mt
source-wordcount: 3094
ht-degree: 0%

---

# Customer Journey Analytics中的Adobe Advertising数据疑难解答

以下是潜在问题、其可能原因和解决方案。

## 所有潜在症状的列表

| 症状 | 更多信息 |
| ------- | ---------------- |
| 在浏览器的“网络”选项卡中看不到alloy()调用 | 请参阅“[安装和设置问题](#issues-installation-setup)”>“[WebSDK扩展未初始化](#websdk-extension-doesn't-initialize)”部分 |
| 控制台错误：未定义alloy | 请参阅“[安装和设置问题](#issues-installation-setup)”>“[WebSDK扩展未初始化](#websdk-extension-doesn't-initialize)” |
| 不与edge.adobedc.net交互或收集请求 | 请参阅“[安装和设置问题](#issues-installation-setup)”>“[WebSDK扩展未初始化](#websdk-extension-doesn't-initialize)” |
| 请求到达边缘，但返回400或500错误 | 请参阅“[安装和设置问题](#issues-installation-setup)”>“[数据流未配置或配置错误](#datastream-not-configured-or-misconfigured)”部分 |
| Adobe Analytics或Adobe Advertising报表中不显示任何数据 | 请参阅“[安装和设置问题](#issues-installation-setup)”>“[数据流未配置或配置错误](#datastream-not-configured-or-misconfigured)”部分 |
| 网络响应错误：“未找到数据流” | 请参阅“[安装和设置问题](#issues-installation-setup)”>“[数据流未配置或配置错误](#datastream-not-configured-or-misconfigured)”部分 |
| 访客ID在页面之间发生更改 | 请参阅“[安装和设置问题](#issues-installation-setup)”>“[标识和ECID问题](#identity-and-ecid-issues)”部分 |
| Advertising受众区段不匹配 | 请参阅“[安装和设置问题](#issues-installation-setup)”>“[标识和ECID问题](#identity-and-ecid-issues)”部分 |
| 调试器会显示不满足规则条件 | 请参阅“[安装和设置问题](#issues-installation-setup)”>“[规则或事件未触发](#rules-or-events-aren't-firing)”部分 |
| [!UICONTROL Send Event]操作从不执行 | 请参阅“[安装和设置问题](#issues-installation-setup)”>“[规则或事件未触发](#rules-or-events-aren't-firing)”部分 |
| 在[!DNL Tags]中所做的更改未反映在实时网站上 | 请参阅“[安装和设置问题](#issues-installation-setup)”>“[库生成和发布问题](#library-build-and-publishing-issues)”部分 |
| 应用了扩展更新，但旧行为仍然存在 | 请参阅“[安装和设置问题](#issues-installation-setup)”>“[库生成和发布问题](#library-build-and-publishing-issues)”部分 |
| `alloy()`发送事件调用成功（响应为200），但报表中缺少Adobe Advertising转化数据 | 请参阅“[安装和设置问题](#issues-installation-setup)”>“[Advertising字段的架构验证问题](#schema-validation-for-advertising-fields)”部分 |
| 调试器中的XDM有效负载未显示`_experience.adcloud`对象 | 请参阅“[安装和设置问题](#issues-installation-setup)”>“[Advertising字段的架构验证问题](#schema-validation-for-advertising-fields)”部分 |
| 不会为网页记录显示到达或点进转化 | 请参阅“[Advertising扩展设置问题](#advertising-extension-setup-issues)”部分 |
| 点进的体验数据模型(XDM)有效负载中缺少`_experience.adcloud` | 请参阅“[Advertising扩展设置问题](#advertising-extension-setup-issues)”部分 |
| 转化在调试器工具中确认，但不显示在Adobe Advertising报表中 | 请参阅“[Advertising扩展设置问题](#advertising-extension-setup-issues)”部分 |

## 安装和设置问题 {#issues-installation-setup}

### WebSDK扩展未初始化#websdk-extension-doesn&#39;t-initialize

#### 问题：

* 在浏览器的“网络”选项卡中看不到alloy()调用
* 控制台错误：未定义alloy
* 不与edge.adobedc.net交互或收集请求

#### 可能的原因和验证/解决方案

+++ 库未发布或处于草稿状态

转到[发布流](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow)，并确保包含WebSDK扩展的库处于已批准/已发布状态。

+++

+++ 嵌入代码缺少或环境错误

验证网页上的[!DNL Tags]嵌入代码是否引用了正确的环境(Dev/Stage/Prod)。 在`<head>`标记中查找`//assets.adobedtm.com/...`脚本标记的环境。

+++

+++ 异步与同步加载冲突

确保每个网页仅存在一个[!DNL Tags]嵌入代码。 重复嵌入代码会导致争用情况。

+++

+++ 内容安全策略(CSP)阻止

将`edge.adobedc.net`和`assets.adobedtm.com`添加到您的CSP `connect-src`和`script-src`指令。

+++

### 数据流未配置或配置错误 {#datastream-not-configured-or-misconfigured}

#### 问题：

* 请求到达边缘，但返回400或500错误
* Adobe Analytics或Adobe Advertising报表中不显示任何数据<!-- It's not useful to organize this info by cause, not symptom -->
* 网络响应错误：“未找到数据流”

#### 可能的原因和验证/解决方案

+++ 标记属性的数据流ID缺失或不正确

1. 在[!DNL Tags]中，打开标记属性的[数据流配置设置](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams)。
1. 确认[!UICONTROL Datastream]字段指向每个环境（开发、暂存和生产）的正确数据流，以及正确的架构和数据集。

   除非您在所有三个环境中明确共享一个数据流，否则每个环境都应拥有自己的数据流。

+++

+++ 没有为tag属性启用数据流服务

[打开数据流设置](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)，并确保已启用以下服务：

* Adobe Advertising（用于转化/受众同步）
* Adobe Experience Platform（用于配置文件摄取）

+++

+++ 沙盒不匹配

确保数据流与您的架构和数据集属于相同的Adobe Experience Platform沙盒。 一个常见错误是在生产沙盒中创建数据流，但将架构指向开发沙盒。

+++

### 身份和ECID问题 {#identity-and-ecid-issues}

#### 问题：

* 访客ID在页面之间发生更改
* Advertising受众区段不匹配

#### 可能的原因和验证/解决方案

+++ 已阻止第三方Cookie

通过在数据流的边缘配置中配置第一方域来迁移到第一方CNAME数据收集。

+++

+++ 存在旧版`s_ecid` Cookie时，`idMigrationEnabled`设置为`false`

在WebSDK基本配置中设置`idMigrationEnabled: true`以从`s_ecid`或`AMCV_` Cookie迁移现有ECID。

+++

### 规则或事件未触发#rules-or-events-aren&#39;t-string

#### 问题：

* 调试器会显示不满足规则条件
* [!UICONTROL Send Event]操作从不执行

#### 核查和解决

+++ 验证以下内容：

* 规则将保存并包含在活动库内部版本中。
* 事件类型与实际页面行为（例如，[!UICONTROL Library Loaded]与[!UICONTROL DOM Ready]对比[!UICONTROL Window Loaded]）匹配。
* 规则的条件限制不太严格。 通过暂时消除条件来测试以隔离问题。
* 规则顺序正确。 如果多个规则共享同一事件，请检查规则顺序。
* 页面上先前没有任何JavaScript错误正在停止执行。 检查浏览器控制台中是否存在未捕获的异常。

+++

### 库生成和发布问题 {#library-build-and-publishing-issues}

#### 问题：

* 在[!DNL Tags]中所做的更改未反映在实时网站上
* 应用了扩展更新，但旧行为仍然存在

#### 可能的原因和验证/解决方案

+++ 更改未添加到库

在[!UICONTROL Publishing Flow]中，确认您的更改已添加到开发环境中的库。 转到[!UICONTROL Libraries]，打开工作库，选择&#x200B;**添加所有更改的资源**，然后选择&#x200B;**保存并生成**。

+++

+++ 浏览器正在缓存旧库

执行硬刷新（Ctrl+Shift+R或Cmd+Shift+R），或在无痕的/专用窗口中打开页面。 如果问题仍然存在，请完全清除浏览器缓存。

+++

+++ 嵌入代码适用于错误的环境

如果要测试生产行为，请确认页面上的嵌入代码是生产嵌入代码。

+++

+++ 库生成以静默方式失败

转到[!UICONTROL Publishing Flow]并检查库是否显示[!UICONTROL Build Failed]状态。 打开库并查看生成日志 — 常见原因是规则配置无效或扩展版本冲突。

+++

### Advertising字段的架构验证问题 {#schema-validation-for-advertising-fields}

#### 问题：

* `alloy()`发送事件调用成功（响应为200），但报表中缺少Adobe Advertising转化数据
* 调试器中的XDM有效负载未显示`_experience.adcloud`对象

#### 可能的原因和验证/解决方案

+++ 架构中缺少[!UICONTROL Advertising]字段组

确保已将[!UICONTROL Advertising]字段组添加到架构中。

1. 转到Adobe Experience Platform > [!UICONTROL Data Management] > [!UICONTROL Schemas]。
1. 打开数据流使用的架构。
1. 在[!UICONTROL Field Groups]面板中，确认已列出&#x200B;**Adobe Advertising Cloud ExperienceEvent完整扩展**。
1. 如果缺少该扩展，请选择&#x200B;**添加**，搜索&#x200B;**Adobe Advertising Cloud**，选择&#x200B;**Adobe Advertising Cloud ExperienceEvent完整扩展**，然后保存设置。

>[!NOTE]
>仅对架构更改而言，不需要重新发布[!DNL Tags]库，但如果添加了新字段，则必须重新映射[!DNL Tags]中的XDM数据元素。

+++

+++ 架构中缺少必需的Adobe Advertising字段。

确保`_experience.adcloud.conversionDetails`下的架构中存在必需的Adobe Advertising字段。

| 字段路径 | 类型 | 描述 |
| ----- | --- | --- |
| `_experience.adcloud.conversionDetails.trackingCode` | 字符串 | 将转化映射到原始广告点击。 从登陆页面URL上的`s_kwcid`查询参数填充。 |
| `_experience.adcloud.conversionDetails.trackingIdentity` | 字符串 | 存储跟踪的显示到达或点进转化事件的唯一标识和其他详细信息。 从登陆页面URL上的`ef_id`查询参数填充。 |

如果缺少任一字段，请确认已将&#x200B;**Adobe Advertising Cloud ExperienceEvent完整扩展**&#x200B;字段组保存到架构，然后刷新架构编辑器。

+++

+++ 登陆页面URL不包括所需的查询参数。

确保登陆页面URL包含必要的查询参数。 在广告点进中，登陆页面URL必须包含两个查询参数，例如`https://www.example.com/landing-page?s_kwcid=AL!12345!3!abc123&ef_id=abc123xyz:G:s`

| 缺少参数 | 可能的原因 |
| ----- | --- |
| `s_kwcid` | 未在Adobe Advertising Search或DSP Campaign设置中启用自动标记。 |
| `ef_id` | 登陆页面URL未使用Adobe Advertising跟踪的重定向，或未在Campaign设置中启用EF ID附加。 |

+++

+++ XDM有效负载中的某些参数缺失或为空。

要验证出站XDM有效负载，请打开[!DNL Adobe Experience Platform]调试器或浏览器[!UICONTROL Network]选项卡，筛选`edge.adobedc.net`，并检查interact请求正文。 有效的点进有效负载类似于以下内容：

```json
{
  "events": [{
    "xdm": {
      "eventType": "advertising.clicks",
      "_experience": {
        "adcloud": {
          "conversionDetails": {
            "trackingCode": "AL!12345!3!abc123",
            "trackingIdentity": "abc123xyz:G:s"
          }
        }
      }
    }
  }]
}
```

如果`trackingCode`或`trackingIdentity`为空或缺失：

* 触发规则时，查询参数在页面上不存在。 检查URL和规则的事件计时。
* 架构中缺少字段组。 重新访问上述架构步骤。

+++

## [!UICONTROL Advertising]扩展设置问题 {#advertising-extension-setup-issues}

### 问题：

* 不会为网页记录显示到达或点进转化。

  验证是否记录了转化：

  1. 打开URL后面附加了`ef_id=test&s_kwcid=test`的网页。
  1. 打开浏览器的代码检查工具（通常称为[!DNL Inspect]），打开[!DNL Network]选项卡，然后从Adobe Experience Platform中查找event_type=&quot;advertising.enrichment_ct&quot;的交互调用。
  1. 在数据收集界面中，[打开要收集的网站数据的架构定义](https://experienceleague.adobe.com/en/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas)，并确认`xdm->_experience->adcloud->conversionDetails->trackingCode`和`trackingIdentities`包含`ef_id`和`s_kwcid`。

* 点进的体验数据模型(XDM)有效负载中缺少`_experience.adcloud`。

* 转化在调试器工具中确认，但不显示在Adobe Advertising报表中

### 可能的原因和验证/解决方案

+++ 未为数据流启用`Adobe Advertising`服务

1. 在[!DNL Tags]中，打开标记属性的[数据流配置设置](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams)。
1. 启用以下服务，并保存设置：
   * Adobe Advertising（用于转化/受众同步）
   * Adobe Experience Platform（用于配置文件摄取）

+++

+++ 没有为[!UICONTROL WebSDK]扩展启用`Adobe Advertising`组件

默认情况下，WebSDK扩展中的`Adobe Advertising`组件处于禁用状态，并且无论XDM架构或规则配置方式如何，都必须在Adobe Advertising点进或查看点进的任何跟踪运行之前显式启用该组件。

1. 在[!DNL Tags]中，在Adobe Experience Platform Web SDK配置设置[&#128279;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/custom-build-components)中打开该属性的生成选项。
1. 启用&#x200B;**Advertising**&#x200B;组件并保存设置。
1. 重建并重新发布库。

+++

+++ 仅记录点进转化；从不显示点进转化

这是正常默认行为。 启用`Adobe Advertising`组件后，点进跟踪将使用`s_kwcid`和`ef_id` URL查询参数自动处于活动状态。 默认情况下，浏览跟踪处于禁用状态，需要额外的配置 — 请参阅下一项。

+++

+++ 未启用或配置显示到达跟踪

1. 为数据流启用Adobe Advertising服务：
   1. 转到Adobe Experience Platform中的[!UICONTROL Data Collection] > [!UICONTROL Datastreams]，然后打开[!DNL Tags]属性使用的数据流。
   1. 选择&#x200B;**添加服务**，选择&#x200B;**Adobe Advertising**&#x200B;和&#x200B;**Adobe Experience Platform**，然后选择&#x200B;**保存**。
1. 在Adobe Advertising DSP中配置广告商：
   1. 在[!DNL Tags]中，转到[!UICONTROL Extensions] > [!UICONTROL Installed] > **Adobe Experience Platform Web SDK** > [!UICONTROL Configure]。
   1. 在[!UICONTROL Advertiser]部分下，从下拉列表中选择一个广告商并启用它。 要配置多个广告商，请选择&#x200B;**添加广告商**。
1. 验证是否触发显示到达转化像素：
   1. 在[!DNL Adobe Experience Platform]调试器中，确认interact调用在`xdm.query`字段下包含`stitchId`。
   1. 在浏览器[!UICONTROL Network]选项卡上确认已触发类型为`advertising.enrichment`的事件，且该事件包含`xdm.query`下的`stitchId`。

无论访问次数如何，显示到达转化仅每30分钟触发一次。 如果您没有看到interact调用，请清除浏览器缓存并重试。

+++

+++ （如果在显示到达交互调用触发后，Experience Platform中没有显示到达事件）则手动键入广告商，而不是从下拉列表中进行选择

从[!UICONTROL Advertiser]下拉列表中重新选择广告商，而不是手动输入。

+++

+++ （如果在触发显示到达交互调用后Experience Platform中没有显示到达事件）将不会随显示到达交互调用发送任何广告商ID

确认在WebSDK扩展配置的[!UICONTROL Advertiser]部分下配置和启用了广告商，然后重建并重新发布库。

+++

在为[!UICONTROL Advertising]扩展设置问题打开支持票证之前，请验证以下内容：

* **Adobe Advertising**&#x200B;和&#x200B;**Adobe Experience Platform**&#x200B;服务已添加到数据流。
* 已在WebSDK扩展配置中启用&#x200B;**Adobe Advertising**&#x200B;组件。
* 在启用该组件后，重新生成并重新发布库。
* 对于点进跟踪，登陆页面URL在广告点击时包含`s_kwcid`和`ef_id`。
* 对于显示到达跟踪，在Adobe Advertising DSP中使用正确的广告商ID配置广告商。
* WebSDK扩展的版本为2.36.0或更高版本。

## 报告问题

### 摘要报告

#### 问题和核查/解决

+++ Customer Journey Analytics中没有可用于Advertising DSP或Advertising Search、Social和Commerce的摘要报表数据。

验证以下内容：

* Customer Journey Analytics Workspace引用了正确的数据视图。

* 从Adobe Advertising到Customer Journey Analytics的信息源已启用。 请与您的Adobe客户团队核实。

* 您的Adobe Advertising维度/分类/查找数据集和摘要数据集包含在您的Customer Journey Analytics连接中。

* 您的Adobe Advertising维度和摘要量度包含在您的Customer Journey Analytics数据视图中。

如果您已验证上述所有设置，但仍看不到摘要数据，请在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)为您的组织打开支持工单。

+++

+++ 摘要报表数据在Customer Journey Analytics中可用于广告商1，但不能用于广告商2。

验证以下内容：

* 已为广告商2启用从Adobe Advertising到Customer Journey Analytics的馈送。 请与您的Adobe客户团队核实。

* 已在Customer Journey Analytics连接中为三个数据集（维度/分类/查找、摘要和事件量度）启用设置“[!UICONTROL Backfill all existing data]”。

如果您验证了上述所有条件，但仍看不到摘要数据，请在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)为您的组织打开支持工单。

+++

+++ （搜索、社交和Commerce用户）汇总报表数据在Customer Journey Analytics中可用于一个[!DNL Google Ads]、[!DNL Meta Ads]或[!DNL Microsoft Advertising]帐户，但不能用于另一个帐户。

验证是否已为特定的广告网络帐户启用从Adobe Advertising到Customer Journey Analytics的馈送。 请与您的Adobe客户团队核实。

如果为某个帐户启用了信息源，但仍看不到摘要数据，请在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)为您的组织打开支持工单。 包含广告网络帐户的[!UICONTROL Account ID]。

+++

+++ Customer Journey Analytics Workspace中的摘要报表数据与Advertising DSP或Advertising Search、Social和Commerce中的数据不同，或者某些营销活动和营销活动实体的摘要数据缺失。

验证以下内容：

* 您在[!DNL Workspace]和Adobe Advertising报表中使用相同的日期范围。

* 在[!DNL Workspace]和Adobe Advertising报表中应用的任何过滤器和区段都不会导致数据差异。

* Customer Journey Analytics数据视图的[!UICONTROL Time Zone]与您的Advertising DSP帐户[&#128279;](/help/dsp/admin/user-own-profile-edit.md)的[!UICONTROL Default Timezone]匹配。

* 已在Customer Journey Analytics连接中为三个数据集（维度/分类/查找、摘要和事件量度）启用设置“[!UICONTROL Backfill all existing data]”。

如果确定数据不一致，请在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)为您的组织打开支持工单。 包含广告网络帐户的[!UICONTROL Account ID]。 要显示差异的证据，请包含屏幕截图和电子表格。 如果需要，您的Adobe客户团队可以追溯修复数据馈送以解决差异。

+++

### 事件级报告

#### 问题和核查/解决

+++ 在CJA Customer Journey Analytics Workspace中，转化数据（如`Page Views`）不可用于报表维度（如`Campaign`）。

从验证障碍最少的物品开始，验证以下内容：

* 您使用了正确的数据视图。

* 适用的转化量度是Web/在线事件，Adobe Advertising可将这些事件归因于维度。

* Adobe Advertising正在跟踪适用网站上的点进和显示点进。<!-- Link to validation instructions in the user guide -->

* 在分类数据集的Customer Journey Analytics连接中，[!DNL Key]和[!DNL Matching Key]设置的值正确： [!DNL Key]： `Tracking Code` (_customername.adLens2.trackingCode)，[!DNL Matching Key]： `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)

* [!DNL Adobe Advertising]服务已添加到Adobe Experience Platform数据流，数据流的映射架构为`XDM ExperienceEvent Schema`，字段组`Adobe Advertising Cloud ExperienceEvent Full Extension`已添加到`XDM ExperienceEvent`架构中。

* 已在WebSDK扩展中正确配置并发布Adobe Advertising设置。

如果您已验证上述所有设置，但仍看不到转化数据，请在[https://experienceleague.adobe.com/home#support](https://experienceleague.adobe.com/home?support-tab=home#support)为您的组织打开支持工单。 包含广告网络帐户的[!UICONTROL Account ID]。

+++

<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

## 验证和调试工具

### Adobe Experience Platform Debugger

为[!DNL Chrome]安装[!DNL Adobe Experience Platform Debugger]扩展。 它提供：

* 所有WebSDK `alloy()`调用的实时视图
* 数据流ID和环境验证
* XDM有效负载检测
* Edge Network请求和响应详细信息

调试器中的键检查：

| 选项卡 | 检查内容 |
| ----- | --- |
| [!UICONTROL Summary] | 确认检测到WebSDK并显示已安装的版本。 |
| [!UICONTROL Adobe Experience Platform WebSDK] | 显示触发的每个事件、完整XDM有效负载和边缘响应。 |
| [!UICONTROL Adobe Advertising] | 确认与`advertising.enrichment`事件类型之间的AMO ID捕获和XDM interact调用。 |

### “浏览器网络”选项卡

按`edge.adobedc.net`筛选以检查原始边缘请求：

* 请求URL： `https://[org-id].data.adobedc.net/ee/v2/interact`
* 方法： `POST`
* 状态： `200` （正常）、`400` （负载错误）或`500` （服务器或数据流错误）

检查请求有效负载：

* 正确的`dataStreamId`
* 存在具有预期字段的`xdm`对象
* 已填充ECID的`identityMap`

### 控制台验证

检查已安装的WebSDK版本：

```js
window.alloy.version
```

手动触发测试事件：

```js
alloy("sendEvent", {
  xdm: {
    eventType: "web.webpagedetails.pageViews",
    web: {
      webPageDetails: { name: "Test Page", URL: window.location.href }
    }
  }
}).then(result => console.log("Edge response:", result))
  .catch(err => console.error("Send event error:", err));
```

## 快速参考清单

在打开支持票证之前，请验证以下各项：

* WebSDK扩展使用的是最新版本。
* 库已发布，并且嵌入代码适用于正确的环境。
* 正确设置了用于开发、暂存和生产的数据流ID。
* 已启用所有必需的数据流服务。
* 已在WebSDK扩展配置中启用[!UICONTROL Advertising]组件，并配置了DSP广告商ID。
* XDM架构包含[!UICONTROL Advertising]字段组。
* [!UICONTROL Send Event]规则包括一个标识映射，并在正确的事件中触发。
* 没有CSP或浏览器隐私设置阻止边缘请求。
* [!DNL Adobe Experience Platform]调试器确认事件已到达边缘。
* 浏览器控制台中没有停止执行的JavaScript错误。
* **Adobe Advertising Cloud ExperienceEvent完整扩展**&#x200B;字段组已添加到架构中。
* 架构中存在`_experience.adcloud.conversionDetails.trackingCode`。
* 架构中存在`_experience.adcloud.conversionDetails.trackingIdentity`。
* 登陆页面URL同时包含`s_kwcid`和`ef_id`点进。
* [!DNL Adobe Experience Platform]调试器会确认已在出站有效负载中填充`conversionDetails`。

## 何时升级

在以下情况下，请上报您的Adobe客户团队或工程团队：

* Edge请求在数据流验证后返回永久性`500`错误。
* 已在调试器中确认[!UICONTROL Advertising]转化，但在24-48小时后不会显示在报表中。
* WebSDK版本更新引入的回归在以前的版本中不存在。 在支持服务单中包含特定的版本号。

>[!MORELIKETHIS]
>
>* [概述](overview.md)
>*  [!DNL Customer Journey Analytics][&#128279;](ids.md)使用的Adobe Advertising ID
>* [先决条件](prerequisites.md)
>* [设置数据收集、数据传输和报告](set-up.md)
>* Customer Journey Analytics中的[Adobe Advertising指标和维度](advertising-data-in-cja.md)
>* （Adobe Analytics用户） [收集AMO ID和EF ID的历史数据以用于Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)。
