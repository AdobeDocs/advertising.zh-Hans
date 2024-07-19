---
title: ' [!DNL Analytics] 和Adobe Advertising之间的预期数据差异'
description: ' [!DNL Analytics] 和Adobe Advertising之间的预期数据差异'
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: e1c1d43c7fe5f44e34ada7dee09afd77f1b3f305
workflow-type: tm+mt
source-wordcount: '3358'
ht-degree: 0%

---

# [!DNL Analytics]和Adobe Advertising之间的预期数据差异

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

具有[!DNL Analytics for Advertising] <!-- (A4AdC) -->集成的广告商通过Adobe Advertising和Adobe Analytics跟踪付费广告。 当您通过多个系统跟踪媒体、营销活动和渠道时，来自不同系统的相同数据集很少完全匹配。 本文档说明应如何期望通过Adobe Advertising贩运的介质的数据与[!DNL Analytics]中跟踪该介质的各系统中的数据进行比较。

>[!NOTE]
>
>本文档重点介绍Adobe Advertising和分析，但许多要点也可以转移到其他跟踪解决方案中。

## 类似报表中的归因差异

### 回顾窗口和归因模型可能有所不同

[!DNL Analytics for Advertising]集成使用两个变量（[!DNL eVars]或[!DNL rVars] \[保留的[!DNL eVars]]\）来捕获[EF ID和AMO ID](ids.md)。 这些变量配置有单个回顾窗口（点进次数和显示次数的归因时间）和归因模型。 除非另有指定，否则变量将配置为与Adobe Advertising中的默认广告商级别点击回顾窗口和归因模型匹配。

但是，回顾窗口和归因模型可在Analytics（通过[!DNL eVars]）和Adobe Advertising中进行配置。 此外，在Adobe Advertising中，归因模型不仅可在广告商级别（用于竞价优化）进行配置，还可在单个数据视图和报告中进行配置（仅用于报告目的）。 例如，组织可能希望使用偶数分布归因模型进行优化，但对Advertising DSP或[!DNL Advertising Search, Social, & Commerce]中的报表使用最后接触归因。 更改归因模型会更改归因转化的数量。

如果在一个产品中修改了报表回顾窗口或归因模型，而在另一个产品中修改了报表回顾窗口或归因模型，则来自每个系统的相同报表会显示不同的数据：

