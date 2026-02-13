---
title: 使用创作AI创建可重用受众
description: 了解如何使用人工智能辅助的受众代理在Adobe Advertising DSP中创建可重用受众。 以自然语言提示描述您的目标受众；代理会建议第三方区段，并构建受众表达式以用作目标或排除项。
feature: DSP Audiences
hidefromtoc: true
hide: true
exl-id: 82c9f122-2bdd-409f-a4d6-1da21ecbe913
source-git-commit: 4eefcca15d4f84152278e7680917b9daed15f45d
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 0%

---

# 使用创作AI创建可重用受众

*Beta功能*

*仅以英语提示*

<!-- I thought it was all segment types? -->

<!-- Redo the legacy file to include the new info. It's probably cleanest to keep it as two separate procedures (gen AI and manually) rather than one big, long procedure. -->

使用人工智能辅助的受众代理，根据您提出的要求，使用您可用的所有第三方区段生成新的可重用受众。 您可以将受众用作多个投放位置的定位或排除项。

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>此功能处于测试版模式，可能会发生更改。 在创建受众并将其用于投放位置之前，请确保生成的受众表达式表示所需受众。

## 使用创作AI创建可重用受众

1. 在主菜单中，单击&#x200B;**[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**。

1. 在数据表上方，单击&#x200B;**[!UICONTROL Create]**。

1. 输入唯一的&#x200B;**[!UICONTROL Audience Name]**。

1. （可选）取消选择&#x200B;**[!UICONTROL Share with all advertisers in my account]**&#x200B;的选项。

   当您共享受众时，该受众将可用作帐户中所有广告商的目标或排除项。 但是，受众中的各个区段仅适用于共享这些区段的用户。

1. 单击&#x200B;**[!UICONTROL Save]**。

1. 构建受众：

   对于具有测试版权限的用户，默认设置为AI选项。 若要[自行组合受众](/help/dsp/audiences/reusable-audience-create.md)，请单击底部的“切换到手动模式”按钮。

   1. 输入一个或多个提示以描述要包含和排除的受众特征。 若要提交每个提示，请单击![提交提示](/help/dsp/assets/submit-prompt.png "提交提示")。

      有关详细信息，请参阅[编写提示](#writing-prompts)和[创建受众简介的最佳实践](#audience-brief-best-practices)。

      当AI代理查找相关区段时，它根据您的条件创建受众表达式。 在查找匹配区段以组合受众之前，它还会要求您审批。

      您可以选择忽略请求并继续指定其他受众条件。

   1. 当AI代理呈现足以描述您的受众的受众表达式时，请告知AI代理继续组装受众。

      您可以输入“继续”、“确定”、“确定”、“是”或其他类似词语。

   1. （如有必要）指定其他标准。 当AI代理呈现符合所有标准的受众表达式时，告诉AI代理继续组装受众。

1. 如果您对组合受众感到满意，请单击&#x200B;**[!UICONTROL Create]**&#x200B;以创建指定的受众。

   >[!NOTE]
   >
   >您以后无法使用AI代理编辑受众。 相反，[手动编辑受众表达式](/help/dsp/audiences/reusable-audience-edit.md)。

## 编写提示的基础知识 {#writing-prompts}

### 提示应包含哪些内容？

* 使用清晰的描述性语言描述目标受众。

  通常，提示不区分大小写，除提供清晰度外，不需要使用标点符号。

* 做到具体，并提供要包含的所有受众特征以及要排除的任何特征的详细信息。 您提供的详细信息越多，您获得满足需求的结果的机会就越大。

* 确定要包括或排除的位置、设备类型和数据提供程序。

* 在保存受众之前，反复提供详细信息以优化您的标准和生成的受众表达式。

* 了解如何通过试验进行提示。

  受众代理不会自动将生成的受众表达式另存为受众。 您只能通过单击提示区域之外的[!UICONTROL Create]按钮来保存受众，因此您可以撤消不想保留的任何更改。

有关优化受众提示的进一步方法，请参阅[创建受众简介的最佳实践](#audience-brief-best-practices)。

<!-- I think these are happening later:

DSP uses "smart" defaults based on the user's previous audiences (all user-created audiences or only ones created via AI prompting?)

you can use a predefined prompt (fill in the blanks, and some fields might have selectors where you can choose values)

Over time, DSP XXXX defaults [clarify this]

 onsider starting by asking for a general template, which contains placeholder values that you can replace with your desired values. The default template is something like "Create a xxx with NNN xxx."

you can give thumbs up or down to [what exactly?]. Verify what info is carried over from session to session and what starts from scratch.

-->

### 在提示中不能包含哪些内容？

* 对现有受众表达式的引用。

* 英语以外的其他语言的文本。

### AI代理响应示例和回复方式

当AI代理需要您响应时，您可以使用请求中的关键字或使用等效的常用术语进行回复。

#### AI代理响应询问您问题

`If you are okay with the proposed expression, I can start searching third party segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

您的肯定回复：“继续”、“确定”、“确定”、“是”或其他类似词语

您还可以忽略请求并继续指定其他受众条件。

#### AI代理响应要求您从多个选项中进行选择

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

您的回复： `1`、`proceed`、`2`、`maximum reach`等。

您还可以忽略请求并继续指定其他受众条件。

## 创建受众的最佳实践摘要 {#audience-brief-best-practices}

受众摘要是一种策略性描述，用于定义营销活动的目标受众。 精心编制的简报可帮助DSP受众代理识别最相关的区段，以汇集您的目标受众。

### 有效受众简报的重要组成部分

在您的简介中尽可能加入以下列表中的受众属性类型。 特定于要排除的属性。

<!-- What about these:

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

### 用于潜在客户活动的结构良好的受众简报示例

以下是促销活动的强大受众简报示例，旨在提高知名度并试用高级套餐订阅服务：

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [复制可重复使用的受众](/help/dsp/audiences/reusable-audience-duplicate.md)
>* [编辑可重复使用的受众](/help/dsp/audiences/reusable-audience-edit.md)
>* [查看有关可重用受众的详细信息](/help/dsp/audiences/reusable-audience-view-details.md)
>* [共享可重复使用的受众](/help/dsp/audiences/reusable-audience-share.md)
>* [导出可重复使用的受众](/help/dsp/audiences/reusable-audience-export.md)
>* [将可重用受众的区段密钥复制到剪贴板](/help/dsp/audiences/reusable-audience-clipboard.md)
>* [删除可重复使用的受众](/help/dsp/audiences/reusable-audience-delete.md)
