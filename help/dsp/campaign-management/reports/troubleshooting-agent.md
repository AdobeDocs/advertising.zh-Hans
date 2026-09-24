---
title: 使用AI助手排查性能和投放问题
description: 了解如何使用AI助理的故障排除代理来诊断DSP包和投放的支出、步调和投放问题。
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
source-git-commit: 2e97652901e16bd1079fac445f9a2a4794dcda56
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%
---
# 使用DSP AI助手排查性能和投放问题

AI助理的故障排除代理可以识别限制性能的因素并提供解决问题的建议。 故障排除代理可以：

* 帮助诊断选定实时包或投放位置的性能和投放问题：

  * （仅限置入）支出问题，包括过度支出、支出不足和无法支出。 代理在诊断过程中会评估相关的步调、竞价、定位和预算上限因素。

  * （仅限包）性能问题，包括CPA上升或ROAS下降。 代理不会诊断参与量度，例如CTR、CPC、点击次数或展示次数。

  每个对话都涵盖单个包或投放位置的单个诊断。 代理提交结果后，即开始新的对话以询问其他问题，或关于其他包或投放位置。

  代理无法更改设置，也无法创建或编辑营销活动或营销活动组件。 它也无法诊断已暂停、已完成、已存档或计划的包或放置的问题。

* 在[Advertising DSP指南](/help/dsp/home.md)和（使用Advertising Creative的广告商）[Advertising Creative指南](/help/creative/home.md)中搜索概念内容和操作方法内容，搜索方式与[代理聊天界面](/help/dsp/agent-chat.md)相同。 您可以询问有关营销活动管理、优化、受众管理、交易、报告和其他产品功能的信息。

>[!IMPORTANT]
>
>AI生成的响应可能不准确或具有误导性。 在将响应和来源用于影响成本或工作量的决策之前，请务必对其进行验证。

## 示例查询

>[!NOTE]
>
>您无需指定日期范围。 如果不包括一个，工程师将根据问题类型选择合理的默认值。

### 投放位置：支出问题

* 尽管交易很活跃，但我的配售昨天停止了支出。 为什么？

* 为什么在过去5天里，此次配售的支出一直偏低？

* 我们飞行已经过半，步调明显落后。 为什么？

### 包：性能问题

* 为什么此程序包的CPA在上周有所增加？

* 为什么ROAS拒绝此包？

>[!TIP]
>
>如果您考虑目标CPA，请将其包含在查询中（例如，“针对目标金额为$50美元诊断CPA”）。 如果未指定目标，则代理将使用默认目标。

### 产品功能：

* 如何创建投放位置？

* Adobe DSP中有哪些定位选项可用？

* 如何将广告附加到投放位置？

* 在投放设置中使用不同的步调选项会有什么后果？

* 何时应使用每种类型的优化目标？

* 为什么程序化保证(PG)投放位置不提供展示次数？

* 哪些报表包含家庭级别的数据？

* 在[!DNL Creative]中，目标体验与非目标体验有何区别？

* 如何为[!DNL Creative]体验创建广告标记？

## 提交实时包或投放位置的查询

您可以在一封邮件中询问多个问题，但一次只能询问一封邮件。 等待响应后再发送另一个响应。

1. 在主菜单中，单击&#x200B;**[!UICONTROL Campaigns]**。

1. 单击营销活动的名称。

1. 执行以下任一操作：

   * （对于包）在[!UICONTROL Packages]视图中，单击包名称旁边的&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**。

   * （对于版面）在子菜单中，单击&#x200B;**[!UICONTROL Placements]**。 在投放位置名称旁边，单击&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**。

1. 输入查询并单击![提交提示](/help/dsp/assets/submit-prompt.png "提交提示")。

   <!-- For more information, see "[Writing prompts](#writing-prompts)." -->

   对于性能和投放查询，响应将包含限制性能的因素，并提供解决问题的建议。

   对于文档查询，响应包含内联引用和底部的&#x200B;**[!UICONTROL Documentation Sources]**&#x200B;列表。 后续问题和建议也可能出现。

1. （仅限文档查询；可选）要打开用作数据源的页面，请执行以下任一操作：

   * 单击编号的引文。

   * 单击&#x200B;**[!UICONTROL Documentation Sources]**&#x200B;以显示响应中引用的所有页面的列表，然后单击页面链接。

1. （可选）使用向上缩略图或向下缩略图图标对响应进行评级。

>[!TIP]
>
>要询问其他问题，或者关于其他包或投放位置，请启动新对话。
