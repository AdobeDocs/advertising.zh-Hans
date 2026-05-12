---
title: 创建可重复使用的受众
description: 了解如何创建可重用受众，这些受众由受众区段和其他保存的受众组成。 可选地使用人工智能辅助的受众代理，方法是在自然语言提示中描述目标受众；该代理会建议第三方区段并构建受众表达式以用作目标或排除项。
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
TQID: https://experienceleague.adobe.com/KhAxVTvMx4yBz3tfDtng3nOur2IodZAFFHMUQM1lKhQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a4b509995f362ed81e00485409b0c729b5130e35
workflow-type: tm+mt
source-wordcount: 1667
ht-degree: 0%

---

# 创建可重复使用的受众

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

您可以保存和管理可重用受众，这些受众是受众区段组，甚至是其他保存的受众，您可以将其用作多个投放位置的定位或排除项。 手动创建受众或使用AI辅助的受众代理，根据您所述的要求，使用您可用的所有第一方和第三方区段生成新的可重用受众。

>[!NOTE]
>
>（DSP将其经过哈希处理的电子邮件ID转换为LiveRamp RampID区段的广告商）未附加到活动、计划或暂停投放位置的第一方RampID区段将会暂停。 该区段在区段列表中标记为“自动暂停”。

## 手动创建可重复使用的受众

1. 在主菜单中，单击&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Create]**。

1. 在[!UICONTROL New Audience]设置中：

   1. 输入唯一的&#x200B;**[!UICONTROL Audience Name]**。

   1. （可选）取消选择&#x200B;**[!UICONTROL Share with all advertisers in my account]**&#x200B;的选项。

      当您共享受众时，该受众将可用作帐户中所有广告商的目标或排除项。 但是，受众中的各个区段仅适用于共享这些区段的用户。 例如，如果您将包含Adobe Analytics区段的受众与未映射到同一[!DNL Analytics]帐户的广告商共享，则该受众不会预览该广告商的区段。 在受众中只会预览对该广告商可用的区段。

   1. 单击&#x200B;**[!UICONTROL Save]**。

1. 单击右侧面板中的&#x200B;**[!UICONTROL Switch to manual mode]**&#x200B;按钮。

   默认选项是AI选项。

1. 构建受众：

   >[!NOTE]
   >
   >构建受众时，右侧面板中更新了[受众规模的详细信息](audience-about.md)

   * 要使用[[!UICONTROL Third Party Segments]、[!UICONTROL First Party Segments]、[!UICONTROL Adobe Segments]、[!UICONTROL Custom Segments]和[!UICONTROL Saved Audiences]选项卡](audience-settings.md)上可用的区段手动创建区段逻辑，请执行以下操作。

      * （可选）搜索区段名称、描述或路径。

        搜索结果包括基于您使用的确切术语的区段。 输入多个术语时，必须找到区段的所有术语。

      * 要添加第一个区段，请在左侧面板中查找该区段，然后选中区段名称旁边的复选框。

      * 要将区段添加到现有区段组，请执行以下操作：

         1. 单击右侧面板中的区段组。

         1. （可选）根据需要将组逻辑更改为&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;或&#x200B;*[!UICONTROL Exclude All]*。

            *[!UICONTROL Exclude All]*&#x200B;不可用于第一个区段组。 对于仅包含排除项的受众，请将此受众构建为&#x200B;*[!UICONTROL Include Any]*，然后在投放位置中，从“排除的受众”菜单中选择该受众。

         1. 在左侧面板中找到新区段，然后选中区段名称旁边的复选框。

            区段组会自动更新为新区段。

      * 要添加新区段组，请执行以下操作：

         1. 单击右侧面板中的&#x200B;**[!UICONTROL + New Group]**。

            1. （可选）根据需要将上一个组与新组之间的逻辑更改为&#x200B;*[!UICONTROL And]*&#x200B;或&#x200B;*[!UICONTROL Or]*。

            1. 在左侧面板中找到新组的区段，并选中区段名称旁边的复选框。

            1. （可选）根据需要将组逻辑更改为&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;或&#x200B;*[!UICONTROL Exclude All]*。

   * 要使用现有受众的区段逻辑，请执行以下操作：

      1. 通过以下任一方式从现有受众复制区段逻辑：

         * 在“所有受众”视图中，将光标悬停在受众行上，然后单击&#x200B;**[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**。

         * 在现有受众的设置中，单击区段逻辑面板顶部的&#x200B;**[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**。

         * 在文本编辑器中，使用字母数字区段ID和[布尔语法](audience-segment-logic-syntax.md)手动创建区段逻辑，并将其复制到剪贴板。

      1. 单击&#x200B;**[!UICONTROL paste in an audience rule to begin building]**，将现有区段逻辑粘贴到输入字段中，然后单击&#x200B;**[!UICONTROL Apply]**。

         >[!NOTE]
         >
         >如果受众已包含任何区段逻辑，则在新的区段逻辑中粘贴将覆盖现有逻辑。

