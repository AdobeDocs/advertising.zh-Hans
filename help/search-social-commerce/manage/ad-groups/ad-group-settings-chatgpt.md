---
title: '[!DNL ChatGPT]广告组设置'
description: 引用[!DNL ChatGPT]广告组的设置。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
source-git-commit: 487af67f7215bf4a070af5e813649288141b0ed4
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%
---
# [!DNL ChatGPT]广告组设置

[!DNL ChatGPT]中的&#x200B;*广告是[!DNL OpenAI]*&#x200B;的试点功能

## [!UICONTROL Basic Settings]选项卡

*仅限新广告组*

**[!UICONTROL Network]：**&#x200B;广告网络。

**[!UICONTROL Account]：**&#x200B;广告网络帐户。

**[!UICONTROL Campaign]：**&#x200B;营销活动。 创建广告组后，无法更改营销活动。

## [!UICONTROL Ad Group Details]选项卡

**[!UICONTROL Ad Group name]：**&#x200B;广告组名称在营销活动中是唯一的，并且至少包含三个字符。

**[!UICONTROL Status]：**&#x200B;广告组的显示状态： *[!UICONTROL Active]*&#x200B;或&#x200B;*[!UICONTROL Paused]*。 新广告组的默认值为&#x200B;*[!UICONTROL Active]*。

**[!UICONTROL Bid strategy]：** （具有目标[!UICONTROL Clicks]或[!UICONTROL Conversions]的促销活动）如何竞价广告组中的广告：

* *[!UICONTROL Autobid]：*（新广告组的默认值） [!DNL OpenAI]根据促销活动目标，自动调整竞价以从预算中获得最多点击次数或转化次数。 您不输入竞价金额。 此选项适用于每日和生命周期营销活动预算。

* *[!UICONTROL Target CPC]：* （具有目标[!UICONTROL Clicks]的营销活动）对每次点击平均成本目标的出价。 在[!UICONTROL Target CPC]字段中输入目标。

* *[!UICONTROL Target CPA]：* （具有目标[!UICONTROL Conversions]的营销活动）对每转化成本平均目标的出价。 在[!UICONTROL Target CPA]字段中输入目标。

* *[!UICONTROL Manual: Max bid]：* （仅现有手动竞价广告组）将现有的最高竞价保留为只读金额。 您可以保留此策略或切换到[!UICONTROL Autobid]或营销活动目标的目标策略。 此选项不适用于新的广告组，也不适用于编辑已使用自动竞价或目标竞价的广告组。

现有的手动竞价广告组不会自动更改为其他策略。 仅编辑目标金额或不相关的设置不会更改现有目标竞价策略。

**[!UICONTROL Target CPC]：** （竞价策略为[!UICONTROL Target CPC]的广告组；必需）您希望实现的每次点击平均成本（以帐户的货币表示）。 输入正金额。 这是平均成本目标，而不是最高出价。

**[!UICONTROL Target CPA]：** （竞价策略为[!UICONTROL Target CPA]的广告组；必需）您希望实现的每次转换的平均成本（以帐户的货币表示）。 输入正金额。 这是平均成本目标，而不是最高出价。

**[!UICONTROL Maximum CPC bid]：** （具有目标[!UICONTROL Clicks]的营销活动；仅限现有手动竞价广告组；只读）每次点击要支付的现有最大金额。

**[!UICONTROL Conversion-optimized bid cap]：** （具有目标[!UICONTROL Conversions]的营销活动；仅现有手动竞价广告组；只读）您愿意为转化竞价的现有最大金额。 [!DNL OpenAI]使用预测的转化率将此值转换为每次展示的拍卖出价。

**[!UICONTROL Maximum CPM bid]：** （具有目标[!UICONTROL Reach]的营销活动）您以帐户的货币支付的1000次展示的最大金额。 输入0.01-5000之间的值。 触及营销活动没有[!UICONTROL Bid strategy]选项。

**[!UICONTROL Context hints (optional)]：**&#x200B;与您的产品或服务相关的对话、主题或关键字的说明。 用逗号或换行符分隔提示。 您的提示可用于指导匹配，但不是完全匹配的定位规则。 请参阅[[!DNL ChatGPT Ads] 有关如何编写有效上下文提示的帮助](https://help.openai.com/en/articles/20001211-create-ad-groups-for-chatgpt#writing-effective-context-hints)。

**[!UICONTROL Landing Page Suffix]：**（可选）任何要附加到登陆页面URL末尾以跟踪信息的参数。 示例： `param1=value1&param2=value2`。

>[!MORELIKETHIS]
>
>* [管理广告组](ad-group-manage.md)
