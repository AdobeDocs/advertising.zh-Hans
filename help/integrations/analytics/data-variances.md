---
title: 之间的预期数据差异 [!DNL Analytics] 和Adobe Advertising
description: 之间的预期数据差异 [!DNL Analytics] 和Adobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '3212'
ht-degree: 0%

---

# 之间的预期数据差异 [!DNL Analytics] 和Adobe Advertising

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

使用的广告商 [!DNL Analytics for Advertising] <!-- (A4AdC) --> 集成可通过Adobe Advertising和Adobe Analytics跟踪付费广告。 当您通过多个系统跟踪媒体、营销活动和渠道时，来自不同系统的相同数据集很少完全匹配。 本文档说明应如何期望通过Adobe Advertising贩运的介质的数据与跟踪该介质的各系统中的数据进行比较 [!DNL Analytics].

>[!NOTE]
>
>本文档重点介绍Adobe Advertising和分析，但许多要点也可以转移到其他跟踪解决方案中。

## 类似报表中的归因差异

### 回顾窗口和归因模型可能有所不同

此 [!DNL Analytics for Advertising] 集成使用两个变量([!DNL eVars] 或 [!DNL rVars] \[保留 [!DNL eVars]]\)捕获 [EF ID和AMO ID](ids.md). 这些变量配置有单个回顾窗口（点进次数和显示次数的归因时间）和归因模型。 除非另有指定，否则变量将配置为与Adobe Advertising中的默认广告商级别点击回顾窗口和归因模型匹配。

但是，回顾窗口和归因模型可以在Analytics中进行配置(通过 [!DNL eVars])和Adobe Advertising中。 此外，在Adobe Advertising中，归因模型不仅可在广告商级别（用于竞价优化）进行配置，还可在单个数据视图和报告中进行配置（仅用于报告目的）。 例如，组织可能希望使用偶数分布归因模型进行优化，但对Advertising DSP中的报表使用最后接触归因，或者 [!DNL Advertising Search, Social, & Commerce]. 更改归因模型会更改归因转化的数量。

如果在一个产品中修改了报表回顾窗口或归因模型，而在另一个产品中修改了报表回顾窗口或归因模型，则来自每个系统的相同报表将显示不同的数据：