* **不同回顾时间范围导致的差异示例：**

  假设Adobe Advertising的点击回顾时间范围为60天，[!DNL Analytics]的回顾时间范围为30天。 假设一位用户通过Adobe Advertising跟踪的广告进入网站，离开，然后在第45天返回网站并转化。 Adobe Advertising将转化归因于初始访问，因为转化发生在60天的回看时段内。 但是，[!DNL Analytics]不能将转化归因于初始访问，因为转化发生在30天的回看窗口过期之后。 在此示例中，Adobe Advertising报告的转化次数比[!DNL Analytics]多。

  ![转化示例归因于Adobe Advertising，但未归因于[!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **不同归因模型导致的差异示例：**

  假设用户在转化之前与三个不同的Adobe Advertising广告进行交互，并将“收入”作为转化类型。 如果Adobe Advertising报表使用均匀分布模型来归因，则它将收入平均归因到所有广告。 但是，如果[!DNL Analytics]使用最后接触归因模型，则会将收入归因于最后一个广告。 在以下示例中，Adobe Advertising将捕获的30美元收入中的平均10美元归因于三个广告中的每个，而[!DNL Analytics]将所有30美元收入归因于用户看到的最后一个广告。 当您比较来自Adobe Advertising和[!DNL Analytics]的报表时，可以预料到归因差异的影响。

  根据不同的归因模型，![归因于Adobe Advertising的其他收入和[!DNL Analytics]](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>最佳做法是在Adobe Advertising和[!DNL Analytics]中使用相同的回顾窗口和归因模型。 根据需要与您的Adobe客户团队合作，确定当前设置并保持配置同步。

这些相同的概念适用于使用不同回顾窗口或归因模型的任何其他类似渠道。

#### 浏览转化跟踪的不同回顾时间范围 {#impression-lookback}

在Adobe Advertising中，归因基于点击次数和展示次数，您可以为点击次数和展示次数配置不同的回顾时间范围。 但是，在[!DNL Analytics]中，归因基于点进和显示到达，您没有选项为点进和显示到达设置不同的归因窗口；跟踪从首次网站访问开始的每个归因窗口。 展示可能在显示到达的同一天或多个天发生，并且时间可能会影响每个系统中归因窗口的开始位置。

通常，大多数显示到达转化发生的速度足够快，以至于两个系统都将其归为点数。 但是，某些转化可能会在Adobe Advertising展示回顾窗口之外但在[!DNL Analytics]回顾窗口内发生；此类转化归因于[!DNL Analytics]中的显示到达而不是Adobe Advertising中的展示。

在以下示例中，假设访客在第1天收到广告，在第2天执行了浏览访问（即，访问了广告的登陆页面，而之前未单击该广告），并在第45天进行了转化。 在这种情况下，Adobe Advertising将从第1天到第14天跟踪用户（使用14天回溯），[!DNL Analytics]将从第2天到第61天跟踪用户（使用60天回溯），第45天的转化将归因于[!DNL Analytics]内的广告，而不是Adobe Advertising内的广告。

![归因于[!DNL Analytics]而非Adobe Advertising的浏览转化示例](/help/integrations/assets/a4adc-viewthrough-example.png)

导致差异的另一个原因是，在Adobe Advertising中，您可以为显示到达转化分配一个自定义&#x200B;*显示到达权重*，该权重与基于点击的转化所归因的权重相关。 默认显示到达权重为40%，这意味着显示到达转化会计为基于点击的转化值的40%。 [!DNL Analytics]不提供此类显示到达转化权重。 因此，例如，如果您使用默认显示到达权重，则[!DNL Analytics]中捕获的100美元收入订单会在Adobe Advertising中折现40美元，两者之差为60美元。

在比较Adobe Advertising报表和[!DNL Analytics]报表之间的显示到达转化时，请考虑这些差异。

#### 可用的归因模型

| Adobe Advertising归因 | [!DNL Analytics]归因 | [!DNL eVar]/[!DNL rVar]分配 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | 不适用 | 不适用 |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>不使用* |
| [!UICONTROL Weight Last Event More] | 不适用 | 不适用 |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | 不适用 |
| 不适用 | [!UICONTROL J-Shaped] | 不适用 |
| 不适用 | [!UICONTROL Inverse-J] | 不适用 |
| 不适用 | [!UICONTROL Custom] | 不适用 |
| 不适用 | [!UICONTROL Participation] | 不适用 |
| 不适用 | [!UICONTROL Algorithmic] | 不适用 |

>[!NOTE]
>
>对于线性分配，[!DNL Analytics]将成功事件平均归因于单次访问中的所有[!DNL eVar]值，因此请使用带有“访问”的[!DNL eVar]到期时间的线性分配。 但是，对于广告，使用线性归因会导致分配不是真正的线性分配，并会导致报表不理想。 例如，如果访客在转化之前与三个广告进行交互，则在三次单独访问中，只有上次访问中看到的广告被归因于转化，而非全部三个广告。
>
>此外，将转化分配切换到“线性”或从其中切换可防止显示历史数据，这可能导致报表中的数据误报。 例如，线性分配可能会将收入除以多个不同的[!DNL eVar]值。 如果将分配更改为“最近”，则该收入的100%将与最近的单个值相关联。 这种关联可能会导致错误的结论。
>
>为避免混淆，[!DNL Analytics]使历史数据在报表界面中不可用。 如果将[!DNL eVar]更改回初始分配设置，则可以查看历史数据，但不应仅为了访问历史数据而更改[!DNL eVar]分配设置。 Adobe建议，当您要为已记录的数据应用新的分配设置时，使用新的[!DNL eVar]，而不是更改已具有大量历史数据的[!DNL eVar]的分配设置。

在[https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html)上查看[!DNL Analytics]归因模型及其定义的列表。

如果您已登录[!DNL Search, Social, & Commerce]，则可以查找列表

* （北美用户） [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* （所有其他用户）[`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Adobe Advertising中的事件日期归因

在Adobe Advertising中，您可以按关联的点击日期/事件日期（点击或展示事件的日期）或交易日期（转化日期）报告转化数据。 [!DNL Analytics]中不存在点击/事件日期报告的概念；[!DNL Analytics]中跟踪的所有转化都按交易日期报告。 因此，可能会报告在Adobe Advertising和[!DNL Analytics]中具有不同日期的相同转化。 例如，假设一位用户在1月1日点击广告并在1月5日转化。 如果您查看的是Adobe Advertising中按事件日期列出的转化数据，则转化报告日期为点击发生的1月1日。 在[!DNL Analytics]中，1月5日报告了相同的转化。

![归因于不同日期的转化示例](/help/integrations/assets/a4adc-conversions-based-on.png)

## [!DNL Analytics Marketing Channels]中的归因

[[!DNL Analytics Marketing Channels] 报告](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html)允许您配置规则，以根据点击信息的不同方面识别不同的营销渠道。 您可以使用`ef_id`查询字符串参数将Adobe Advertising跟踪的渠道（[!UICONTROL Display Click Through]、[!UICONTROL Display View Through]和[!UICONTROL Paid Search]）作为[!DNL Marketing Channels]进行跟踪，以标识该渠道。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. -->但是，即使[!DNL Marketing Channels]报表可以跟踪Adobe Advertising渠道，数据可能由于若干原因与Adobe Advertising报表不匹配。 有关更多信息，请参阅以下部分。

>[!NOTE]
>
> 以下核心概念还适用于任何涉及Adobe Advertising中未跟踪的营销活动的多渠道跟踪，如[`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html)变量（也称为“跟踪代码”维度或“[!DNL eVar] 0”）和自定义[!DNL eVar]跟踪。

### [!DNL Marketing Channels]中可能不同的归因模型

大多数[!DNL Marketing Channels]报告配置了[!UICONTROL Last Touch]归因，其中检测到的最后一个营销渠道被分配100%的转化值。 对[!DNL Marketing Channels]报表和Adobe Advertising报表使用不同的归因模型会导致归因转化出现差异。

### [!DNL Marketing Channels]中可能不同的回顾时间范围

可以自定义[!DNL Marketing Channels]的回看窗口期。 在Adobe Advertising中，点击回顾窗口是可配置的，但通常为60天的固定窗口。 如果这两种产品使用不同的回顾时间范围，则可能会出现数据差异。

### [!DNL Marketing Channels]中的其他渠道归因

Adobe Advertising报表仅捕获通过Adobe Advertising贩运的付费媒体(对[!DNL Advertising Search, Social, & Commerce]个广告进行付费搜索，对Advertising DSP广告进行显示)，而[!DNL Marketing Channels]报表可以跟踪所有数字渠道。 这可能会导致归因转化的渠道不一致。

例如，付费搜索和免费搜索渠道通常具有共生关系，每个渠道相互协助。 [!DNL Marketing Channels]报表将某些转化归因为Adobe Advertising未跟踪的免费搜索，因为它不跟踪免费搜索。

再考虑查看展示广告、单击付费搜索广告、单击电子邮件内容，然后下达30美元订单的客户。 即使Adobe Advertising和[!DNL Marketing Channels]都使用最后接触归因模型，转化仍会以不同的方式归因于每一个。 Adobe Advertising无权访问[!UICONTROL Email]渠道，因此它将计入转换的付费搜索。 但是，[!DNL Marketing Channels]有权访问所有三个渠道，因此它将计入[!UICONTROL Email]的转化积分。

![Adobe Advertising中的其他转化归因与[!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)的示例

有关指标可能不同的更多解释，请参阅“[为什么渠道数据在Adobe Advertising和 [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)之间可能不同”。

## Adobe Analytics [!DNL Paid Search Detection]中的数据差异

[!DNL Analytics]中的[旧版 [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html)功能允许公司[定义规则以跟踪指定搜索引擎的付费和免费搜索流量](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html)。 [!DNL Paid Search Detection]规则同时使用查询字符串和反向链接域来标识付费和免费搜索流量。 [!DNL Paid Search Detection]报告是更大的[查找方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html)报告组的一部分，这些报告将在发生指定事件（例如购物车结帐）或访问结束时过期。

以下是创建[!DNL Paid Search Detection]规则集的接口：

![在[!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)中设置的付费搜索检测规则示例

生成的[!DNL Paid Search Detection]报告包括[!UICONTROL Paid Search Engine]、[!UICONTROL Paid Search Keywords]、[!UICONTROL Natural Search Engine]和[!UICONTROL Natural Search Keywords]报告。

请注意[!DNL Paid Search Detection]报表中数据的以下两个限制：

* [!UICONTROL Paid Search Keywords]和[!UICONTROL Natural Search Keywords]报表显示由反向链接URL标识的搜索查询，而不是用户竞价的关键字。 Adobe Advertising和[!DNL Analytics]报表显示实际的关键字，因此不要期望它们与[!DNL Paid Search Detection]关键字报表一致。

* 当[!DNL Paid Search Detection]功能最初创建时，原始搜索查询（用户在搜索引擎的搜索栏中输入的字符字符串）更容易通过反向链接URL提供给广告商。 现在，搜索引擎在很大程度上混淆了搜索查询，并且[!DNL Paid Search Detection]关键词报告的值有限，因为大多数查询数据都在“未指定”下。

  使用[!DNL Analytics for Advertising]，广告商仍可以跟踪[!DNL Analytics]中的付费关键字。 反向链接域将通知引擎报告哪个搜索引擎驱动了流量。 由于特定于广告商的帐户信息未绑定到反向链接域，因此所有流量都会列在搜索引擎下。 同一搜索引擎中具有多个帐户的广告商应该参考Adobe Advertising或[!DNL Analytics]报表，以获取特定于帐户的报表。

### 为什么要配置[!DNL Paid Search Detection]？

[!DNL Paid Search Detection]报告允许您在[[!DNL Analytics Marketing Channels] 报告](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html)中识别免费搜索流量。 将付费搜索流量与免费搜索流量区分开来是了解免费搜索为整个营销生态系统带来价值的一个极好的方法。

## [!DNL Analytics for Advertising]的点进数据验证 {#data-validation}

对于集成，您应该验证点进数据，以确保网站上的所有页面都正确跟踪点进。

在[!DNL Analytics]中，验证[!DNL Analytics for Advertising]跟踪的最简单方法之一是使用“AMO ID实例与点击次数”计算量度将实例与点击次数进行比较，该计算量度的计算方式如下：

```
AMO ID Instances to Clicks = ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

[!UICONTROL AMO ID Instances]表示在网站上跟踪[AMO ID](ids.md)的次数。 每次单击广告时，都会向登陆页面URL添加AMO ID (`s_kwcid`)参数。 因此，[!UICONTROL AMO ID Instances]的数量与点击量类似，可根据实际的广告点击量进行验证。 我们通常看到[!DNL Search, Social, & Commerce]的匹配率为85%，[!DNL DSP]流量的匹配率为30%（在筛选为仅包括点进[!UICONTROL AMO ID Instances]时）。 搜索和显示之间的预期差异可以用预期流量行为来解释。 搜索会捕捉意图，因此，用户通常打算单击其查询中的搜索结果。 但是，查看显示或在线视频广告的用户更有可能无意中单击该广告，然后要么从网站弹回，要么放弃在跟踪页面活动之前加载的新窗口。

在Adobe Advertising报表中，您可以使用“[!UICONTROL EF ID Instances]”量度而不是[!UICONTROL AMO ID Instances]来类似地比较实例与点击次数：

```
EF ID Instances to Clicks = ([!UICONTROL EF ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

虽然AMO ID和EF ID之间的匹配率应该较高，但请不要预期100%的奇偶校验，因为AMO ID和EF ID从根本上跟踪不同的数据，这种差异可能会导致总[!UICONTROL AMO ID Instances]和[!UICONTROL EF ID Instances]之间的细微差异。 但是，如果[!DNL Analytics]中的总[!UICONTROL AMO ID Instances]与Adobe Advertising中的[!UICONTROL EF ID Instances]的差异超过1%，请联系您的Adobe客户团队寻求帮助。

有关AMO ID和EF ID的详细信息，请参阅[Analytics使用的Adobe AdvertisingID](ids.md)。

<!--  Need to create a new report to show tracking instances to clicks, instead of clicks to instances as shown, and replace this screenshot.

The following is an example of a workspace to track clicks to instances.

![Example of a workspace to track clicks to instances to clicks](/help/integrations/assets/a4adc-clicks-to-instances-example.png)
-->

### 解决点击和实例之间的差异问题

如果[!UICONTROL EF ID Instances]与点击量的比率低于85%，请检查以下各项：

* 您是否缺少帐户或任何子级别的点击跟踪，或者您是否具有重复的点击跟踪（例如，帐户和促销活动级别均如此）？

  在Search、Social和Commerce中，[下载帐户的批量工作表](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)以检查跟踪URL。

  此外，在[!DNL Analytics]中，您可以看到是否始终使用“[!DNL AMO ID]到[!DNL EF ID]”计算量度附加AMO ID和EF IF，计算方式如下：

  ```
  [!DNL AMO ID] to [!DNL EF ID] = ([!UICONTROL AMO ID] / [!DNL EF ID])
  ```

  如果值大于100%，则表示缺少的EF ID数大于AMO ID数。

* 登陆页面是否存在加载问题，以便不捕获AMO ID和EF ID？

* 是否重定向了登陆页面URL，从而导致AMO ID和EF ID丢失？

* 是否所有登陆页面都使用配置的报表包？

>[!NOTE]
>
>理论上，一个实例可能具有多次点击。 确保检查不同设备（如台式机、移动设备和平板电脑）上的点击次数。

## 比较[!DNL Analytics for Advertising]中的数据集与Adobe Advertising中的数据集

[AMO ID](ids.md) （s_kwcid查询字符串参数）用于[!DNL Analytics]中的报表，而[EF ID](ids.md) （ef_id查询字符串参数）用于Adobe Advertising中的报表。 由于它们是不同的值，因此一个值可能会被损坏或未添加到登陆页面。

例如，假设我们有以下登陆页面：

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

其中EF ID为“`test_ef_id`”，AMO ID为“`test_amo_id`”。

如果发生站点端重定向，则URL可能最终如下所示：

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

其中EF ID为“`test_ef_id`”，AMO ID为“`test_amo_id#redirectAnchorTag`”。

在此示例中，添加锚标记会向AMO ID添加意外字符，从而导致Analytics无法识别的值。 此AMO ID将不会进行分类，并且在[!DNL Analytics]报表中，与其关联的转化将属于“[!UICONTROL unspecified]”或“[!UICONTROL none]”。

幸运的是，尽管这类问题很常见，但通常不会造成很大的差异。 但是，如果您发现[!DNL Analytics]中的AMO ID与Adobe Advertising中的EF ID之间存在很大差异，请联系您的Adobe客户团队以获取帮助。

## 其他量度注意事项

### 点击量和访问量之间的区别 {#clicks-vs-visits}

它们看起来类似，但点击量和访问量代表不同的数据：

* **Click：** [!DNL DSP]，或者当访客点击发布者网站上的广告时，搜索引擎会记录一次点击。

* **访问：** [!DNL Analytics]将[访问](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)定义为用户的一系列页面查看，并根据多个条件之一结束，例如30分钟不活动。

顾名思义，单击可导致多次访问。

请考虑以下示例：用户1和用户2均可通过单击Adobe Advertising广告来访问站点。 用户1查看了4个页面，然后离开去一天，因此初始点击导致一次访问。 用户2查看两个页面，离开时享受45分钟的午餐，回访，再查看两个页面，然后离开；在这种情况下，最初的点击导致两次访问。

![点击次数与访问次数之间差异的示例](/help/integrations/assets/a4adc-visits-example.png)

### 点击次数和点进次数的区别

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

点击量和点进次数是两个不同的量度：

* **Click：** [!DNL DSP]，或者当访客点击发布者网站上的广告时，搜索引擎会记录一次点击。

* **点进次数：** [!DNL Analytics]在访客登陆目标网站并加载登陆页面且页面底部的[!DNL Analytics]请求将数据发送到[!DNL Analytics]时记录点进。

由于意外广告点击，点击和点进次数可能会有很大差异。 我们观察到显示广告上的大多数点击是意外点击，这些意外访客在加载登陆页面之前点击了“返回”按钮，因此[!DNL Analytics]无法记录点进。 这尤其适用于更有可能意外点击的广告，例如移动广告、视频广告和填充屏幕的广告，并且必须在用户查看页面之前将其关闭。

由于带宽或可用处理能力较低，因此加载到移动设备上的网站也不太可能导致点进，从而导致加载登陆页面所需的时间较长。 50-70%的点击不会导致点进的情况并不少见。 在移动环境中，差异可能高达90%，这是因为浏览器速度较慢，并且用户在滚动页面或尝试关闭广告时意外单击广告的可能性较高。

点击数据还可能会记录在使用当前跟踪机制（例如进入或离开移动设备应用程序的点击）无法记录点进次数，或者广告商只为其部署了一种跟踪方法(例如，使用浏览式JavaScript方法，即阻止第三方Cookie跟踪点击但不跟踪点进的浏览器)的环境中。 Adobe建议同时部署点击URL跟踪和JavaScript浏览跟踪方法的一个关键原因是，可以最大程度地提高可跟踪点进的覆盖率。

### 对非Adobe AdvertisingDimension使用Adobe Advertising流量指标

Adobe Advertising为Analytics提供了来自 [!DNL DSP] 和 [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md)的[广告特定流量量度和相关维度。 Adobe Advertising提供的度量仅适用于指定的Adobe Advertising维度，并且数据对于[!DNL Analytics]中的其他维度不可用。

例如，如果您按帐户查看[!UICONTROL Adobe Advertising Clicks]和[!UICONTROL Adobe Advertising Cost]指标(一个Adobe Advertising维度)，则按帐户显示总计[!UICONTROL Adobe Advertising Clicks]和[!UICONTROL Adobe Advertising Cost]。

![使用Adobe Advertising维度的报表中Adobe Advertising量度的示例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

但是，如果您通过页面维度（例如页面）查看Adobe Advertising不提供数据的[!UICONTROL Adobe Advertising Clicks]和[!UICONTROL Adobe Advertising Cost]指标，则每个页面的[!UICONTROL Adobe Advertising Clicks]和[!UICONTROL Adobe Advertising Cost]均为零(0)。

![使用不受支持的维度的报告中Adobe Advertising量度的示例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### 将[!UICONTROL AMO ID Instances]用作非Adobe AdvertisingDimension点击次数的替代项

由于您无法将[!UICONTROL AMO Clicks]与网站上的维度一起使用，因此您可能希望找到等同于点击量的维度。 您可能倾向于使用访问次数作为替代，但这并不是最佳选择，因为每个访客可能具有多次访问。 (请参阅&quot;[点击次数与访问次数的差异](#clicks-vs-visits)&quot;。 我们建议改用[!UICONTROL AMO ID Instances]，这是捕获AMO ID的次数。 虽然[!UICONTROL AMO ID Instances]与[!UICONTROL AMO Clicks]不完全匹配，但它们是测量网站点击流量的最佳选项。 有关详细信息，请参阅“[针对 [!DNL Analytics for Advertising]](#data-validation)的点进数据验证”。

对于不支持的维度](/help/integrations/assets/a4adc-amo-id-instances.png)，为![示例[!UICONTROL AMO ID Instances]而不是[!UICONTROL Adobe Advertising Clicks]

>[!MORELIKETHIS]
>
>* [概述 [!DNL Analytics for Advertising]](overview.md)
>*  [!DNL Analytics]](/help/integrations/analytics/ids.md)使用的[Adobe AdvertisingID
>* 在Analysis Workspace中[Adobe Advertising指标](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe Advertising中的数据](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [为什么数据在Adobe Advertising和 [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)之间可能不同
