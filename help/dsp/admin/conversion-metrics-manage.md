---
title: 在DSP中管理广告商的转化量度。
description: 了解如何将Adobe Advertising跟踪的转化量度用于DSP广告商。
feature: Conversions
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# 管理广告商的转化量度

广告商的转化量度在整个Adobe Advertising中使用：

* 在Advertising DSP中，您可以在营销活动管理视图、自定义目标和自定义报表中包含转化量度。 您还可以使用广告商的转化量度来创建[自定义目标](/help/dsp/admin/custom-objectives-manage.md)，这些目标用于优化包。

* （具有Advertising Search、Social和Commerce的广告商）在Search、Social和Commerce中，转化量度的数据可以显示在营销活动、组合和目标管理视图以及报表的列中。 具有足够访问权限的用户还可以使用转化量度创建目标，以优化项目组合。

<!--
The conversion metrics that Adobe Advertising tracks for an advertiser &mdash; including [conversion and site engagement metrics synced from Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md), [site events synced from Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md), and custom feeds &mdash; are used throughout Advertising DSP. You can include conversion metrics in campaign management views, custom objectives, and custom reports. You can also use conversion metrics to create [custom objectives](/help/dsp/admin/custom-objectives-manage.md), which are used to optimize packages.

By default, none of an advertiser's conversion metrics are available for campaign management views, custom objectives, and reports. They are available only when you specifically make them available. When you make a conversion metric available, you can either use the metric name exactly as it is spelled in the retrieved data or change the display name that's shown in column headings for readability.

From the list of visible metrics, each user with access to the advertiser's data can customize the metrics they see for campaign management views, objectives, and reports by including or omitting specific metrics. Users with sufficient access privileges can also optimize for specific metrics by associating them with DSP package-level custom goals.

-->

为DSP用户跟踪的指标类型包括：

* Adobe Advertising跟踪广告商的转化量度。

* [转化和网站参与度量度已从Adobe Analytics同步](/help/integrations/analytics/analytics-data-in-advertising.md)。

* 从Adobe Customer Journey Analytics[&#128279;](/help/integrations/customer-journey-analytics/overview.md)同步的网站事件。

* 来自自定义馈送的转化。

从可用的转化量度列表中，每个有权访问广告商数据的用户都可以自定义他们看到的可用于管理视图和报表的量度，包括或忽略他们选择的特定量度。 您可以使用与检索数据中拼写完全相同的量度名称，也可以更改列标题中显示的名称以提高可读性。

>[!IMPORTANT]
>
>默认情况下，广告商的转化量度均不可包含在促销活动管理视图、自定义目标和自定义报表中。 要使转化量度可用，您必须明确使其可用。

>[!TIP]
>
>一旦广告商（或广告网络）停止收集转化量度，[将其从管理视图和报告中隐藏](#conversion-metrics-change-available)，除非您想要将其用于查看历史数据。

## 查看为广告商跟踪的转化量度

* 在主菜单中，单击&#x200B;**[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**。

将列出为广告商收集的所有转化量度以及为其分配的任何不同的显示名称。 每个量度行都包含量度的源。

## 更改转化量度的显示名称

例如，如果您使用名为&#x200B;*reg*&#x200B;的转化量度收集注册数据，则可以选择更改显示名称，使其显示为“注册”。

您无法删除现有的显示名称。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**。

1. 将光标悬停在行上并单击&#x200B;**[!UICONTROL Edit Display Name]**。

1. 输入应显示的名称，然后单击&#x200B;**[!UICONTROL Save]**。

   显示名称必须是唯一的，并且不能包含以下特殊字符： `\"<'>&`

## 更改营销活动管理视图、自定义目标和自定义报表中可用的转化量度 {#change-the-conversion-metrics-available-in-ui}

1. 在主菜单中，单击&#x200B;**[!UICONTROL Settings]>[!UICONTROL Conversions]**。

   将列出为广告商收集的所有转化量度，以及已指定用于显示的任何不同名称。

1. （可选）筛选列表：

   1. 单击列表上方的![筛选器](/help/dsp/assets/filter.png "筛选器")。

   1. 指定筛选器，然后单击&#x200B;**[!DNL Apply]**。

      您可以按AMO客户端ID、量度在UI中是可见还是隐藏以及按数据源过滤量度。

1. 更改可用于管理视图和报表的转化量度：

   * 要显示度量，请将光标悬停在行上并单击&#x200B;**[!UICONTROL Show in UI and Reports]**。

   * 要隐藏度量，请将光标悬停在行上并单击&#x200B;**[!UICONTROL Hide in UI and Reports]**。

>[!MORELIKETHIS]
>
>* [管理您的营销活动数据视图](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [管理自定义目标](/help/dsp/admin/custom-objectives-manage.md)
