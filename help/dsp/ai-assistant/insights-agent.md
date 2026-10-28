---
title: 使用AI助手创建报告
description: 了解如何使用Adobe Advertising DSP AI Assistant的分析代理查询促销活动量度、生成报表和下载CSV文件。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 0f6d32b5409cc95f09d0b0f28cdeee72a7861892
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%
---
# 使用AI助手创建报告

*Beta功能*

*仅支持英语*

使用AI助手的分析代理获取营销活动、营销活动组件、Advertising Creative体验、广告商和广告目标的量度和完整报表，而无需手动创建报表。 您可以询问有关特定量度的简单问题，例如营销活动的支出或CPA，或针对特定维度（例如单个营销活动或受众）或跨维度（每个营销活动和广告商的细分）请求更复杂的报表。 可以将结果下载为CSV文件。

>[!IMPORTANT]
>
>AI生成的响应可能不准确或具有误导性。 在将响应和来源用于影响成本或工作量的决策之前，请务必对其进行验证。

## 示例查询

* [促销活动名称]上周花费了多少？

* [促销活动名称]本月进行了多少次转化？

* 按包显示[促销活动名称]的CPA。

* 哪些职位安排落后于步伐20%以上？

* 比较过去15天所有营销活动和资源包的净支出。

## 提交查询

您可以在一封邮件中询问多个问题，但一次只能询问一封邮件。 等待响应后再发送另一个响应。

1. 单击任意页面右上角的![代理聊天](/help/dsp/assets/agent-chat.png "代理聊天")。

1. 构建查询：

   1. 执行以下任一操作：

      * 输入您自己的查询。

      * 要查看查询示例，请执行以下操作：

        1. 单击&#x200B;**[!UICONTROL Insights]**&#x200B;展开该部分。

        1. （可选）要将示例查询的文本复制到输入字段中，请执行以下操作：

           1. 单击示例。

           1. （可选）根据您的需要编辑文本。

   1. （可选）要将查询焦点放在特定维度值（如特定营销活动）上，可以选择在要显示维度值的位置插入光标，单击![提及实体](/help/dsp/assets/prompt-entity.png "提及实体")，选择维度，然后选择维度值。

      例如，对于维度[!UICONTROL Campaign]，您可以从要报告的所有营销活动的列表中选择项。

      可用的维度包括：

      * 营销活动实体： [!UICONTROL Campaign]、[!UICONTROL Package]、[!UICONTROL Placement]、[!UICONTROL Ad]
      * 广告商： [!UICONTROL Advertiser]
      * Advertising Creative实体： [!UICONTROL Experience]
      * 广告目标： [!UICONTROL Audience]、[!UICONTROL City]、[!UICONTROL Country]、[!UICONTROL State]、[!UICONTROL DMA]、[!UICONTROL Retargeting Pixel]、[!UICONTROL Device OS]、[!UICONTROL Device Browser]、[!UICONTROL Device Type]、[!UICONTROL Zip Code]

   有关查询的详细信息，请参阅“[编写查询和提示的最佳实践](ai-assistant-about.md#writing-queries)”。

1. 单击![提交查询](/help/dsp/assets/submit-prompt.png "提交查询")或按键盘上的&#x200B;**Enter**&#x200B;键。 如果代理请求其他信息，请提供所需信息。

   将显示报告的前几行，其中包含用于预览完整报告和下载报告的链接。

   将显示所生成报告的几行。

>[!TIP]
>
>若要询问其他问题，或者关于其他包或投放位置，[开始一个新对话](#conversation-new)。

## 从聊天盒下载或预览完整报告

* 要下载完整报告的副本，请单击![导出](/help/dsp/assets/download.png "导出")。

  根据浏览器的正常过程，该文件将下载为[!DNL Microsoft Excel]个逗号分隔值文件(.csv)。 文件名为“DSP_Insights_Report_&lt;job_number>”。

* 要在侧面板中预览完整报告，请单击![预览](/help/dsp/assets/agent-chat-preview.png "预览")。 要从预览中下载报告，请单击![导出](/help/dsp/assets/download.png "导出")。

  如果您下载报表，则它是作为一个[!DNL Microsoft Excel]逗号分隔值文件(.csv)按照浏览器的正常过程进行下载的。 文件名为“DSP_Insights_Report_&lt;job_number>”。

## 开始新对话 {#conversation-new}

每个对话或查询线程将单独保存，以便您能够区分以前的对话。

1. 在[聊天盒](#ai-assistant-open)的顶部，单击![开始新对话](/help/dsp/assets/new-selection.png "开始新对话")。

1. [提交查询](#query-submit)。

## 展开并最小化聊天盒

1. 在[聊天盒](#ai-assistant-open)的顶部，单击![进入全屏](/help/dsp/assets/fullscreen.png "进入全屏")以进入全屏模式。

1. 若要将聊天盒返回到面板模式，请单击&#x200B;**[!UICONTROL < Back>]**。

>[!MORELIKETHIS]
>
>* [关于Advertising DSP中的AI助手](ai-assistant-about.md)
>* [处理以前的AI助手对话](previous-conversations.md)
