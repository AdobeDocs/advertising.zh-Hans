---
title: 关于自定义报表的常见问题解答
description: 了解有关性能报表的常见问题解答，包括数据问题疑难解答。
exl-id: 1232efce-25eb-48d8-a3fb-f57711fa14e5
feature: Search Reports
source-git-commit: 01fe9264fee43ed29f6cee022dadeb29fbd26f45
workflow-type: tm+mt
source-wordcount: '3922'
ht-degree: 0%

---

# 关于自定义报表的常见问题解答

## 一般问题

+++如果报表的日期范围在报表数据可用之前开始，该怎么办？
会生成报告，但其中仅包含可用日期的数据。 有关每个报表类型何时有可用数据的详细信息，请参阅“[用于报表的数据](data-used-for-reports.md)”。
+++

+++基于点击日期和基于交易日期的报表之间有何区别？
在按事务处理日期报告转换时，数据包括事务处理日期在指定时间期内发生的事务处理。 此选项是基本报表和高级报表中的默认设置，它显示在指定时间段内赚取的收入。

在按点击日期报告转化时，数据包含在指定时间段内发生的点击所导致的交易。 当项目组合在点击和交易之间存在重大延迟时，此类报表会显示项目组合每次点击的历史收入，这使您能够了解随着时间的推移会有什么收入行为。

![按点击日期报告与按交易日期报告](/help/search-social-commerce/assets/click-date-vs-txn-date.png "按点击日期报告与按交易日期报告")
+++

+++如果更改点击回顾窗口或展示回顾窗口，会发生什么情况？
(仅限具有基于Advertising像素的转化跟踪服务的广告商)较长时间或更短的时段内会收集由初始点击产生的事件数据。

