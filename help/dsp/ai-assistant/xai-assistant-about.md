---
title: 关于Advertising DSP中的AI助手
description: 了解如何使用DSP AI助手对包和投放位置进行故障诊断、报告和搜索产品使用情况帮助。
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
source-git-commit: 8bab50fe8bf737d208d059d89b2592e16bc40c69
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%
---
# 关于Advertising DSP中的AI助手

DSP中的AI助手是一个对话界面，可让您从单个聊天盒执行DSP中可用的任何代理工作流。 您可以创建新任务，或寻求继续先前任务的帮助。

您的对话历史记录会保留在所有工作流中，每个对话都会自动命名。 您的查询未与其他用户共享。

<!-- Update this:  ![Example of a query and response](/help/dsp/assets/agent-chat-response.png "Example of a query and response") -->

## 支持的工作流

以下工作流可以帮助您更有效地完成工作：

<!-- And links to all sections/pages -->

| 功能 | 描述 | 示例查询 | 响应 |
| --- | --- | --- | --- |
| [疑难解答](troubleshooting-agent.md) | 诊断选定实时包或投放位置的性能和投放问题。<ul><li>仅限投放位置：诊断过度支出、支出不足和支出失败。 代理会评估相关的步调、竞价、定位和预算限制因素。</li><li>仅限包：诊断性能问题，包括CPA上升或ROAS下降。 代理不会诊断参与量度，例如CTR、CPC、点击次数或展示次数。</li></ul>每个对话都涵盖针对一个包或投放位置的一个诊断。 收到结果后，启动新对话以诊断另一个问题、包或位置。<br><br>代理无法更改设置，也无法创建或编辑营销活动或营销活动组件。 它也无法诊断已暂停、已完成、已存档或已计划的包或投放位置。 | 配售支出问题：<ul><li>尽管交易很活跃，但我的配售昨天停止了支出。 为什么？</li><li>为什么在过去5天里，此次配售的支出一直偏低？</li><li>我们飞行已经过半，步调明显落后。 为什么？</li></ul>包性能问题：<ul><li>为什么此程序包的CPA在上周有所增加？</li><li>为什么ROAS拒绝此包？</li></ul> | 响应中包含限制性能的因素，并提供解决问题的建议。 |
| [分析](insights-agent.md) | 无需手动创建报告即可获取促销活动量度和完整报告。 您可以询问有关特定量度的简单问题，如促销活动的支出或CPA，或询问有关特定维度（如单个促销活动、投放位置或受众）或跨维度（按促销活动和广告商进行划分）的更复杂报表。 可以将结果下载为CSV文件。 | <ul><li>[促销活动名称]上周花费了多少？<li>[促销活动名称]本月进行了多少次转化？</li><li>哪些职位安排落后于步伐20%以上？</li></li>按包显示[促销活动名称]的CPA</li></ul> | 显示报告的前几行，其中包含预览完整报告以及以[!DNL Microsoft Excel]逗号分隔值文件(.csv)格式下载报告的链接。 |
| [产品文档搜索](documentation-search.md) | 在[Advertising DSP指南](/help/dsp/home.md)中搜索概念内容和操作方法内容，在使用Advertising Creative的广告商中搜索[Advertising Creative指南](/help/creative/home.md)。 答案仅基于[Experience League](https://experienceleague.adobe.com/en/docs/advertising)中记录的这些产品的内容。<br><br>询问有关促销活动管理、优化、受众管理、交易、报告及其他产品功能的信息。 | <ul><li>如何将广告附加到投放位置？</li><li>Adobe DSP中有哪些定位选项可用？</li><li>在投放设置中使用不同的步调选项会有什么后果？</li><li>哪些报表包含家庭级别的数据？</li><li>如何为[!DNL Creative]体验创建广告标记？</li></ul> | 响应包括内联引用和底部的可扩展[!UICONTROL Documentation Sources]列表。 单击任意引文或源列表以打开相关页面。<br><br>响应可能还包括后续问题和建议，以帮助您优化查询和查找更多信息。 |

## 打开AI助手 {#ai-assistant-open}

* 单击任意页面右上角的![代理聊天](/help/dsp/assets/agent-chat.png "代理聊天")。

## 展开聊天盒

1. 在[聊天盒](#ai-assistant-open)的顶部，单击![进入全屏](/help/dsp/assets/fullscreen.png "进入全屏")以进入全屏模式。

1. 若要将聊天盒返回到面板模式，请单击&#x200B;**[!UICONTROL < Back>]**。

<!-- 

No ability to narrow down list of child entities for a selected parent as of 10/26/26.

## Submit a query {#query-submit}

1. [Open AI Assistant](#ai-assistant-open).

1. Build the query:

   * To see examples of queries by topic and optionally copy one to use:
   
     1. Click **[!UICONTROL Learn]**, **[!UICONTROL Troubleshoot]**, or **[!UICONTROL Insights]** to expand the section.
     
     1. (Optional) To copy the text of an example query into the input field:
     
        1. Click the example.
        
        1. (Optional) Edit the text to suit your needs. 

   * To enter your own query:
   
     1. (Insights and troubleshooting queries only; optional) To focus your query on a specific dimension value, such as a specific campaign, click ![Mention an entity](/help/dsp/assets/prompt-entity.png "Mention an entity"), select the dimension, and then select the dimension value.
     
        For example, for the dimension [!UICONTROL Campaign], you can select from a list of all your campaigns to report on.
        
        Available dimensions include:
        
        * Campaign entities: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
        * The advertiser: [!UICONTROL Advertiser]
        * Advertising Creative entities: [!UICONTROL Experience]
        * Ad targets: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

     1. Enter your query, and then click ![Submit query](/help/dsp/assets/submit.png "Submit query") or press the **Enter** key on your keyboard.
        
   You can ask multiple questions in one message, but only one message at a time. Wait for a response before sending another.

   >[!NOTE]
   >
   >* (Troubleshooting and insight queries) If you don't specify a date range, then the agent selects a reasonable default based on the type of issue. For example, if you ask about campaign metrics without specifying a date range, then the results are for the duration of the campaign.
   >* (Troubleshooting queries) If you have a target CPA in mind, then include it in your query (for example, "diagnose CPA against a target of $50"). If you don't specify one, then the agent uses a default target.

1. If AI Assistant asks for additional information, provide it.

1. (Product documentation queries only; optional) To open a page used as a data source for the response, do either of the following:

   * Click the numbered citation.

   * Click **[!UICONTROL Documentation Sources]** to show a list of all pages cited in the response, and then click the page link.

>[!IMPORTANT]
>
>AI-generated responses may be inaccurate or misleading. Always verify responses and sources before using them for decisions that affect cost or effort.

>[!TIP]
>
>To ask another query that you want to be saved as a separate thread, [start a new conversation](#conversation-new).

## (Insight queries) Download or preview a full report from the chatbox

* To download a copy of the full report, click ![Export](/help/dsp/assets/download.png "Export").

   The file is downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

* To preview the full report in a side panel, click ![Preview](/help/dsp/assets/agent-chat-preview.png "Preview"). To download the report from the preview, click ![Export](/help/dsp/assets/download.png "Export").

   If you download the report, it's downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

## Start a new conversation {#conversation-new}

Each conversation, or query thread, is saved separately so you can distinguish between your previous conversations.

1. At the top of the [chatbox](#ai-assistant-open), click ![Start a new conversation](/help/dsp/assets/new-selection.png "Start a new conversation").

1. [Submit a query](#query-submit).

 -->

<!--

## Work with previous conversations

### List previous conversations

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

### Open a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Click the conversation entry.

To repeat the same topic verbatim, copy the key details into a new conversation. Otherwise, you can ask AI Assistant to repeat a finite task within a specific conversation.

### Rename a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Next to the conversation entry, click **[!UICONTROL ...] > [!UICONTROL Rename]**.

1. Edit the conversation name, and then click **[!UICONTROL Save]**.

-->

## 编写查询和提示的最佳实践 {#writing-queries}

* **清晰明确**。 使用完整的问题（“如何订阅按需清单？”）、任务短语（“订阅按需清单”）或主题短语（“按需清单”）。

* **不要在同一查询中组合不同类型的请求**，除非您希望它们存储在同一对话中。

* **相关时包含日期范围**&#x200B;以缩小所需数据的范围。

* 尽可能与产品功能（如“促销活动”或“交易”）的UI术语&#x200B;**匹配**。

  对于常见操作（如“添加”、“附加”或“分配”），您可以使用同义词。

* **添加详细信息**&#x200B;以缩小或扩大结果。 根据需要通过跟进问题进行优化。

* **不要担心标点符号和大小写**，除非它们会影响含义。

>[!MORELIKETHIS]
>
>* [使用AI助手创建报告](insights-agent.md)
>* [使用AI助手排查性能和投放问题](troubleshooting-agent.md)
>* [创建可重复使用的受众](/help/dsp/audiences/reusable-audience-create.md)
>* [使用AI助手搜索产品文档](documentation-search.md)
>* [处理以前的AI助手对话](previous-conversations.md)
