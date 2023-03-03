---
title: 之间的预期数据差异 [!DNL Analytics] 和Adobe广告
description: 之间的预期数据差异 [!DNL Analytics] 和Adobe广告
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '3282'
ht-degree: 0%

---

# 之间的预期数据差异 [!DNL Analytics] 和Adobe广告

*仅具有AdobeAdvertising-Adobe Analytics集成的广告商*

使用的广告商 [!DNL Analytics for Advertising] <!-- (A4AdC) --> 通过Adobe广告和Adobe Analytics集成跟踪付费广告。 当您通过多个系统跟踪媒体、营销活动和渠道时，来自不同系统的相同数据集很少完全匹配。 本文档说明了应如何期望通过Adobe广告贩运的媒体的数据与在其内跟踪媒体的不同系统中的数据进行比较 [!DNL Analytics].

>[!NOTE]
>
>本文档重点介绍Adobe广告和分析，但许多要点也可以转移到其他跟踪解决方案中。

## 类似报表中的归因差异

### 回顾窗口和归因模型可能不同

此 [!DNL Analytics for Advertising] 集成使用两个变量（eVar或rVar \[保留的eVar]\）来捕获 [EF ID和AMO ID](ids.md). 这些变量配置为单个回顾窗口（点进和显示到达的归因时间）和归因模型。 除非另有指定，否则变量将配置为与Adobe广告中的默认广告商级别点击回顾窗口和归因模型匹配。

但是，回顾窗口和归因模型可以在Analytics（通过eVar）和Adobe广告中进行配置。 此外，在Adobe广告中，归因模型不仅可以在广告商级别进行配置（用于竞价优化），还可以在单个数据视图和报告中进行配置（仅用于报告目的）。 例如，组织可能偏好使用偶数分布归因模型进行优化，但对Advertising DSP中的报表使用最后接触归因，或者 [!DNL Advertising Search]. 更改归因模型会更改归因转化的数量。

如果在一个产品中修改了报表回顾窗口或归因模型，而在另一个产品中修改了报表回顾窗口或归因模型，则来自每个系统的相同报表将显示不同的数据：

