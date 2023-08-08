---
title: 从Adobe Analytics eVar和prop创建转化量度
description: 使用eVar和prop级别的数据配置自定义成功事件量度。
feature: Integration with Adobe Analytics, Conversions
source-git-commit: d4f439ad23fc386bc85d95cc1291ec668ecf1cd2
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# 从Adobe Analytics eVar和prop创建转化量度

*仅具有Adobe Advertising-Adobe Analytics集成的广告商*

您可以使用成功事件量度根据Adobe Analytics网站数据优化DSP包以及搜索、社交和商务促销活动，以最符合您的品牌目标。 您可以根据现有配置自定义成功事件量度 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) 和 [prop](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) 将eVar级别和属性级别的数据漏斗到事件中。 其他 [!DNL Analytics] 量度（包括标准、自定义和保留的转化量度以及流量量度）在DSP和Search、Social以及Commerce中自动可用。

![使用示例](/help/integrations/assets/a4adc-conversion-evar-example.jpg "使用示例")

以下大多数任务必须由 [!DNL Analytics] 管理员或其他用户。 如果您需要帮助，请通过以下电子邮件联系(DSP用户) DSP技术支持团队： `adcloud_support@adobe.com` 或（Search、Social和Commerce用户）您的Adobe帐户团队。

1. 在 [!DNL Analytics]， [创建占位符成功事件](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   使用以下附加参数：

   **类型：** `Counter`

   **极性：**  或者 `Up is Good` 或 `Up is Bad`

   **可见性：** `Visible Everywhere`

   **独特事件记录：** `Always Record Event`

   **参与率：** `Enabled`

   您无需在品牌网站上实施新事件，因为它使用已捕获的现有数据。

1. 在中创建处理规则 [!DNL Analytics]：

   >[!NOTE]
   >
   >仅 [!DNL Analytics] 除非已向非管理员授予权限，否则帐户管理员可以创建处理规则。

   1. [创建处理规则](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en)，使用以下配置：

      * 对于必须满足的条件，指定所需的eVar或prop。

        您可以根据需要配置其他级别的粒度，以确保创建最准确的事件。

        >[!TIP]
        >
        >最佳实践为仅使用一个eVar或prop。

      * 对于操作，选择 **设置事件** 并选择占位符事件。

   1. 在 [!DNL Analytics] [!DNL Analysis Workspace]， [创建项目](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) 并将新事件提取到自由格式表中，以确保为eVar或prop量度填充数据。

1. 请联系您的Adobe客户团队，以将新指标同步到Adobe Advertising。

量度可用后，可以使用该量度创建目标，然后可以将该目标分配给搜索、社交和商务项目组合或用作 [自定义目标](/help/dsp/optimization/custom-goal-about.md) 用于DSP包。

有关创建目标的更多信息，请参阅有关“目标”的“优化指南”一章，该章可从“搜索”、“社交”和“商务”中获取。

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Adobe Advertising中的数据](/help/integrations/analytics/analytics-data-in-advertising.md)
<!--
>* [](/help/search-social-commerce/admin/conversion-metrics/ ????????)
-->