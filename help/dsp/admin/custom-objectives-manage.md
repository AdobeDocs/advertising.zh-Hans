---
title: 管理自定义目标
description: 了解如何定义帮助您实现包级别优化目标的成功事件。
role: User, Admin
feature: DSP Optimization, DSP Packages
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '1312'
ht-degree: 0%

---

# 管理自定义目标

*适用于链接到Search、Social和Commerce帐户的DSP帐户*

目标定义广告商为实现其业务目标而设置的成功事件。 目标可作为[自定义目标](/help/dsp/campaign-management/packages/package-settings.md)用于DSP包。 每个使用优化目标“[!UICONTROL Highest Return on Ad Spend (ROAS)"]”或“[!UICONTROL Lowest Cost per Acquisition (CPA)]”的包都必须包含一个自定义目标，以帮助实现整体优化目标。

目标由要跟踪和优化的量度（属性）以及这些量度的相对权重组成。 每个目标可以包括：

* **[!UICONTROL Goal]个量度**，这些量度表示广告商的主要成功量度。 它们通常包括包的核心业务成果，如Revenue 、 Leads或Sales。 每个目标必须具有至少一个目标量度。

* 可选&#x200B;**[!UICONTROL Assist]个量度**，这些量度可协助、预测、优先于或有助于推动目标量度。 示例包括参与量度，如测试驱动和试用。

  您可以让[!DNL Adobe AI]自动分配和更新加权协助事件，以最大限度地提高您的目标事件。 如果您希望分配自己的加权协助量度，DSP可以选择根据Adobe Advertising和Adobe Analytics中的过去性能数据推荐协助量度。 您可以选择是否应用推荐。

对目标选项的所有更改都将在字段级别进行跟踪，并列在更改日志中。

>[!PREREQUISITES]
>
>在创建目标之前，必须将DSP帐户链接到具有相同Adobe Experience Cloud组织ID的Search、Social和Commerce帐户，即使您不是Search、Social和Commerce客户。 如果您的DSP帐户未关联到[!DNL Search, Social, & Commerce]帐户，请联系您的Adobe帐户团队。

>[!NOTE]
>
>* Advertising Search、Social和Commerce也使用目标。 每个“搜索”、“社交”和“Commerce”项目组合都必须有一个目标，以便优化功能可以为该项目组合创建点击和收入模型。
>* 您可以对多个DSP包和/或多个搜索、Social和Commerce项目组合使用同一目标。

## 可用量度

您可以在目标中包含以下任意内容：

* Adobe Advertising使用[Adobe Advertising转化跟踪像素](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)跟踪的指标。

* （具有[!DNL Adobe Analytics for Advertising]的广告商） [转化和网站参与度量度已从Adobe Analytics](/help/integrations/analytics/overview.md)同步。

<!-- Do DSP-only clients have these? * [Advertiser-tracked metrics from conversion feed files](/help/search-social-commerce/tracking/conversion-tracking-about.md).  -->

## 目标状态

[!UICONTROL Settings] > [!UICONTROL Custom Objectives]视图指示每个目标的状态。 值可以包括：

* *[!UICONTROL Waiting]*：在生成推荐之前，目标处于草稿状态。

* *[!UICONTROL Active]*：目标已保存并可用。

## 推荐状态

* *[!UICONTROL Not Initiated]*：未请求推荐。

* *[!UICONTROL Generating]*：正在生成推荐。

* *[!UICONTROL Ready]*：建议可供应用。

* *[!UICONTROL Error]*：无法生成推荐。

## 创建目标

1. 在主菜单中，单击&#x200B;**[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**。

1. 单击右上角的&#x200B;**[!UICONTROL Create]**。

1. 输入[目标设置](#custom-objective-settings)。

   当您选择自动竞价时，可以将属性（量度）作为&quot;[!UICONTROL Goal]&quot;量度分配给目标。 对于自定义竞价，您可以将属性分配为“[!UICONTROL Goal]”或加权的“[!UICONTROL Assist]”量度，但必须至少包含一个目标量度。

   目标和辅助标签不会影响优化。 只有所包含量度的权重会影响优化。

1. （带有自定义竞价的目标；可选）要根据过去的性能数据生成推荐的协助量度，请单击底部部分的&#x200B;**[!UICONTROL Generate]**。 在&#x200B;**[!UICONTROL Generate Recommendation]**&#x200B;中，单击&#x200B;**[!UICONTROL Generate]**。

   建议的量度最多需要20分钟才能生成。 在生成推荐时，自定义目标的状态为&#x200B;*[!UICONTROL Waiting]*。 生成推荐后，您可以“[查看并应用推荐的协助事件](#view-apply-recommendations)”。

1. （如果未生成推荐）在右上角，单击&#x200B;**[!UICONTROL Save]**。

在使用优化目标“[!UICONTROL Highest Return on Ad Spend (ROAS)"]”或“[!UICONTROL Lowest Cost per Acquisition (CPA)]”的包的[DSP包设置](/help/dsp/campaign-management/packages/package-settings.md)中，目标名称现已包含在[!UICONTROL Custom Goals]列表中。 当您选择目标作为包的自定义目标时，[!UICONTROL Conversion Metric]列表包括该目标的所有目标量度。

## 编辑目标

1. 在主菜单中，单击&#x200B;**[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**。

1. 在行中，单击&#x200B;**...*** > **[!UICONTROL Edit]**。

1. 更改任何[目标设置](#custom-objective-settings)。

1. （当建议可用时；可选）查看并（可选）应用建议的量度：

   1. 在底部，单击&#x200B;**[!UICONTROL View Recommendations]**。

   1. 要应用推荐，请执行下列任一操作：

      * 单击推荐旁边的&#x200B;**[!UICONTROL Apply]**。

      * 手动调整推荐，然后单击推荐旁边的&#x200B;**[!UICONTROL Apply]**。

   1. 单击&#x200B;**[!UICONTROL Close]**&#x200B;以关闭[!UICONTROL Recommendations]列表。

   同步目标设置后，更改将生效。

1. （带有自定义竞价的目标；可选）要根据过去的性能数据生成推荐的协助量度，请单击底部部分的&#x200B;**[!UICONTROL Generate]**。 在&#x200B;**[!UICONTROL Generate Recommendation]**&#x200B;中，单击&#x200B;**[!UICONTROL Generate]**。

   建议的量度最多需要20分钟才能生成。 在生成推荐时，自定义目标的状态为&#x200B;*[!UICONTROL Waiting]*。 生成推荐后，您可以“[查看并应用推荐的协助事件](#view-apply-recommendations)”。

1. （如果未生成新推荐）在右上角，单击&#x200B;**[!UICONTROL Save]**。

## 查看并应用建议的协助事件 {#view-apply-recommendations}

*自定义竞价目标*

当目标状态为&#x200B;*[!UICONTROL Active]*&#x200B;且[!UICONTROL Recommendation Status]为&#x200B;*[!UICONTROL Ready]*&#x200B;时，您可以查看推荐，并可以选择应用推荐。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**。

1. 在行中，单击&#x200B;**...*** > **[!UICONTROL Edit]**。

1. 在底部，单击&#x200B;**[!UICONTROL View Recommendations]**。

1. （可选）要应用推荐，请执行以下任一操作：

   * 单击推荐旁边的&#x200B;**[!UICONTROL Apply]**。

   * 手动调整推荐，然后单击推荐旁边的&#x200B;**[!UICONTROL Apply]**。

1. 单击&#x200B;**[!UICONTROL Close]**&#x200B;以关闭[!UICONTROL Recommendations]列表。

1. 单击右上角的&#x200B;**[!UICONTROL Save]**。

   同步目标设置后，更改将生效。

## 查看自定义目标的更改日志

1. 在主菜单中，单击&#x200B;**[!UICONTROL Settings]>[!UICONTROL Custom Objectives]**。

1. 在行中，单击&#x200B;**...*** > **[!UICONTROL Change Log]**。

<!--

Not used as of 2/6. If added, verify and edit:

## Delete an objective

You can delete an objective that's not assigned to a package.

1. In the main menu, click **[!UICONTROL Settings] > [!UICONTROL Custom Objectives]**.

1. In the row, click **...*** > **[!UICONTROL Delete]**.

1. In the confirmation message, click **[!UICONTROL Confirm]**.

-->

## 自定义目标设置 {#custom-objective-settings}

<!-- Are we going to keep the heading "Properties" rather than "Metrics" (or Events, which is mentioned in the UI? Need a consistent naming convention. Ideally, it should be the same as the new SSC UI. -->

| 部分 | 参数 | 描述 |
|---------|-----------|-------------|
| 基本详细信息 | 阿莫克客户端 | 广告商的唯一Adobe Advertising ID。 |
| 基本详细信息 | 目标名称 | 目标的名称。<br><br>Advertising DSP的所有目标名称必须以“ADSP_”（不区分大小写）作为名称的前缀，如“ADSP_Registrations”。 当要将其分配给包时，请使用易于识别的名称。 |
|  | 描述 | （可选）目标的描述。 当您将光标悬停在“自定义目标”列表中的名称上时，将显示说明。 如果不包括描述，则重复目标名称。 |
| 竞价策略 |  | 目标的竞价策略，它确定您可以配置的事件类型：<ul><li><b>[!UICONTROL Automated Bidding]：</b>将属性（量度）作为[!DNL goal]量度分配给目标。 [!DNL Adobe AI]自动分配和更新加权协助事件，以使用平衡funnel方法最大化您的目标事件。</li><li><b>[!UICONTROL Custom Bidding]：</b>通过将属性分配为“[!DNL goal]”或加权的“[!DNL assist]”事件来设置您自己的竞价策略。 将此高级选项用于预定义策略。</li></ul>更改竞价策略会清除所有以前选定的量度。 |
| 属性 | [!UICONTROL Available Metrics] | 为广告商跟踪的所有指标。 要将某个量度添加为目标，请单击该量度名称旁边的<b>[!UICONTROL Goal]</b>。 （仅限[!UICONTROL Custom Bidding]）要添加有助于分配的目标量度的量度，请单击量度名称旁边的<b>[!UICONTROL Assist]</b>。<br><br><b>注意：</b> [!DNL Analytics]自定义事件遵循以下命名约定： `custom_event_[*event #*]_[*Analytics report suite ID*]`。 示例： `custom_event_16_examplersid.` [!DNL Analytics]维度和区段不可用于Adobe Advertising优化。<br><br><b>提示：</b>为获得最佳性能，自定义目标（目标）中的组合量度每天必须至少总计10次转化。 如果不包含，最佳实践是为目标添加其他支持转化量度，如产品页面或应用程序启动次数。 有关准则，请参阅[构建自定义目标的最佳实践](#custom-goal-best-practices)。 |
|  | 选定的量度 | 目标中包含的每个转化量度的名称。 执行以下任一操作：<ul><li>要将某个量度添加为目标，请在[!UICONTROL Available Metrics]列中单击该量度名称旁边的<b>[!UICONTROL Goal]</b>。</li><li>（仅限[!UICONTROL Custom Bidding]策略）要添加有助于分配的目标量度的量度，请在[!UICONTROL Available Metrics]列中单击量度名称旁边的<b>[!UICONTROL Assist]</b>。 然后，输入相对于目标中其他指标的指标的数字权重。 权重必须介于0.001到1之间，并且可以包括小数。 默认权重为1。</li><li>（仅限[!UICONTROL Custom Bidding]策略）要编辑协助量度的权重，请在字段中单击，然后输入该量度相对于目标中其他量度的数字权重。 权重必须大于零(0)，并且可以包含小数。 默认权重为1。</li><li>要从目标中删除量度，请将光标悬停在量度名称上，然后单击&#x200B;**[!UICONTROL X]**。/li></ul>**注释：**<ul><li>确保不同的量度及其权重相对合理。 例如，您不能直接比较计数与美元金额。</li><li>目标权重之间较大的相对变化会引起绩效的暂时波动，因此在变化后对绩效进行监控。</li></ul>. |

>[!MORELIKETHIS]
>
>* [优化目标及使用方法](/help/dsp/optimization/optimization-goals.md)
>* 自定义目标的[最佳点数](/help/dsp/optimization/custom-goal.md)
>* [包设置](/help/dsp/campaign-management/packages/package-settings.md)
>* [管理转化](/help/dsp/admin/conversion-metrics-manage.md)