* **不同回顾窗口导致的差异示例：**

  假设Adobe Advertising具有60天的点击回顾窗口并且 [!DNL Analytics] 具有30天的回溯时段。 假设一位用户通过Adobe Advertising跟踪的广告进入网站，离开，然后在第45天返回网站并转化。 由于转化发生在60天的回看时段内，因此Adobe Advertising会将转化归因于初始访问。 [!DNL Analytics]但是，无法将转化归因于初始访问，因为转化发生在30天的回顾窗口过期之后。 在此示例中，Adobe Advertising报告的转化次数将高于 [!DNL Analytics] 会。

  ![在Adobe Advertising中归因但未归因的转化示例 [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **不同归因模型导致的差异示例：**

  假设用户在转化之前与三个不同的Adobe Advertising广告进行交互，并将收入作为转化类型。 如果Adobe Advertising报表使用均匀分布模型来归因，则它会将收入平均归因于所有广告。 如果 [!DNL Analytics] 使用最后接触归因模型，但随后会将收入归因于最后一个广告。 在以下示例中，Adobe Advertising将捕获到三个广告中的每一个的30美元收入中的平均10美元归因于三个广告，而 [!DNL Analytics] 将所有30美元的收入归因于用户看到的最后一个广告。 比较来自Adobe Advertising的报告和 [!DNL Analytics]，您将会看到归因不同的影响。

  ![归属于Adobe Advertising及合营业务的 [!DNL Analytics] 基于不同的归因模型](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>最佳实践是在Adobe Advertising和中使用相同的回顾窗口和归因模型 [!DNL Analytics]. 根据需要与您的Adobe客户团队合作，确定当前设置并保持配置同步。

这些相同的概念适用于使用不同回顾窗口或归因模型的任何其他类似渠道。

#### 浏览转化跟踪的不同回顾时间范围 {#impression-lookback}

在Adobe Advertising中，归因基于点击次数和展示次数，您可以为点击次数和展示次数配置不同的回顾时间范围。 在 [!DNL Analytics]但是，归因基于点进和显示点进，并且您无权选择为点进和显示点进设置不同的归因窗口；每次跟踪从首次网站访问开始。 展示可能在显示到达的同一天或多个天发生，这可能会影响每个系统中归因窗口的开始位置。

通常，大多数显示到达转化发生的速度足够快，以至于两个系统都将其归为点数。 但是，某些转化可能会发生在Adobe Advertising展示回顾窗口之外，但也可能发生在 [!DNL Analytics] 回顾窗口；此类转化归因于 [!DNL Analytics] 但不是为了给Adobe Advertising留下印象。

在以下示例中，假设访客在第1天收到广告，在第2天执行了浏览访问（即，访问了广告的登陆页面，而之前未单击该广告），并在第45天进行了转化。 在这种情况下，Adobe Advertising将从第1天到第14天跟踪用户（使用14天回溯）， [!DNL Analytics] 将跟踪第2天至第61天内的用户（使用60天回溯），第45天的转化将归因于 [!DNL Analytics] 但不会在Adobe Advertising内。

![在中归因的浏览转化示例 [!DNL Analytics] 但不包括Adobe Advertising](/help/integrations/assets/a4adc-viewthrough-example.png)

导致差异的另一个原因是，在Adobe Advertising中，您可以为显示到达转化分配自定义 *显示到达权重* 与归属于基于点击的转化的权重相关的值。 默认显示到达权重为40%，这意味着显示到达转化会计为基于点击的转化值的40%。 [!DNL Analytics] 没有提供此类显示到达转化权重。 例如，在中捕获到一个100美元的收入订单 [!DNL Analytics] 如果您使用默认显示到达权重，则Adobe Advertising折价为40美元 — 相差60美元。

在比较Adobe Advertising和之间的显示到达转化时，请考虑以下差异 [!DNL Analytics] 报表。

#### 可用的归因模型

| Adobe Advertising归因 | [!DNL Analytics] 归因 | [!DNL eVar]/[!DNL rVar] 分配 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | 不适用 | 不适用 |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>请勿使用* |
| [!UICONTROL Weight Last Event More] | 不适用 | 不适用 |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | 不适用 |
| 不适用 | [!UICONTROL J-Shaped] | 不适用 |
| 不适用 | [!UICONTROL Inverse-J] | 不适用 |
| 不适用 | [!UICONTROL Custom] | 不适用 |
| 不适用 | [!UICONTROL Participation] | 不适用 |
| 不适用 | [!UICONTROL Algorithmic] | 不适用 |

>[!NOTE]
>
>对于线性分配， [!DNL Analytics] 对所有受众平均分配成功事件 [!DNL eVar] 单次访问中的值，因此请使用线性分配和 [!DNL eVar] “访问”过期。 但是，对于广告，使用线性归因会导致分配不是真正的线性分配，并会导致报表不理想。 例如，如果访客在转化之前与三个广告进行交互，则在三次单独访问中，只有上次访问中看到的广告被归因于转化，而非全部三个广告。
>
>此外，将转化分配切换到“线性”或从其中切换可防止显示历史数据，这可能导致报表中的数据误报。 例如，线性分配可能会将收入划分为多个不同的 [!DNL eVar] 值。 如果将分配更改为“最近”，则该收入的100%将与最近的单个值相关联。 这种关联可能会导致错误的结论。
>
>为了避免混淆， [!DNL Analytics] 使历史数据在报表界面中不可用。 如果您更改了 [!DNL eVar] 返回到初始分配设置，但不应更改 [!DNL eVar] 分配设置仅用于访问历史数据。 Adobe建议使用新的 [!DNL eVar] 适用于已经记录的数据的新分配设置，而不是更改 [!DNL eVar] 已拥有大量历史数据的客户。

查看列表 [!DNL Analytics] 归因模型及其定义，位于 [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

如果您已登录 [!DNL Search, Social, & Commerce]，您可以找到列表

* （北美用户） [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* （所有其他用户） [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Adobe Advertising中的事件日期归因

在Adobe Advertising中，您可以按关联的点击日期/事件日期（点击或展示事件的日期）或交易日期（转化日期）报告转化数据。 中不存在点击/事件日期报表的概念 [!DNL Analytics]；中跟踪的所有转化 [!DNL Analytics] 按交易日期报告。 因此，同一转化可能会以不同的Adobe Advertising和日期报告 [!DNL Analytics]. 例如，假设一位用户在1月1日点击广告并在1月5日转化。 如果您查看的是Adobe Advertising中按事件日期列出的转化数据，则转化报告日期为点击发生的1月1日。 在 [!DNL Analytics]，相同的转化报告于1月5日。

![归因于不同日期的转化示例](/help/integrations/assets/a4adc-conversions-based-on.png)

## 归因 [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] 报告](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) 允许您配置规则，以根据点击信息的不同方面标识不同的营销渠道。 您可以跟踪Adobe Advertising跟踪渠道([!UICONTROL Display Click Through]， [!UICONTROL Display View Through]、和 [!UICONTROL Paid Search])作为 [!DNL Marketing Channels] 通过使用 `ef_id` 用于标识渠道的查询字符串参数。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> 然而，即使 [!DNL Marketing Channels] 报表可以跟踪Adobe Advertising渠道，由于多种原因，数据可能与Adobe Advertising报表不匹配。 有关更多信息，请参阅以下部分。

>[!NOTE]
>
> 以下核心概念也适用于任何涉及Adobe Advertising中未跟踪的营销活动的多渠道跟踪，例如 [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) 变量(也称为“跟踪代码”维度或&quot;[!DNL eVar] 0&quot;)和自定义 [!DNL eVar] 跟踪。

### 中的可能不同的归因模型 [!DNL Marketing Channels]

最多 [!DNL Marketing Channels] 报告配置有 [!UICONTROL Last Touch] 归因，对于该归因，上次检测到的营销渠道将被分配100%的转化值。 将不同的归因模型用于 [!DNL Marketing Channels] 报表和Adobe Advertising报表将导致归因转化中出现差异。

### 中可能不同的回顾时间范围 [!DNL Marketing Channels]

的回顾窗口 [!DNL Marketing Channels] 可进行自定义。 在Adobe Advertising中，点击回顾窗口是可配置的，但通常为60天的固定窗口。 如果这两种产品使用不同的回顾时间范围，则可能会出现数据差异。

### 中的其他渠道归因 [!DNL Marketing Channels]

Adobe Advertising报表仅捕获通过Adobe Advertising贩运的付费媒体（付费搜索） [!DNL Advertising Search, Social, & Commerce] 广告，和显示(对于Advertising DSP广告)， [!DNL Marketing Channels] 报表可以跟踪所有数字渠道。 这可能会导致归因转化的渠道不一致。

例如，付费搜索和免费搜索渠道通常具有共生关系，每个渠道相互协助。 此 [!DNL Marketing Channels] 报表将某些转化归因为Adobe Advertising没有跟踪免费搜索而没有的免费搜索。

再考虑查看展示广告、单击付费搜索广告、单击电子邮件内容，然后下达30美元订单的客户。 即使Adobe Advertising和 [!DNL Marketing Channels] 这两种模型都使用最后接触归因模型，因此转化仍会以不同的方式归因于每种。 Adobe Advertising无权访问 [!UICONTROL Email] 渠道，因此它将计入针对转化的付费搜索。 [!DNL Marketing Channels]但是，可以访问所有三个渠道，因此会获得点数 [!UICONTROL Email] 进行转换。

![Adobe Advertising与中的不同转化归因示例 [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

有关量度可能不同的原因的更多解释，请参阅&quot;[为什么渠道数据可能因Adobe Advertising和渠道而异 [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)“

## Adobe Analytics中的数据差异 [!DNL Paid Search Detection]

此 [legacy [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) 中的功能 [!DNL Analytics] 允许公司 [定义用于跟踪付费和免费搜索流量的规则](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) 指定搜索引擎的日志。 此 [!DNL Paid Search Detection] 规则同时使用查询字符串和反向链接域来标识付费和免费搜索流量。 此 [!DNL Paid Search Detection] 报告属于更大的组 [查找方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) 报表，当发生指定事件（例如购物车结账）或访问结束时过期。

下面是创建 [!DNL Paid Search Detection] 规则集：

![中设置的付费搜索检测规则示例 [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

结果 [!DNL Paid Search Detection] 报告包括 [!UICONTROL Paid Search Engine]， [!UICONTROL Paid Search Keywords]， [!UICONTROL Natural Search Engine]、和 [!UICONTROL Natural Search Keywords] 报表。

请注意以下两种数据限制 [!DNL Paid Search Detection] 报告：

* 此 [!UICONTROL Paid Search Keywords] 和 [!UICONTROL Natural Search Keywords] 报表显示由反向链接URL标识的搜索查询，而不是用户竞价的关键字。 Adobe Advertising和 [!DNL Analytics] 报表显示实际的关键字，因此不要期望它们与 [!DNL Paid Search Detection] 关键词报告。

* 当 [!DNL Paid Search Detection] 该功能最初创建，因此广告商更容易通过引荐URL获得原始搜索查询（用户输入到搜索引擎的搜索栏中的字符串）。 如今，搜索引擎在很大程度上模糊了搜索查询，并且 [!DNL Paid Search Detection] 关键字报表的值有限，因为大多数查询数据属于“未指定”范围。

  替换为 [!DNL Analytics for Advertising]，广告商仍然可以在以下位置跟踪付费关键字： [!DNL Analytics]. 反向链接域将通知引擎报告哪个搜索引擎驱动了流量。 由于特定于广告商的帐户信息未绑定到反向链接域，因此所有流量都会列在搜索引擎下。 在同一搜索引擎中有多个帐户的广告商应该参考Adobe Advertising或 [!DNL Analytics] 帐户特定报表的报表。

### 为何配置 [!DNL Paid Search Detection]？

此 [!DNL Paid Search Detection] 通过报表，您可以识别 [[!DNL Analytics Marketing Channels] 报表](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). 将付费搜索流量与免费搜索流量区分开来是了解免费搜索为整个营销生态系统带来价值的一个极好的方法。

## 的点进数据验证 [!DNL Analytics for Advertising] {#data-validation}

对于集成，您应该验证点进数据，以确保网站上的所有页面都正确跟踪点进。

在 [!DNL Analytics]，验证最简单的方法之一 [!DNL Analytics for Advertising] 跟踪是指使用“点击次数”将点击次数与实例数进行比较 [!UICONTROL AMO ID Instances]&quot;计算指标，其计算方式如下：

```
Clicks to [!UICONTROL AMO ID Instances] = ([!UICONTROL AMO ID Instances] / Adobe Advertising Clicks)
```

[!UICONTROL AMO ID Instances] 表示达到此值的次数： [AMO ID](ids.md) 会在网站上跟踪。 每次点击广告时，一个AMO ID (`s_kwcid`)参数会被添加到登陆页面URL。 的数量 [!UICONTROL AMO ID Instances]因此，类似于点击次数，可根据实际广告点击进行验证。 我们通常看到80%的匹配率 [!DNL Search, Social, & Commerce] 30%的匹配率 [!DNL DSP] 流量（在筛选为仅包含点进时） [!UICONTROL AMO ID Instances])。 搜索和显示之间的预期差异可以用预期流量行为来解释。 搜索会捕捉意图，因此，用户通常打算单击其查询中的搜索结果。 但是，查看显示或在线视频广告的用户更有可能无意中单击该广告，然后要么从网站弹回，要么放弃在跟踪页面活动之前加载的新窗口。

在Adobe Advertising报表中，您可以使用&quot;[!UICONTROL ef_id_instances]”量度而不是 [!UICONTROL AMO ID Instances]：

```
Clicks to [EF ID Instances = (ef_id_instances / Clicks)
```

虽然您可以预期AMO ID与EF ID之间的匹配率很高，但请不要预期100%的奇偶校验，因为AMO ID和EF ID从根本上跟踪不同的数据，这种差异可能会导致总数略有差异 [!UICONTROL AMO ID Instances] 和 [!UICONTROL EF ID Instances]. 如果总计 [!UICONTROL AMO ID Instances] 在 [!DNL Analytics] 不同于 [!UICONTROL EF ID Instances] 但是，如果Adobe Advertising超过1%，请联系您的Adobe客户团队寻求帮助。

有关AMO ID和EF ID的更多信息，请参阅 [Analytics使用的Adobe AdvertisingID](ids.md).

以下是跟踪实例点击的工作区示例。

![用于跟踪实例点击的工作区示例](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## 比较中的数据集 [!DNL Analytics for Advertising] 与Adobe Advertising中的比较

此 [AMO ID](ids.md) （s_kwcid查询字符串参数）用于报表 [!DNL Analytics]，和 [EF ID](ids.md) 用于Adobe Advertising中的报表。 由于它们是不同的值，因此一个值可能会被损坏或未添加到登陆页面。

例如，假设我们有以下登陆页面：

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

其中EF ID为&quot;`test_ef_id`”且AMO ID为“`test_amo_id`“

如果发生站点端重定向，则URL可能最终如下所示：

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

其中EF ID为&quot;`test_ef_id`”且AMO ID为“`test_amo_id#redirectAnchorTag`“

在此示例中，添加锚标记会向AMO ID添加意外字符，从而导致Analytics无法识别的值。 此AMO ID将不会进行分类，并且与其关联的转化将归入”[!UICONTROL unspecified]”或“[!UICONTROL none]中的&quot; [!DNL Analytics] 报表。

幸运的是，尽管这类问题很常见，但通常不会造成很大的差异。 但是，如果您发现中的AMO ID之间存在很大差异， [!DNL Analytics] 和EF IDAdobe Advertising时，请联系您的Adobe客户团队寻求帮助。

## 其他量度注意事项

### 点击量和访问量之间的区别 {#clicks-vs-visits}

它们看起来类似，但点击量和访问量代表不同的数据：

* **单击：** [!DNL DSP] 或者，当访客点击发布者网站上的广告时，搜索引擎会记录一次点击。

* **访问：** [!DNL Analytics] 定义 [访问](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) 作为用户进行的一系列页面查看，并根据多个条件之一结束，例如30分钟处于不活动状态。

顾名思义，单击可导致多次访问。

请考虑以下示例：用户1和用户2均可通过单击Adobe Advertising广告来访问站点。 用户1查看了4个页面，然后离开去一天，因此初始点击导致一次访问。 用户2查看两个页面，离开时享受45分钟的午餐，回访，再查看两个页面，然后离开；在这种情况下，最初的点击导致两次访问。

![点击量和访问量之间差异的示例](/help/integrations/assets/a4adc-visits-example.png)

### 点击次数和点进次数的区别

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

点击量和点进次数是两个不同的量度：

* **单击：** [!DNL DSP] 或者，当访客点击发布者网站上的广告时，搜索引擎会记录一次点击。

* **点进次数：** [!DNL Analytics] 记录访客登陆目标网站、登陆页面加载以及 [!DNL Analytics] 位于页面底部的请求会将数据发送至 [!DNL Analytics].

由于意外广告点击，点击和点进次数可能会有很大差异。 我们已经发现，展示广告上的大多数点击是意外点击，这些意外访客在加载登陆页面之前点击了“返回”按钮，因此 [!DNL Analytics] 无法录制点进。 这尤其适用于更有可能意外点击的广告，例如移动广告、视频广告和填充屏幕的广告，并且必须在用户查看页面之前将其关闭。

由于带宽或可用处理能力较低，因此加载到移动设备上的网站也不太可能导致点进，从而导致加载登陆页面所需的时间较长。 50-70%的点击不会导致点进的情况并不少见。 在移动环境中，差异可能高达90%，这是因为浏览器速度较慢，并且用户在滚动页面或尝试关闭广告时意外单击广告的可能性较高。

点击数据还可能会记录到以下环境中：无法使用当前跟踪机制记录点进次数（例如进入或离开移动设备应用程序的点击），或者广告商只为其部署了一种跟踪方法（例如，使用浏览式JavaScript方法，阻止第三方Cookie的浏览器将跟踪点击，而不是点进）。 Adobe建议同时部署点击URL跟踪和显示到达的JavaScript跟踪方法的一个关键原因是，尽可能扩大可跟踪点进的覆盖范围。

### 对非Adobe AdvertisingDimension使用Adobe Advertising流量指标

Adobe Advertising为Analytics提供了 [广告特定的流量量度和以下来源的相关维度： [!DNL DSP] 和 [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). Adobe Advertising提供的指标仅适用于指定的Adobe Advertising维度，并且对于中的其他维度没有数据可用 [!DNL Analytics].

例如，如果您查看 [!UICONTROL Adobe Advertising Clicks] 和 [!UICONTROL Adobe Advertising Cost] 按帐户划分的指标，这是一个Adobe Advertising维度，您将会看到总计 [!UICONTROL Adobe Advertising Clicks] 和 [!UICONTROL Adobe Advertising Cost] 按帐户。

![使用Adobe Advertising维度的报表中的Adobe Advertising指标示例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

但是，如果您查看 [!UICONTROL Adobe Advertising Clicks] 和 [!UICONTROL Adobe Advertising Cost] 量度（例如“页面”），如果Adobe Advertising不为其提供数据，则 [!UICONTROL Adobe Advertising Clicks] 和 [!UICONTROL Adobe Advertising Cost] 对于每一页，则是零(0)。

![使用不受支持的维度的报表中的Adobe Advertising指标示例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### 使用 [!UICONTROL AMO ID Instances] 代替非Adobe AdvertisingDimension的点击

因为你不能 [!UICONTROL AMO Clicks] 对于站点维度，您可能希望找到等同于点击的维度。 您可能倾向于使用访问次数作为替代，但这并不是最佳选择，因为每个访客可能具有多次访问。 (请参阅&quot;[点击量和访问量之间的区别](#clicks-vs-visits)“ 为此，我们建议使用 [!UICONTROL AMO ID Instances]，即捕获AMO ID的次数。 同时 [!UICONTROL AMO ID Instances] 不匹配 [!UICONTROL AMO Clicks] 准确地说，它们是测量网站点击流量的最佳选项。 有关更多信息，请参阅&quot;[的点进数据验证 [!DNL Analytics for Advertising]](#data-validation)“

![示例 [!UICONTROL AMO ID Instances] 而不是 [!UICONTROL Adobe Advertising Clicks] 对于不支持的维度](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [使用的Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Analysis Workspace中的Adobe Advertising指标](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe Advertising中的数据](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [为什么数据可能因Adobe Advertising和原因而异 [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
