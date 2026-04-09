---
title: 管理广告商的转化量度
description: 了解如何将Adobe Advertising跟踪的转化量度用于广告商。
feature: Conversions
source-git-commit: ba96414b7104192d36d62842f52f73a5850190f9
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# 管理广告商的转化量度

广告商的[转化](/help/search-social-commerce/glossary.md#c-d)量度在整个Adobe Advertising中使用：

* 在“搜索”、“社交”和“Commerce”中，转化指标的数据可显示在营销活动、项目组合和目标管理视图以及报表的列中。 具有足够访问权限的用户还可以使用转化量度创建目标，以优化项目组合。

* （使用Advertising DSP的广告商）在DSP中，您可以在营销活动管理视图、自定义目标和自定义报表中包含转化量度。 您还可以使用转化量度来创建用于优化包的[自定义目标](/help/dsp/optimization/custom-goal.md)。

可用的量度包括：

* Adobe Advertising跟踪广告商的转化量度。

* [转化和网站参与度量度已从Adobe Analytics同步](/help/integrations/analytics/analytics-data-in-advertising.md)。

* 从Adobe Customer Journey Analytics[同步的](/help/integrations/customer-journey-analytics/overview.md)网站事件。

* [!DNL Google Ads]跟踪的转化和[!DNL Microsoft Advertising]通用事件跟踪标记跟踪的转化。

* （当[您已配置特定 [!DNL Google Analytics] 帐户、属性和视图组合作为搜索、社交和Commerce的数据源](/help/search-social-commerce/admin/data-sources/data-source-about.md)时） [!DNL Google Analytics]所跟踪的转化。

* 来自自定义馈送的转化。

从可用的转化量度列表中，每个有权访问广告商数据的用户都可以自定义他们看到的可用于管理视图和报表的量度，包括或忽略他们选择的特定量度。 您可以使用与检索数据中拼写完全相同的量度名称，也可以更改列标题中显示的名称以提高可读性。

>[!IMPORTANT]
>
>默认情况下，广告商的转化量度（由[!DNL Google Ads]、[!DNL Google Analytics]和[!DNL Microsoft Advertising]通用事件跟踪标记跟踪的转化除外）均不可包含在营销活动和项目组合管理视图、目标和报告中。 要使转化量度可用，您必须明确使其可用。
>
>由[!DNL Google Ads]、[!DNL Google Analytics]和[!DNL Microsoft Advertising]通用事件跟踪标记跟踪的新转化始终自动可用。

>[!TIP]
>
>一旦广告商（或广告网络）停止收集转化量度，[将其从管理视图和报告中隐藏](#conversion-metrics-change-available)，除非您想要将其用于查看历史数据。

## 查看为广告商跟踪的转化量度

* 在主菜单中，单击&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversions]**。

将列出为广告商收集的所有转化量度以及为其分配的任何不同的显示名称。 每个量度行都包含量度的源。

## 更改转化量度的显示名称

例如，如果您使用名为&#x200B;*reg*&#x200B;的转化量度收集注册数据，则可以选择更改显示名称，使其显示为“注册”。

您无法删除现有的显示名称。

>[!NOTE]
>
>对于来自[的 [!DNL Google Analytics]](/help/search-social-commerce/admin/data-sources/data-source-about.md)个量度，如果更新或重新验证集成，则会覆盖对显示名称所做的任何手动更改。 同样，除非您[!DNL Google Analytics]更新[或](/help/search-social-commerce/admin/data-sources/data-source-edit.md)重新验证[集成，否则将忽略](/help/search-social-commerce/admin/data-sources/data-source-reauthenticate.md)中的任何名称更改。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversions]**。

1. 在度量的&#x200B;**[!UICONTROL Conversion Display Name]**&#x200B;列中，将光标悬停在度量名称上，然后单击&#x200B;**...** > **[!UICONTROL Rename]**。

1. 输入应显示的名称，然后单击&#x200B;**[!UICONTROL Apply]**。

   显示名称必须是唯一的，并且不能包含以下特殊字符： `\"<'>&`

## 更改管理视图、目标和报告中可用的转化量度 {#conversion-metrics-change-available}

>[!NOTE]
>
>当您隐藏以前可用的转化量度时，它会从包含该转化量度的任何派生量度中删除。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Goals]>[!UICONTROL Conversions]**。

   将列出为广告商收集的所有转化量度，以及已指定用于显示的任何不同名称。

1. （可选）从工具栏[或](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)列标题[筛选列表](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)。

1. 更改可用于管理视图和报表的转化量度：

   * 要显示或隐藏单个量度，请单击&#x200B;**[!UICONTROL Visibility]**&#x200B;列中的开关以更改设置。

   * 要显示或隐藏多个量度，请执行以下操作：

      1. 选中每个转化量度旁边的复选框。

         有关选择多行的提示，请参阅“[选择多行](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)”。

      1. 在批量操作工具栏中，单击![可见性](/help/search-social-commerce/assets/visible.png "可见性")可显示量度，单击![可见性关闭](/help/search-social-commerce/assets/visibility-off.png "可见性关闭")可隐藏量度。

      1. （要隐藏量度）在确认消息中，单击&#x200B;**[!UICONTROL Confirm]**&#x200B;可隐藏量度，包括从包含这些量度的任何派生量度中删除这些量度。

>[!MORELIKETHIS]
>
>* 
