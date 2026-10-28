---
title: 使用AI助手排查性能和投放问题
description: 使用Adobe Advertising DSP AI Assistant的故障排除代理诊断DSP包和投放的支出、步调和投放问题。
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
source-wordcount: '808'
ht-degree: 0%
---
# 使用AI Assistant排查性能和投放问题

*Beta功能*

*仅支持英语*

AI Assistant的故障排除代理可识别限制实时包和投放位置的性能的因素，并根据历史数据提供分步说明和建议，以解决问题。 故障排除代理可帮助诊断以下类型的性能和传递问题：

* （仅限置入）支出问题，包括过度支出、支出不足和无法支出。 代理在诊断过程中会评估相关的步调、竞价、定位和预算上限因素。

* （仅限包）性能问题，包括CPA上升或ROAS下降。 代理不会诊断参与量度，例如CTR、CPC、点击次数或展示次数。

每个对话都涵盖单个包或投放位置的单个诊断。 代理提交结果后，即开始新的对话以询问其他问题，或关于其他包或投放位置。

代理无法更改设置、创建或编辑营销活动或营销活动组件，也无法诊断已暂停、已完成、已存档或计划软件包或投放位置的问题。

>[!IMPORTANT]
>
>AI生成的响应可能不准确或具有误导性。 在将响应和来源用于影响成本或工作量的决策之前，请务必对其进行验证。

## 示例查询

### 排查置入支出问题

* 尽管交易很活跃，但我的配售昨天停止了支出。 为什么？

* 为什么在过去5天里，此次配售的支出一直偏低？

* 我们飞行已经过半，步调明显落后。 为什么？

### 包性能问题疑难解答

* 为什么此程序包的CPA在上周有所增加？

* 为什么ROAS拒绝此包？

## 从AI助手提交查询

您可以在一封邮件中询问多个问题，但一次只能询问一封邮件。 等待响应后再发送另一个响应。

1. 单击任意页面右上角的![代理聊天](/help/dsp/assets/agent-chat.png "代理聊天")。

1. 构建查询：

   * 输入您自己的查询。

   * 要查看查询示例，请单击&#x200B;**[!UICONTROL Troubleshoot]**&#x200B;展开部分。

     1. （可选）要将示例查询的文本复制到输入字段中，请执行以下操作：

        1. 单击示例。

        1. （可选）根据您的需要编辑文本。

   有关查询的详细信息，请参阅“[编写查询和提示的最佳实践](ai-assistant-about.md#writing-queries)”。

   >[!NOTE]
   >
   >* 如果您未指定日期范围，代理将根据问题类型选择合理的默认值。 例如，如果您在不指定日期范围的情况下询问促销活动量度，则结果会反映促销活动的持续时间。
   >* 如果您考虑目标CPA，请将其包含在查询中（例如，“针对目标金额为$50美元诊断CPA”）。 如果未指定目标，则代理将使用默认目标。

1. 单击![提交查询](/help/dsp/assets/submit-prompt.png "提交查询")或按键盘上的&#x200B;**Enter**&#x200B;键。

1. 如果AI助手需要其他信息，请提供。

>[!TIP]
>
>若要询问其他问题，或者关于其他包或投放位置，[开始一个新对话](#conversation-new)。

## 从[!UICONTROL Packages]或[!UICONTROL Placements]视图提交查询

您可以在一封邮件中询问多个问题，但一次只能询问一封邮件。 等待响应后再发送另一个响应。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击营销活动的名称。

1. 执行以下任一操作：

   * （对于包）在[!UICONTROL Packages]视图中，单击包名称旁边的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**。

   * （对于版面）在子菜单中，单击&#x200B;**[!UICONTROL Placements]**。 在投放位置名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**。

1. 构建查询：

   * 输入您自己的查询。

   * 要查看查询示例，请单击&#x200B;**[!UICONTROL Troubleshoot]**&#x200B;展开部分。

     1. （可选）要将示例查询的文本复制到输入字段中，请执行以下操作：

        1. 单击示例。

        1. （可选）根据您的需要编辑文本。

   有关查询的详细信息，请参阅“[编写查询和提示的最佳实践](ai-assistant-about.md#writing-queries)”。

   >[!NOTE]
   >
   >* 如果您未指定日期范围，代理将根据问题类型选择合理的默认值。 例如，如果您在不指定日期范围的情况下询问促销活动量度，则结果会反映促销活动的持续时间。
   >* 如果您考虑目标CPA，请将其包含在查询中（例如，“针对目标金额为$50美元诊断CPA”）。 如果未指定目标，则代理将使用默认目标。

1. 单击![提交查询](/help/dsp/assets/submit-prompt.png "提交查询")或按键盘上的&#x200B;**Enter**&#x200B;键。

1. 如果AI助手需要其他信息，请提供。

>[!TIP]
>
>若要询问其他问题，或者关于其他包或投放位置，[开始一个新对话](#conversation-new)。

## 开始新对话 {#conversation-new}

每个对话（或查询线程）单独保存，以便您能够区分以前的对话。

1. 在[聊天盒](#ai-assistant-open)的顶部，单击![开始新对话](/help/dsp/assets/new-selection.png "开始新对话")。

1. [提交查询](#query-submit)。

## 展开并最小化聊天盒

1. 在[聊天盒](#ai-assistant-open)的顶部，单击![进入全屏](/help/dsp/assets/fullscreen.png "进入全屏")以进入全屏模式。

1. 若要将聊天盒返回到面板模式，请单击&#x200B;**[!UICONTROL < Back>]**。

>[!MORELIKETHIS]
>
>* [关于Advertising DSP中的AI助手](ai-assistant-about.md)
>* [处理以前的AI助手对话](previous-conversations.md)