1. 单击&#x200B;**[!UICONTROL Create]**。

## 使用创作AI创建可重用受众

*Beta功能*

*仅支持英语*

>[!NOTE]
>
>此功能处于测试版模式，可能会发生更改。 在创建受众并将其用于投放位置之前，请确保生成的受众表达式表示所需受众。

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

1. 在主菜单中，单击&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Create]**。

1. 在[!UICONTROL New Audience]设置中：

   1. 输入唯一的&#x200B;**[!UICONTROL Audience Name]**。

   1. （可选）取消选择&#x200B;**[!UICONTROL Share with all advertisers in my account]**&#x200B;的选项。

      当您共享受众时，该受众将可用作帐户中所有广告商的目标或排除项。 但是，受众中的各个区段仅适用于共享这些区段的用户。 例如，如果您将包含Adobe Analytics区段的受众与未映射到同一[!DNL Analytics]帐户的广告商共享，则该受众不会预览该广告商的区段。 在受众中只会预览对该广告商可用的区段。

   1. 单击&#x200B;**[!UICONTROL Save]**。

1. 构建受众：

   1. 输入一个或多个提示以描述要包含和排除的受众特征。 若要提交每个提示，请单击![提交提示](/help/dsp/assets/submit-prompt.png "提交提示")。

      有关详细信息，请参阅&quot;[正在编写提示](#writing-prompts)&quot;和&quot;[创建受众简介的最佳实践](#audience-brief-best-practices)&quot;。

      如果适用，代理会建议使用其他区段过滤器，以帮助您创建更有效的受众摘要。 您可以接受或拒绝建议。

      当受众代理找到相关区段时，它根据您的条件创建一个布尔受众表达式。 在查找匹配区段以组合受众之前，它还会要求您审批。 您可以选择忽略请求并继续指定其他受众条件。

   1. 当受众代理呈现足以描述您的受众的受众表达式时，请告知受众代理继续组合受众。

      您可以输入“继续”、“确定”、“确定”、“是”或其他类似词语。 工程师会列出每个特征的所有建议区段（如“Parents”）。 展开任何特征可查看有关为该特征建议的各个区段的详细信息。

   1. （如有必要）指定其他标准。 当受众代理呈现符合所有标准的受众表达式时，请告知受众代理继续组合受众。

      要集合受众，请输入“继续”、“确定”、“是”或其他类似词语。 工程师会列出每个特征的所有建议区段（如“Parents”）。 展开任何特征可查看有关为该特征建议的各个区段的详细信息。

1. 如果您对组合受众感到满意，请单击&#x200B;**[!UICONTROL Create]**&#x200B;以创建指定的受众。

   >[!NOTE]
   >
   >您之后无法使用受众代理编辑受众。 相反，[手动编辑受众表达式](/help/dsp/audiences/reusable-audience-edit.md)。

### 编写提示的基础知识 {#writing-prompts}

<!-- Change heading level for this whole section to fit under AI procedure -->

#### 提示应包含哪些内容？

* 使用清晰的描述性语言描述目标受众。

   * 您可以输入完整的句子，也可以只输入一串特征。 除非为清楚起见，否则不需要标点。

   * 通常，提示不区分大小写。

   * 受众代理可识别最常见的同义词。

* 做到具体，并提供要包含的所有受众特征以及要排除的任何特征的详细信息。 您提供的详细信息越多，您获得满足需求的结果的机会就越大。

* 确定要包括或排除的位置、设备类型和数据提供程序。

* 在保存受众之前，反复提供详细信息以优化您的标准和生成的受众表达式。

* 了解如何通过试验进行提示。

  如果您的提示不清晰，则受众代理将仅请求另一个提示，以便您可以重试。

  受众代理不会自动将生成的受众表达式另存为受众。 您只能通过单击提示区域之外的[!UICONTROL Create]按钮来保存受众，因此您可以撤消不想保留的任何更改。

有关优化受众提示的进一步方法，请参阅[创建受众摘要](#audience-brief-best-practices)的最佳实践。

<!--
Consider starting by asking for what you should include.

you can give thumbs up or down to [what exactly?].

Verify what info is carried over from session to session and what starts from scratch.

-->

#### 在提示中不能包含哪些内容？

* 对现有受众表达式的引用。

* 英语以外的其他语言的文本。

#### 受众代理响应示例以及如何回复

当受众代理需要您做出响应时，您可以使用请求中的关键字或使用通用同义词进行回复。

#### Audience Agent询问您问题

`If you are okay with the proposed expression, I can start searching segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

您的肯定回复：“继续”、“确定”、“确定”、“是”或其他类似词语

您还可以忽略请求并继续指定其他受众条件。

##### 受众代理，要求您从多个选项中进行选择

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

您的回复： `1`、`proceed`、`2`、`maximum reach`等。

您还可以忽略请求并继续指定其他受众条件。

### 创建受众简介的最佳实践 {#audience-brief-best-practices}

受众摘要是一种策略性描述，用于定义营销活动的目标受众。 精心编制的简报可帮助DSP受众代理识别最相关的区段，以汇集您的目标受众。

#### 有效的受众简报的重要组成部分

在您的简介中尽可能加入以下列表中的受众属性类型。 特定于要排除的属性。

<!--
 What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **人口统计**

  包括年龄范围、性别、婚姻状况、家庭组成（家庭规模、子女情况、多代家庭）等属性。

* **社会经济指标**

  通过家庭收入(HHI)范围、教育水平、职业/职称、就业状况和房屋所有权状况建立财政能力。

* **地理参数**

  定义地点范围，包括国家/国家、区域（欧洲、中东和非洲、亚太及北非）、人口密度（城市/郊区/农村）。

* **兴趣和喜好**

  识别激情和偏好设置，例如爱好（运动、艺术、户外活动）、媒体消费模式、品牌亲和力和生活方式活动（旅游、就餐、娱乐）。

* **心理图形**

  捕获心态和价值，包括抱负（寻求地位、自我改进）、核心价值（可持续性、创新、传统）、个性特征（风险承担者、早期采用者）和购买动机。

* **行为信号**

  可观察的操作包括购买行为（购物频率、渠道偏好设置、品牌忠诚度）、在线行为（网站访问、内容参与、社交媒体活动）和离线行为（商店访问、事件出席、成员资格）。

* **市场内意图**

  通过正在研究的产品/服务类别、购买时间表（即时、近期、长期）以及触发购买决策的相关生命周期事件确定购买就绪性。

* **生命阶段**

  当前阶段的理解包括职业发展阶段（学生、入门级、职业生涯中期、高管、退休）、家庭阶段（新婚、新父母、空巢家庭）和人生重大转变。

#### 用于潜在客户活动的结构良好的受众简报示例

以下是促销活动的强大受众简报示例，旨在提高知名度并试用高级套餐订阅服务：

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [关于受众管理](audience-about.md)
>* [受众设置](audience-settings.md)
>* [受众区段逻辑的语法](audience-segment-logic-syntax.md)
>* [可用的第三方数据提供程序](third-party-data-providers.md)
>* [创建和实施自定义区段](custom-segment-create.md)
>* [创建并实施[!UICONTROL CCPA Opt-Out-of-Sale]区段](ccpa-opt-out-segment-create.md)
>* [位置设置](/help/dsp/campaign-management/placements/placement-settings.md)
