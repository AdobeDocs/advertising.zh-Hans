---
title: 从Adobe Analytics [!DNL eVars] 和prop创建转化指标
description: 使用 [!DNL eVar]和 [!DNL prop]级别的数据配置自定义成功事件量度。
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
TQID: https://experienceleague.adobe.com/DRwNcYJ4-tv6CWhaIHc-qZ-xNsM8sSqoSNkG8AaYI2c
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
  - id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2:
  - id: cfd751d4-ee56-4323-8fd1-dc174b031709
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 0%

---

# 从Adobe Analytics [!DNL eVars]和[!DNL props]创建转化指标

*仅集成Adobe Advertising-Adobe Analytics的广告商*

您可以使用成功事件量度根据DSP网站数据优化最符合您的品牌目标的Adobe Analytics包以及Search、Social和Commerce促销活动。 通过将[[!DNL Analytics] [!DNL eVars]和](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=zh-Hans)级别的数据导入事件，您可以根据现有[[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html?lang=zh-Hans)和[!DNL eVar]&#x200B;[!DNL prop]配置自定义成功事件量度。 其他[!DNL Analytics]指标，包括标准、自定义和保留的转化指标以及流量指标，可在DSP和Search、Social及Commerce中自动使用。

![使用示例](/help/integrations/assets/a4adc-conversion-evar-example.jpg "使用示例")

以下大多数任务必须由[!DNL Analytics]管理员或其他用户执行。 如果您需要帮助，请联系您的Adobe客户团队。

1. 在[!DNL Analytics]中，[创建占位符成功事件](https://experienceleague.adobe.com/zh-hans/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-event)。

   使用以下附加参数：

   **类型：** `Counter`

   **极性：** `Up is Good`或`Up is Bad`

   **可见性：** `Visible Everywhere`

   **独特事件录制：** `Always Record Event`

   **参与率：** `Enabled`

   您无需在品牌网站上实施新事件，因为它使用已捕获的现有数据。

1. 在[!DNL Analytics]中创建并验证处理规则：

   >[!NOTE]
   >
   >只有[!DNL Analytics]帐户管理员可以创建处理规则，除非他们已授予非管理员权限。

   1. [使用以下配置创建处理规则](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=zh-Hans)：

      * 对于必须满足的条件，请指定所需的[!DNL eVars]或[!DNL props]。

        您可以根据需要配置其他级别的粒度，以确保创建最准确的事件。

        >[!TIP]
        >
        >最佳做法是只使用一个[!DNL eVar]或[!DNL prop]。

      * 对于操作，选择&#x200B;**设置事件**&#x200B;并选择占位符事件。

   1. 在[!DNL Analytics] [!DNL Analysis Workspace]中，[创建一个项目](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=zh-Hans)并将新事件提取到自由格式表中，以确保为[!DNL eVar]或[!DNL prop]指标填充数据。

1. 请联系您的Adobe客户团队，以将新量度同步到Adobe Advertising。

量度可用后，您可以使用该量度创建目标，然后可以将该目标分配给Search、Social和Commerce项目组合，或用作DSP包的[自定义目标](/help/dsp/optimization/custom-goal.md)。

有关创建目标的更多信息，请参阅有关“目标”的“优化指南”一章，该章可从“搜索”、“社交”和“Commerce”中获取

>[!MORELIKETHIS]
>
>* Adobe Advertising中的[[!DNL Analytics] 数据](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [查看为广告商跟踪的转化量度](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