* **不同回顾时间范围导致的差异示例：**

   假设Adobe广告具有60天的点击回顾窗口，并且 [!DNL Analytics] 有30天的回溯时段。 假设用户通过Adobe广告跟踪的广告进入网站，离开，然后在第45天返回网站并转化。 Adobe广告会将转化归因于初始访问，因为转化发生在60天的回溯时段内。 [!DNL Analytics]但是，无法将转化归因于初始访问，因为转化发生在30天的回溯时段过期之后。 在此示例中，Adobe广告报告的转化次数将高于 [!DNL Analytics] 会。

   ![在Adobe广告中归因但未归因的转化示例 [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **不同归因模型导致的差异示例：**

   假设用户在转化之前与三个不同的Adobe广告进行交互，并将revenue作为转化类型。 如果Adobe广告报表使用偶数分布模型进行归因，则它将平均将收入归因于所有广告。 如果 [!DNL Analytics] 使用最后接触归因模型，但随后会将收入归因于最后一个广告。 在以下示例中，Adobe广告将捕获的30美元收入中的平均10美元归因于三个广告中的每个，而 [!DNL Analytics] 将所有30 USD的收入归因于用户看到的最后一个广告。 当您比较来自Adobe广告和的报表时 [!DNL Analytics]，您将会看到归因差异的影响。

   ![Adobe广告及媒体宣传产生之 [!DNL Analytics] 基于不同的归因模型](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>最佳实践是在Adobe广告和分类中使用相同的回顾窗口和归因模型 [!DNL Analytics]. 根据需要与您的Adobe客户团队合作，确定当前设置并使配置保持同步。

这些相同的概念适用于使用不同回顾窗口或归因模型的任何其他类似渠道。

#### 浏览转化跟踪的不同回顾时间范围 {#impression-lookback}

在Adobe广告中，归因基于点击次数和展示次数，您可以为点击次数和展示次数配置不同的回顾时间范围。 In [!DNL Analytics]但是，归因基于点进和显示到达次数，并且您无权选择为点进和显示到达设置不同的归因窗口；对每次的跟踪都会在首次网站访问时开始。 展示可能在浏览发生的同一天或多天发生，这可能会影响每个系统中归因窗口的开始位置。

通常，大多数显示到达转化发生的速度足够快，以至于两个系统都归于点数。 但是，某些转化可能会发生在Adobe广告展示回顾窗口之外，但在 [!DNL Analytics] 回顾窗口；此类转化归因于 [!DNL Analytics] 但不是为了给Adobe广告留下印象。

在以下示例中，假设某位访客在第1天收到一个广告，在第2天执行了浏览访问（即，访问了广告的登陆页面，而之前未单击该广告），并在第45天进行了转化。 在这种情况下，Adobe广告将从第1天至第14天跟踪用户（使用14天回溯）， [!DNL Analytics] （使用60天回溯）第2天至第61天跟踪用户，第45天的转化将归因于 [!DNL Analytics] 但不适用于Adobe广告。

![在中归因的浏览转化示例 [!DNL Analytics] 但不包括Adobe广告](/help/integrations/assets/a4adc-viewthrough-example.png)

导致差异的另一个原因是，在Adobe广告中，您可以为显示到达转化分配自定义 *显示到达权重* 与归属于基于点击的转换的权重相关。 默认显示到达权重为40%，这意味着显示到达转化会计为基于点击的转化值的40%。 [!DNL Analytics] 不提供此类显示到达转化权重。 例如，在中捕获了一个100美元的收入订单 [!DNL Analytics] 如果您使用默认显示到达权重，则Adobe广告中将打折到40美元，二者的差额为60美元。

在比较Adobe广告和之间的显示到达转化时，请考虑以下差异 [!DNL Analytics] 报告。

#### 可用的归因模型

| Adobe广告归因 | [!DNL Analytics] 归因 | eVar/rVar分配 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | 不适用 | 不适用 |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>不要使用* |
| [!UICONTROL Weight Last Event More] | 不适用 | 不适用 |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | 不适用 |
| 不适用 | [!UICONTROL J-Shaped] | 不适用 |
| 不适用 | [!UICONTROL Inverse-J] | 不适用 |
| 不适用 | [!UICONTROL Custom] | 不适用 |
| 不适用 | [!UICONTROL Participation] | 不适用 |
| 不适用 | [!UICONTROL Algorithmic] | 不适用 |

>[!NOTE]
>
>对于线性分配， [!DNL Analytics] 将成功事件平均分配给单次访问中的所有eVar值，因此使用线性分配并设置“访问”的eVar过期时间。 但是，对于广告，使用线性归因会导致分配不是真正的线性分配，并会导致报表不理想。 例如，如果访客在转化之前与三个广告进行交互，则在三次单独访问中，只有上次访问中看到的广告归因于转化，而不是全部三个广告。
>
>此外，将转化分配切换到“线性”或从“线性”切换到，可防止显示历史数据，这可能导致报表中的数据误报。 例如，线性分配可能会将收入划分为多个不同的eVar值。 如果将分配更改为“最近”，则该收入的100%将与最近的单个值相关联。 此关联可能会导致错误的结论。
>
>为了避免混淆， [!DNL Analytics] 使历史数据在报表界面中不可用。 如果将eVar更改回初始分配设置，则可以查看历史数据，但不应仅为了访问历史数据而更改eVar分配设置。 Adobe建议，当您想要为已记录的数据应用新的分配设置时，使用新eVar，而不是更改已具有大量历史数据的eVar的分配设置。

查看列表 [!DNL Analytics] 归因模型及其定义位于 [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

如果您已登录 [!DNL Search]，您可以找到列表

* （北美用户） [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* （所有其他用户） [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Adobe广告中的事件日期归因

在Adobe广告中，您可以按关联的点击日期/事件日期（点击或展示事件的日期）或交易日期（转化日期）报告转化数据。 点击/事件日期报告的概念在中不存在 [!DNL Analytics]；中跟踪的所有转化 [!DNL Analytics] 按交易日期报告。 因此，在Adobe广告和促销活动中，可能会报告具有不同日期的相同转化 [!DNL Analytics]. 例如，假定用户在1月1日点击了广告并在1月5日转化。 如果您在Adobe广告中查看按事件日期划分的转化数据，则转化将在1月1日发生点击时报告。 In [!DNL Analytics]，相同的转换将在1月5日报告。

![归因到不同日期的转化示例](/help/integrations/assets/a4adc-conversions-based-on.png)

## 归因 [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] 报告](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) 允许您配置规则，以根据点击信息的不同方面标识不同的营销渠道。 您可以跟踪Adobe广告跟踪渠道([!UICONTROL Display Click Through]， [!UICONTROL Display View Through]、和 [!UICONTROL Paid Search])作为 [!DNL Marketing Channels] 通过使用 `ef_id` 用于标识渠道的查询字符串参数。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> 然而，即使 [!DNL Marketing Channels] 报表可以跟踪Adobe广告渠道，由于多种原因，数据可能与Adobe广告报表不匹配。 有关更多信息，请参阅以下部分。

>[!NOTE]
>
> 以下核心概念也适用于任何涉及Adobe广告中未跟踪的促销活动的多渠道跟踪，例如 [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) 变量(也称为“跟踪代码”Dimension或“eVar0”)和自定义eVar跟踪。

### 中的可能不同的归因模型 [!DNL Marketing Channels]

最多 [!DNL Marketing Channels] 报告配置有 [!UICONTROL Last Touch] 归因，对于该归因，上次检测到的营销渠道将被分配100%的转化值。 将不同的归因模型用于 [!DNL Marketing Channels] 报表和Adobe广告报表将导致归因转化中的差异。

### 中可能不同的回顾时间范围 [!DNL Marketing Channels]

的回看窗口 [!DNL Marketing Channels] 可进行自定义。 在Adobe广告中，点击回顾窗口是可配置的，但通常为60天固定窗口。 如果这两种产品使用不同的回顾时间范围，则可能会出现数据差异。

### 中的不同渠道归因 [!DNL Marketing Channels]

Adobe广告报表仅捕获通过Adobe广告(付费搜索 [!DNL Advertising Search] 广告，和显示广告的DSP广告)，而 [!DNL Marketing Channels] 报表可以跟踪所有数字渠道。 这可能会导致归因转化的渠道不一致。

例如，付费搜索和免费搜索渠道通常具有共生关系，其中每个渠道都相互帮助。 此 [!DNL Marketing Channels] 报表会将某些转化归因于Adobe广告不会进行的免费搜索，因为它不跟踪免费搜索。

再考虑查看展示广告、单击付费搜索广告、单击电子邮件内部，然后下达30美元订单的客户。 即使Adobe广告和 [!DNL Marketing Channels] 这两种模型都使用最近联系归因模型，但每种模型的转化仍会采用不同的方式归因。 Adobe广告无权访问 [!UICONTROL Email] 渠道，所以将转化归功于付费搜索。 [!DNL Marketing Channels]但是，可以访问所有三个渠道，因此将计入 [!UICONTROL Email] 进行转换。

![Adobe广告中的不同转化归因示例 [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

有关量度可能不同的原因的更多解释，请参阅&quot;[为什么渠道数据可能因Adobe广告和以下内容而异 [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).”

## Adobe Analytics中的数据差异 [!DNL Paid Search Detection]

此 [legacy [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) 中的功能 [!DNL Analytics] 允许公司 [定义规则以跟踪付费和免费搜索流量](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) 指定搜索引擎的。 此 [!DNL Paid Search Detection] 规则同时使用查询字符串和反向链接域来标识付费和免费搜索流量。 此 [!DNL Paid Search Detection] 报告属于更大的报告组 [查找方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) 报告，当指定的事件（例如购物车结账）发生或访问结束时会过期。

以下是用于创建 [!DNL Paid Search Detection] 规则集：

![中设置的付费搜索检测规则示例 [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

结果 [!DNL Paid Search Detection] 报告包括 [!UICONTROL Paid Search Engine]， [!UICONTROL Paid Search Keywords]， [!UICONTROL Natural Search Engine]、和 [!UICONTROL Natural Search Keywords] 报告。

请注意以下两种数据限制 [!DNL Paid Search Detection] 报告：

* 此 [!UICONTROL Paid Search Keywords] 和 [!UICONTROL Natural Search Keywords] 报表显示由反向链接URL标识的搜索查询，而不是用户竞价的关键字。 Adobe广告和 [!DNL Analytics] 报表显示实际的关键字，因此不要期望它们与 [!DNL Paid Search Detection] 关键词报告。

* 当 [!DNL Paid Search Detection] 该功能最初创建，因此广告商更容易通过引荐URL获得原始搜索查询（用户输入到搜索引擎搜索栏中的字符字符串）。 如今，搜索引擎在很大程度上模糊了搜索查询，并且 [!DNL Paid Search Detection] 关键字报表的值有限，因为大多数查询数据都属于“未指定”范围。

   替换为 [!DNL Analytics for Advertising]，广告商仍然可以在以下位置跟踪付费关键字： [!DNL Analytics]. 反向链接域会通知引擎报告哪个搜索引擎推动了流量。 由于广告商特定的帐户信息未绑定到反向链接域，因此所有流量都列在搜索引擎下。 在同一搜索引擎中有多个帐户的广告商应该指Adobe广告或 [!DNL Analytics] 帐户特定报表的报表。

### 为何配置 [!DNL Paid Search Detection]？

此 [!DNL Paid Search Detection] 利用报告，可识别 [[!DNL Analytics Marketing Channels] 报告](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). 将付费搜索流量与免费搜索流量区分开来是了解免费搜索为整个营销生态系统带来的价值的绝佳方法。

## 的点进数据验证 [!DNL Analytics for Advertising] {#data-validation}

对于集成，您应该验证点进数据，以确保网站上的所有页面都正确跟踪点进。

In [!DNL Analytics]，验证最简单的方法之一 [!DNL Analytics for Advertising] 跟踪是指使用“AMO ID实例的点击次数”计算量度将点击次数与实例数进行比较，该计算量度计算如下：

```
Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)
```

[!UICONTROL AMO ID Instances] 表示AMO ID (`s_kwcid` 参数)进行跟踪。 每次点击广告时， `s_kwcid` 参数将添加到登陆页面URL。 的数量 [!UICONTROL AMO ID Instances]因此，与点击量类似，可根据实际广告点击量进行验证。 我们通常看到80%的匹配率 [!DNL Search] 30%的匹配率 [!DNL DSP] 流量（过滤后仅包括点进） [!UICONTROL AMO ID Instances])。 搜索和显示之间的预期差异可以用预期流量行为来解释。 搜索可捕获意图，因此，用户通常打算单击其查询中的搜索结果。 但是，查看显示广告或在线视频广告的用户更有可能无意中单击该广告，然后或者从网站弹回，或者放弃在跟踪页面活动之前加载的新窗口。

在Adobe广告报表中，您还可以使用&quot;[!UICONTROL ef_id_instances]”量度而不是 [!UICONTROL AMO ID Instances]：

```
Clicks to [EF ID Instances = (ef_id_instances / Clicks)
```

虽然AMO ID和EF ID之间的匹配率应该很高，但请不要期望100%的奇偶校验，因为AMO ID和EF ID从根本上跟踪不同的数据，并且此差异可能会导致总数中的细微差异 [!UICONTROL AMO ID Instances] 和 [!UICONTROL EF ID Instances]. 如果总计 [!UICONTROL AMO ID Instances] 在 [!DNL Analytics] 不同于 [!UICONTROL EF ID Instances] 但是，在Adobe广告中，如果点击率超过1%，请联系您的Adobe客户团队寻求帮助。

有关AMO ID和EF ID的更多信息，请参阅 [Analytics使用的Adobe广告ID](ids.md).

下面是一个用于跟踪实例点击的工作区示例。

![用于跟踪实例点击的工作区示例](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## 比较中的数据集 [!DNL Analytics for Advertising] 与Adobe广告中的比较

此 [AMO ID](ids.md) （s_kwcid查询字符串参数）用于在以下位置报告： [!DNL Analytics]，以及 [EF ID](ids.md) 用于Adobe广告中的报表。 由于它们是不同的值，因此一个值可能已损坏或未添加到登陆页面。

例如，假设我们具有以下登陆页面：

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

其中EF ID为&quot;`test_ef_id`”且AMO ID为“`test_amo_id`.”

如果发生站点端重定向，则URL可能最终如下所示：

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

其中EF ID为&quot;`test_ef_id`”且AMO ID为“`test_amo_id#redirectAnchorTag`.”

在此示例中，添加锚标记会向AMO ID添加意外字符，从而导致Analytics无法识别的值。 此AMO ID不会进行分类，并且与其关联的转化将属于&quot;[!UICONTROL unspecified]“或”[!UICONTROL none]中的“” [!DNL Analytics] 报告。

幸运的是，尽管这类问题很常见，但通常不会造成很大的差异。 但是，如果您发现中的AMO ID之间存在很大差异 [!DNL Analytics] 和EF ID在Adobe广告中，请联系您的Adobe客户团队寻求帮助。

## 其他量度注意事项

### 点击次数和访问次数的区别 {#clicks-vs-visits}

它们看起来有类似之处，但点击次数和访问次数代表不同的数据：

* **单击：** [!DNL DSP] 或者，当访客单击发布者网站上的广告时，搜索引擎会记录一次点击。

* **访问：** [!DNL Analytics] 定义 [访问](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) 作为用户进行的一系列页面查看，并根据多个条件之一结束，例如30分钟处于非活动状态。

根据定义，单击可导致多次访问。

请考虑以下示例：用户1和用户2均可通过单击Adobe广告广告来访问网站。 用户1查看了四个页面，然后在一天内离开，因此初始点击导致一次访问。 用户2查看了两个页面，离开时需要45分钟的午餐，返回，又查看了两个页面，然后离开；在这种情况下，最初的点击导致两次访问。

![点击次数和访问次数之间差异的示例](/help/integrations/assets/a4adc-visits-example.png)

### 点击次数和点进次数的区别

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

点击和点进是两个不同的量度：

* **单击：** [!DNL DSP] 或者，当访客单击发布者网站上的广告时，搜索引擎会记录一次点击。

* **点进次数：** [!DNL Analytics] 记录访客登陆目标网站、登陆页面加载并且 [!DNL Analytics] 位于页面底部的请求会将数据发送至 [!DNL Analytics].

点击和点进次数可能会因意外广告点击而有很大的差异。 我们已经发现，展示广告上的大多数点击都是意外点击，这些意外访客在加载登陆页面之前点击了“返回”按钮，因此 [!DNL Analytics] 无法记录点进。 对于更有可能意外点击的广告（例如移动广告、视频广告和填充屏幕的广告）尤其如此，并且必须在用户查看页面之前将其关闭。

由于带宽或可用处理能力较低，在移动设备上加载的网站也不太可能导致点进，从而导致登陆页面的加载时间较长。 50-70%的点击不会导致点进的情况并不少见。 在移动环境中，差异可能高达90%，这是因为浏览器速度较慢，并且用户在滚动浏览页面或尝试关闭广告时意外点击广告的可能性较高。

点击数据还可能会记录到以下环境中：无法使用当前跟踪机制记录点进次数（例如进入或离开移动应用程序的点击），或者广告商只为其部署了一种跟踪方法（例如，使用显示到达JavaScript方法，阻止第三方Cookie的浏览器将跟踪点击，但不跟踪点进）。 Adobe建议同时部署点击URL跟踪和显示到达JavaScript跟踪方法的一个关键原因是，尽可能扩大可跟踪点进的覆盖范围。

### 对非Adobe广告Dimension使用Adobe广告流量量度

Adobe广告为Analytics提供 [广告特定的流量量度和来自的相关维度 [!DNL DSP] 和 [!DNL Search]](advertising-metrics-in-analytics.md). Adobe广告提供的指标仅适用于指定的Adobe广告维度，并且对于中的其他维度没有可用的数据 [!DNL Analytics].

例如，如果您查看 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] “按帐户列出的指标”是一个“Adobe广告”维度，您会看到总计 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] 按帐户。

![使用“Adobe广告”维度在报表中Adobe广告量度的示例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

但是，如果您查看 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] 量度（例如“页面”），其中Adobe广告不提供数据，则 [!UICONTROL AMO Clicks] 和 [!UICONTROL AMO Cost] 对于每一页，该值将为零(0)。

![使用不受支持的维度在报表中Adobe广告量度的示例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### 使用 [!UICONTROL AMO ID Instances] 用非Adobe广告Dimension代替点击

因为您无法使用 [!UICONTROL AMO Clicks] 对于现场维度，您可能希望找到与点击量等效的值。 您可能倾向于使用访问作为替代，但它们不是最佳选择，因为每个访客可能有多次访问。 (请参见“ ”[点击次数和访问次数的区别](#clicks-vs-visits).” 我们建议改用 [!UICONTROL AMO ID Instances]，即捕获AMO ID的次数。 While [!UICONTROL AMO ID Instances] 不匹配 [!UICONTROL AMO Clicks] 准确地说，它们是测量网站点击流量的最佳选项。 有关更多信息，请参阅“[数据验证 [!DNL Analytics for Advertising]](#data-validation).”

![示例 [!UICONTROL AMO ID Instances] 而不是 [!UICONTROL AMO Clicks] 对于不支持的维度](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>* [使用的Adobe广告ID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Analysis Workspace中的Adobe广告量度](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe广告中的数据](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [为什么数据可能因Adobe广告和以下内容而异 [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