广告商的[点击回顾窗口](/help/search-social-commerce/glossary.md#c-d)和[展示回顾窗口](/help/search-social-commerce/glossary.md#i-j)将分别确定付费点击或展示展示发生后（事件可归因于转化）的天数。 将值更改为更长或更短的时段对于点击收入或显示展示收入时段的广告商可能很重要。

**最佳实践：**&#x200B;确保回顾时间范围比大多数关键词或广告的点击收入时间和展示收入时间长。 如果转换时间较短，则某些转化不会与初始点击或展示关联。
+++

+++如何知道[!DNL Google Ads]广告扩展或产品列表产生了哪些转化？
您可以通过生成[!DNL Google Ads]来查看哪些转化是由于单击[!UICONTROL Transaction Report]广告扩展（而不是广告本身）或产品列表导致的。 [!UICONTROL Link Type]列值显示所点击链接的类型和标题：

* 产品清单列为`pla:<product ID>`，如`pla:8525822`。

* 站点链接作为`sl:<Sitelink text>`列出，如`sl:See Current Offers`。

  如果您在报表中包含[!UICONTROL Tracking URL]列，则还可以标识站点链接。 Sitelink的[!UICONTROL Tracking URL]包括属性`&ev_ltx=sl:<link-name>`。

>[!NOTE]
>
>来自[!DNL Google Ads]位置的转化和电话分机包含在其伴随的广告的数据中。 它们不会单独报告。

+++

+++我的报表中的“[!UICONTROL Keyword]”列包含值“（广告组内容）&lt;*广告组名称*>”。
当行包含支持内容的搜索促销活动、显示促销活动或社交促销活动（不包含关键字）的数据时，[!UICONTROL Keyword]列将改为显示适用的广告组名称。
+++

+++由于季节性或市场变化，我的报表会显示非典型数据。 一旦条件发生更改，这是否会影响竞价？
优化功能每天为每个竞价单位构建收入模型，以确保它识别并立即响应趋势，并且模型包含长期历史数据以帮助预测季节性表现。 项目组合的收入模型半衰期设置<!-- add link to glossary? -->还确定最近收入数据的加权程度。 最佳实践是在非典型绩效期间降低半衰期，但在调整收入模型后提高半衰期。 如果您对是否需要调整半衰期存有疑问，请联系您的Adobe客户团队。

如果您根本不希望该期间的数据影响将来的竞价，则可以选择从模型中排除这些日期。 请联系您的Adobe客户团队以排除日期。
+++

+++我能否创建有关特定帐户属性指标（如[!UICONTROL Device]或[!UICONTROL Objective Name]）的报告？
对于营销活动实体报表（[!UICONTROL Campaign Report]、[!UICONTROL Ad Group Report]、[!UICONTROL Ad Variation Report]、[!UICONTROL Keyword Report]和[!UICONTROL Product Group Report]），量度数据由您在报表中包含的属性列动态聚合。 您可以选择删除报表的键列，并仅包括要为其聚合数据的属性列。

例如，如果您生成包含[!UICONTROL Keyword Report]和[!UICONTROL Ad Group]设备列的，则默认情况下，报告会按广告组和设备类型汇总每个关键字的量度。 但是，如果您在生成报告之前删除了[!UICONTROL Keyword]列，则报告会按设备类型动态地为指定的广告组生成量度。

>[!NOTE]
>
>您无法使用此功能按标签分类聚合数据。 报表中的任何标签分类列都将被忽略。 请改用[标签分类报告](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md)。

+++

## 一般数据问题

+++使用不同的归因规则生成的报表显示不同的总计。
如果使用相同的报表参数多次生成报表，但归因规则不同，则数据可能会因以下任一原因而有所不同：

* 点击基于日期的数据可能不在指定的日期范围内。

  如果使用报表参数“[!UICONTROL Conversions based on click date]”，则指定的日期范围将应用于点击的日期，而不是交易的日期。 如果报表还使用归因规则“第一个事件”或“最后一个事件”，则导致转化的第一个或最后一个事件可能不在指定的日期范围内。 例如，假设用户在4月30日点击了Keyword_1，在5月20日点击了Keyword_2，然后在5月21日进行了转换。 如果报告使用“[!UICONTROL First Event]”归因规则并且日期范围为5月1日至21日，则第一个事件（在4月30日单击Keyword_1）不会包含在报告中。 如果您使用相同的日期范围但使用“[!UICONTROL Last Event]”归因规则运行报表，则转换将包含在报表中，因为最后一次单击发生在指定的日期范围内。

* 项目组合过滤器选择排除了一些导致转化的事件。

  如果您报告项目组合的子集，则可能不包括包含根据某个归因规则将转化归因到的事件的营销活动。 例如，假设用户从Portfolio_1单击Keyword_1，从Portfolio_2单击Keyword_2，然后进行转换。 如果报表使用“[!UICONTROL First Event]”归因规则，则必须包含Portfolio_1才能将转化包含在报表中。 但是，如果报表使用“Last Event”归因规则，则必须包含Portfolio_2。

>[!TIP]
>
>如果要比较不同归因规则下的转化总计，请使用报表参数“[!UICONTROL Conversions based on transaction date]”运行报表，然后选择所有广告网络或所有项目组合。 如果不设置其他过滤器，则转化总数应该匹配。

+++

+++尽管总计正确无误，但个别数据字段仍然不正确。
当量度格式使用整数时，可能会出现这种情况：

* 如果您创建格式为[没有小数点的数字](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md)的&#x200B;*自定义量度*（将数据显示为整数），并将其包含在使用加权转化归因规则（[!UICONTROL Weight First Event More]、[!UICONTROL Weight Last Event More]或[!UICONTROL Even Distribution]）的视图或报表中，则输出将以整数而不是小数形式显示。 在这种情况下，单个数据字段可能不正确，尽管总数正确。 例如，如果某个顺序在三个事件之间平均分配，则三个事件的每个都会获得一个顺序（而不是0.33顺序）。 要解决此问题，[将度量格式](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md)更改为&#x200B;*数字为2小数点*。

* 同样，如果您有一个收入量度以整数形式发送，则会出现同样的问题。 （收入格式由提交数据的转化标记控制。） 要解决此问题，[创建一个自定义量度](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md)，该量度仅由收入量度组成，格式为&#x200B;*数值到2小数点*，并将其包含在视图和报表中，而不是原始量度。
+++

+++当点击或收入数据缺失时，我如何防止它影响将来的竞价？
当Search、Social和Commerce与广告网络不同步时，会发生点击数据问题。 请联系您的Adobe帐户团队以手动同步该帐户。 如果整天的点击数据缺失，请让您的Adobe客户团队将该天排除在成本模型之外。

由于跟踪或信息源文件问题，可能会出现收入数据问题。 请联系您的Adobe客户团队以调查此问题。 如果缺少一整天的收入数据，请让您的Adobe客户团队从收入模型中排除该天。
+++

+++货币数据以错误的格式显示。
默认情况下，报表中的所有货币数据均以美元的格式显示（如1,000.00）。 要以正确的货币格式显示值（但不包括CSV和TSV格式中的任何货币符号），请向报表中添加“[!UICONTROL Currency]”列。 如果报表包含具有不同货币的帐户的数据，则任何“[!UICONTROL Total]”货币值只是列中所有数字的总和，而不考虑货币。
+++

+++为什么我会看到转化量度应是自然数（1、2等）的小数值？
在以下情况下，您可能会看到小数值：

* 如果您使用除[!UICONTROL Last Event]或[!UICONTROL First Event]之外的任何转化归因规则参数运行报告，则收入可能会在转化路径中的多个事件之间拆分。

* 在[!UICONTROL Transaction Report]中，如果多个具有不同匹配类型的[竞价单位](/help/search-social-commerce/glossary.md#a-b)具有相同的交易ID，则跟踪ID的收入将按照指定点击日期的点击数进行拆分。
+++

## 标准绩效指标

+++报表中缺少点击数据。
以下是缺少点击数据的常见原因。

| 原因 | 检测/分析 | 解决方法 |
|---|---|---|
| 从广告帐户检索点击数据的进程失败。 | 没有系统化的方法可以检测到此问题，但您可能会注意到即使广告帐户花费了资金，营销活动仍不会显示成本或点击信息。 | 请联系您的Adobe客户团队。<br><br>如果数据缺失超过24小时，则从成本预测中排除这些日期，直到检索到数据为止。 您的Adobe客户团队可以排除这些日期。 |
| 广告商和广告网络之间的计费问题导致广告帐户无法支出。 | 没有系统化的方法可以检测到此问题，但您可能会注意到营销活动未显示任何成本或点击信息。 | 如果您知道广告帐户由于开单问题而无法支出，则从成本预测中排除这些日期。 您的Adobe客户团队可以排除这些日期。 |

+++

+++性能数据不同于广告网络编辑器中的数据。
当广告网络发送对先前数据的更新（通常是因为他们将点击欺诈归因于某些点击）时，搜索、社交和Commerce不会更新数据，除非存在超过5%的差异并且Adobe客户团队提交了请求。

此外，在比较某个日期范围内汇总的展示共享数据时，“搜索”、“社交”和“Commerce”报表的数据可能与广告网络报表的数据不同。 造成这种差异的原因在于广告网络的API报告数据的方式， Search、Social和Commerce使用该API来提取数据。 例如，对于[!DNL Google Ads]数据：

* 对于大多数展示份额量度，[!DNL Google Ads]对小于10%或大于90%的值报告的低端或高端设置上限。 低于10%的数据报告为0.0999 ，超过90%的数据报告为0.9001

* 当日期范围内同时存在有上限和没有上限的数据时，Search、Social和Commerce会使用在API中按原样发送的值聚合展示份额数据，对小于10%的行使用0.0999，对大于90%的行使用0.9001。 此聚合可能会导致[!DNL Google Ads]预聚合数据出现差异，因为[!DNL Google Ads]可以使用实际百分比值，如7%或97%。
+++

+++报表中的性能数据与[!DNL Google Analytics]中的数据不同。
这两个系统测量不同的数据，因此您应该看到不同的数据。 例如：

* 搜索、社交和Commerce(以及Google广告)跟踪点击次数，而[!DNL Google Analytics]跟踪每30分钟浏览器会话的访问次数。 例如，如果用户单击了您的广告一次，单击“返回”按钮，然后再次单击该广告，则Search、Social和Commerce会记录两次单击，但[!DNL Google Analytics]会记录一次访问。

* [!DNL Google Analytics]显示所有流量数据，而Search、Social和Commerce（以及[!DNL Google Ads]）过滤无效点击（例如过度的、重复的点击）。

* [!DNL Google Analytics]包含所有点击的点击和收入数据。 Search、Social和Commerce无法跟踪跟踪URL不正确或缺失的广告和关键字的点击和收入数据。
+++

## 转化量度

+++我的报表未显示转化数据。
报表可能不包括发生转化的转化量度。
+++

+++报表中缺少收入。

**使用Adobe Advertising转化标记的广告商**

*可能的原因：*

* 添加了关键字或广告，但没有在跟踪模板或目标URL中添加Search、Social和Commerce点击跟踪前缀，或者跟踪前缀不正确。

* 未在所有适用的网页上正确实施转化跟踪标记，或者未对转化跟踪标记进行编辑。

* Search、Social和Commerce跟踪的转化指标已从报表中排除，因此不可见。

* 未实施客户端的收入分析器。

*可能的解决方案或解决方法：*

1. 验证报表或数据视图中是否包含正确的列。 如果无法添加正确的列，则您或您的Adobe帐户团队必须[使转化指标可用于报表](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md)。

1. 验证是否在所有适用的网页上实施了正确的转化跟踪标记。 如有必要，请让您的Adobe客户团队为每个适用的转化跟踪标记创建一个测试交易，并从Cookie中捕获交易的详细信息（如`transactionid`和详细信息，如`trackingid`、`clickid`等）。

1. 如果为营销活动禁用了[!UICONTROL Auto Upload]选项，并且您已添加关键词或广告，请确保已生成跟踪模板或目标URL，其中包含“搜索”、“社交”和“Commerce”的每次点击重定向跟踪。 Adobe帐户团队可以运行内部报表，以查看是否有任何点击跟踪URL（跟踪模板或目标URL）缺失或格式不正确。

   如有必要，请使用正确的URL创建批量工作表文件来生成跟踪，并使用&#x200B;**生成跟踪URL**&#x200B;选项将文件发布到相应的帐户。

   目标URL应以“http://pixel.everesttech.net”或“https://pixel.everesttech.net”开头。

1. 如果这些步骤均无法解决问题，则[联系客户关怀团队](/help/search-social-commerce/get-help.md)。

   如果客户尚未启动或新启动，则客户关怀团队会验证是否已设置收入分析器。 如果设置了解析器，则他们将验证Search、Social和Commerce是否接收到任何像素转换并排查问题。

**发送转化数据馈送的广告商**

*可能的原因：*

* 馈送文件未提交、未完全解析或馈送包含孤立事务。

* 相关转化量度将从报表中排除，因此不可见。

>[!NOTE]
>
>通常情况下，在收到馈送的2-4小时后，数据才会出现在用户界面中。

*可能的解决方案或解决方法：*

1. 验证报表或数据视图中是否包含正确的列。 如果无法添加正确的列，则您或您的Adobe帐户团队必须[使转化指标可用于报表](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-available.md)。

1. 运行[!UICONTROL Portfolio Report]。 如果为空，则运行[!UICONTROL Campaign Report]和[!UICONTROL Search Engine Report]以查看收入是否出现在这些报表中。 如果是这样，则营销策划可能没有分配到相应的项目组合。

1. 验证文件是否已发送到收入服务器，以及文件是否遵循与以前文件相同的格式和文件命名约定。

   如果格式或文件命名惯例发生更改，请更正文件并重新发送它。

1. 如果文件已发送，则[联系客户关怀团队](/help/search-social-commerce/get-help.md)。

   客户关怀团队将检查文件是否已收到并解析。 如果处理文件时没有出现错误，则会检查孤立事务。
+++

+++某些高级报表不包含广告商信息源提供的转化数据。
[!UICONTROL Geo Distribution Report]和[!UICONTROL Domain Referral Report]使用通过Adobe Advertising转换跟踪服务捕获的数据，并且只能为使用该服务的广告商生成。 这些报表不包括在Adobe Advertising转化跟踪系统之外跟踪的转化数据。
+++

+++收入数据与广告商自己的收入数据不同。

**使用Adobe Advertising转化标记的广告商**

*可能的原因：*

* Search、Social和Commerce在Cookie过期或删除时忽略收入，但广告商可能将其视为有效收入。

* 广告商页面的流量来自书签或免费搜索，而不是广告。

* 未在所有适用的网页上正确实施转化跟踪标记，或者未对转化跟踪标记进行编辑。

*可能的解决方案或解决方法：*

1. 转到&#x200B;**[!UICONTROL Insights & Reports]>[!UICONTROL Reports]**&#x200B;并生成[!UICONTROL Transaction Report]。 将Search、Social和Commerce收到的交易与广告商的数据进行比较。

1. 如果某些事务不正确或缺少某些事务，请确保在所有适用的网页上实施了相关的转化跟踪标记，并且除非您的Adobe客户团队建议您这样做，否则不会进行编辑。 如果最近更新了网站，则标记可能会丢失或发生更改。

   Search、Social和Commerce需要在`ef_transaction_properties`变量中和`src`标记的`img`元素内有格式正确的URL（具有名称 — 值对中的参数）。

1. 如果无法确定并无法解决问题，请[联系客户关怀团队](/help/search-social-commerce/get-help.md)。

   客户关怀团队将尝试识别缺少的交易，然后检查是否存在孤立的交易和非来自广告的交易（“不相关的转化”）。

**具有使用`ef_id`值的转化数据馈送的广告商**

请参阅上面像素实施的可能原因和解决方案。

**具有使用交易ID的转化数据馈送的广告商**

*可能的原因：*

* Search、Social和Commerce在Cookie过期或删除时忽略收入，但广告商可能将其视为有效收入。

* 广告商页面的流量来自书签或免费搜索，而不是广告。

* 在进行具有相同交易ID的在线交易之前，已报告离线转化。 联机事务必须首先发生。

*可能的解决方案或解决方法：*

1. 转到&#x200B;**[!UICONTROL Insights & Reports]>[!UICONTROL Reports]**&#x200B;并生成[!UICONTROL Transaction Report]。 将Search、Social和Commerce收到的交易与广告商的信息源数据进行比较。

1. 如果报表中缺少信息源文件中的交易，则检查在离线转化之前是否发生了具有相同交易ID（通过像素跟踪）的在线交易。

1. 如果无法确定并无法解决问题，请[联系客户关怀团队](/help/search-social-commerce/get-help.md)。

   客户关怀部门将检查数据解析错误和[孤立事务](/help/search-social-commerce/glossary.md#o-p)。

**具有其他转化数据馈送类型的广告商**

*可能的原因：*

* Search、Social和Commerce在Cookie过期或删除时忽略收入，但广告商可能将其视为有效收入。

* 广告商页面的流量来自书签或免费搜索，而不是广告。

* 存在[个孤立交易](/help/search-social-commerce/glossary.md#o-p)，因此Search、Social和Commerce不计算它应获得的所有收入。

* 广告商针对在馈送中发送的其他数据集验证了“搜索、社交和Commerce”报表。

* 事务ID （`ev_transid`个值）未发送、不唯一或不正确。

* 馈送文件包含重复的跟踪ID。

* 分析文件时出错。

* 广告商的重复数据消除逻辑与搜索、社交和Commerce逻辑不同。

*可能的解决方案或解决方法：*

1. 转到&#x200B;**[!UICONTROL Insights]和[!UICONTROL Reports > Reports]**&#x200B;并生成[!UICONTROL Transaction Report]。 将Search、Social和Commerce收到的交易与广告商的数据进行比较。

1. 如果某些交易不正确或丢失，请确保a)信息源文件包含所有必需的交易ID且没有重复的跟踪ID，以及b)交易ID唯一且正确。

1. 如果无法确定并无法解决问题，请[联系客户关怀团队](/help/search-social-commerce/get-help.md)。

   客户关怀团队将检查数据解析错误和孤立事务。
+++

+++收入数据不同于Adobe Analytics中的数据
请参阅[https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html?lang=zh-Hans](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html?lang=zh-Hans).<!-- change link URL to relative link -->
+++

## 特定报告

+++[!UICONTROL Portfolio Report]是否应该显示与[!UICONTROL Portfolios]视图相同的数字？
当视图、报表参数以及视图和报表的数据列的所有筛选器都相同时，[!UICONTROL Portfolio Report]和[!UICONTROL Portfolios]视图显示相同的数据。 例如，如果[!UICONTROL Portfolios]视图显示的项目组合在日期范围“[!UICONTROL All but inactive]”为“[!UICONTROL Last 7 days]”且只显示默认数据列，则使用默认参数的[!UICONTROL Portfolio Report]会显示相同的数据。 如果您在[!UICONTROL Portfolios]视图中更改了任何报表参数或使用不同的筛选器，则数据值可能会不同。
+++

+++我的[!UICONTROL Portfolio Report]中的数据与我的[!UICONTROL Search Engine Report]或[!UICONTROL Search Engine Account Report]中的数据不匹配。
[!UICONTROL Portfolio Report]仅显示分配给指定项目组合的市场活动的数据，但[!UICONTROL Search Engine Report]和[!UICONTROL Search Engine Account Report]可能还包含未分配给项目组合的市场活动的数据。
+++

+++[!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report]与项目组合级别[!UICONTROL Model Accuracy Report]有何不同？
(仅限代理客户经理、Adobe客户经理和管理员用户)从[!UICONTROL Forecast Accuracy Report] > [!UICONTROL Reports]中可用的[!UICONTROL Model Accuracy]与项目组合级别[!UICONTROL Model Accuracy Report]提供相同数据，只是您可以跨多个项目组合运行它并更改归因规则。 您还可以使用自定义参数运行和计划报表，并使用该报表创建电子表格馈送。 此外，[!UICONTROL Forecast Accuracy Report]比旧版项目组合级别报表更准确，因为它使用项目组合的历史目标而不是当前目标评估收入准确性，并且它更准确地表示适用时区的数据。
+++

+++广告级别的数据不适用于[!DNL Google Ads]动态搜索广告(DSA)、最佳效果、智能购物和[!DNL YouTube]营销活动。
广告网络不提供将收入归因于这些促销活动的单个广告所需的标识符。 因此，广告级别的效果数据对于[!UICONTROL Ads]视图或[!UICONTROL Ad Variation Report]中的这些营销活动类型不可用。 预计营销活动的广告级别数据总数与营销活动数据总数之间存在差异。
+++

+++在[!UICONTROL Transaction Report]中，如何知道哪个转化量度来自数据馈送或被Adobe Advertising跟踪像素跟踪？
在交易报表中，如果您包含自定义列“[!UICONTROL Tracking URL]”，则可以判断所包含的转化量度是否被Adobe Advertising跟踪像素跟踪。 使用Adobe Advertising跟踪像素跟踪URL以“`http://pixel.everesttech.net`”开头。
+++

+++我的[!UICONTROL Transaction Report]中的数据与我的[!UICONTROL Keyword Report]中的数据不匹配。
在按项目组合生成这两个报表时，如果使用历史数据（即基于指定日期内的项目组合配置）而不是使用当前营销活动的数据来生成[!UICONTROL Keyword Report]，则数据将不同。 在按项目组合生成[!UICONTROL Transaction Report]时，它包括项目组合中当前促销活动的数据。
+++

## 电子表格馈送

+++报告输出包含日期范围的组合。
如果信息源使用“[!UICONTROL Daily]”以外的任何数据聚合级别聚合数据，则您可能会看到不同的日期范围。

要解决此问题，请更新电子表格馈送以包含每天汇总的数据。 此任务包括更新报告模板、使用该模板生成报告、使用该报告创建自定义[!DNL Microsoft Excel]模板，然后更新馈送设置以包括新的Excel模板。 有关详细信息，请参阅“[编辑电子表格报表源设置](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)”。
+++

+++电子表格馈送导致内部错误。
如果您更改报告模板中的列，但未相应地更新[!DNL Microsoft Excel]模板，则可能会发生此错误。

要解决此问题，请更新电子表格馈送以包含新列。 此任务包括更新报告模板、使用该模板生成报告、使用该报告创建自定义[!DNL Excel]模板，然后更新馈送设置以包括新的Excel模板。 有关详细信息，请参阅“[编辑电子表格报表源设置](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)”。
+++

+++当我尝试在[!DNL Excel]中打开电子表格馈送时，[!DNL Excel]报告“无法读取的内容”错误，并从恢复的内容中删除数据。
当[!DNL Microsoft Excel]模板不按开始日期升序对数据排序时，电子表格馈送可能包含空白行。 特别是，[!DNL Excel]报告错误“Excel在“&lt;*报告名称*>.xlsx”中发现不可读的内容。 是否要恢复工作簿的内容？ 如果您信任此工作簿的来源，请单击“是”。 如果单击“是”，您将收到以下消息：“删除的记录：来自/xl/worksheets/sheet1.xml部件的单元格信息”，并且电子表格馈送包含空白行。

要解决此问题，请编辑与馈送关联的[!DNL Excel]模板以按[!DNL Start date in Ascending (Oldest to Newest) order]对数据排序，然后通过电子表格馈送设置上传更新的模板。 有关详细信息，请参阅“[编辑电子表格报表源](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md)”。
+++
